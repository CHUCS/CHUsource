---
title: Flutter 026 - Presentation Login & Splash Screen (part10)
keywords: flutter-026-presentation-login
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 22:03:45
---
### 前言
Hi, 今天就是把之前寫的一堆功能放到Screen裡面，由於是UI的部分所以程式碼會很長，有些地方我只會擷取片段，建議大家看完整程式碼。
> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day26)
<!-- more -->
#### 需要具備知識
- [基本元件應用](https://chucs.github.io/flutter-001-root)
- [專案架構 (Domain Driven Design)](https://chucs.github.io/flutter-017-domain-driven-design)
- [管理程式碼好幫手 ( Bloc )](https://chucs.github.io/flutter-013-bloc)
- [大海撈針不是辦法 ( Dartz )](https://chucs.github.io/flutter-015-dartz)

### Splash Screen
把首頁的MultiBlocProvider加上AuthenticationBloc，並觸發事件AppStarted()來檢查是否有登入過。

```dart
// main.dart

BlocProvider(
  create: (context) => AuthenticationBloc(
    authRepository: authRepository,
  )..add(AppStarted()),
),
```

把這個畫面設置成初始畫面，然後當事件觸發後BlocListener會監聽AuthenticationBloc現在的狀態進行頁面切換。

```dart
class SplashScreen extends StatelessWidget {
  const SplashScreen({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return BlocListener<AuthenticationBloc, AuthenticationState>(
      listener: (context, state) {
        if (state is Unauthenticated) {
          context.replaceRoute(LoginScreen());
        }
        if (state is Authenticated) {
          context.replaceRoute(HomeScreen());
        }
      },
      child: Scaffold(
        backgroundColor: Theme.of(context).backgroundColor,
      ),
    );
  }
}

```

### Login Screen
在`LoginScreen`這邊一樣加一個`AuthenticationBloc`監聽器，檢查是否登入成功取得驗證。

```dart
class LoginScreen extends StatelessWidget {
  const LoginScreen({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return BlocListener<AuthenticationBloc, AuthenticationState>(
      listener: (context, state) {
        if (state is Authenticated) {
          context.replaceRoute(HomeScreen());
        }
      },
      child: Scaffold(
        backgroundColor: Theme.of(context).backgroundColor,
        body: Container(
          width: MediaQuery.of(context).size.width,
          height: MediaQuery.of(context).size.height,
          child: Stack(
            alignment: Alignment.center,
            children: [
              Positioned(
                top: 200,
                child: Text(
                  "Hello",
                  style: Theme.of(context).textTheme.bodyText1,
                ),
              ),
              Positioned(
                top: 370,
                child: BlocProvider(
                  create: (context) =>
                      SignInBloc(authRepository: AuthRepository()),
                  child: LoginFrom(),
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```

### Login From
創建`SignInBloc`然後在`LoginForm`裡面寫一個`SignInBloc`的監聽器來檢查登入成功或失敗，如果登入成功的話就觸法`LoggedIn`的事件。

```dart
Positioned(
    top: 370,
    child: BlocProvider(
      create: (context) =>
          SignInBloc(authRepository: AuthRepository()),
      child: LoginFrom(),
    ),
),
```

```dart
class LoginFrom extends StatelessWidget {
  const LoginFrom({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return BlocListener<SignInBloc, SignInState>(
      listener: (context, state) {
        if (state is SignInStateSuccess) {
          BlocProvider.of<AuthenticationBloc>(context).add(LoggedIn());
        }
        if (state is SignInStateFailure) {
          // TODO: Display a snackbar
        }
      },
      child: Column(
        children: [
          GoogleSignInButton(),
        ],
      ),
    );
  }
}
```
![](https://raw.githubusercontent.com/Daviswww/stunning_tribble/day26/assets/images/ZcRe5Cm.png)

### Home Screen
在首頁檢查驗證登入狀態，然後在登出按鈕(左上角的小啤酒)新增LoggedOut事件。
```dart
return BlocListener<AuthenticationBloc, AuthenticationState>(
  listener: (context, state) {
    if (state is Unauthenticated) {
      context.replaceRoute(LoginScreen());
    }
  },
```

```dart
class SignOutButton extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return IconButton(
      onPressed: () {
        BlocProvider.of<AuthenticationBloc>(context).add(LoggedOut());
      },
      icon: Icon(
        Icons.sports_bar_rounded,
        color: Theme.of(context).shadowColor,
        size: 30,
      ),
    );
  }
}
```

![](https://raw.githubusercontent.com/Daviswww/stunning_tribble/day26/assets/images/iuheepo.gif)