---
title: Flutter 006 - 置中容器 ( Center )
keywords: flutter-006-center
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:39:51
---
### 前言
Hi, 我是魚板伯爵今天要教大家 Center 這個元件，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/triathlon_flutter/tree/master/day06)
<!-- more -->
### Center 容器
想讓元件置中的話，可以使用 Center。

```dart
class DemoCenter extends StatelessWidget {
  const DemoCenter({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Center(
      child: Container(
        width: 100,
        height: 100,
        color: Colors.amber,
      ),
    );
  }
}
```
![](https://raw.githubusercontent.com/Daviswww/triathlon_flutter/master/day06/image/DrT35ku.png)