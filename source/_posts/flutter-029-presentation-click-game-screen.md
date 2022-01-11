---
title: Flutter 029 - Presentation Click Game Screen (part13)
keywords: flutter-029-presentation-click-game-screen
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 22:07:16
---
### 前言
Hi, 今天要來創建一個CountBloc，然後就可以開始製作我們的CountButton了，我加了讓數字有彈跳的效果寫了一些動畫，有興趣的可以看原本程式碼。

> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day29)
<!-- more -->
#### 需要具備知識
- [基本元件應用](https://chucs.github.io/flutter-001-root)
- [專案架構 (Domain Driven Design)](https://chucs.github.io/flutter-017-domain-driven-design)
- [管理程式碼好幫手 ( Bloc )](https://chucs.github.io/flutter-013-bloc)
- [大海撈針不是辦法 ( Dartz )](https://chucs.github.io/flutter-015-dartz)

### CountBloc
創建一個CountBloc，把我們的按鈕畫面放進去。
```
...
BlocProvider(
    create: (context) => CountBloc(
      countRepository: CountRepository(),
    ),
    child: CountButton(),
),
...
```

然後創建一個BlocBuilder來檢查每次累加數字的狀態。
```
  @override
  Widget build(BuildContext context) {
    return BlocBuilder<CountBloc, CountState>(
      builder: (context, state) {
        return AnimatedContainer(
          .....
        );
      },
    );
  }
```

在按下按鈕時觸發CountIncrementEvent的事件，並將我們現在count的數字傳進去做累加。
```
...
  Material(
    color: Colors.transparent,
    child: InkWell(
      highlightColor: Colors.transparent,
      splashColor: Colors.transparent,
      onTap: () => _tapUp(), // onTapUp
      onTapDown: (TapDownDetails details) => _tapDown(state.count),
    ),
  ),
...
```


```
...
  void _tapDown(int count) {
    _animationController.forward();
    HapticFeedback.heavyImpact();
    BlocProvider.of<CountBloc>(context).add(CountIncrementEvent(count));
  }
...
```

![](https://raw.githubusercontent.com/Daviswww/stunning_tribble/day29/assets/images/sadjuf.gif)