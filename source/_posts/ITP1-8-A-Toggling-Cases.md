---
title: AOJ ITP1_8_A
keywords: ITP1_8_A Toggling Cases
date: 2020-06-14 12:31:23
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_8_A - Toggling Cases
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_8_A)

#### 題意:
把字串的內英文字母小轉大，大轉小。
<!-- more -->
#### 思路:
用getline(cin ,str)讀取整行包含空白，isalpha判斷是否為英文如果不為就輸出那個字元，如果是的話判斷他是小寫還是大寫並轉換。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/efba99d8da45aad2f6d8fbc67cf22213.js"></script>