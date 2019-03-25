---
title: "Hands-On Design Patterns with Julia 1.0 (Outline)"
author: Tom Kwong
date: March 17, 2019
geometry: margin=1.5in
output: pdf_document
---

# SUMMARY

**Subtitle**: A comprehensive guide to create robust, reusable, performant and maintainable applications using proven design patterns.

**Author**: Tom Kwong

**Description**: 
The goal of the book is to provide solutions to a common problem and help reader become familiar with the solutions developed by experienced developers. Equipped with the knowledge of these patterns, reader will spend less time searching for a solution to a common problem and learn an efficient way to communicate. With this comprehensive guide, reader will gain a deep understanding of design patterns to create robust, reusable, performant and maintainable code.

This book will cover both traditional and modern design patterns specific to Julia programming.   These patterns are useful in any domain, including enterprise applications, data science, scientific computing, parallel and distributed computing.

**Page Count**: 320-350 pages	

_**Notes**: Some contents in the outline below are still in the early stage and could change throughout the course of authoring.  Keep in mind that all changes are made with the intention of better organization and material for the reader.  By now means that the changes will bring deviation to the intended objectives stated in the above._ 

## ABOUT THE AUTHOR

Tom Kwong (GitHub handle: tk3369) has over 25 years of software development experience.  He holds a M.S. Computer Science degree from University of California, Santa Barbara (UCSB) from 1993.  Over the years, he worked on many large-scale enterprise applications that require solid design, high performance and scalability.  He has extensive development experience in C, Java, JavaScript, PHP, Objective-C, etc. before falling in love with the Julia programming language in 2017.

Tom specializes in the financial services domain and currently works at Western Asset Management Company as a Software Engineering Manager.  He is a CFA charter holder, a prestige designation for investment management professionals.  He loves agile development and is a Certified Scrum Master (CSM).  Finally, he holds a patent for developing a bid-for-placement system for Overture Services (formerly GoTo.com), a search engine company that was acquired by Yahoo in 2003.

## Can you recommend a good technical reviewer for your book?

Confirmed:
Scott Jones (scott@gandalfsoftware.com)

_Will find more reviewers depending on how much time commitment is required._

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

1. A Brave New World
2. Julia Fundamentals
3. Design Patterns
4. Case Studies

### CHAPTER OUTLINE

>_Each chapter should have a clear focus. Each chapter title should clearly state what aspect of the overall topic the chapter deals with.. Continuing the example of Building Machine Learning Systems with Python your section on “Book Learning” might be broken down into 4 chapters as follows: “Clustering – sorting text into groups”, “Topic Modeling – creating non-exclusive groups”; “Logistic Regression – evaluating text quality”; “Bayes Classification – sentiment analysis”. PLEASE NOTE: Chapter titles appear on Amazon_

#### Part 1. A Brave New World

Page count: 10%

1. History of Design Patterns

2. Characteristics of a Well-Designed Application

3. Julia Programming Paradigm

#### Part 2. Julia Fundamentals

Page count: 15%

4. Modules and Packages

5. Types

6. Functions

7. Interfaces

8. Macros

#### Part 3. Design Patterns

Page count: 60%

9. Traditional Patterns

10. Julia Patterns

11. Julia Anti-Patterns

#### Part 4. Case Studies

Page count: 15%

12. Project X

13. Project Y

14. etc...

## PART FOUR: DETAILED OUTLINE

### Part 1. A Brave New World

The objective of this part is to introduce the reader to the use of design patterns in general and how Julia is different from the object-oriented programming paradigm.

#### Chapter 1. History of Design Patterns

_Objective_: The reader will learn some history about design patterns and an overview of the traditional patterns and design principles.

_Level_: Basic

_Description_: This chapter will provide some context about why design patterns is useful and how it has served us well in the past several decades.  It provides an overview of the the traditional "Gang-of-Four" design patterns and some of the most well-known design principles such as SOLID.

Main Chapter Headings (3-5):

1. When and how?

2. Gang-of-Four

3. Design Principles

Skills Learned:

1. History of object-oriented programming and the rise of design patterns

