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
   - Metaprogramming
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

Chapter 3 provides some history about the wide-spread patterns from the GofF book and discusses various aspects of Julia language design that sets apart from the object oriented progrmaming paradigm.

Chapter 4 covers a list of design patterns coming from the object-oriented programming paradigm and how the same concepts can be applied to Julia programming.  Then, it discusses a list of Julia-specific design patterns and anti-patterns.

Chapter 5 provides various real-life examples that show cases specific design patterns.  Most content will come from existing open-source projects.   

## Some Details

### Julia vs OOP

(Use Java for comparison purpose.)

Julia
- Struct and functions are separate
- Behavioral Inheritance only (no structural inheritance)
- Interfaces are by convention (not defined in language)
- Invariant parametric type (vs covariant/contravariant)

SOLID(?)
- Single Responsibility principle
- Open-close principle
- Liskov substitution principle
- Interface segregation principle
- Dependency inversion principle

### OOP Patterns 

(Determine which patterns are applicable to Julia or not)

(Is this section really useful?)

- Singleton, Builder, Factory, AbstractFactory, Prototype
- Chain of Responsibility, Command, Iterator, Mediator, Memento, Observer, State, Strategy, Template, Visitor
- Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Proxy

### Julia Patterns

(Don't have catchy titles yet and not sure if need them.)

Structure
- Use Module over Script
- Accessor functions over direct struct attribute access 
- Export Only What's Needed
- Propagating Keyword Arguments

Reusability
- Composition
- Holy Traits
- Parametric Types
- Generic

Performance
- Memory map for Out-of-Core Programming
- Constant Globals
- Struct of Array
- Array of Struct
- Pure functions
- Immutable Objects (?)

Readability
- Domain Specific Languages
- Small functions

Testability
- Generated Test Cases

Convention
- Proper use of nothing vs. missing


### Anti Patterns

- Type Priracy
- Excessive Exception Handling
- Untyped struct members
- Premature optimization

