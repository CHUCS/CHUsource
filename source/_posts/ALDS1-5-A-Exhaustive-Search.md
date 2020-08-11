---
title: AOJ ALDS1_5_A - Exhaustive Search
keywords: ALDS1_5_A Exhaustive Search
date: 2020-07-14 16:13:31
categories: AOJ
tags:
    - implementation
---
# 全面搜索
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_5_A)

#### 題意:
給N個整數數列A，Q個整數數列M，判斷A任意數字加起來是否等於Mi，如果有輸出"yes"，否則輸出"no"。

<!-- more -->
#### 思路:
直接建一張查詢表把所有的可能加一遍並修改，之後直接查表。
累加後遞迴然後把位子移動到下一個數字。
```C++
build(sum+a[index], index+1, n);
```
把自己也改變。
build(sum, index+1, n);
#### 程式碼:
<script src="https://gist.github.com/Daviswww/ca85b1798c3535457231e0d3a4c645e9.js"></script>