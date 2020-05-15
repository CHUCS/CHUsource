---
title: UVA 10107
date: 2019-11-17 10:56:25
tags:
- implementation
---
[One-Two-Three](https://onlinejudge.org/external/101/10107.pdf)


#### 題意:
找中位數。
<!-- more -->
#### 思路:
每次都排序然後計算，如果是偶數就(ary[k/2-1] + ary[k/2]) / 2，奇數就直接印ary[k/2]。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/e746a371f7628ac2bec3bda186854e9c.js"></script>