---
title: Swift 011 Optionals
keywords: swift 011 optionals
date: 2021-01-22 13:30:19
categories: Swift tutorials
tags:
    - swift
---
# 可選
如果在不知道可選的元素是什麼的情形下，我們可以利用?來代表有可能是空的值，接著我們利用if let 的方式判斷，如果是nil就會跳掉else。
<!-- more -->

```swift
func myNameIs(name: String) -> String? {
    if name == "joy" {
        return nil
    } else {
        return "Good"
    }
}

var s : String?
s = myNameIs(name: "davis")

if let a = myNameIs(name: "davis") {
    print("\(a)")
} else {
    print("Is nil!!")
}
```

