---
title: CodeForces 1176C
date: 2019-11-26 15:35:15
keywords: CodeForces 1176C, CodeForces Lose it
categories: Codeforces
tags:
    - dp
    - implementation
    - greedy
    - 簡單
---
# CodeForces 1176C - Lose it
[Lose it](http://codeforces.com/problemset/problem/1176/C)


#### 題意:
找出集合中有幾個序列為[4,8,15,16,23,42]的序列
<!-- more -->
#### 思路:
依照題意，可以得到說順序不能變，故由前向後搜，開始統計每個數字的個數，當碰到前面數字個數>後面字數個數時表示可以形成序列，最後統計有多少個序列後計算n-6*序列數。

例如:
[4,8,4,15,16,8,23,15,16,42,23,42]

第一個為4，並且4為序列的第一個，故 sequence_count[0]++;
第二個為8，為序列中第二個，判斷序列中第一個是否有個數，有則 sequence_count[1]++;sequence_count[0]--;將前面的抵銷。
以此類推
sequence_count[0]++
sequence_count[2]++;sequence_count[1]--;
.
.
.

#### 程式碼:
<script src="https://gist.github.com/Daviswww/d83328cdf1580e2bed0b468b045ac0bd.js"></script>