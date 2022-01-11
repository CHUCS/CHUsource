---
title: Flutter 017 - 實作篇：專案架構 (Domain Driven Design)
keywords: flutter-017-domain-driven-design
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:50:26
---
### 前言
Hi, 身為一個軟體工程師，我們最常見的問題就是變動的需求。而程式碼變更，就會有機會出現不可預期 Bug，有時候已經不是小拇指和食指動一動就可以解決的問題，因此設計模式可以降低程式的債務。本次專案目標就是利用DDD架構一步步帶大家寫出一個點擊小遊戲。

在這篇中給大家一些基本的概念可以在往後的實作中漸漸熟悉，如果想要更了解這個架構，可以到文章的最下面我放了幾篇推薦的文章還有一個對專案管理有幫助的影片，雖然他是用 Ruby 來講解的。
<!-- more -->
### Domain Driven Design
在這個架構在於每一層都有獨立的事情，我們可以使他們的工作分割得更乾淨，這將帶給程式乾淨、易於測試和閱讀。有的人認為小型團隊使用這種架構只會拖累開發速度，雖然我並不反對，但是壯大後會下定決心更改架構的很少，因為要改成新架構時要投入的時間可能會是好幾倍，有時候幾乎是打掉重練，這就是我想分想給大家的原因。
![](https://raw.githubusercontent.com/Daviswww/triathlon_flutter/master/day17/image/NUHhgax.png)

從上圖可以發現流程就跟蓋房子一樣，每個功能都是一棟房子不斷的循環著固定的建造流程，可以想像你的的專案就是一座城市。

### 架構優缺點
優點：
- 專注在核心業務上
- 能夠應對未來的成長
- 保護業務邏輯
- 快速找到Bug

缺點：
- 需要一個熟悉架構的人來分配
- 開發速度慢


### 資料夾結構
這是我的簡單創建的資料夾結構範例，裡面最主要包含了上面所講的`application`(infrastructure與presentation的橋樑)、`presentation`(所有場景)、`infrastructure`(功能)和`domain`(輸出資料)清楚的分類著，乾淨的資料夾可以讓你更好找到你需要的檔案，往後的教學都會遵循這個規則創建任何檔案。
```
├── lib
│   ├── application
│   │   ├── auth
│   │   │   ├── auth_bloc.dart
│   │   │   ├── auth_event.dart
│   │   │   └── auth_state.dart
│   │   └── sign_in
│   │       ├── sign_in_bloc.dart
│   │       ├── sign_in_event.dart
│   │       └── sign_in_state.dart
│   ├── config
│   │   └── environment.dart
│   ├── domain
│   │   └── failure.dart
│   ├── infrastructure
│   │   └── auth
│   │       └── auth_repository.dart
│   ├── main.dart
│   └── presentation
│       ├── router
│       │   └── router.dart
│       └── screens
│           ├── home
│           ├── login
│           └── splash
```

### 需要具備的知識
- [基本元件與套件教學](https://chucs.github.io/flutter-001-root)
- [Auto Router](https://chucs.github.io/flutter-012-auto-router)
- [Bloc](https://chucs.github.io/flutter-013-bloc)
- [Dartz](https://chucs.github.io/flutter-015-dartz)
- [Firebase Authentication & Google Sign-In ( IOS & Android )](https://chucs.github.io/flutter-016-authentication)

### 目錄
- [[Day17] Flutter - Architecture: Domain Driven Design (part1)](https://chucs.github.io/flutter-017-domain-driven-design)
- [[Day18] Flutter - Environment (part2)](https://chucs.github.io/flutter-018-environment)
- [[Day19] Flutter - Const: Shared (part3)](https://chucs.github.io/flutter-019-const)
- [[Day20] Flutter - Theme: Dark mode & Light mode (part4)](https://chucs.github.io/flutter-020-theme)
- [[Day21] Flutter - Presentation AutoRouter (part5)](https://chucs.github.io/flutter-021-presentation-auto-router)
- [[Day22] Flutter - Infrastructure Authentication (part6)](https://chucs.github.io/flutter-022-infrastructure-authentication)
- [[Day23] Flutter - Domain Error Handle (part7)](https://chucs.github.io/flutter-023-domain-error-handle)
- [[Day24] Flutter - Application Login (part8)](https://chucs.github.io/flutter-024-application-login)
- [[Day25] Flutter - Application Authentication (part9)](https://chucs.github.io/flutter-025-application-authentication)
- [[Day26] Flutter - Presentation Login & Splash Screen (part10)](https://chucs.github.io/flutter-026-presentation-login)
- [[Day27] Flutter - Infrastructure Click Game (part11)](https://chucs.github.io/flutter-027-infrastructure-click-game)
- [[Day28] Flutter - Application Click Game (part12)](https://chucs.github.io/flutter-028-application-click-game)
- [[Day29] Flutter - Presentation Click Game Screen (part13)](https://chucs.github.io/flutter-029-presentation-click-game-screen)
- [[Day30] Flutter - Flutter App Icon (part14)](https://chucs.github.io/flutter-030-application-icon)

### 推薦文章
- [An Introduction to Domain Driven Design and Its Benefits](https://apiumhub.com/tech-blog-barcelona/introduction-domain-driven-design/)
- [關於 Domain-Driven Design 以及他的魅力](https://ithelp.ithome.com.tw/articles/10216645)
- [RailsConf 2014 - All the Little Things by Sandi Metz](https://youtu.be/8bZh5LMaSmE)

### Note:
本次專案會頻繁的使用 Bloc 套件請大家熟悉。

程式碼就跟泥巴球一樣只會越滾越大，乾淨的程式可以降低維護成本。