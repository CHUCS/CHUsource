---
title: Flutter 025 - Application Authentication (part9)
keywords: flutter-025-application-authentication
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 22:02:54
---
### 前言
Hi, 接著就是來驗證登入狀態，如果已經登入就跳轉到首頁否則就在登入畫面，看完我這句話就知道要使用Bloc了，只要是畫面與功能就要使用到Bloc。以上是一個基本的狀態你還可以檢查有沒有重複登入等...。

> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day25)
<!-- more -->
#### 需要具備知識
- [基本元件應用](https://chucs.github.io/flutter-001-root)
- [專案架構 (Domain Driven Design)](https://chucs.github.io/flutter-017-domain-driven-design)
- [管理程式碼好幫手 ( Bloc )](https://chucs.github.io/flutter-013-bloc)
- [大海撈針不是辦法 ( Dartz )](https://chucs.github.io/flutter-015-dartz)

### Authentication：Event
事件分成三個，AppStarted用於開啟APP時觸發的事件，用來檢查有沒有登入，如果沒有就跳轉到登入介面，LoggedIn用於登入成功時觸發把`未登入狀態`切換成`已登入狀態`，最後就LoggedOut是登出按鈕觸發時使用，將`已登入`狀態切換成`未登入狀態`。
```dart
part of 'authentication_bloc.dart';

abstract class AuthenticationEvent extends Equatable {
  const AuthenticationEvent();

  @override
  List<Object> get props => [];
}

class AppStarted extends AuthenticationEvent {}

class LoggedIn extends AuthenticationEvent {}

class LoggedOut extends AuthenticationEvent {}

```

### Authentication：State
狀態可以分成兩個，未認證與認證，如果認證成功就切換到首頁否則就停留在登入畫面。

```dart
part of 'authentication_bloc.dart';

abstract class AuthenticationState extends Equatable {
  const AuthenticationState();

  @override
  List<Object> get props => [];
}

class AuthenticationInitial extends AuthenticationState {}


class Authenticated extends AuthenticationState {
  final String displayName;

  const Authenticated(this.displayName);

  @override
  List<Object> get props => [displayName];
}

class Unauthenticated extends AuthenticationState {}

```

### Authentication：Bloc
判斷三個事件所要觸法的功能，寫到這邊時大家應該都對這個架構感覺了吧，是不是覺得越來越美了呢。

```dart
import 'dart:async';
import 'dart:developer';

import 'package:bloc/bloc.dart';
import 'package:equatable/equatable.dart';
import 'package:stunning_tribble/infrastructure/auth/auth_repository.dart';

part 'authentication_event.dart';
part 'authentication_state.dart';

class AuthenticationBloc
    extends Bloc<AuthenticationEvent, AuthenticationState> {
  final AuthRepository _userRepository;

  AuthenticationBloc({
    required AuthRepository userRepository,
  })  : _userRepository = userRepository,
        super(AuthenticationInitial());

  @override
  Stream<AuthenticationState> mapEventToState(
    AuthenticationEvent event,
  ) async* {
    if (event is AppStarted) {
      yield* _mapAppStartedToState();
    } else if (event is LoggedIn) {
      yield* _mapLoggedInToState();
    } else if (event is LoggedOut) {
      yield* _mapLoggedOutToState();
    }
  }

  Stream<AuthenticationState> _mapAppStartedToState() async* {
    final isSignedIn = await _userRepository.isSignedIn();
    yield* isSignedIn.fold(
      (failure) async* {
        log("$failure");
        yield Unauthenticated();
      },
      (isSignedInSuccess) async* {
        yield* _mapLoggedInToState();
      },
    );
  }

  Stream<AuthenticationState> _mapLoggedInToState() async* {
    final user = await _userRepository.getUser();
    yield* user.fold(
      (failure) async* {
        log("$failure");
        yield Unauthenticated();
      },
      (user) async* {
        yield Authenticated(user.displayName.toString());
      },
    );
  }

  Stream<AuthenticationState> _mapLoggedOutToState() async* {
    final signOut = await _userRepository.signOut();
    yield* signOut.fold(
      (failure) async* {
        log("$failure");
        yield Unauthenticated();
      },
      (r) async* {
        yield Unauthenticated();
      },
    );
  }
}

```