---
title: AOJ ALDS1_4_A - Linear Search
keywords: ALDS1 Linear Search
date: 2020-07-14 12:39:48
categories: AOJ
tags:
    - implementation
---
# 線性排序
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_4_A)

#### 題意:
給N個整數數列S，還有q個整數數列T，請輸出T在S裡面有找到幾個。利用線性搜索來尋找。

<!-- more -->
#### 思路:
逐一檢查，如果相等count加一然後斷開避免重複加到。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/be27322df4e6cf323429cc22b66ebcd3.js"></script>