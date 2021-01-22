---
title: Swift 004 String Interpolation
keywords: swift 004 string interpolation
date: 2021-01-22 13:28:18
categories: Swift tutorials
tags:
    - swift
---
# 字串變化
字串的可以有很多種變化，我們可以宣告一個字串後利用運算符加上新的字串，我們也可以用括號`\()`來把變數放入字串中。
<!-- more -->
```swift
var str = "Hello, playground"
str + " hello1"
str += " hello2"

var age = 25
var myAge = "My age is \(age)"
```

