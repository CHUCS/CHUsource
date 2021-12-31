---
title: Flutter 004 - 水平佈局容器 ( Row )
keywords: flutter-004-row
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:34:41
---
### 前言
Hi, 我是魚板伯爵今天要教大家 Row 這個容器，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/triathlon_flutter/tree/master/day04)
<!-- more -->
### 常用屬性
Row 裡面的容器會以水平方式排列，`mainAxisAlignment`控制橫向對齊，`crossAxisAlignment`則是以縱向對齊，下面範例是置中。

```dart
class DemoRow extends StatelessWidget {
  const DemoRow({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Row(
      mainAxisAlignment: MainAxisAlignment.center,
      crossAxisAlignment: CrossAxisAlignment.center,
      children: [
        Container(
          width: 50,
          height: 50,
          color: Colors.amber,
        ),
        Container(
          width: 50,
          height: 50,
          color: Colors.redAccent,
        ),
        Container(
          width: 50,
          height: 50,
          color: Colors.blueAccent,
        ),
        Container(
          width: 50,
          height: 50,
          color: Colors.cyanAccent,
        ),
        Container(
          width: 50,
          height: 50,
          color: Colors.limeAccent,
        ),
      ],
    );
  }
}
```

![](https://raw.githubusercontent.com/Daviswww/triathlon_flutter/master/day04/image/83caJhD.png)
