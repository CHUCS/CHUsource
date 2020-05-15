---
title: CodeForces 1325A
date: 2020-04-02 15:36:49
tags:
    - constructive algorithms
    - number theory
    - greedy
    - 普通
---

[EhAb AnD gCd](https://codeforces.com/problemset/problem/1325/A)


#### 題意:
依照公式GCD(a, b) + LCM(a, b) = x。現在給你x，請輸出一組符合這個式子的a、b？
<!-- more -->
#### 思路:
GCD(1, n) = 1、LCM(1, n) = n，因此GCD(1, n) + LCM(1, n) = 1 + n。現在另x = 1 + n，因此至少有一組1, x – 1符合題目要求，輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/46dd942f5333b36555552d6dd52cfdbe.js"></script>