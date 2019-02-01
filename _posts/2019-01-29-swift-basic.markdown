---
title: "Swift - Part 1: The Basics"
layout: post
date: 2019-01-29 11:45
image: /assets/blog/apple-ios.png
headerImage: false
tag:
- swift
- programming
- ios
- apple
category: blog
author: huyduong
description: "Understading the basic Swift syntax."
---

### Introduction

"Our goals for Swift are ambitious: we want to make programming simple things easy, and difficult things possible". According to <a href="https://swift.org" target="_blank">Swift.org</a>

---

### Constants and variables
The value of a constant can’t be changed once it’s set, whereas a variable can be set to a different value in the future.
```swift
let maximumNumberOfLoginAttempts = 10 // constants
var currentLoginAttempt = 0 // variables
```

---

### Type annotations
When declaring a constant or variable, we use type annotations to clarify the kind of values the constant or variable can store.
```swift
var welcomeMessage: String
```

---

### Comments
Comments used as noting or reminding a block of code to yourself. Swift compiler ignore comments when your code is compiled.
```swift
// This is a comment.

/* This is also a comment
but is written over multiple lines. */
```

---

### Integers
Integers are whole numbers with no fractional component, and are either signed (positive, zero, or negative) or unsigned (positive or zero).
```swift
let integerValue = 29 
```

---

### Floating-point numbers
Floating-point numbers are numbers with a fractional component, such as 3.14159, 0.1, and -273.15.
```swift
let pi = 3.14159
```

---

### Type aliases
Type aliases define an alternative name for an existing type.
```swift
typealias AudioSample = UInt16
```

---

### Booleans
Boolean values are referred to as logical, which only be true or false.
```swift
let orangesAreOrange = true
let turnipsAreDelicious = false
```

---

### Tuples:
Tuples group multiple values into a single compound value.
```swift
let http200Status = (statusCode: 200, description: "OK")
```

---

### Optionals
Optionals hold a value that may be absent.
```swift
var surveyAnswer: String?
```

---

### Error handling
Error handling use to respond to error conditions your program may encounter during execution.
```swift
func canThrowAnError() throws {
    // this function may or may not throw an error
}
```

```swift
do {
    try canThrowAnError()
    // no error was thrown
} catch {
    // an error was thrown
}
```

### Assertions and preconditions
Assertions and preconditions are checks that happen at runtime.
```swift
// This assertion fails because -3 is not >= 0.
let age = -3
assert(age >= 0, "A person's age can't be less than zero.")
```
```swift
// In the implementation of a subscript...
precondition(index > 0, "Index must be greater than zero.")
```
---

