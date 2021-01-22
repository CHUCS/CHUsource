---
title: Swift 010 Functions
keywords: swift 010 functions
date: 2021-01-22 13:30:00
categories: Swift tutorials
tags:
    - swift
---
# 函式
函式可以幫助你將程式的區塊給打包，打包後的程式你可以重複使用，可以增加可讀性與簡潔等。
<!-- more -->
```swift
func myfunc() {
    print("I like func!!")
}
myfunc()
```
由於函式中的變數與主程式中的變數是分開的，因為在每個區域都有自己的變數，因此我們可以把變數傳入函式中來取的外部的變數。
```swift
func myProfilefunc(name: String, age: Int) {
    print("My name is \(name), age is \(age)!!")
}
myProfilefunc(name: "Davis", age: 22)
```

在變數宣告中我們可以改變輸入的名稱，前面的變數代表外面使得這個函式所使用的名稱，後面的則是函式內所使用的名稱。而第二種方法則是給他一個底線，這個底線代表任何，所以外面也不需要輸入變數名稱。

```
func myProfilefunc(myName name: String, myAge age: Int) {
    print("My name is \(name), age is \(age)!!")
}
myProfilefunc(myName: "Emily", myAge: 20)

func myProfilefunc(_ name: String, _ age: Int) {
    print("My name is \(name), age is \(age)!!")
}
myProfilefunc("Joy", 13)
```

在函式中我們有時候必須將計算完的變數回傳回主程式，就如我們剛剛所說過的每個區域都有自己的變數，因此主程式並不會拿到函式中的變數。

```swift
func piArea(r: Float) -> Float {
    let pi: Float = 3.14
    
    return pi * r * r
}

print("Area: \(piArea(r: 3))")
```