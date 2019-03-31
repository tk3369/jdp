# References

Type-Dispatch Design: Post Object-Oriented Programming for Julia
http://www.stochasticlifestyle.com/type-dispatch-design-post-object-oriented-programming-julia/
- duck typing
- type hierarchies
- small functions and constant propagation
- traits and THTT (Tim Holy Trait Trick)
- composition vs inheritance

Lyndon White on Multiple Dispatch & Traits
https://white.ucc.asn.au/2018/10/03/Dispatch,-Traits-and-Metaprogramming-Over-Reflection.html

# Discourse posts

https://discourse.julialang.org/t/composition-and-inheritance-the-julian-way/

https://discourse.julialang.org/t/julep-taking-multiple-dispatch-export-import-binary-compilation-seriously/

https://discourse.julialang.org/t/julia-motivation-why-werent-numpy-scipy-numba-good-enough/2236

https://discourse.julialang.org/t/function-name-conflict-adl-function-merging/10335
generic programming name clashes
this is a controversial topic

https://discourse.julialang.org/t/cumbersome-scoping-rules-for-try-catch-finally/4582/8
using do-syntax to abstract away pre/post work normally done in try/catch/finally

https://discourse.julialang.org/t/clarification-on-type-piracy/5926
type piracy

# Blogs
Invariant, Co-variant, Contra-variant
https://blog.codecentric.de/en/2015/03/scala-type-system-parameterized-types-variances-part-1/

The Expression problem
https://eli.thegreenplace.net/2016/the-expression-problem-and-its-solutions/

# Open source packages

OnlineStats

StatsBase
Plots
DifferentialEquations
MLK? or Koala.

# GoF Criticism

Singletons are evil
http://wiki.c2.com/?SingletonsAreEvil
http://wiki.c2.com/?SimpletonPattern

# Related Books

Design patterns in Dynamic Languages
http://www.norvig.com/design-patterns/design-patterns.pdf

# SOLID

Single Responsibility Principle
- _"Every software module should have only one reason to change"_
- every function should focus on doing one thing
- try to write small functions, long functions are code smell

Open/Closed Principle
- _"A software module/class is open for extension and closed for modification"_
- Open for extension, closed for modification
- Design packages as if they're frozen and not modifiable
- Leverage types and multiple dispatch to allow for extension

Liskov Substitution Principle
- _"you should be able to use any derived class instead of a parent class and have it behave in the same manner without modification". It ensures that a derived class does not affect the behavior of the parent class, in other words that a derived class must be substitutable for its base class"_
- Julia does not allow down-casting to a subtype!
- Julia does allow runtime check as a subtype
- See [solid_liskov_substitution.md](solid_liskov_substitution.md)

Interface Segregation Principle
- _"clients should not be forced to implement interfaces they don't use. Instead of one fat interface many small interfaces are preferred based on groups of methods, each one serving one sub module."_
- Design small interfaces e.g. iterator is only a single function
- Use traits for a complete implementation (why doesn't iterators do that?)

Dependency Inversion Principle
- _"high-level modules/classes should not depend on low-level modules/classes. Both should depend upon abstractions. Secondly, abstractions should not depend upon details. Details should depend upon abstractions."_
- Use abstract types and multiple dispatch for different situations
- An example is Logger. How to implement it such that it's easy to change e.g. adding a new logging destination like splunk

# Challenges

1. Find a way to illustrate patterns not using UML
1. 

# Ideas

Package version and dependencies / semantic versioning
Managing changes and lifecycle of code
How to learn design patterns
Notes sections - e.g. using Revise for rapid prototyping and development
Have a chapter about anti-patterns
Reference SOLID when describing the patterns
Invariant types (vs covariant and contra-variant)

Related topics: 
- Dependency Injection
- MVC
- Async programming 
- Struct of Arrays (over Array of Structs)
- get/setindex 
- get/setproperty
- do syntax
- NamedTuples over struct's
- Keyword args... passing down.
- Producer/Consumer pattern (Tasks/co-routines) => manual not too detail and lacks examples https://docs.julialang.org/en/v1/manual/control-flow/#man-tasks-1
- Empty generic function https://docs.julialang.org/en/v1/manual/methods/#Empty-generic-functions-1

# Julia Manual

Base.show is a good example of multiple dispatch

https://docs.julialang.org/en/v1/manual/methods/#Design-Patterns-with-Parametric-Methods-1

https://docs.julialang.org/en/v1/manual/methods/#man-methods-orthogonalize-1

https://docs.julialang.org/en/v1/manual/methods/#Dispatch-on-one-argument-at-a-time-1 (easier mentally but the drawback is that it's not extendable)

https://docs.julialang.org/en/v1/manual/methods/#Abstract-containers-and-element-types-1 (don't understand)

https://docs.julialang.org/en/v1/manual/methods/#Complex-method-"cascades"-with-default-arguments-1

# Tips/Tricks

Package Alias 
https://github.com/malmaud/TensorFlow.jl/blob/859d2b4b08eaef3019cc2a4075e112e76b346a77/src/variable.jl#L17-L18

Debug macro
https://github.com/denizyuret/Knet.jl/blob/1a306d011c4f0b5ad0e3517495840debe665aa4b/src/Knet.jl#L6

Using init function
https://github.com/denizyuret/Knet.jl/blob/1a306d011c4f0b5ad0e3517495840debe665aa4b/src/Knet.jl#L148-L157

Sample BenchmarkTools usage
https://github.com/JuliaArrays/BlockArrays.jl/blob/master/benchmark/runbenchmarks.jl
- benchmark suite
- testing implementation by constructing different types
- generates reports

Kubernetes binding via Swagger.jl
https://github.com/JuliaComputing/Kuber.jl
- Very interesting with submodule alias


