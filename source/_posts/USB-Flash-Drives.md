---
title: Codeforces 609A
date: 2019-03-21 09:50:43
keywords: Codeforces 609A, Codeforces USB Flash Drives
categories: Codeforces
tags:
    - CodeForces
    - sortings
    - greedy
    - 簡單
---
# Codeforces 609A - USB Flash Drives
[USB Flash Drives](https://codeforces.com/problemset/problem/609/A)

Sean is trying to save a large file to a USB flash drive. He has n USB flash drives with capacities equal to a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> megabytes. The file size is equal to m megabytes.
<!-- more -->
Find the minimum number of USB flash drives needed to write Sean's file, if he can split the file between drives.

#### Input:
The first line contains positive integer n (1 ≤ n ≤ 100) — the number of USB flash drives.

The second line contains positive integer m (1 ≤ m ≤ 10<sup>5</sup>) — the size of Sean's file.

Each of the next n lines contains positive integer a<sub>i</sub> (1 ≤ a<sub>i</sub> ≤ 1000) — the sizes of USB flash drives in megabytes.

It is guaranteed that the answer exists, i. e. the sum of all a<sub>i</sub> is not less than m.

#### Output:
Print the minimum number of USB flash drives to write Sean's file, if he can split the file between drives.

#### 範例:
input:
```
3
5
2
1
3
```
output:
```
2
```
input:
```
3
6
2
3
2
```
output:
```
3
```
input:
```
2
5
5
10
```
output:
```
1
```

#### Note:
In the first example Sean needs only two USB flash drives — the first and the third.

In the second example Sean needs all three USB flash drives.

In the third example Sean needs only one USB flash drive and he can use any available USB flash drive — the first or the second.

#### 題意:
有n個隨身碟的容量是a<sub>1</sub>、a<sub>2</sub>、…、a<sub>n</sub>，有筆資料的容量是m，問你最少要幾個隨身碟才裝得下？

#### 思路:
排序後由大的開始扣，容量扣完或全部用完了的時候就結束。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/796d0bc74e046275763493f76b904146.js"></script>