2. An overview of traditional design patterns 

3. An overview of commonly used design principles

#### Chapter 2. Characteristics of a Well-Designed Application

_Objective_: The reader will learn the characteristics of a well-designed application and how they relate to design patterns.

_Level_: Basic

_Description_: This chapter will discuss the characteristics of a well-designed application such as ease of maintenance, reusability, extensibility, performance, testability, safety, etc.  These concepts are important to be kept in mind when developing software. 

Main Chapter Headings (3-5):

1. Ease of maintenance

2. Reusability and Extensibility

3. Performance

4. Testability

5. Safety

Skills Learned:

1. Understand when software is easy to maintain

2. Understand why code should be reusable and be extended easily

3. Understand the benefits of high performance code

4. Understand the benefits of highly testable code

5. Understand the reason and outcome of safe code

#### Chapter 3. Julia Programming Paradigm

_Objective_: The reader will learn at a high level how the Julia programming language work differently than a traditional object-oriented language.

_Level_: Intermediate

_Description_:  This chapter will discuss several major differences between Julia and a general object-oriented programming language like Java.  This is an important chapter that provides the reader some context about Julia's unique language design before diving into actual design patterns.

Main Chapter Headings (3-5):

1. Separation of data and operations

2. Behavioral inheritance 

3. Interfaces and Traits

4. Reusable/Parametric types

Skills Learned:

1. Understand how Julia dispatch works differently than 
OOP

2. Articulate difference between behavioral inheritance vs. structural inheritance

3. Become familiar with the concepts of interfaces and traits

4. How to define and use parametric types

_**TBD**: Should this chapter come after Part 2 Julia Fundamentals since it has more advanced material?_

### Part 2. Julia Fundamentals

The objective of this part is to quickly bring the reader up to speed about the fundamental concepts and features in the Julia programming language.  A clear understanding of Julia Fundamentals is essential for the reader to fully appreciate the beauty of the design patterns in upcoming chapters.  

#### Chapter 4. Modules and Packages

_Objective_: the reader will learn how to put together source codes into a well organized structure of modules and packages.

_Level_: Basic

_Description_:  This chapter focuses on breaking down large source code into a manageable set of modules and packages.  It will discuss the benefits and possible nuances when splitting source code into decoupled components.

Main Chapter Headings (3-5):

1. The Growing Pain

2. Namespace Matters

3. Managing Dependencies 

Skills Learned:

1. Identify the signs of an organizational problem

2. Understand Julia's namespace and scoping rules

3. Ability to manage package and module dependencies effectively

#### Chapter 5. Types

_Objective_: The reader will learn about Julia's type hierarchy concepts and how to construct his/her own hierarchy for an application.

_Level_: Basic

_Description_:  This chapter will dive into Julia's type system.  It will first discuss abstract and concrete types and the respective type hierarchy.  Then, it will talk about parametric types and how helps to make the system more flexible and performant.  

Main Chapter Headings (3-5):

1. Abstract Types

2. Concrete Types

3. Parametric Types

4. Conversion 

Skills Learned:

1. Understand abstract types and the type hierarchy

2. Understand concrete types and how they are constructed

3. Ability to design parametric types

4. Learn how to convert between data types

#### Chapter 6. Functions

_Objective_: The reader will learn how to design and create various types of functions in different situations.

_Level_: Intermediate

_Description_:  This chapter will discuss various ways of defining functions in Julia.  It will also demonstrate how to use multiple dispatch and parametric functions under specific circumstances.

Main Chapter Headings (3-5):

1. Function definitions

2. Multiple Dispatch 

3. Parametric functions

Skills Learned:

1. Write functions using various kinds of arguments

2. Leverage multiple dispatch effectively

3. Design parametric functions that work with the type hierarchy

#### Chapter 7. Interfaces

_Objective_: The reader will learn how to design interfaces that models specific behaviors.

_Level_: Intermediate

_Description_: This chapter will discuss when interfaces would be desired and how one can create a generic interface that is extensible to multiple data types.  

Main Chapter Headings (3-5):

1. Modeling behaviors

