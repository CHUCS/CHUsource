---
title: Flutter 021 - Presentation AutoRouter (part5)
keywords: flutter-021-presentation-auto-router
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:58:13
---
### 前言
Hi, 今天要在我們的專案裡面加入場景的路由，這樣可以方便管理我們每個場景，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day19)
<!-- more -->
#### 需要準備的知識
- [Auto Router教學](https://chucs.github.io/flutter-012-auto-router)

### AutoRouter
創建一個路徑並設置為初始路徑，完成後就可以執行生成檔案的指令，你將會得到router.gr.dart檔案，並且終端機會顯示成功。

```bash
$ flutter pub run build_runner watch --delete-conflicting-outputs
```

```dart
import 'package:auto_route/auto_route.dart';
import 'package:stunning_tribble/presentation/screens/home/home_screen.dart';

@MaterialAutoRouter(
  replaceInRouteName: 'Page,Route',
  routes: <AutoRoute>[
    AutoRoute(
      page: HomeScreen,
      initial: true,
    ),
  ],
)
class $AppRouter {}
```

接著宣告一個AppRouter()傳入APP內使用，如果改完後APP報錯，重新啟動後就可以使用了。

```dart
void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await ConfigReader.initializeApp(Environment.dev);
  final AppRouter appRouter = AppRouter();
  runApp(
    MultiBlocProvider(
      providers: [
        BlocProvider(
          create: (context) => ThemeBloc(),
        ),
      ],
      child: MyApp(
        appRouter: appRouter,
      ),
    ),
  );
}
```

```dart
class MyApp extends StatelessWidget {
  final AppRouter _appRouter;

  const MyApp({
    Key? key,
    required AppRouter appRouter,
  })  : _appRouter = appRouter,
        super(key: key);

  @override
  Widget build(BuildContext context) {
    return BlocBuilder<ThemeBloc, ThemeState>(
      builder: (context, state) {
        return MaterialApp.router(
          debugShowCheckedModeBanner: ConfigReader.config().DEBUG,
          title: 'Flutter Demo',
          theme: state.themeData,
          darkTheme: ThemeData(),
          routerDelegate: _appRouter.delegate(),
          routeInformationParser: _appRouter.defaultRouteParser(),
          builder: (context, router) => router!,
        );
      },
    );
  }
}

```
