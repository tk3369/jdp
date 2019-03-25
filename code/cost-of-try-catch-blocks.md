## The Cost of Try-Catch Blocks 

```julia
julia> function ex1(n)
           badones = Int[]
           for i in 1:n
             try
               isodd(i) && throw(DomainError("cannot be add"))
             catch e
               push!(badones, i)
             end
           end
           return badones
       end

julia> function ex2(n)
         badones = Int[]
         for i in 1:n
           if isodd(i) 
             push!(badones, i)
           end
         end
         return badones
       end

julia> @btime ex1(100);
  2.258 ms (56 allocations: 2.70 KiB)

julia> @btime ex2(100);
  636.024 ns (6 allocations: 1.14 KiB)
```