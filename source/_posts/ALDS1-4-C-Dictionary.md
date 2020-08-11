---
title: AOJ ALDS1_4_C - Dictionary
keywords: ALDS1 Dictionary
date: 2020-07-14 14:51:04
categories: AOJ
tags:
    - implementation
---
# 字典
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_4_C)

#### 題意:
寫一個具備以下功能的字典程式:
insert str: 插入一個字串到字典裡。
find str: 找尋字串如果找到輸出"yes"，否則"no"。
<!-- more -->
#### 思路:
利用C++的map函式來加入，使用find的功能來查詢，如果沒找會輸出0，所以我們就可以放在判斷式裡面做判斷。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/0e68ebaec599b3a3b31c9e84fbac8840.js"></script>