---
title: SwiftUI Color
keywords: swiftui color
date: 2020-07-14 11:44:25
categories: SwiftUI tutorials
tags:
    - swiftui
---
# SwiftUI Hex Color 十六進至顏色轉換
如果想要使用hex的色碼的話可以先定義好轉換方式，之後只需要設定Color裡面的hex就可以轉換成想要的顏色。當然你必須先定義好你的函式。
<!-- more -->
首先你需要在extension定義好色碼轉換方法，例如下面的代碼。

```swift
import SwiftUI

extension Color {
    static let cloloABC = Color(hex: "#FFFFFF", alpha: 0.5)

    init(hex: String, alpha: CGFloat = 1.0) {
        var hex = hex.trimmingCharacters(in: CharacterSet.alphanumerics.inverted)
        if hex.hasPrefix("#") {
            hex = String(hex.dropFirst())
        }
        assert(hex.count == 3 || hex.count == 6 || hex.count == 8, "Invalid hex code used. hex count is #(3, 6, 8).")
        var int: UInt64 = 0
        Scanner(string: hex).scanHexInt64(&int)
        let r, g, b: UInt64
        switch hex.count {
        case 3: // RGB (12-bit)
            (r, g, b) = ((int >> 8) * 17, (int >> 4 & 0xF) * 17, (int & 0xF) * 17)
        case 6: // RGB (24-bit)
            (r, g, b) = (int >> 16, int >> 8 & 0xFF, int & 0xFF)
        case 8: // ARGB (32-bit)
            (r, g, b) = (int >> 16 & 0xFF, int >> 8 & 0xFF, int & 0xFF)
        default:
            (r, g, b) = (1, 1, 0)
        }

        self.init(
            .sRGB,
            red: Double(r) / 255,
            green: Double(g) / 255,
            blue:  Double(b) / 255,
            opacity: Double(alpha)
        )
    }
}
```
定義完成後，你可以在ContentView裡面直接使用。
```swift
Text("Hello, World!")
    .foregroundColor(Color.init(hex: "#FFFFFF", alpha: 1.0))
```
也可以定義在extension內這樣就可以直接使用而且不必重新設定色碼。
```swift
Text("Hello, World!")
    .foregroundColor(Color.cloloABC)
```