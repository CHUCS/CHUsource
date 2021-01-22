---
title: Swift 016 Properties
keywords: swift 016 properties
date: 2021-01-22 13:31:48
categories: Swift tutorials
tags:
    - swift
---
# Properties
我們可以在struct中設置一些程式，讓他告訴我們修改了什麼資料。而在swift中提供了willSet和didSet兩個可以使用，在willSet中預設的變數名稱是newValue，didSet中預設的變數名稱是oldValue，一個是先做一個是後做，你可以根據你的喜好選則使用。
<!-- more -->
```swift
struct Person {
    var clothes: String {
        willSet {
            update(msg: "I'm changing from \(clothes) to \(newValue)")
        }
        
        didSet {
            update(msg: "I just changed from \(oldValue) to \(clothes)")
        }
    }
}

func update(msg: String) {
    print(msg)
}


var k = Person(clothes:  "T-shirts")
k.clothes = "K-shirts"
```

想要對一個變數進行修改的話可以使用get，這將會得到age後進行修改。
```swift
struct Cat {
    var age: Int
    
    var ageInPersonYears: Int {
        get {
            return age * 7
        }
    }
}


var cat = Cat(age: 12)

cat.age
cat.ageInPersonYears
```