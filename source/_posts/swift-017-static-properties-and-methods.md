---
title: Swift 017 Static Properties and Methods
keywords: swift 017 static properties and methods
date: 2021-01-22 13:32:08
categories: Swift tutorials
tags:
    - swift
---
# 靜態屬性
Static可以讓你創建一個靜態的屬性，他可以快速儲存共享數據，不需要先創建一個類別才能使用。
<!-- more -->
```swift
struct Cat {
    static var favoriteColor = "Red"
    
    var name: String
    var age: Int
}

let myCat = Cat(name: "dodo", age: 12)
print("\(Cat.favoriteColor)")
```