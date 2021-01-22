---
title: Swift 008 Loop
keywords: swift 008 loop
date: 2021-01-22 13:29:21
categories: Swift tutorials
tags:
    - swift
---
# 迴圈
迴圈是為了解決重複的事情時所建構的，我們可以簡單地使用迴圈來幫助我們減少程式碼中重複的動作。例如我們可以將下面的重複動作簡化成一個簡單的回圈。
<!-- more -->
未使用回圈：
```swift
print("1 x 1 is \(1 * 1)")
print("1 x 2 is \(1 * 2)")
print("1 x 3 is \(1 * 3)")
print("1 x 4 is \(1 * 4)")
```
使用回圈後：

```swift
for i in 1...4 {
    print("1 x \(i) is \(1 * i)")
}
```

除了自己設定回圈範圍外，我們可以將資料放入設置迴圈數的地放，而temp則會逐一顯示出陣列中的內容。

```swift
var temps = ["qwe", "asd", "zxc", "rty"]
for temp in temps {
    print("Hi, \(temp)")
}
```

如果想要指定一個陣列的範圍可以使用count來得知他的數量。
```swift
var ops = ["qwe", "asd", "zxc", "rty"]
for i in 0..<ops.count {
    print("Hey, \(ops[i])")
}
```
除了上敘的for迴圈外我們還可以使用while。

```swift
var count = 5
while count > 0 {
    print("GGLA::\(count)")
    count-=1
}
```