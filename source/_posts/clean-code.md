---
title: Clean Code
date: 2023-02-27 19:26:24
tags:
---
# Naming
Purpose: programmers should know what it means easily. 
* Meaningful
  - E.g. use `source` and `destination` instead of `a1` and `a2`
* Avoid disinformation
  - Do not use `accountList` if the variable is not of type `List`
* Make distinctions
  - Other people will not know easily which method to call if there are `getActiveAccount()` and `getActiveAccountInfo()`
* Pronounceable 
* Searchable
* Avoid redundant words
  - `name` instead of `nameString` as Java is typed
* Interface and implementation: `ShapeFactory` and `ShapeFactoryImpl`
* When constructors are overloaded, use static factory methods with names that describe the arguments, and make some constructors private.
  - `Complex fulcrumPoint = Complex.FromRealNumber(23.0)` instead of `Complex fulcrumPoint = new Complex(23.0)`
* Consistent
* Add meaningful context
  - `addrState` is easier to understand than `state`

# Functions
* Have few lines
* Encapsulate codes in decision points such as `if` and `while`
* Do one thing
  - Avoid flag argument
  - Error handling is one thing. If `try` exists in the function, it should be the very first word in the function and that there should be nothing after `catch` and `finally` blocks
* Have few arguments
* Output argument should be avoided
  - `StringBuffer transform(StringButter in)` is better than `void transform(StringBuffer out)`
* Avoid user having to remember the sequence of arguments
* Have no side effect
* Prefer exception to returning error codes
* Extract try/catch blocks into functions

# Comment
* Don't use a comment when you can use a function or variable
* Types
  - Explain intent
  - Clarification
  - Warning of consequences
  - TODO
  - Amplify the importance
* Avoid outdated comments because it is misleading
* Delete commented-out codes
* Avoid nonlocal information
* Avoid Javadoc in nonpublic codes

# Formatting
* Files are typically 200 lines long with an upper limit of 500.
* A file should be ordered from high-level info to low-level info
* If one function calls another, they should be vertically close, and the caller should be above the callee. 

# Object and Data Structure
* Objects expose behaviour and hide data. Data structures expose data and have no significant behaviour. Avoid creating a mix. 
* Should not ask an object about its internal

# Error Handling
* Write the try-catch-finally statement first
