---
title: SwiftUI Stack
keywords: swiftui stack
date: 2020-07-14 12:04:13
categories: SwiftUI tutorials
tags:
    - swiftui
---
# SwiftUI Stack 堆疊方式
在SwiftUI中有三種堆疊分別為VStack、ZStack和HStack，這些堆疊可以讓顯示的東西以不同的方式呈現。
<!-- more -->
## VStack 縱向堆疊
VStack可以使文字逐一縱向的堆疊。
```swift
VStack() {
    Text("Hello")
    Text("SwiftUI")
}
```
顯示的結果為：
Hello
SwiftUI

## HStack 橫向堆疊
HStack可以使文字逐一橫向的堆疊。
```swift
HStack() {
    Text("Hello")
    Text("SwiftUI")
}
```
顯示的結果為：
Hello SwiftUI

## ZStack 重疊
HStack可以使文字重疊。
```swift
ZStack() {
    Text("Hello")
    Text("SwiftUI !!")
}
```

## alignment與spacing 校準與間距
alignment可以控制校準的位置，你可以把VStack內的東西靠左靠右等等等...。spacing可以控制每個區塊距離。
```swift
VStack(alignment: .leading, spacing: 50) {
    Text("Hello")
    Text("SwiftUI !!")
}
```

## 多個Stack
你可以使用多個堆疊來表現不同的樣式，例如下面代碼。

```swift
HStack(){
    VStack() {
        Text("1. Hello")
        Text("SwiftUI")
    }
    VStack() {
        Text("2. Hello")
        Text("SwiftUI")
    }
}
```