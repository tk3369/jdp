# Design Patterns in Julia

## Outline

1. Introduction
   - Intended audience
   - How to use this book
   - About the author
2. Julia Fundamentals
   - Modules and Packages
   - Types
   - Multiple Dispatch
   - Interfaces
   - Meta-programming
   - etc.
3. Programming Paradigm
   - Benefits of using design patterns
   - OOP and the Gang of Four design patterns
   - How is Julia different than OOP
4. Design Patterns 
   - OOP patterns
   - Julia patterns
   - Julia anti-patterns
5. Real-Life Examples

## Scope/Expectation

Chapter 1 is just introduction about the book.

Chapter 2 contains a brief introduction of the most fundamental concepts that are needed for new Julia developers.  

Chapter 3 provides some history about the wide-spread patterns from the GofF book and discusses various aspects of Julia language design that sets apart from the object oriented programming paradigm.

Chapter 4 covers a list of design patterns coming from the object-oriented programming paradigm and how the same concepts can be applied to Julia programming.  Then, it discusses a list of Julia-specific design patterns and anti-patterns.

Chapter 5 provides various real-life examples that show cases specific design patterns.  Most content will come from existing open-source projects.   

## Some Details

### Julia Overview

The Julia overview section is intended to provide necessary basic knowledge for the reader to understand the various patterns in the book. This is not a substitute of the Julia manual or other beginners book/material.  Hence, the pace will be relatively fast and only specific subjects are chosen here.

Modules and Packages
- Defining a new module
- Generally a single module is defined per package
- How to use sub-modules
- Exports and imports

Types 
- Construction
- Type hierarchy, abstract vs concrete types
- Type promotion
- Multiple Dispatch
- Parametric types

Interfaces
- Purpose and benefits of using interfaces
- How to define interfaces and compare with other languages
- Example

Meta-programming
- First look at a simple macro example
- Discuss whether macro is necessary compared to regular functions
- Another example 


### Julia vs OOP

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

### OOP Patterns 

(Should determine which patterns are applicable to Julia or not)

(Is this section really useful?)

From wikipedia.

- Creational: Abstract factory, Builder, Dependency injection, Factory method, Lazy initialization, Multiton, Object pool, Prototype, RAII, Singleton
- Structural: Adapter, Bridge, Composite, Decorator, Delegation, Facade, Flyweight, Front, controller, Marker, interface, Module, Proxy, Twin
- Behaviorial: Blackboard, Chain of responsibility, Command, Interpreter, Iterator, Mediator, Memento, Null object, Observer, Servant, Specification, State, Strategy, Template method, Visitor
- Functional: Closure, Currying, Function composition, Functor, Monad, Generator
- Concurrency: Active object, Actor, Balking, Barrier, Binding properties, Coroutine, Compute kernel, Double-checked locking,Event-based asynchronous, Fiber, Futex, Futures and promises, Guarded suspension, Immutable object, Join, Lock, Messaging, Monitor, Nuclear, Proactor, Reactor, Read write lock, Scheduler, Thread pool, Thread-local storage

### Julia Patterns

Organizational (?)
- Sub-Module Pattern: separate concerns in sub-modules
- Accessor Pattern: accessor functions over direct struct attribute access
- Keyword Argument Extraction Pattern

Reusability and Extendability
- Method Forwarding Pattern (forwarding child object methods)
- Holy Trait Pattern
- Parametric Type Pattern
- Generic Function Pattern (extending from Base.whatever)

Performance
- Constant Global Pattern
- Struct of Arrays Pattern
- Pure Function Pattern
- Memory Map Pattern
- Shared Memory Pattern

Maintainability / Readability
- Keyword Definition Pattern (`Base.@kwdef`)
- Boilerplate Reduction Pattern (`@eval` macro to define functions)
- Domain Specific Language Pattern (Diff Eq ecosystem?)
- (???) Generated Functions Pattern 

Testability
- Clear Type Pattern (Specify types for function arguments)
- Single Responsibility Pattern
- Mocking Pattern

Safety
- Minimum Viable Interface Pattern (Export Only What's Needed)
- Minimum Dependency Pattern (Import Only What's Needed)
- Nothingness Pattern (handle nothingness for programmer's null cases)
- Missingness Pattern (use missing for unknown data; propagation)
- Status Result Pattern (function returning status and result tuple)
- Exception Handling Pattern

### Anti Patterns

- Untyped Struct Members Pattern (boxed)
- Abstract Struct Members Pattern (boxed)
- Type Piracy Pattern
- Excessive Exception Handling (hurting performance)

**Other ideas?**
- Premature optimization (anti-pattern)
- Type Stability



