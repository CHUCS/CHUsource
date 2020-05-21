---
title: Codeforces 1088B
date: 2020-04-15 13:17:35
keywords: Codeforces 1088B, Codeforces Ehab and subtraction
tags:
    - implementation
    - sortings
    - 簡單
---
# Codeforces 1088B - Ehab and subtraction
[Ehab and subtraction](https://codeforces.com/problemset/problem/1088/B)


#### 題意:
給你一個數列，然後執行下列動作k次：先挑出數列中最小的非零正整數，輸出，然後將整個陣列減掉這個數。問你每次輸出的數是多少？
<!-- more -->
#### 思路:
排序，然後從依照題目敘述，每次找最小的非零正整數，輸出，只有減的時候紀錄目前為止減了多少，不用真的減整個陣列，較省時。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/e573aee1ccb5f6ffd757ec02c778c7a6.js"></script>