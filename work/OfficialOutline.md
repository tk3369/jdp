---
title: "Hands-On Design Patterns with Julia 1.0 (Outline)"
author: Tom Kwong
date: March 25, 2019
geometry: margin=1.5in
output: pdf_document
---

# SUMMARY

**Subtitle**: A comprehensive guide to create robust, reusable, performant and maintainable applications using proven design patterns.

**Author**: Tom Kwong

**Description**: 
The goal of the book is to provide solutions to a common problem and help reader become familiar with the solutions developed by experienced developers. Equipped with the knowledge of these patterns, reader will spend less time searching for a solution to a common problem and learn an efficient way to communicate. With this comprehensive guide, reader will gain a deep understanding of design patterns to create robust, reusable, performant and maintainable code.

This book will cover both traditional and modern design patterns specific to Julia programming. These patterns are useful in any domain, including enterprise applications, data science, parallel and distributed computing.

**Page Count**: 320-350 pages	

_**Notes**: Some contents in the outline below are still in the early stage and could change throughout the course of authoring.  Keep in mind that all changes are made with the intention of better organization and material for the reader.  By no means that the changes will bring deviation to the intended objectives stated in the above._ 

## ABOUT THE AUTHOR

Tom Kwong (GitHub handle: tk3369) has over 25 years of software development experience.  He holds a M.S. Computer Science degree from University of California, Santa Barbara (UCSB) from 1993.  Over the years, he worked on many large-scale enterprise applications that require solid design, high performance and scalability.  He has extensive development experience in C, Java, JavaScript, PHP, Objective-C, etc. before falling in love with the Julia programming language in 2017.

Tom specializes in the financial services domain and currently works at Western Asset Management Company as a Software Engineering Manager.  He is a CFA charter holder, a prestige designation for investment management professionals.  He loves agile development and is a Certified Scrum Master (CSM).  Finally, he holds a patent for developing a bid-for-placement system for Overture Services (formerly GoTo.com), a search engine company that was acquired by Yahoo in 2003.

## Can you recommend a good technical reviewer for your book?

Scott Jones (scott@gandalfsoftware.com)


## PART ONE: BACKGROUND RESEARCH

### TARGET AUDIENCE 

Who is your audience?

1. This book is intended for beginner to intermediate-level Julia programmers who want to advance their skills in designing and developing large scale applications.

2. The reader is expected to have some basic knowledge about the Julia programming language although this book does attempt to provide an overview of some of the fundamental concepts as a convenience.

3. People who have prior knowledge about design patterns and object-oriented programming may find this book interesting as they can transition  existing knowledge to a new way of programming.

What is important to them?

1. The reader wants to know how to develop well-designed Julia applications upfront.

2. The reader may have prior experience with object-oriented programming but wants to transition to more _Julian_ coding style.

3. People who are new to the Julia programming language may be challenged with its unique way of coding.  
   - How to write reusable and extendable code?
   - How to write performant code?
   - How to write readable code?
   - How to write safe code?

4. Readers will likely demand:
   - A recap of Julia's fundamentals 
   - Traditional design patterns
   - Julia patterns
   - Julia anti-patterns
   - Case studies and examples

## COMPETITIVE BOOK TITLES

_What is unique about your book? You will need to look on Amazon at books that have been well-received – what are the top three market leading books that your book will compete with?  Examine the description, table of contents and book reviews._

Most books on the market either focuses on specific use cases (e.g. data science, numerical analysis) or the language itself.  

This book is unique because of its focus on design patterns.  Possible overlap would be in the _Julia Fundamentals_ section.

Here are some of the competitive books:

