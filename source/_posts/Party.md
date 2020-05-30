---
title: Codeforces 115A
keywords: Codeforces Party, Codeforces 115A
date: 2020-05-30 20:48:45
categories: Codeforces
tags:
    - dfs and similar
    - graphs
    - trees
    - 900
---
# Codeforces 115A - Party
[題目網址](https://codeforces.com/problemset/problem/115/A)


#### 題意:
一家公司裡有n位員工，每位員工不是沒有直屬經理就是只有一位直屬經理，如果滿足以下至少一項條件，則員工A被認為是另一員工B的「上級」：
1.員工A是員工B的直屬經理
2.若員工A是員工C的上級，則員工C也是員工B的直屬經理。
不會有一名員工是直屬經理的上級。
<!-- more -->
這家公司想要辦派對，想要將n位員工分成幾組，每位員工都有組別，但每一組的成員中不會有員工A是員工B的上級，請問「最少」能分成幾組?
員工1~n，為每位員工輸入他的直屬經理號碼，若員工沒有直屬經理則輸入-1。
#### 思路:
對每位員工找出上級-下屬關係最多層的數量就是答案。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/59f4f5856921759acb4957c8700501f1.js"></script>