---
title: CodeForces 1321C
date: 2020-03-20 13:25:41
link: Remove-Adjacent
keywords: Codeforces 1321C, Codeforces Remove Adjacent
tags:
    - 普通
    - brute force
    - constructive algorithms
    - greedy
    - strings
---
# CodeForces 1321C - Remove Adjacent
[Remove Adjacent](https://codeforces.com/problemset/problem/1321/C)

#### 題意:
給你一個泉小寫英文字母字串，你能夠對字串執行的動作是把滿足條件的1個目標字元刪除，條件是要刪除的字元隔壁至少要有一個字元的英文字母順序再此字元前面1位(因此你永遠無法刪除a)，問你最多可以刪除幾個字元？
<!-- more -->
#### 思路:
觀察後可以發現，同樣文字的刪除順序不會影響結果，因此從z開始往a刪除，記錄刪除次數就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/5f31b3e317535b12c8075e8d4764c11e.js"></script>