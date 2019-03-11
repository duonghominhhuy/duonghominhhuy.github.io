---
title: "Swift - Part 3: Strings and Characters"
layout: post
date: 2019-03-11 21:41
image: /assets/blog/apple-ios.png
headerImage: false
tag:
- swift
- programming
- ios
- apple
category: blog
author: huyduong
description: "Understading the Swift Strings and Characters."
---

### Introduction

A string is a series of characters, such as "hello, world" or "albatross". Swift strings are represented by the String type. The contents of a String can be accessed in various ways, including as a collection of Character values.

---

### String Literals
You can include predefined String values within your code as string literals. A string literal is a sequence of characters surrounded by double quotation marks (").
```swift
let someString = "Some string literal value"
```

---

### Multiline String Literals
Multiline string literal is a sequence of characters surrounded by three double quotation marks.
```swift
let quotation = """
The White Rabbit put on his spectacles.  "Where shall I begin,
please your Majesty?" he asked.

"Begin at the beginning," the King said gravely, "and go on
till you come to the end; then stop."
"""
```

---

### Special Characters in String Literals
String literals can include the following special characters:

- The escaped special characters \0 (null character), \\ (backslash), \t (horizontal tab), \n (line feed), \r (carriage return), \" (double quotation mark) and \' (single quotation mark).
- An arbitrary Unicode scalar value, written as \u{n}, where n is a 1–8 digit hexadecimal number (Unicode is discussed in Unicode below).

```swift
let wiseWords = "\"Imagination is more important than knowledge\" - Einstein"
// "Imagination is more important than knowledge" - Einstein
let dollarSign = "\u{24}"        // $,  Unicode scalar U+0024
let blackHeart = "\u{2665}"      // ♥,  Unicode scalar U+2665
let sparklingHeart = "\u{1F496}" // 💖, Unicode scalar U+1F496

let threeDoubleQuotationMarks = """
Escaping the first quotation mark \"""
Escaping all three quotation marks \"\"\"
"""
```

---

### Initializing an Empty String
Create an empty *String* value as the starting point for building a longer string.
```swift
var emptyString = ""               // empty string literal
var anotherEmptyString = String()  // initializer syntax
// these two strings are both empty, and are equivalent to each other

if emptyString.isEmpty {
    print("Nothing to see here")
}
// Prints "Nothing to see here"
```

---

### String Mutability
*String* can be modified (or mutated) by assigning it to a variable (in which case it can be modified), or to a constant (in which case it can’t be modified)
```swift
var variableString = "Horse"
variableString += " and carriage"
// variableString is now "Horse and carriage"
```

---

### Strings Are Value Types
If you create a new String value, that String value is copied when it’s passed to a function or method, or when it’s assigned to a constant or variable.
```swift
var firstName = "Huy"
var lastName = firstName
lastName = "Duong"
print("firstName: \(firstName) - lastName: \(lastName)")
// firstName: Huy - lastName: Duong
```

---

### Working with Characters
You can access the individual *Character* values for a *Strin*g by iterating over the string with a for-in loop:
```swift
for character in "Dog!🐶" {
    print(character)
}
// D
// o
// g
// !
// 🐶
```
*String* values can be constructed by passing an array of *Character* values as an argument to its initializer:
```swift
let catCharacters: [Character] = ["C", "a", "t", "!", "🐱"]
let catString = String(catCharacters)
print(catString)
// Prints "Cat!🐱"
```

---

### String Interpolation
String interpolation is a way to construct a new String value from a mix of constants, variables, literals, and expressions by including their values inside a string literal. 
```swift
let multiplier = 3
let message = "\(multiplier) times 2.5 is \(Double(multiplier) * 2.5)"
// message is "3 times 2.5 is 7.5"
```

---

### Unicode
Unicode is an international standard for encoding, representing, and processing text in different writing systems. It enables you to represent almost any character from any language in a standardized form, and to read and write those characters to and from an external source such as a text file or web page.
```swift
let eAcute: Character = "\u{E9}"                         // é
let combinedEAcute: Character = "\u{65}\u{301}"          // e followed by ́
// eAcute is é, combinedEAcute is é
```

---

### Counting Characters
To retrieve a count of the Character values in a string, use the count property of the string:
```swift
let unusualMenagerie = "Koala 🐨, Snail 🐌, Penguin 🐧, Dromedary 🐪"
print("unusualMenagerie has \(unusualMenagerie.count) characters")
// Prints "unusualMenagerie has 40 characters"
```

---

### Substrings
When you get a substring from a string, the result is an instance of *Substring*, not another string.
```swift
let greeting = "Hello, world!"
let index = greeting.firstIndex(of: ",") ?? greeting.endIndex
let beginning = greeting[..<index]
// beginning is "Hello"

// Convert the result to a String for long-term storage.
let newString = String(beginning)
```

---

### Comparing Strings

```swift
let quotation = "We're a lot alike, you and I."
let sameQuotation = "We're a lot alike, you and I."
if quotation == sameQuotation {
    print("These two strings are considered equal")
}
// Prints "These two strings are considered equal"
```

---

### Unicode Representations of Strings
- UTF-8 Representation
```swift
for codeUnit in dogString.utf8 {
    print("\(codeUnit) ", terminator: "")
}
print("")
// Prints "68 111 103 226 128 188 240 159 144 182 "
```
- UTF-16 Representation
```swift
for codeUnit in dogString.utf16 {
    print("\(codeUnit) ", terminator: "")
}
print("")
// Prints "68 111 103 8252 55357 56374 "
```
- Unicode Scalar Representation
```swift
for scalar in dogString.unicodeScalars {
    print("\(scalar.value) ", terminator: "")
}
print("")
// Prints "68 111 103 8252 128054 "
```

---