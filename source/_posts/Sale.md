---
title: Codeforces 34B
date: 2019-04-20 18:50:51
keywords: Codeforces 34B, Codeforces Sale
categories: Codeforces
tags:
    - greedy
    - sortings
    - 簡單
---
# Codeforces 34B - Sale
[Sale](https://codeforces.com/problemset/problem/34/B)

Once Bob got to a sale of old TV sets. There were n TV sets at that sale. TV set with index i costs ai bellars. Some TV sets have a negative price — their owners are ready to pay Bob if he buys their useless apparatus. Bob can «buy» any TV sets he wants. Though he's very strong, Bob can carry at most m TV sets, and he has no desire to go to the sale for the second time. Please, help Bob find out the maximum sum of money that he can earn.
<!-- more -->
#### Input:
The first line contains two space-separated integers n and m (1 ≤ m ≤ n ≤ 100) — amount of TV sets at the sale, and amount of TV sets that Bob can carry. The following line contains n space-separated integers ai ( - 1000 ≤ a<sub>i</sub> ≤ 1000) — prices of the TV sets.

#### Output:
Output the only number — the maximum sum of money that Bob can earn, given that he can carry at most m TV sets.

#### 範例:
input:
```
5 3
-6 0 35 -2 4
```
output:
```
8
```
input:
```
4 2
7 0 0 -7
```
output:
```
7
```

#### 題意:
有n個商品及售價，你最多拿得動m個，問你最多可以賺多少？

#### 思路:
因為只有負的可以賺，所以從小的開始拿最多m個負的累加即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/31b38649f55b7f93e7e46ccafe952bee.js"></script>
