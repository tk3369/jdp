# References

Type-Dispatch Design: Post Object-Oriented Programming for Julia
http://www.stochasticlifestyle.com/type-dispatch-design-post-object-oriented-programming-julia/
- duck typing
- type hierarchies
- small functions and constant propagation
- traits and THTT (Tim Holy Trait Trick)
- composition vs inheritance

# Discourse posts

https://discourse.julialang.org/t/composition-and-inheritance-the-julian-way/

https://discourse.julialang.org/t/julep-taking-multiple-dispatch-export-import-binary-compilation-seriously/

https://discourse.julialang.org/t/julia-motivation-why-werent-numpy-scipy-numba-good-enough/2236

https://discourse.julialang.org/t/function-name-conflict-adl-function-merging/10335
generic programming name clashes
this is a controversial topic

https://discourse.julialang.org/t/cumbersome-scoping-rules-for-try-catch-finally/4582/8
using do-syntax to abstract away pre/post work normally done in try/catch/finally

# Open source packages

StatsBase
Plots
DifferentialEquations
MLK? or Koala.

# Criticism

Singletons are evil
http://wiki.c2.com/?SingletonsAreEvil
http://wiki.c2.com/?SimpletonPattern

# Books

Design patterns in Dynamic Languges
http://www.norvig.com/design-patterns/design-patterns.pdf

# Ideas

Package version and dependencies / semantic versioning
Managing changes
Testability
Notes sections - e.g. using Revise for rapid prototyping and development
Find a way to illustrate patterns not using UML
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

Base.show is a good example of multiple dispatch

https://docs.julialang.org/en/v1/manual/methods/#Design-Patterns-with-Parametric-Methods-1

https://docs.julialang.org/en/v1/manual/methods/#man-methods-orthogonalize-1

https://docs.julialang.org/en/v1/manual/methods/#Dispatch-on-one-argument-at-a-time-1 (easier mentally but the drawback is that it's not extendable)

https://docs.julialang.org/en/v1/manual/methods/#Abstract-containers-and-element-types-1 (don't understand)

https://docs.julialang.org/en/v1/manual/methods/#Complex-method-"cascades"-with-default-arguments-1

Invariant, Co-variant, Contra-variant
https://blog.codecentric.de/en/2015/03/scala-type-system-parameterized-types-variances-part-1/
