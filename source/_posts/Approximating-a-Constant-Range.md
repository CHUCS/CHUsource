---
title: Approximating a Constant Range
date: 2020-04-15 13:18:25
tags:
    - implementation
    - two pointers
    - dp
    - 普通
---
[Codeforces 985B](https://codeforces.com/problemset/problem/602/B)
<!-- more -->

#### 題意:
給你一個數列，每一項的值都保證會是前一項的加1或減1，現在想找一個區段，其中最大的數字減最小的數字差在1以內，問你符合條件最長的區段是多長？


#### 思路:
套用雙指標的方法，符合條件時嘗試擴張，尋找更長的區段；不符合時縮減區段，嘗試符合條件。每次擴張或縮減時都記錄上一次出現最大值跟最小值的位置，方便之後快速的更新左邊界。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/e7edb8ece9fa31bf333bfde68c2b7bf1.js"></script>