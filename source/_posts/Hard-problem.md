---
title: CodeForces 706C
date: 2019-12-22 15:10:43
tags:
    - 一般
    - strings
    - dp
---
[Hard problem](http://codeforces.com/problemset/problem/706/C)


#### 題意:
輸入N(有多少字)、每個字顛倒的成本和每個字，問你不改變這串字的先後順序，藉由顛倒某些字來將這些字排成字典順序最少需要多少成本？
<!-- more -->
#### 思路:
直接將所有字及所有顛倒後的字存起來，然後紀錄後面的字要滿足比前面的字大的最小成本，逐個更新就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/e14147a86c576dffff606a831ef76104.js"></script>