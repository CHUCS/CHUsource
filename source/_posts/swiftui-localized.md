---
title: SwiftUI Localized
keywords: swiftui localized
date: 2021-01-22 13:23:48
categories:
tags:
---
# SwiftUI 根據Localized切換語言

Localized.strings file
```
widget_upcoming = "即將到來"
widget_upcoming = "UPCOMING"
```
<!-- more -->
顯示範例
```swift
struct todoList: View {
    let widget_upcoming = NSLocalizedString("widget_upcoming", comment: "UPCOMING")
    var body: some View {
      Text(widget_upcoming)
    }
}
```