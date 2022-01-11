---
title: Flutter 022 - Infrastructure Authentication (part6)
keywords: flutter-022-infrastructure-authentication
categories: Flutter tutorials
tags:
  - flutter
date: 2021-12-31 21:59:22
---
### 前言
Hi, 今天要把登入的Repository寫好備用，教學內容只會擷取片段程式碼，建議大家搭配完整程式碼來練習。

> [完整程式碼](https://github.com/Daviswww/stunning_tribble/tree/day22)
<!-- more -->
### 安裝
```yaml
google_sign_in: ^5.0.5
firebase_auth: ^3.0.1
firebase_core: ^1.4.0
```

### Google 登入
在登入時會有三個功能，第一個是按按鈕的時候觸發的google登入和第二個登出，第三個則是在開啟app時檢查有沒有登入過，有的話就可以跳過登入畫面，如果還不知道Google登入怎麼設定的可以到[Day16 - Google登入教學](https://ithelp.ithome.com.tw/articles/10259691)。

```dart
abstract class AuthRepositoryImpl {
  Future<bool> signInWithGoogle();
  Future<void> signOut();
  Future<bool> isSignedIn();
}

class AuthRepository implements AuthRepositoryImpl {
  final FirebaseAuth _firebaseAuth;
  final GoogleSignIn _googleSignIn;

  AuthRepository()
      : _firebaseAuth = FirebaseAuth.instance,
        _googleSignIn = GoogleSignIn();

  @override
  Future<bool> signInWithGoogle() async {
    final GoogleSignInAccount? googleUser = await _googleSignIn.signIn();
    if (googleUser == null) {
      return false;
    }
    final GoogleSignInAuthentication googleAuth =
        await googleUser.authentication;
    final AuthCredential credential = GoogleAuthProvider.credential(
      accessToken: googleAuth.accessToken,
      idToken: googleAuth.idToken,
    );
    await _firebaseAuth.signInWithCredential(credential);

    return true;
  }

  @override
  Future<void> signOut() async {
    Future.wait([
      _firebaseAuth.signOut(),
      _googleSignIn.signOut(),
    ]);
  }

  @override
  Future<bool> isSignedIn() async {
    try {
      final User? currentUser = _firebaseAuth.currentUser;
      if (currentUser != null) {
        return true;
      } else {
        return false;
      }
    } catch (_) {
      return false;
    }
  }
}

```