---
title: AOJ ITP1_8_C
keywords: ITP1_8_C Counting Characters
date: 2020-06-14 12:45:11
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_8_C - Counting Characters
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_8_C)

#### 題意:
計算並報告每個字母的數量。忽略字符的大小寫。 

<!-- more -->
#### 思路:
使用getline(cin, str)讀取一行包含空白，用isalpha判斷字元是否為英文，用index方式計數ary[str[i] - 'A']++。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/aec8999fda97164d2ba8a1ded029ffda.js"></script>