---
title: Swift 018 Access Control
keywords: swift 018 access control
date: 2021-01-22 13:32:24
categories: Swift tutorials
tags:
    - swift
---
# 類別屬性限制
在創建類別時我們有時候會給屬性一些限制。public意味著每個人都可以在內部讀取和寫入屬性。private只有內部可以使用，也是最嚴格的限制。
<!-- more -->
```swift
class Cat {
    public var name: String?
    private var age: Int?
}
```