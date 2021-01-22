---
title: SwiftUI Text
keywords: swiftui text
date: 2020-07-13 15:47:34
categories: Swift tutorials
tags:
    - swiftui
---
## Text 用法
### 顯示簡單文字
ContentView已在中生成的範例代碼向你展示瞭如何顯示一行文字。
```swift
Text("Hello, World!")
```
<!-- more -->
### 更改字體類型
#### fontWeight 文字類型
你可以使用fontWeight來更改字體的類型，例如下面所使用的粗體字，當然字體類型有很多種像是heavy, light, medium等等等...
```swift
Text("Hello, World!")
    .fontWeight(.bold)
```

#### font 字體樣式
字體樣式中你可以修改字體的大小, 字形和大小。
```swift
Text("Hello, World!")
    .font(.title)
```
如果想要進一步修改字體的設計你可以像這樣寫：
```swift
.font(.system(.largeTitle, design: .rounded))
```
這樣寫字體就會被修成largeTitle的樣式而且是圓弧的。

該font修改器可以更改字體屬性。在上面的代碼中，我們指定使用標題字體類型以放大文本。

如果要使用固定大小的字體你只要在system裡面設定size就可以了。
```swift
.font(.system(size: 20))
```

如果想更改字體的字型的話可以使用custom來更改字型。
```swift
.font(.custom("Helvetica Neue", size: 25))
```
字體名稱可以在“字體書”中找到。您可以打開Finder應用程序，然後單擊字體簿以啟動該應用程序。
#### shadow 陰影
為文本增加陰影效果可以使字體更有感覺，而radius可以設定陰影的風格。
```swift
.shadow(color: .black, radius: 2, x: 0, y: 15)
```
### 更改字體顏色
#### foregroundColor 修改顏色
您可以使用其他內置值喜歡.red，.purple等等。如果你想知道如何使用hex色碼的話可以參考[SwiftUI Color](https://chucs.github.io/swiftui-text/)。

```swift
Text("Hello, World!")
    .foregroundColor(.red)
```

### 多個修處理多行文字飾
在SwiftUI裡支持多個修飾，你可以使用foregroundColor修改顏色fontWeight修改字體類型等等等...
```swift
Text("Hello, World!")
    .fontWeight(.bold)
    .font(.title)
```
### 處理多行文字
Text默認情況下支持多行，因此它可以顯示文本段落，而無需使用任何其他修飾符。但你可以使用一些函式來修改文本。
```swift
Text("Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!Hello, World!")
    .fontWeight(.bold)
    .font(.title)
```

#### multilineTextAlignment 修改文字位置
要使文本置中對齊，請插入multilineTextAlignment修飾符並將值設置為.center如下所示，當然你也可以靠左對齊靠右對齊。
```swift
.multilineTextAlignment(.center)
```

#### lineLimit 行數行數限制
你可能希望將行數限制為一定數量。
```swift
.lineLimit(3)
```
### 設置填充和行距
#### lineSpacing 行距調整
默認行間距足以應付大多數情況。如果要更改默認設置，可以使用lineSpacing修飾符來調整行距。
```swift
.lineSpacing(10)
```
#### padding 填充空間

如您所見，文本太靠近邊緣的左側和右側。要給它更多的空間，可以使用padding修飾符，該修飾符為文本的每一側增加一些額外的空間。
```swift
.padding()
```
如果沒有在裡面設定數字的話就會是默認的長度。如果想要設定固定長度的話可以直接帶入數字。
```swift
.padding(10)
```
在padding修飾符中也可以設定你想要哪幾個邊做增加。
```swift
.padding([.top, .leading, .trailing])
```

### 旋轉文字
#### rotationEffect 旋轉
SwiftUI框架提供了API，無論是2D還是3D都可以讓您輕鬆旋轉文本。

2D旋轉
```swift
.rotationEffect(.degrees(20), anchor: UnitPoint(x: 0, y: 0))
```
3D旋轉
```swift
.rotation3DEffect(.degrees(60), axis: (x: 1, y: 0, z: 0))
```
