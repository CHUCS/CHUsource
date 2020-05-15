---
title: CodeForces 1311A
date: 2020-03-04 08:15:07
tags:
    - greedy
    - implementation
    - math
    - 簡單
---
[Add Odd or Subtract Even](https://codeforces.com/problemset/problem/1311/A)
<!-- more -->

#### 題意:
輸入a, b兩個數字，現在一個行動可以將a加上任意正奇數，或是減掉任意正偶數。問最少需要幾個行動可以將a變成b？

#### 思路:
先判斷大小關係，a==b時，輸出0；a &lt; b時，差距是奇數輸出1，偶數輸出2(加1、加差距-1)；a&gt;b時，差距是奇數輸出2(加1減差距+1)，偶數輸出1。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/aac217a151f71cd00e822322c2f960d1.js"></script>