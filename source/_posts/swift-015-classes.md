---
title: Swift 015 Classes
keywords: swift 015 classes
date: 2021-01-22 13:31:29
categories: Swift tutorials
tags:
    - swift
---
# 類別
在創建類別後，我們必須初始化程式，將我們的屬性提供值，有幾種可以給定預設的值，一種是直接他們默認的值，或者我們自己寫一個初始化程式，而我們自己寫一個初始化得程式是比較聰明的選擇，init是內建的一個初始化方法，我們可以在裡面初始我們的宣告的屬性等。
<!-- more -->
```swift
class Person {
    var clothes: String
    var shoes: String
    
    init(clothes: String, shoes: String) {
        self.clothes = clothes
        self.shoes = shoes
    }
}
```

在這邊我們創造一個狗的類別，這裡面包含他的名字和顏色的訊息，而我們還可以在這個類別寫一個函式狗的聲音，我們可以將著一包類別重複的使用。
```swift
class Dog {
    var name: String
    var color: String
    
    init(name: String, color: String) {
        self.name = name
        self.color = color
    }
    
    func Sing() {
        print("dog dog dog!")
    }
}

var myDog = Dog(name: "Kor", color: "blue")
myDog.name
myDog.color
myDog.Sing()
```

當我們想要建立更大一個類別時我們可以在創建一個類別，我們可以繼承類別。如果我們想要修改參數的話可以使用`override`。
```swift
class BigDog: Dog {
    override func Sing() {
        print("BigDog BigDog BigDog")
    }
}

var myBigDog = BigDog(name: "Kor", color: "blue")
myBigDog.name
myBigDog.color
myBigDog.Sing()
```

