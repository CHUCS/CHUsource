---
title: Flutter 010 - 文字輸入元件 ( TextField )
keywords: flutter-010-textfield
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:43:43
---
### 前言
Hi, 今天要教大家 TextField 這個元件，這可以讓使用者用鍵盤輸入文字，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/triathlon_flutter/tree/master/day10)
<!-- more -->
### TextField 元件，常用屬性
- `controller`：TextField控制元件可以取得相關屬性
- `keyboardType`：鍵盤的型態`TextInputType.text`(文字)、`TextInputType.text`(數字)
- `maxLines`：最大行數
- `onChanged`：當輸入有變更時會調用

```dart
class DeomBaseTextField extends StatelessWidget {
  const DeomBaseTextField({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    final TextEditingController myController = new TextEditingController();
    return Column(
      children: [
        TextField(
          controller: myController,
          keyboardType: TextInputType.text,
          maxLines: 4,
          onChanged: (String value) {
            log("${value}");
          },
        ),
        ElevatedButton(
          child: Text('送出'),
          onPressed: () {
            log("${myController.text}");
          },
        ),
      ],
    );
  }
}
```

![](https://raw.githubusercontent.com/Daviswww/triathlon_flutter/master/day10/image/j8JSFnk.png)



### TextField : decoration 客製化風格
- `contentPadding`: 文字間距
- `hintText`: 文字輸入框內提示的字
- `hintStyle`: 文字輸入框內提示字的風格
- `filled`: 是否使用背景顏色
- `fillColor`: 背景顏色
- `helperText`: 文字輸入框外的提示字
- `prefixIcon`: 左邊文字輸入框的圖示
- `suffixIcon`: 右邊文字輸入框的圖示
- `enabledBorder`: 未點擊時外框顏色
- `focusedBorder`: 點即時外框顏色
- `border`:外框顏色


```dart
InputDecoration(
      isDense: true,
      contentPadding: EdgeInsets.only(left: 15, top: 12, bottom: 12),
      hintText: hintText,
      hintStyle: TextStyle(
        color: Colors.redAccent,
      ),
      filled: true,
      fillColor: Colors.tealAccent,
      helperText: helperText,
      prefixIcon: Icon(Icons.ac_unit),
      suffixIcon: Icon(Icons.cabin_rounded),
      enabledBorder: OutlineInputBorder(
        borderSide: BorderSide(
          color: Colors.amber,
          width: 1,
        ),
      ),
      focusedBorder: OutlineInputBorder(
        borderSide: BorderSide(
          color: Colors.blueAccent,
          width: 1,
        ),
      ),
      border: OutlineInputBorder(
        borderSide: BorderSide(
          color: Colors.limeAccent,
          width: 1,
        ),
      ),
    );
```

![](https://raw.githubusercontent.com/Daviswww/triathlon_flutter/master/day10/image/MGIO6oV.png)
