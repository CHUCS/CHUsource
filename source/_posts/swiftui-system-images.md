---
title: SwiftUI System Images
keywords: swift system images
date: 2021-01-22 13:18:01
categories: Swift tutorials
tags:
    - swift
---
# 顯示系統圖案
SF symbol 繪製了許多常見的圖案，很適合當遮罩，比方我們使用 SF symbols 的星星 star.fill 當遮罩，這樣就不用自己寫程式畫星星的形狀了。
<!-- more -->
```swift
struct ContentView: View {
    var body: some View {
        
        Image("friends")
            .mask(
                Image(systemName: "star.fill")
                    .resizable()
                    .scaledToFit()
        )
    }
}
```
