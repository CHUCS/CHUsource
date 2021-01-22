---
title: Swift 005 Arrays
keywords: swift 005 arrays
date: 2021-01-22 13:28:32
categories: Swift tutorials
tags:
    - swift
---
# 陣列
陣列的宣告可以使的一個變數中可以儲存許多個資料，但這邊要注意的一點是資料中的型態必須要是一致的否則會出現錯誤，還有在陣列中第一個資料是從0開始計算，如下為例aryNumbers[0]就會得到2。
<!-- more -->
```swift
var aryNumbers = [2, 4, 6, 8]
aryNumbers[0]
aryNumbers[3]

var aryString = ["ABC", "DEF", "GGG"]
aryString[0]
```

如果想要儲存更多的資料可以利用append來加入新的資料。
```swift
var temp = [String]()
temp.append("Hello")
```