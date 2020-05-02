---
title: Codeforces 985B Switches and Lamps
date: 2020-04-15 13:17:22
tags:
    - 普通
    - implementation
---
[Codeforces 985B](https://codeforces.com/problemset/problem/985/B)
<!-- more -->

#### 題意:
給你n個開關跟排成一排的m個燈，再輸入每個開關會開啟那些燈，開關1會開燈，0無動作，燈一旦開了就不會關，問你能否只用n – 1個開關就將所有燈打開？

#### 思路:
輸入後先將開關數累加，紀錄每個燈有幾個開關可以開。然後跑每個開關，看這個開關可以開的燈是否每個都有2個以上的開關接著，是的話表示這個開關是多的，可以拿掉，輸出YES；找不到這樣的開關的話輸出NO。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/fdb447a92830049826ce20745663d70d.js"></script>