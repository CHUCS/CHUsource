---
title: Swift Variables and Constants
keywords: swift variables and constants
date: 2021-01-22 13:24:47
categories: Swift tutorials
tags:
    - swift
---
# 宣告
宣告一個變數，使用var用此宣告的變數可以任意更改裡面存的值。
<!-- more -->
```swift
var name = "Davis"
name = "John"
```

若不允許修改值可使用let，注意使用let後若進行修改，則會發生錯誤。所以這個變數如果不會被修改的話，建議使用let來進行宣告。

```swift
let name = "Davis"
```