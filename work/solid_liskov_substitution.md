# Liskov Substitution Principle

In OOP, the Liskov Substitution Principle says you should be able to use any derived class instead of a parent class and have it behave in the same manner without modification.  

For Julia, one can define functions for various subtypes and the Julia runtime will dispatch to those function properly.  Following this pattern guarantees that the right implementation is executed according to the type that is being passed.

Let's take a look at an example.  Suppose that we define an abstract type called `Animal`.  We then define the obvious subtypes `Cat` and `Dog`.  Finally, we have a `play` function that describes how the animal plays with human.

```julia
abstract type Animal end
struct Cat end
struct Dog end
play(x::Animal) = x isa Cat ? :scratch : :roll
```

Naively, we just defined a single function with a simple if-condition and call it done.  The trouble is that we may adopt a new kind of pet later on and have to make changes.  Let's say you visited a pet store and they've got pretty-looking turtles.  

```julia
struct Turtle end
play(x::Animal) = x isa Cat ? :scratch : (x isa Turtle ? :crawl : :roll)
```

However, the code is getting so much uglier.  Since we have already defined a nice animal hierachy, we could rewrite as the play function as several small implementations.  

```julia
play(x::Animal) = error("Programmer error.  Please define play function for this animal type: ", typeof(x))
play(x::Cat) = :scratch
play(x::Dog) = :roll
play(x::Turtle) = :crawl
```

Now, anytime a new animal type is added, we just need to define a new play function for that type.  The program can be extended much more easily without worrying about changing any existing functions.