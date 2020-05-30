---
title: Insertion Sort
keywords: ALDS1_1_A , Insertion Sort
date: 2020-05-30 16:20:45
categories: Algorithms and Data Structures
tags:
    - sortings
---
# ALDS1_1_A - Insertion Sort
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/1/ALDS1_1_A)
<!-- more -->

#### 題意:
編寫一個插入排序算法的程序，該程序按升序對序列A進行排序。

#### 思路:
插入排序在每一次都會先刪除起始的數字，然後一直往後排直到有人大於他就插入。
範例：
5 3 2 4 | 起始數列
3 5 2 4 | 3差到5前面
2 3 5 4 | 2差到3前面
2 3 4 5 | 4差到5前面

#### 程式碼:
<script src="https://gist.github.com/Daviswww/2fe34965f5ebae84b864e2f8e54aa299.js"></script>