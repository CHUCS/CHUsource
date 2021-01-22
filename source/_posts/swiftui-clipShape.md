---
title: SwiftUI ClipShape & Clipped
keywords: swift clipShape
date: 2021-01-22 13:20:32
categories:
tags:
---
# SwiftUI 切割圖片
clipShape 的參數 shape 可傳入任何遵從 protocol Shape 的形狀，以下我們傳入內建的 Circle() 將圖片裁切成圓形。
<!-- more -->
```swift
Image(uiImage: (friend.avatarUrl?.load())!)
    .resizable()
    .aspectRatio(1, contentMode: .fit)
    .frame(width: 24, height: 24)
    .background(Color.white)
    .clipShape(Circle())
```

切割圖片邊緣
```swift
  Image(uiImage: (entry.canvasUrl?.load())!)
    .resizable()
    .aspectRatio(contentMode: .fill)
    .clipped(antialiased: true)
    .blur(radius: 4.0)
```