1. _[Think Julia](https://www.amazon.com/Think-Julia-Like-Computer-Scientist/dp/1492045039/ref=sr_1_5?keywords=julia+programming&qid=1552241159&s=gateway&sr=8-5)_ - Mostly introductory text about the Julia language.  The target audience is more towards beginner level.

2. _[Mastering Julia 1.0](https://www.amazon.com/Mastering-Julia-1-0-processing-problems-ebook/dp/B07FSFWLRH/ref=sr_1_17?keywords=julia+programming&qid=1552241159&s=gateway&sr=8-17)_ - This book has some overlaps e.g. type system and multiple dispatch. 

3. _[Julia 1.0 Programming](https://www.amazon.com/Julia-1-0-Programming-Science-projects/dp/1788999096/ref=sr_1_fkmrnull_1_sspa?keywords=julia+1.0+programming&qid=1552872720&s=gateway&sr=8-1-fkmrnull-spons&psc=1) - This book is an introductory text that focuses on the Julia language itself._

3. _[Julia 1.0 Programming Cookbook](https://www.amazon.com/Julia-1-0-Programming-Cookbook-distributed-ebook/dp/B07KX4CSHL/ref=sr_1_14?keywords=julia+programming&qid=1552241159&s=gateway&sr=8-14)_ - Contains recipes for specific problems as it’s written as a cookbook style.  It is focused more on the usage and related ecosystem such as IDE, calling Python/R, etc.

## PART TWO: BOOK OVERVIEW

### Overview

This book will demonstrate how to leverage design patterns when developing Julia applications.  Design patterns are fundamental techniques for  developing reusable and maintainable code.  

Software engineers who have mastered object-oriented programming before are most likely familiar with the “Gang-of-Four” design patterns.  Remember singleton, factory, and facade patterns?  This book not only covers the traditional OOP patterns in the context of Julia language but will also go beyond and introduce other patterns that are more natural and useful to Julia programmers.

This book starts with an introduction about design patterns and the Julia programming paradigm.  Next, you will dive deeper and learn some of the most fundamental Julia language features.  You will then explore the most well-known design patterns from the object-oriented programming era and how they can also be applied in Julia.  You will also see additional patterns and anti-patterns that are specific to Julia.  Finally, you will learn from the best Julia developers how they use design patterns in their open-source packages.

### LEARNING OUTCOME - WHAT WILL THE READER LEARN AND DO?

The reader will be able to:

1. Master Julia language features that are key to developing large-scale software applications

2. Improve overall application architecture and design

3. Develop programs that are modular, reusable, extendable, performant, and easy to maintain

4. Articulate the pros and cons of specific design patterns for particular use cases

5. Transition from object-oriented programming to using the equivalent or better _Julia_ techniques

6. Communicate and transition source code to other Julia developers more effectively

7. Develop applications more quickly by using proven design patterns

## PART THREE: BOOK STRUCTURE

### GENERAL STRUCTURE

>_Divide the book into approximately 3-5 parts. The learning outcomes you listed previously will help to inform these. These “parts” are a group of chapters that work toward the same goal. Each part will consist of 3-5 chapters. For example: A book on Building Machine Learning Systems with Python might be split into 5 parts as follows: “The Basics”; “Book Learning”; “Numbers, Forecasts and Recommendations”; “Sound and Vision” and finally, “Practical Matters”._

1. Motivation
2. Julia Fundamentals
3. Design Patterns
4. Advanced Topics

### CHAPTER OUTLINE

>_Each chapter should have a clear focus. Each chapter title should clearly state what aspect of the overall topic the chapter deals with.. Continuing the example of Building Machine Learning Systems with Python your section on “Book Learning” might be broken down into 4 chapters as follows: “Clustering – sorting text into groups”, “Topic Modeling – creating non-exclusive groups”; “Logistic Regression – evaluating text quality”; “Bayes Classification – sentiment analysis”. PLEASE NOTE: Chapter titles appear on Amazon_

#### Part 1. Motivation

1. Understanding Design Patterns and Application Design (20)

#### Part 2. Julia Fundamentals

2. Modules, Packages and Julia’s Type Concepts (30)

3. Defining​ ​Functions and Designing Interfaces (40)

4. Macros and Meta Programming Techniques (25)

#### Part 3. Implementing Design Patterns

_**Note**: Please beware that I expect to add a couple more patterns during the course of authoring the book._

5. Object Oriented Traditional Patterns (25)

6. Reusability Patterns (30)

7. Performance Patterns (30)

8. Maintainability Patterns (30)

9. Safety Patterns (40)

10. Miscellaneous Patterns (30)

11. Anti-Patterns (20)

#### Part 4. Advanced Topics

12. Behavioral Inheritance (20)

13. Invariant Parametric Types (15)

## PART FOUR: DETAILED OUTLINE

### Part 1. Motivation

The objective of this part is to introduce the reader to the use of design patterns in general and what characteristics one should be looking for when developing large-scale applications.

#### Chapter 1. Understanding Design Patterns and Application Design

_Objective_: The reader will learn some history about design patterns and an overview of the traditional patterns and design principles.  The reader will also learn the characteristics of a well-designed application and how they relate to design patterns.

_Level_: Basic

_Description_: This chapter will provide some context about why design patterns is useful and how it has served us well in the past several decades.  It provides an overview of the the traditional "Gang-of-Four" design patterns and some of the most well-known design principles such as SOLID.  This chapter will also discuss the characteristics of a well-designed application such as reusability, performance, maintainability, safety, etc.  These concepts are important to be kept in mind when developing software. 

Main Chapter Headings (3-5):

1. When and how?

2. Gang-of-Four

3. Design Principles

4. Reusability

5. Performance

6. Maintainability

7. Safety

Skills Learned:

1. History of object-oriented programming and the rise of design patterns

2. An overview of traditional design patterns 

3. An overview of commonly used design principles

4. Understand how software becomes easy to maintain

5. Understand why code should be reusable and be extended easily

6. Understand the benefits of high performance code

7. Understand the reason and outcome of safe code

### Part 2. Julia Fundamentals

The objective of this part is to quickly bring the reader up to speed about the fundamental concepts and features in the Julia programming language.  A clear understanding of Julia Fundamentals is essential for the reader to fully appreciate the beauty of the design patterns in upcoming chapters.  

#### Chapter 2. Modules, Packages and Julia’s Type Concepts

_Objective_: the reader will learn how to put together source codes into a well organized structure of modules and packages. The reader will also learn about Julia's type hierarchy concepts and how to construct his/her own hierarchy for an application.

_Level_: Basic

_Description_:  This chapter focuses on breaking down large source code into a manageable set of modules and packages.  It will discuss the benefits and possible nuances when splitting source code into decoupled components. This chapter will dive into Julia's type system.  It will first discuss abstract and concrete types and the respective type hierarchy.  Then, it will talk about parametric types and how helps to make the system more flexible and performant. 

Main Chapter Headings (3-5):

1. The Growing Pain

2. Namespace Matters

3. Managing Dependencies 

4. Abstract Types

5. Concrete Types

6. Parametric Types

7. Conversion 

Skills Learned:

1. Identify the signs of an organizational problem

2. Understand Julia's namespace and scoping rules

3. Ability to manage package and module dependencies effectively

4. Understand abstract types and the type hierarchy

5. Understand concrete types and how they are constructed

6. Ability to design parametric types

7. Learn how to convert between data types

#### Chapter 3. Defining​ ​Functions and Designing Interfaces

_Objective_: The reader will learn how to design and create various types of functions in different situations. The reader will learn how to design interfaces that models specific behaviors.

_Level_: Intermediate

_Description_:  This chapter will discuss various ways of defining functions in Julia.  It will also demonstrate how to use multiple dispatch and parametric functions under specific circumstances. This chapter will discuss when interfaces would be desired and how one can create a generic interface that is extensible to multiple data types.

Main Chapter Headings (3-5):

1. Function definitions

2. Multiple Dispatch 

3. Parametric functions

4. Modeling behaviors

5. Interface examples

6. Documentation

Skills Learned:

1. Write functions using various kinds of arguments

2. Leverage multiple dispatch effectively

3. Design parametric functions that work with the type hierarchy

4. Articulate the need to formalize behavior

5. Learn how to build interfaces from examples

6. Understand the need for documenting interfaces

#### Chapter 4. Macros and Meta Programming Techniques

_Objective_: The reader will learn  meta-programming techniques - code that generates code.

_Level_: Intermediate

_Description_: This chapter will discuss the need for meta-programming and under what circumstances that it will be most useful.  It will provide several use cases for macros and the use of eval function.

Main Chapter Headings (3-5):

1. Why meta-programming?

2. Macros

3. Code generation

Skills Learned:

1. Articulate when to use meta-programming techniques

2. Design macros that runs in the parent execution context

3. Reduce boilerplates by code generation techniques

### Part 3. Design Patterns

The objective of this part is provide an inventory of well known traditional design patterns as well as the more modern Julia-specific design patterns.  The reader will learn how to properly apply these patterns in various problems.

#### Chapter 5. Object-Oriented Traditional Patterns

_Objective_: The reader will learn some of the most common traditional design patterns from the world of object-oriented programming and how to apply them in Julia programming language.

_Level_: Intermediate

_Description_: This chapter will bring together traditional design patterns that are widely publicized and used in object-oriented languages for building enterprise-class applications.  It will discuss how some of these patterns are relevant or irrelevant for Julia programmers. It will also demonstrate some examples of how they can be implemented in Julia.

Main Chapter Headings (3-5):

1. Creational Patterns

2. Structural Patterns

3. Behavioral Patterns

Skills Learned:

1. Articulate the need for creational patterns and how to apply them in Julia

2. Articulate the need for structural patterns and how to apply them in Julia

3. Articulate the need for behavioral patterns and how to apply them in Julia

#### Chapter 6. Reusability Patterns

_Objective_: The reader will learn a set of design patterns that are related to reusability and extendability of modules and components.

_Level_: Intermediate

_Description_: This chapter will cover several reusability patterns.

Main Chapter Headings (3-5):

1. Method Forwarding Pattern

2. Holy Trait Pattern

3. Parametric Type Pattern

4. Generic Function Pattern

Skills Learned:

1. How to leverage method forwarding pattern in a composite type. 

2. How to use the Holy Trait pattern to implement trait-specific behavior.

3. How to parameterize types for maximum reusability.

4. How to leverage generic functions to extend existing behavior. 

#### Chapter 7. Performance Patterns

_Objective_: The reader will learn some patterns related to improving system performance.

_Level_: Intermediate

_Description_: This chapter will cover patterns that make the compiler generate more efficient code as well as ones that allows programs to be more memory efficient. 

Main Chapter Headings (3-5):

1. Constant Global Pattern

2. Struct of Arrays Pattern

3. Memory Map Pattern

4. Shared Memory Pattern

Skills Learned:

1. How to use constant globals for optimal performance.

2. How to turn array of structs into structs of arrays.

3. How to deal with large data sets with limited memory.

4. How to utilize shared memory across multiple parallel processes.

#### Chapter 8. Maintainability Patterns

_Objective_: The reader will learn

_Level_: Intermediate

_Description_: This chapter will cover 

Main Chapter Headings (3-5):

1. Sub-Module Pattern

2. Keyword Definition Pattern

3. Boilerplate Reduction Pattern

4. Domain Specific Language Pattern

Skills Learned:

1. How to use sub-modules to break down large codebase effectively.

2. How to use the keyword definition macro to assign default values to struct members.

3. How to reduce boilerplate code using macros.

4. How to design domain specific language for optimal readability.

#### Chapter 9. Safety Patterns

_Objective_: The reader will learn about various patterns related to writing safe code.

_Level_: Intermediate

_Description_: This chapter will cover several patterns that can be used encapsulate data or functions.  Also, it gets into more details about the nothing-ness and missing-ness patterns for representing programmer's null and unknown data respectively.  Finally, it presents the let-scope pattern for avoid leaked variables.

Main Chapter Headings (3-5):

1. Accessor Pattern

2. Minimum Exposure Pattern

3. Minimum Dependency Pattern

4. Nothing-ness Pattern

5. Missing-ness Pattern

6. Let-Scope Pattern

Skills Learned:

1. How to design clean interface using accessors.

2. How to limit exposure of internal state to external code.

3. How to limit external dependency and conflicts.

4. How to use `nothing` effectively.

5. How to use `missing` effectively.

6. How to limit variable leakage using let-block's.

#### Chapter 10. Miscellaneous Patterns

_Objective_: The reader will learn about miscellaneous patterns that are useful but does not fall into any of the categories in the above.

_Level_: Intermediate

_Description_: This chapter will cover singleton types and how it can be used for dynamic dispatch use cases.  It then describes the re-export pattern for exposing dependent package functions, mocking pattern for improving testability, and return status pattern as an alternative method for exception handling.

Main Chapter Headings (3-5):

1. Singleton Type Dispatch Pattern

2. Re-export Pattern

3. Mocking Pattern

4. Return Status Pattern

Skills Learned:

1. How to use singleton type for dynamic dispatch use cases.

2. How to expose dependent module's functions.

3. How to improve testability by using mock data.

4. How to use return status for reporting both positive and negative statuses and respective results.

#### Chapter 11. Anti-Patterns

_Objective_: The reader will learn some anti-patterns and know when to avoid them when developing Julia programs.

_Level_: Basic

_Description_:  This chapter will focus on anti-patterns.  It will cover patterns that are known to destroy performance e.g. type instability. In addition, it describes the type piracy pattern, which can lead to system instability or non-deterministic results.
 
Main Chapter Headings (3-5):

1. Untyped Struct Members Anti-Pattern

2. Abstract Struct Members Anti-Pattern

3. Type Piracy Anti-Pattern

Skills Learned:

1. How to avoid performance issue that arises from untyped struct members.

2. How to avoid performance issue that arises from abstract struct members.

3. How to avoid system instability introduced from type piracy code.

### Part 4. Advanced Topics

The objective of this part is to provide a more in-depth analysis about the Julia language.  Understanding these advanced concepts would help readers come up with better designs.

#### Chapter 12. Behavioral Inheritance

_Objective_: The reader will learn about how behavioral inheritance differs from structural inheritance.

_Level_: Advanced

_Description_:  This chapter will discuss Julia unique design of inheritance that sets it apart from ordinary object-oriented programming languages.  

Main Chapter Headings (3-5):

1. Structural inheritance

2. Behavioral inheritance 

3. Pros and Cons

Skills Learned:

1. Understand what structural inheritance means and its applications

2. Understand behavioral inheritance and its applications 

3. Appreciate Julia's unique design by knowing the pros/cons of each approach

#### Chapter 13. Invariant Parametric Types

_Objective_: The reader will learn more about parametric types in greater details.

_Level_: Advanced

_Description_:  This chapter will discuss Julia unique design of parametric types that sets it apart from ordinary object-oriented programming languages.  

Main Chapter Headings (3-5):

1. Parametric Types Revisited

2. Pros and Cons

Skills Learned:

1. Understand the implication of parametric types being invariant.

2. Appreciate Julia's unique design by knowing the pros/cons of invariant, covariant, and contra-variant.
