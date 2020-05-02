---
title: Codeforces 734A Anton and Danik
date: 2020-04-12 16:28:11
tags:
    - implementation
    - strings
    - 新手
---
[Codeforces 734A](https://codeforces.com/contest/734/problem/A)
<!-- more -->

#### 題意:
Anton 和 Danik 在玩遊戲幫他們計算誰是贏家，出現A代表Anton贏，D代表Danik贏。

#### 思路:
輸入時使用char這樣就可以一個一個輸入接著每次輸入時把每個字元當成index的值做增加，最後比較陣列內的值就可以得到答案了。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/1b2fec18d40c76e37755a65faec8cae3.js"></script>