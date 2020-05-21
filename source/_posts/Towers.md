---
title: Codeforces 37A
date: 2019-04-27 18:41:23
keywords: Codeforces 37A, Codeforces Towers
tags:
    - 簡單
    - sortings
---
# Codeforces 37A - Towers
[Towers](https://codeforces.com/problemset/problem/37/A)

Little Vasya has received a young builder’s kit. The kit consists of several wooden bars, the lengths of all of them are known. The bars can be put one on the top of the other if their lengths are the same.
<!-- more -->
Vasya wants to construct the minimal number of towers from the bars. Help Vasya to use the bars in the best way possible.

#### Input:
The first line contains an integer N (1 ≤ N ≤ 1000) — the number of bars at Vasya’s disposal. The second line contains N space-separated integers l<sub>i</sub> — the lengths of the bars. All the lengths are natural numbers not exceeding 1000.

#### Output:
In one line output two numbers — the height of the largest tower and their total number. Remember that Vasya should use all the bars.

#### 範例:
input:
```
3
1 2 3
```
output:
```
1 3
```
input:
```
4
6 5 6 7
```
output:
```
2 3
```

#### 題意:
給你N根木棒，長度一樣的會疊在一起，每一疊稱為一座塔，問你最高的塔是多高和總共有幾座塔？

#### 思路:
排序後計算每個數字各出現幾次，紀錄最大值；計算出現幾種數字。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/fa84e180769bcd1b2ba6b72bd859c455.js"></script>
