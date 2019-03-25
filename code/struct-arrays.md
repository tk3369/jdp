## Struct Arrays

### Description

Convert an array of struct's into a struct of arrays.

### Motivation

Numerical analysis often involves basic statistics or matrix calculations and such operation can be computed efficiently when the data is stored in a dense array format.  However, the data may be oriented in a different way, such as in an array of struct, and that does not lead to good performance.  The strategy is to convert the array of structs into a struct of arrays.

### Examples

Let's first read and examine the iris data set.

```julia
julia> lines = readlines("iris.csv")

julia> records = Iris[]; for L in lines[2:end]
         v = split(L, ",")
         obs = Iris(parse(Int, strip(v[1], '"')),
                    parse(Float64, v[2]),
                    parse(Float64, v[3]),
                    parse(Float64, v[4]),
                    parse(Float64, v[5]))
         push!(records, obs)
       end

julia> records
150-element Array{Iris,1}:
 Iris(1, 5.1, 3.5, 1.4, 0.2)  
 Iris(2, 4.9, 3.0, 1.4, 0.2)  
 Iris(3, 4.7, 3.2, 1.3, 0.2)  
...
```

Now, suppose that we want to calculate the standard deviation for a property of the samples.  To do that, we must extract the data into an array and than pass it over to the `std` function.  

```
julia> @btime std(r.sepal_width for r in $records)
  1.358 μs (1 allocation: 16 bytes)
```

Another way to design this is to have a struct of arrays rather than an array of structs.  DataFrame is an example of such design.  Here, let's do this manually.

```julia
julia> struct IrisTable 
         sepal_length::Vector{Float64}
         sepal_width::Vector{Float64}
         petal_length::Vector{Float64}
         petal_width::Vector{Float64}
       end

julia> iristable = IrisTable(getproperty.(records, :sepal_length), 
                             getproperty.(records, :sepal_width),
                             getproperty.(records, :petal_length),
                             getproperty.(records, :petal_width))

julia> @btime std($iristable.sepal_width)
  71.711 ns (0 allocations: 0 bytes)
```

That's a 20x difference!  Now, you might wonder why I cheated on you.  If the data is oriented properly for numerical functions then the extra step is skipped then of course it is fast!  Well, that's exactly what we did that.  While the original format seems to be more user-friendly, it come with a cost for numerical analysis.  

The trouble is that if we have to create a new struct and convert data format for everything then we have more code to maintain! Fortunately, the (StructArrays.jl)[https://github.com/piever/StructArrays.jl] package comes to rescue. It's easy to construct a `StructArray` from an iteration of any struct.

```julia
julia> s = StructArray(r for r in records)
150-element StructArray{Iris,1,NamedTuple{(:id, :sepal_length, :sepal_width, :petal_length, :petal_width),Tuple{Array{Int64,1},Array{Float64,1},Array{Float64,1},Array{Float64,1},Array{Float64,1}}}}:
 Iris(1, 5.1, 3.5, 1.4, 0.2)  
 Iris(2, 4.9, 3.0, 1.4, 0.2)  
 Iris(3, 4.7, 3.2, 1.3, 0.2)  

julia> @btime std($s.sepal_width)
  74.525 ns (0 allocations: 0 bytes)
```

What if you have a nested data structure?  It's a just little bit more work.  Let's explore the same iris data set in a custom struct.

```julia
julia> struct Dimension
         length::Float64
         width::Float64
       end

julia> struct IrisRec
         id::Int
         sepal::Dimension
         petal::Dimension
       end

julia> records2 = IrisRec[]; for L in lines[2:end]
         v = split(L, ",")
         obs = IrisRec(parse(Int, strip(v[1], '"')), 
                       Dimension(parse(Float64, v[2]), parse(Float64, v[3])), 
                       Dimension(parse(Float64, v[4]), parse(Float64, v[5])))
         push!(records2, obs)
       end

julia> records2[1]
IrisRec(1, Dimension(5.1, 3.5), Dimension(1.4, 0.2))
```

We can create the `StructArray` with a nested structure that mimics the original.

```julia
julia> s2 = StructArray(
               sepal = StructArray(r.sepal for r in records2),
               petal = StructArray(r.petal for r in records2))
150-element StructArray{NamedTuple{(:sepal, :petal),Tuple{Dimension,Dimension}},1,NamedTuple{(:sepal, :petal),Tuple{StructArray{Dimension,1,NamedTuple{(:length, :width),Tuple{Array{Float64,1},Array{Float64,1}}}},StructArray{Dimension,1,NamedTuple{(:length, :width),Tuple{Array{Float64,1},Array{Float64,1}}}}}}}:
 (sepal = Dimension(5.1, 3.5), petal = Dimension(1.4, 0.2))
 (sepal = Dimension(4.9, 3.0), petal = Dimension(1.4, 0.2))
 (sepal = Dimension(4.7, 3.2), petal = Dimension(1.3, 0.2))
...
```

The result is a nested structure of `StructArray`'s, and we can reference to the leaf node where it's stored as a plain array.

```julia
julia> s2.sepal
150-element StructArray{Dimension,1,NamedTuple{(:length, :width),Tuple{Array{Float64,1},Array{Float64,1}}}}:
 Dimension(5.1, 3.5)
 Dimension(4.9, 3.0)
 Dimension(4.7, 3.2)
...

julia> s2.sepal.width
150-element Array{Float64,1}:
 3.5
 3.0
 3.2
...
```

Let's test performance again.  Perfect!

```julia
julia> @btime std($s2.sepal.width)
  73.137 ns (0 allocations: 0 bytes)
0.43586628493669827
```

### Variations

None

### Counter Situation

When performance is not a concern, there is no need to do this extra conversion.

### See Also

None
