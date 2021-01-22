---
title: Swift TimeIntervalSince1970
keywords: swift timeIntervalSince1970
date: 2021-01-22 13:14:59
categories: Swift tutorials
tags:
    - swift
---
# TimeIntervalSince1970 時間換算
有時您需要以特定格式計算兩個日期之間的差。例如，您可能需要了解日期之間的時差（以小時為單位）。或者，也許您想找出兩個日期之間有多少天。一種方法是使用以下方法確定兩個日期之間的秒數timeIntervalSince：
<!-- more -->
```swift
    let ddsd = Date(timeIntervalSince1970: TimeInterval(Int(truncating: tree.timestamp ?? 0)/1000))
    if(Date().timeIntervalSince(ddsd) / 86400 > 7){
    print("\(Date().timeIntervalSince(ddsd) / 86400)")
    continue
    }
```
輸出：79838.98233294487