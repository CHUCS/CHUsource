---
title: Beautiful Matrix
date: 2020-04-12 16:29:04
tags:
    - implementation
    - 新手
---
[題目網址](https://chucs.github.io/site/)
<!-- more -->

#### 題意:
有個5X5得矩陣，裡面有24個0和1個1，問你需要幾步可以把1移到中間。

#### 思路:
取得1的位置後將他與中間的位置相減取絕對值並相加，假設1得位置為[1, 1]那麼中間的位置為[3, 3]，相減後可得到行要移動兩格，列要移動兩格才可以到中間。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/92fe6578203256455873d894f5fcd7dc.js"></script>