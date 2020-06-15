---
title: AOJ ITP1_11_C
keywords: ITP1_11_C Dice III
date: 2020-06-15 12:40:32
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_11_C - Dice III
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_11_C)

#### 題意:
比對兩顆骰子是不是一樣的。

<!-- more -->
#### 思路:
先將上下左右的翻轉寫好，比對每一面是否相同，若相同count++，如果count等於六就代表這兩顆骰子是一樣的。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/0e765d546f82f32465226327ebd1f98f.js"></script>