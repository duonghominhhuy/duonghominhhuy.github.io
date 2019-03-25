---
title: "Swift - Part 4: Collection Types"
layout: post
date: 2019-03-26 19:30
image: \assets\blog\apple-ios.png
headerImage: false
tag:
- swift
- programming
- ios
- apple
category: blog
author: huyduong
description: "Understading the Swift Collection Types."
---

### Introduction

Swift provides three primary collection types, known as arrays, sets, and dictionaries, for storing collections of values. 
- Arrays are ordered collections of values. 
- Sets are unordered collections of unique values.
- Dictionaries are unordered collections of key-value associations.

---

### Arrays
An array stores values of the same type in an ordered list. The same value can appear in an array multiple times at different positions.
```swift
var someInts = [Int]()
print("someInts is of type [Int] with \(someInts.count) items.")
// Prints "someInts is of type [Int] with 0 items."
```

---

### Sets
A set stores distinct values of the same type in a collection with no defined ordering. You can use a set instead of an array when the order of items is not important, or when you need to ensure that an item only appears once.
```swift
var letters = Set<Character>()
print("letters is of type Set<Character> with \(letters.count) items.")
// Prints "letters is of type Set<Character> with 0 items."
```

---

### Dictionaries
A dictionary stores associations between keys of the same type and values of the same type in a collection with no defined ordering. 
Each value is associated with a unique key, which acts as an identifier for that value within the dictionary.
```swift
var namesOfIntegers = [Int: String]()
// namesOfIntegers is an empty [Int: String] dictionary
```

---