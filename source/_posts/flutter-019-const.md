---
title: Flutter 019 - Const Shared (part3)
keywords: flutter-019-const
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:55:59
---
### 前言
Hi, 我是魚板伯爵今天要介紹Const，利用它來宣告一些重複使用且不變的值，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day19)
<!-- more -->
### Const
Const 在 Flutter 扮演著重要的角色，當你使用`const`的變數時，只要在 APP 的生命週期中他永遠不會改變，因此它只會創建一次，這可以降低一些不必要的資源。

```dart
const String word = "Hello world";
```


### 魚板範例
在寫Flutter時常常會重複使用一些顏色、字體和圖片，我們可以創建一個檔案將這些宣告成一個變數以便我們重複使用。

```dart
import 'package:flutter/material.dart';

const Color oil1Color = Color(0xFFFBF5EF);
const Color oil2Color = Color(0xFFF2D3AB);

const Color oil3Color = Color(0xFFC69FA5);
const Color oil4Color = Color(0xFF8B6D9C);

const Color oil5Color = Color(0xFF494D7E);
const Color oil6Color = Color(0xFF272744);

```

```dart
class Home extends StatelessWidget {
  const Home({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: oil2Color,
      body: Center(
        child: Text("Hello"),
      ),
    );
  }
}
```
![](https://raw.githubusercontent.com/Daviswww/stunning_tribble/day19/assets/images/TyCb6wo.png)