2. Interface examples

3. Documentation

Skills Learned:

1. Articulate the need to formalize behavior

2. Learn how to build interfaces from examples

3. Understand the need for documenting interfaces

#### Chapter 8. Meta-programming

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

#### Chapter 9. Traditional Patterns

_Objective_: The reader will learn the traditional design patterns from the world of object-oriented programming and how to apply them in Julia programming language.

_Level_: Intermediate

_Description_: This chapter will bring together traditional design patterns that are widely publicized and used in object-oriented languages for building enterprise-class applications.  It will discuss how some of these patterns are relevant or irrelevant for Julia programmers. It will also demonstrate some examples of how they can be implemented in Julia.

Main Chapter Headings (3-5):

1. Creational Patterns

2. Structural Patterns

3. Behavioral Patterns

4. Functional Patterns

5. Concurrency Patterns

Skills Learned:

1. Articulate the need for creational patterns and how to apply them in Julia

2. Articulate the need for structural patterns and how to apply them in Julia

3. Articulate the need for behavioral patterns and how to apply them in Julia

4. Articulate the need for functional patterns and how to apply them in Julia

5. Articulate the need for concurrency patterns and how to apply them in Julia

#### Chapter 10. Julia Patterns

_Objective_: The reader will learn a set of design patterns that are unique to Julia programming language.

_Level_: Intermediate

_Description_: This chapter will describe several sets of design patterns that have evolved in the past several years.  Julia is a versatile and expressive programming language.  When the language is used properly, a software engineer can develop very robust programs.

_**Notes**: This chapter will contain a lot of patterns that can be applied in various use cases and domains such as scientific computing and data science._

Main Chapter Headings (3-5):

1. Organizational Patterns

2. Reusability Patterns

3. Performance Patterns

4. Readability Patterns

5. Testability Patterns

Skills Learned:

1. Articulate the need for organizational patterns and how to apply them in Julia

2. Articulate the need for reusability patterns and how to apply them in Julia

3. Articulate the need for performance patterns and how to apply them in Julia

4. Articulate the need for readability patterns and how to apply them in Julia

5. Articulate the need for testability patterns and how to apply them in Julia

#### Chapter 11. Julia Anti-Patterns

_Objective_: The reader will learn some anti-patterns and know when to avoid them when developing Julia programs.

_Level_: Basic

_Description_:  This chapter will focus on anti-patterns.  It will cover patterns that are known to destroy performance e.g. type instability or incorrect exception handling.  

Main Chapter Headings (3-5):

1. Data Type Anti-Patterns

2. Control Flow Anti-Patterns

Skills Learned:

1. Avoid specific anti-patterns related to the design of data types

2. Avoid specific anti-patterns related to the control flow of programs


### Part 4. Case Studies

The objective of this part is demonstrate some of the best designed packages in the Julia open-source ecosystem and how design patterns are utilized in those places.  The reader will learn from real-life examples and be able to apply to similar situations in their own journey.

_**NOTE: The specific projects will be determined at a later stage.  I may choose 1, 2, or 3 projects depending on the size of the open source projects.**_

#### Chapter 12.  HTTP

_Objective_: The reader will learn from the design of the HTTP.jl package.

_Level_: Basic

_Description_:  This chapter will focus on examining some code fragments from the HTTP.jl package, which is highly modularized and uses many of the key design patterns.

Main Chapter Headings (3-5):

1. Package Organization

2. Macros 

3. Synchronization

Skills Learned:

1. How to apply Separation of Concern 

2. How to reduce boilerplate code using macros

3. How to protect critical part of code with locks

#### Chapter 13.  DataFrames

_Objective_: The reader will learn from the design of the DataFrames.jl package.

_Level_: Basic

_Description_:  This chapter will focus on examining some code fragments from the DataFrames.jl package.  

Main Chapter Headings (3-5):

1. Abstract type hierarchy

2. Generic functions 

3. Type Promotion

Skills Learned:

1. How to create a type hierarchy for extensible code 

2. How to utilize generic functions from other packages e.g. describe

3. How to convert data types using type promotion techniques