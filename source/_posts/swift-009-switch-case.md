---
title: Swift 009 Switch Case
keywords: swift 009 switch case
date: 2021-01-22 13:29:42
categories: Swift tutorials
tags:
    - swift
---
# 選擇
在判斷中switch可以判斷你給他的一個變量做對應的case，當他完成後他會退出那個case得區塊。
<!-- more -->
```swift
let caseNum = 2

switch caseNum {
case 0:
    print("Your case number is \(caseNum)")
case 1:
    print("Your case number is \(caseNum)")
case 2:
    print("Your case number is \(caseNum)")
default:
    print("Out of case!")
}
```

也可以在case中設置一個範圍來，只要在範圍中的都屬於那個case。
```swift
let caseNumNum = 6

switch caseNumNum {
case 0...3:
    print("Your case number is \(caseNumNum)")
case 4...5:
    print("Your case number is \(caseNumNum)")
case 5...7:
    print("Your case number is \(caseNumNum)")
default:
    print("Out of case!")
}

```