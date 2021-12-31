---
title: Flutter 027 - Infrastructure Click Game (part11)
keywords: flutter-027-infrastructure-click-game
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 22:04:42
---
### 前言
Hi, 我是魚板伯爵寫到這邊時不知道大家都已經非常熟練了，這次我們要來做一個有趣的小遊戲，就是點一下螢幕數字就會加一，是不是很有趣呢？

> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day27)
<!-- more -->
#### 需要具備知識
- [基本元件應用](https://ithelp.ithome.com.tw/articles/10258878)
- [專案架構 (Domain Driven Design)](https://ithelp.ithome.com.tw/articles/10259714)
- [管理程式碼好幫手 ( Bloc )](https://ithelp.ithome.com.tw/articles/10259564)
- [大海撈針不是辦法 ( Dartz )](https://ithelp.ithome.com.tw/articles/10259644)


### Repository & Domain
即便是一個小小的程式還是要照著流程走。

```dart
import 'package:equatable/equatable.dart';

class CountAddFailure extends Equatable {
  final String message;

  CountAddFailure({required this.message});

  @override
  List<Object> get props => [message];
}

```

```dart
import 'package:dartz/dartz.dart';
import 'package:stunning_tribble/domain/count/count_failure.dart';

abstract class CountRepositoryImp {
  /// Count model
  ///
  /// Increment one
  Future<Either<CountAddFailure, int>> increment(int count);
}

class CountRepository implements CountRepositoryImp {
  @override
  Future<Either<CountAddFailure, int>> increment(count) async {
    try {
      return right(++count);
    } catch (e) {
      return left(CountAddFailure(message: "$e"));
    }
  }
}
```


## Note:
應該滿有趣的吧～