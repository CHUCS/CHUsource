---
title: SwiftUI Circle
keywords: swift circle
date: 2021-01-22 13:09:47
categories: Swift tutorials
tags:
    - swiftui
---
# SwiftUI 畫一個圓餅圖

在swift中並沒有支援畫出一個圓餅圖，這邊使用了一個比較簡單的方法來達成圓餅圖，先使用drawpath來畫出一個圓圈，再將圓圈線的寬度條寬，這樣就可以輕鬆地畫出一個圓圈，當然你也可以使用套件來畫出更美的圓餅圖。
<!-- more -->
![](LE81oZ0.png)

```swift
import SwiftUI

struct ContentView: View {
    @State var dynamicSize: CGFloat = 100
    var body: some View {
        VStack{
            ZStack{
                Circle()
                  .strokeBorder(Color.red,lineWidth: 1)
                  .frame(width: 16, height: 16)
                CircleShape(angle: 120)
                    .fill(Color.blue)
            }.frame(width: 165, height: 30)
            Text("HH")
        }
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}


struct CircleShape : Shape {
    var angle: Double
    let stratAngle:Double = -90
    func path(in rect: CGRect) -> Path {
        var p = Path()
        p.addArc(center: CGPoint(x: rect.maxX/2, y:rect.maxY/2), radius:4, startAngle: .degrees(-90), endAngle: .degrees(stratAngle+angle), clockwise: false)

        return p.strokedPath(.init(lineWidth: 8))
    }
}
```

