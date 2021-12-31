---
title: Flutter 030 - App Icon (part14)
keywords: flutter-030-application-icon
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 22:08:04
---
### 前言
Hi, 我是魚板伯爵今天鐵人賽的最後一天了感謝大家的支持，不知道大家對這個架構是不是有一點感覺了，雖然因為時間的關西很可惜沒機會教大家如何寫測試，如果加測試可能還要再加個好幾天，不過你已經學會了60%的基本概念，要開發一個APP基本上沒有問題，在教學的最後要教大家如更改App的圖示。
<!-- more -->
#### 需要具備知識
- [基本元件應用](https://chucs.github.io/flutter-001-root)
- [專案架構 (Domain Driven Design)](https://chucs.github.io/flutter-017-domain-driven-design)
- [管理程式碼好幫手 ( Bloc )](https://chucs.github.io/flutter-013-bloc)
- [大海撈針不是辦法 ( Dartz )](https://chucs.github.io/flutter-015-dartz)

### 安裝
```yaml
dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_launcher_icons: ^0.9.2

flutter_icons:
  ios: true
  android: true
  image_path_ios: "assets/launcher/icon.png"
  image_path_android: "assets/launcher/icon.png"
```


### 生成圖片
將圖片加入資料夾中(`assets/launcher/Icon.png`)，然後輸入下面的命令，完成後重新建構專案App的圖示就會出現囉。

```bash
$ flutter pub run flutter_launcher_icons:main
```


![](https://raw.githubusercontent.com/Daviswww/stunning_tribble/master/assets/image/aytgubhj.png)

### Note:
有夢想才會進步，祝大家都可以寫出自己的APP