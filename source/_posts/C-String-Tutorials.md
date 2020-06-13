---
title: String Tutorials
date: 2020-04-15 13:48:58
keywords: C++ String tutorials
categories: C++ tutorials
tags:
    - tutorials
    - cpp
---
# C++ String Tutorials
### #字串
+ C++
+ #include <string>
+ using namespace std;
+ string宣告，是一個class
+ 可以用cin直接輸入
+ 跟陣列一樣支援[]存取
<!-- more -->
### #常用功能

> length()回傳長度。

> 支援+、+=，可以直接串接字串。

> erase(p, n)，從第p格開始移除n個字。

> substr(p, n)，從第p格開始拿出n個字作為子字串回傳。

> find(str)，找出第一次出現str是在第幾格，以str[0]為回傳位置，找不到會回傳string::npos。

> 要輸入包含空白的字串的話使用getline(cin, str)，跟整數輸入混合使用時要注意getline有可能會擷取到前面輸入的換行。

<script src="https://gist.github.com/Daviswww/75d830723ac386c2ab333899af69b9d2.js"></script>