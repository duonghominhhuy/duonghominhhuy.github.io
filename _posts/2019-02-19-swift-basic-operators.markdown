---
title: "Swift - Part 2: Basic Operators"
layout: post
date: 2019-02-19 21:20
image: /assets/blog/apple-ios.png
headerImage: false
tag:
- swift
- programming
- ios
- apple
category: blog
author: huyduong
description: "Understading the Swift Basic Operators."
---

### Introduction

An operator is a special symbol or phrase that you use to check, change, or combine values. For example, the addition operator (+) adds two numbers, as in let i = 1 + 2, and the logical AND operator (&&) combines two Boolean values, as in if isLoggedIn && isUpdatedProfile.

---

### Assignment Operator
The assignment operator (a = b) initializes or updates the value of a with the value of b.
```swift
let b = 10
var a = 5
a = b // a is now equal to 10

let (x, y) = (1, 2)
// x is equal to 1, and y is equal to 2
```

---

### Arithmetic Operators
Swift supports the four standard arithmetic operators for all number types: (+), (-), (*), (/).
```swift
1 + 2       // equals 3
5 - 3       // equals 2
2 * 3       // equals 6
10.0 / 2.5  // equals 4.0 

"hello, " + "world"  // equals "hello, world"
```

---

### Remainder Operator
The remainder operator (a % b) works out how many multiples of b will fit inside a and returns the value that is left over (known as the remainder).
a = (b x some multiplier) + remainder
```swift
9 % 4    // equals 1, (9 = (4 x 2) + 1)
-9 % 4   // equals -1, (9 = (4 x -2) + -1)
```

---

### Comparison Operators
Swift supports all standard C comparison operators:
- Equal to (a == b)
- Not equal to (a != b)
- Greater than (a > b)
- Less than (a < b)
- Greater than or equal to (a >= b)
- Less than or equal to (a <= b)
```swift
1 == 1   // true because 1 is equal to 1
2 != 1   // true because 2 is not equal to 1
2 > 1    // true because 2 is greater than 1
1 < 2    // true because 1 is less than 2
1 >= 1   // true because 1 is greater than or equal to 1
2 <= 1   // false because 2 is not less than or equal to 1
```

---

### Logical Operators
Logical operators modify or combine the Boolean logic values *true* and *false*.
- Logical NOT (!a)
- Logical AND (a && b)
- Logical OR (a || b)

You can also combine multiple logical operators to create longer compound expressions:
```swift
if enteredDoorCode && passedRetinaScan || hasDoorKey || knowsOverridePassword {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}
// Prints "Welcome!
```
The parentheses make the example above clearer, it’s useful to add parentheses around the first part of the compound expression to make its intent explicit:
```swift
if (enteredDoorCode && passedRetinaScan) || hasDoorKey || knowsOverridePassword {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}
// Prints "Welcome!
```

---
