---
title: Swift 012 Optional Chaining
keywords: swift 012 optional chaining
date: 2021-01-22 13:30:37
categories: Swift tutorials
tags:
    - swift
---
# 可選中的問號與驚嘆號
您可以通過在要調用其屬性的方法或下標的可選值之後放置問號（?）來指定可選，如果可選值不是`nil`即可使用。這非常類似於將感嘆號（!）放在可選值之後以強制展開其值。主要區別在於，問號時會正常失敗`nil`。驚嘆號會強制展開會觸發運行時錯誤`nil`。
<!-- more -->
```swift
func helloYear(year: Int) -> String? {
    switch year {
    case 2020: return "Hello 2020"
    case 2021: return "Hello 2021"
    default: return nil
    }
}

let msg = helloYear(year: 2020)
print("\(msg) swift!")
```

如果我們要再回傳回來的參數後面使用一些函式來改變參數的時候，我們可以加上`?`來確保是否有參數可以調用，如果是`nil`將會出現錯誤訊息。

```swift
func helloYear2(year: Int) -> String? {
    switch year {
    case 2020: return "Hello 2020"
    case 2021: return "Hello 2021"
    default: return nil
    }
}

let msg2 = helloYear2(year: 203)?.uppercased()
print("\(msg2) swift!")
```

如果想讓程式碼更加的安全，可以在後面加上`??`，當參數為`nil`時，將會使用`??`後面所設置的參數。


```swift
func helloYear2(year: Int) -> String? {
    switch year {
    case 2020: return "Hello 2020"
    case 2021: return "Hello 2021"
    default: return nil
    }
}

let msg2 = helloYear2(year: 203) ?? "unknown"
print("\(msg2) swift!")
```