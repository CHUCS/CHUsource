---
title: Flutter 015 - 大海撈針不是辦法 ( Dartz )
keywords: flutter-015-dartz
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:48:06
---
### 前言
Hi, 在原本的try＆catch中我們可以截取大部分的錯誤，但是這僅能告訴我程式崩潰然後就噴一堆錯誤出來，對我來說就好像有人把整個程式丟給我說不能動一樣，因此try＆catch並不能滿足我對程式追求的完美，這就是我要介紹Dartz的原因，它可以幫助你排除掉一些問題。

本篇教學會延續上一篇[[Day14] Flutter - 怎麼串接API ( Http )](https://ithelp.ithome.com.tw/articles/10259641)的程式碼進行修改。

> [完整程式碼](https://github.com/Daviswww/triathlon_flutter/tree/master/day15)
<!-- more -->
### 安裝
```yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^0.13.3
  dartz: ^0.9.2
  equatable: ^2.0.3
```

### Folding Either
Either這個型態分成左右兩邊，左邊狀態是`錯誤`時回傳，右邊則是`成功`的時候回傳，像是這樣子`Either<Failure, User>`。

```dart
return createUser.post.fold(
  (failure) => log("$failure"),
  (post) => log("$post"),
);
```

### 修改程式碼

首先創建一些錯誤時回傳的類別，當遇到錯誤時就會丟出我們指定的訊息。

```dart
abstract class ServiceFailure extends Equatable {
  const ServiceFailure();

  @override
  List<Object> get props => [];
}

class PostFailure extends ServiceFailure {
  final code;
  final message;

  PostFailure(this.code, this.message);

  @override
  List<Object> get props => [code, message];
}

class ServerException extends ServiceFailure {
  final message;

  ServerException(this.message);

  @override
  List<Object> get props => [message];
}

```

可以看到下面回傳有left和right兩種，當我post出去結果沒有創建新的使用者時，就可以馬上知道是程式出問還是我的API出問題。

```dart
  Future<Either<ServiceFailure, User>> _createUser(
    Uri url,
    User body,
  ) async {
    try {
      final response = await client.post(
        url,
        headers: {
          'Content-Type': 'application/json',
        },
        body: body.toJson(),
      );
      if (response.statusCode == 201) {
        log(
          "${response.body}",
          name: response.statusCode.toString(),
        );
        return right(User.fromJson(response.body));
      } else {
        return left(PostFailure(
          response.statusCode,
          response.body,
        ));
      }
    } catch (e) {
      return left(ServerException(e));
    }
  }
```

### Note:
雖然他的功能有很多，但是你想要追求更完美更細節的偵錯導致綁手綁腳，那可就不是件好事了。