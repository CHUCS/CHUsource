---
title: Swift Type of Data
keywords: swift type of data
date: 2021-01-22 13:26:15
categories: Swift tutorials
tags:
    - swift
---
# 資料與型態
類型的宣吿可以使變數擁有一個型態，swift會根據創建時給定的型態來做分配。下面會介紹幾種型態，並做一些範例來讓你更了解。
<!-- more -->
`str`存的是字串，你可以輸入多個文字。
```swift
var name: String
name = "Davis"
```

`int`存的的是一個正整數。
```swift
var age: Int
age = 26
```

`float`和`double`分別為短的浮點數和長的浮點數，可以由輸出中看到`float`和`double`印出來的浮點數數量發現他們的差別。

```swift
var pi: Float
pi = 3.14159265359

var longpi: Double
longpi = 3.14159265359
```

`bool`只能存在`true`或是`false`。
```swift
var isTrue: Bool
isTrue = true
isTrue = false
```

