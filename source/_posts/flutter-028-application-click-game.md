---
title: Flutter 028 - Application Click Game (part12)
keywords: flutter-028-application-click-game
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 22:06:19
---
### 前言
Hi, 我是魚板伯爵今天要把按下螢幕時觸發的事件接上去，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day28)
<!-- more -->
#### 需要具備知識
- [基本元件應用](https://chucs.github.io/flutter-001-root)
- [專案架構 (Domain Driven Design)](https://chucs.github.io/flutter-017-domain-driven-design)
- [管理程式碼好幫手 ( Bloc )](https://chucs.github.io/flutter-013-bloc)
- [大海撈針不是辦法 ( Dartz )](https://chucs.github.io/flutter-015-dartz)

### Count：Event
按下螢幕時IncrementEvent事件觸發並把數字傳進來。

```dart
part of 'count_bloc.dart';

abstract class CountEvent extends Equatable {
  const CountEvent();

  @override
  List<Object> get props => [];
}

class IncrementEvent extends CountEvent {
  final int count;

  const IncrementEvent(this.count);

  @override
  List<Object> get props => [count];
}

```

### Count：State
將計數器切成三個階段，初始數字、計數成功和計數失敗，成功的時候就會回傳加一的結果。

```dart
part of 'count_bloc.dart';

abstract class CountState extends Equatable {
  const CountState();

  @override
  List<Object> get props => [];
}

class CountInitial extends CountState {
  final int count = 0;

  @override
  List<Object> get props => [count];
}

class CountSuccess extends CountState {
  final int count;

  const CountSuccess(this.count);

  @override
  List<Object> get props => [count];
}

class CountFailure extends CountState {}

```

### Count：Bloc
IncrementEvent事件觸發時把數字傳進來加一然後回傳加一結果。

```dart
import 'dart:async';
import 'dart:developer';

import 'package:bloc/bloc.dart';
import 'package:equatable/equatable.dart';
import 'package:stunning_tribble/infrastructure/count/count_repository.dart';

part 'count_event.dart';
part 'count_state.dart';

class CountBloc extends Bloc<CountEvent, CountState> {
  CountRepository _countRepository;
  CountBloc({required CountRepository countRepository})
      : _countRepository = countRepository,
        super(CountInitial());

  @override
  Stream<CountState> mapEventToState(
    CountEvent event,
  ) async* {
    if (event is IncrementEvent) {
      yield* _mapIncrementToState(event.count);
    }
  }

  Stream<CountState> _mapIncrementToState(int _count) async* {
    final increment = await _countRepository.increment(_count);
    yield* increment.fold(
      (countFailure) async* {
        log("$countFailure");
        yield CountFailure();
      },
      (count) async* {
        yield CountSuccess(count);
      },
    );
  }
}

```

### Note
距離遊戲完成就剩最後幾步了。