---
title: Codeforces 1323A
keywords: Codeforces Even Subset Sum Problem, Codeforces 1323A
date: 2020-05-29 19:03:42
categories: Codeforces
tags:
    - dp
    - greedy
    - brute force
    - implementation
    - 800
---
# Codeforces 1323A - Even Subset Sum Problem
[題目網址](https://codeforces.com/problemset/problem/1323/A)

#### 題意:
給你一個陣列a，有n個正整數，找出一個非空的子集合，並且元素加總為偶數，印出共有幾個元素並把元素在陣列a中的位置印出來，如果找不到就印出-1。
<!-- more -->
#### 思路:
共分三種情況:
1.陣列a中有偶數 (子集合元素為1，並印出偶數在陣列a中的位置)
2.陣列a中只有一個元素並且為奇數 (印出-1)
3.陣列a中有一個以上的奇數 (子集合元素為2，位置為1、2)
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/bc4473376e327fee857828cdb1bd46ed.js"></script>