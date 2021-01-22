---
title: Swift 007 Conditional Statements
keywords: swift 007 conditional statements
date: 2021-01-22 13:29:05
categories: Swift tutorials
tags:
    - swift
---
# 判斷式
可以利用if else 來判斷變數，而在if後面的判斷中永遠只檢查是否是對的，而大括弧內的則是判斷通過條件後所執行的程式碼，你可以在裡面寫下任何想要執行的程式。
<!-- more -->
```swift
var price: String
var person = "Davis"


if person == "Davis" {
    price = "100"
} else if person == "Joy" {
    price = "200"
}
```

如果想要多個判斷的話我們可以使用&&和||，&&代表兩邊的成立，||則代表只要有一邊成立就成立。
```swift
var toolA = true
var toolB = false

if toolA && toolB {
    price = 1000
} else if toolA || toolB {
    price = 2000
}else{
    price = 999
}
```
我們還可以使用!來將原本的變數變成相反的。
```swift
var toolC = true
var toolD = false

if toolC && !toolD {
    price = 1000
}else{
    price = 9999
}
```

