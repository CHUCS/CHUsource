---
title: flutter 005 - 垂直佈局容器 ( Column )
keywords: flutter-005-column
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:38:10
---
### 前言
Hi, 我是魚板伯爵今天要教大家 Column 這個容器，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/triathlon_flutter/tree/master/day05)
<!-- more -->
### 常用屬性
Column裡面的容器會以水平方式排列，`mainAxisAlignment`控制縱向對齊，`crossAxisAlignment`則是以橫向對齊，下面範例是置中。

```dart
class DemoColumn extends StatelessWidget {
  const DemoColumn({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Column(
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

![](https://raw.githubusercontent.com/Daviswww/triathlon_flutter/master/day05/image/peWco3y.png)
