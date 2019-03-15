# Ideas

## Package

Script vs Package
- difference between script and package
- which is more reusable and why?
- consideration about parallelism inside a module (need research)

Package Organization
- how many top level modules in a single package
- where to put export statement
- how to organize files within a package
- when to use (or not use) sub-modules

Packge Metadata
- when is a package too big?
- what's the best naming convention?
- how to specify external package depdencies
- project.toml vs manifest.toml
- how to incorporate with binary dependencies
- package registration

Continuous Integration
- test coverage: codecov, coverall, appveyor, etc.
- how to execute test cases
- organizing unit tests
- test driven development
- mocking

Documentation
- Comments / convention
- Documeter.jl


## Core Patterns

GofF patterns

Coding Style
- naming convention: use underscore, don't smash.
- use ! for side effect
- use unicode symbols judiciously

Structs
- inner vs outer construction 
- singleton... or not?

Functions
- Avoid type priracy
- Use multiple dispatch to optimize away certain branches (see Chris R blog)
- Throw exceptions or return error code?
- Return regular data along with error code/object?

Intefaces
- documenting interfaces

Traits
- Holy Traits 

File Processing
- Use mmap for out-of-core processing

Clean syntax
- Use do-syntax for anon function as first argument
- Use do-syntax to ensure opened file is closed after block

Data
- Use missing for representing unknown data
- Use nothing for representing programmer's null
- pay attention to numeric overflow issue

## Integration Patterns

Messaging
- introduction to ZeroMQ
- pub/sub
- dead letter queue
- etc.

UI 
- MVC
- MVVM
- Reactive programming

Microservices
- building RESTful service


## Performance Related Patterns

Data Types
- Use const keyword for global variables
- Specify types in struct's

Array
- Remember column major... do nested loops in reverse dimenison order
- Use array views to avoid memory allocation
- Do not use array views for performance

Loops
- Leverage loop fusion
- Use generator syntax e.g. sum(x.value for x in xs)

Type Safety
- Use zero/one functions
- Use OneTo() for ranges.... (does not matter anymore?)

Optimization Macros
- Use @inline
- Use @simd
- Use @inbounds
- Use @fastmath

Parallel Computing
- Multi-processing with shared memory
- Specify BLAS number of threads
- ZeroMQ
- Clean up (remove child processes when finished)

Functions
- avoid ... when the list may be big
