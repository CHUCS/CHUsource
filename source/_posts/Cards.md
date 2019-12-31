---
title: Cards
date: 2019-12-31 15:46:45
tags:
    - 新手
    - implementation
    - sortings
    - strings
---
[CodeForces 1220A](https://codeforces.com/problemset/problem/1220/A)
<!-- more -->

#### 題意:
給你一條字串裡面只有 'z', 'e', 'r', 'o' 和 'n'，請將字串裡的英文'zero'和'one'轉成數字1和0並以最大的二進制方式輸出，例如：nznooeeoer有兩個1和一個0，最大的數字為110。

#### 思路:
先將所有1列印出來再印0，而0和1的英文不一樣的有z, r, n，所以我們可以用此來找出有幾個零與一。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/aacc51a67599af7e1e7f778bf921e76e.js"></script>