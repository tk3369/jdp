# Hands-On Design Patterns in Julia 1.0

## Objectives

The reader will be able to:

1. Master Julia language features that are key to developing large-scale software applications
2. Improve overall application architecture and design
3. Develop programs that are modular, reusable, extendable, performant, and easy to maintain
4. Articulate the pros and cons of specific design patterns for particular use cases
5. Transition from object-oriented programming to using the equivalent or better Julia techniques
6. Communicate to other Julia developers more effectively
7. Develop applications more quickly by using proven design patterns

## Julia Fundamentals

Modules and Packages
- Defining a new module
- Single module per package
- Sub-modules
- Exports and imports

Types 
- Construction
- Type hierarchy, abstract vs concrete types
- Type promotion
- Parametric types

Functions
- Definitions
- Multiple Dispatch
- Parametric functions

Interfaces
- Purpose and benefits 
- Documenting interfaces

Meta-programming
- First look at a simple macro examples
- How are macros different from regular functions
- Why meta-programming? Is it really necessary?

## Application Design

SOLID
- Single Responsibility principle (function level)
- Open-close principle
- Liskov substitution principle
- Interface segregation principle
- Dependency inversion principle

Microsoft [Architecture Design Patterns](https://docs.microsoft.com/en-us/dotnet/standard/modern-web-apps-azure-architecture/architectural-principles)
- Separation of concerns
- Encapsulation
- Dependency inversion
- Explicit dependencies
- Single responsibility
- DRY
- Persistence ignorance
- Bounded contexts

Others
- YAGNI
- Principle of Least Astonishment (POLA)

### Object Oriented Patterns

_From wikipedia, we shall select a subset of these patterns and analyze which ones are applicable to Julia and how._

- Creational: Abstract factory, Builder, Dependency injection, Factory method, Lazy initialization, Multiton, Object pool, Prototype, RAII, Singleton
- Structural: Adapter, Bridge, Composite, Decorator, Delegation, Facade, Flyweight, Front, controller, Marker, interface, Module, Proxy, Twin
- Behavioral: Blackboard, Chain of responsibility, Command, Interpreter, Iterator, Mediator, Memento, Null object, Observer, Servant, Specification, State, Strategy, Template method, Visitor
- Functional: Closure, Currying, Function composition, Functor, Monad, Generator
- Concurrency: Active object, Actor, Balking, Barrier, Binding properties, Coroutine, Compute kernel, Double-checked locking,Event-based asynchronous, Fiber, Futex, Futures and promises, Guarded suspension, Immutable object, Join, Lock, Messaging, Monitor, Nuclear, Proactor, Reactor, Read write lock, Scheduler, Thread pool, Thread-local storage

### Julia Patterns

Reusability Patterns
- Method Forwarding Pattern (composition, forwarding methods)
- Holy Trait Pattern
- Parametric Type Pattern (more generic types)
- Generic Function Pattern (e.g. extending from Base.whatever)

Performance Patterns
- Constant Global Pattern 
- Struct of Arrays Pattern
- Memory Map Pattern
- Shared Memory Pattern
- (?) Pure Function Pattern

Maintainability Patterns
- Sub-Module Pattern: separate concerns in sub-modules
- Keyword Definition Pattern (`Base.@kwdef`)
- Boilerplate Reduction Pattern (`@eval` macro to define functions)
- Domain Specific Language Pattern (Diff Eq ecosystem?)
- (*) Keyword Argument Extraction Pattern (extract specific keyword args from variable keyword arg)
- (?) Generated Functions Pattern 

Safety Patterns
- Accessor Pattern (accessor functions over direct struct access)
- Minimum Exposure Pattern (Export Only What's Needed)
- Minimum Dependency Pattern (Import Only What's Needed)
- Nothing-ness Pattern (handle nothingness for programmer's null cases)
- Missing-ness Pattern (use missing for unknown data; propagation)
- Let Scope Pattern (use let-block to avoid leak variables)
(?) Exception Handling Pattern

Miscellaneous Patterns
- Singleton Type Dispatch Pattern
- Re-export Pattern
- Mocking Pattern 
(?) Return Status Pattern (function returning status and result tuple)

Testability Patterns
- (?) Clear Type Pattern (Specify types for function arguments)

Anti Patterns
- Untyped Struct Members Pattern (boxed)
- Abstract Struct Members Pattern (boxed)
- Type Piracy Pattern
- (?) Excessive Exception Handling (hurting performance)

## Advanced Topics

- Behavioral Inheritance only (no structural inheritance)
- Invariant parametric type (vs covariant/contravariant)