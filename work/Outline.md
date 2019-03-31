# Design Patterns in Julia

## Julia Fundamentals

The Julia Fundamentals section is intended to provide necessary basic knowledge for the reader to understand the various patterns in the book. This is not a substitute of the Julia manual or other beginners book/material.  Hence, the pace will be relatively fast and only specific subjects are chosen here.

Modules and Packages
- Defining a new module
- Generally a single module is defined per package
- How to use sub-modules
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
- Purpose and benefits of using interfaces
- How to define interfaces and compare with other languages
- Examples

Meta-programming
- First look at a simple macro example
- Discuss whether macro is necessary compared to regular functions
-  example

## Julia Paradigm (vs OOP)

(Use Java for comparison purpose.)

Julia
- Struct and functions are separate
- Behavioral Inheritance only (no structural inheritance)
- Interfaces are by convention (not defined in language)
- Invariant parametric type (vs covariant/contravariant)

SOLID
- Single Responsibility principle (function level)
- Open-close principle
- Liskov substitution principle
- Interface segregation principle
- Dependency inversion principle

### Traditional Patterns (from OOP)

(Should determine which patterns are applicable to Julia or not)

From wikipedia.

- Creational: Abstract factory, Builder, Dependency injection, Factory method, Lazy initialization, Multiton, Object pool, Prototype, RAII, Singleton
- Structural: Adapter, Bridge, Composite, Decorator, Delegation, Facade, Flyweight, Front, controller, Marker, interface, Module, Proxy, Twin
- Behaviorial: Blackboard, Chain of responsibility, Command, Interpreter, Iterator, Mediator, Memento, Null object, Observer, Servant, Specification, State, Strategy, Template method, Visitor
- Functional: Closure, Currying, Function composition, Functor, Monad, Generator
- Concurrency: Active object, Actor, Balking, Barrier, Binding properties, Coroutine, Compute kernel, Double-checked locking,Event-based asynchronous, Fiber, Futex, Futures and promises, Guarded suspension, Immutable object, Join, Lock, Messaging, Monitor, Nuclear, Proactor, Reactor, Read write lock, Scheduler, Thread pool, Thread-local storage

### Julia Patterns

Reusability Patterns
- Method Forwarding Pattern (forwarding child object methods)
- Holy Trait Pattern
- Parametric Type Pattern
- Generic Function Pattern (extending from Base.whatever)

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

Miscellaneous Patterns
- Singleton Type Dispatch Pattern
- Re-export Pattern
- Mocking Pattern 

Testability Patterns
- (?) Clear Type Pattern (Specify types for function arguments)
- (?) Single Responsibility Pattern
- (?) Mocking Pattern

Safety Patterns
- Accessor Pattern (accessor functions over direct struct access)
- Minimum Exposure Pattern (Export Only What's Needed)
- Minimum Dependency Pattern (Import Only What's Needed)
- Nothing-ness Pattern (handle nothingness for programmer's null cases)
- Missing-ness Pattern (use missing for unknown data; propagation)
- Status Result Pattern (function returning status and result tuple)
- Let Scope Pattern (use let-block to avoid leak variables)
- Exception Handling Pattern

### Anti Patterns

- Untyped Struct Members Pattern (boxed)
- Abstract Struct Members Pattern (boxed)
- Type Piracy Pattern
- (?) Excessive Exception Handling (hurting performance)

**Other ideas?**
- Premature optimization (anti-pattern)
- Type Stability



