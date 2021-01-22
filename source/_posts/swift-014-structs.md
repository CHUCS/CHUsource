---
title: Swift 014 Structs
keywords: swift 014 structs
date: 2021-01-22 13:31:13
categories: Swift tutorials
tags:
    - swift
---
# 結構
`Struct`可以將多個元素包裝再一起，一但創建了結構，就可以通過下面方式讀取對應屬性。
<!-- more -->
```swift
struct Point {
    var x: Int
    var y: Int
}

let pointA = Point(x: 1, y: 2)
let pointB = Point(x: 3, y: 4)

print("\(pointA.x)")
print("\(pointA.y)")

```