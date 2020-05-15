---
title: Codeforces 967B
date: 2019-04-12 23:05:47
tags:
    - CHU Training
    - CodeForces
    - sortings
    - 簡單
---
[Watering System](https://codeforces.com/problemset/problem/967/B)

Arkady wants to water his only flower. Unfortunately, he has a very poor watering system that was designed for n flowers and so it looks like a pipe with n holes. Arkady can only use the water that flows from the first hole.
<!-- more -->
Arkady can block some of the holes, and then pour A liters of water into the pipe. After that, the water will flow out from the non-blocked holes proportionally to their sizes s<sub>1</sub>,s<sub>2</sub>,…,s<sub>n</sub>. In other words, if the sum of sizes of non-blocked holes is S, and the i-th hole is not blocked, (s<sub>i</sub>*A)/S liters of water will flow out of it.

What is the minimum number of holes Arkady should block to make at least B liters of water flow out of the first hole?

#### Input:
The first line contains three integers n, A, B (1≤n≤100000, 1≤B≤A≤10<sup>4</sup>) — the number of holes, the volume of water Arkady will pour into the system, and the volume he wants to get out of the first hole.

The second line contains n integers s<sub>1</sub>,s<sub>2</sub>,…,s<sub>n</sub> (1≤s<sub>i</sub>≤10<sup>4</sup>) — the sizes of the holes.

#### Output:
Print a single integer — the number of holes Arkady should block.

#### 範例:
input:
```
4 10 3
2 2 2 2
```
output:
```
1
```
input:
```
4 80 20
3 2 1 4
```
output:
```
0
```
input:
```
5 10 10
1000 1 1 1 1
```
output:
```
4
```
#### Note:
In the first example Arkady should block at least one hole. After that, (10*2)/6≈3.333 liters of water will flow out of the first hole, and that suits Arkady.

In the second example even without blocking any hole, (80*3)/10=24 liters will flow out of the first hole, that is not less than 20.

In the third example Arkady has to block all holes except the first to make all water flow out of the first hole.

#### 題意:
現在有A公升的水，會流到n個洞中，每個洞的流量會根據佔洞口的總尺寸比例而佔據等比例的流量，現在問你假設1號洞要流過B公升以上的水時，最少要把幾個洞堵起來？

#### 思路:
為了讓1號洞的流量上升，就必須要把其他洞堵起來，而堵的洞愈大，就會因為佔總面積愈大上升的愈多，因此將2~n號洞排序後由大的開始堵。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/90d9bdcc8d2015c0ddf60c339600b94f.js"></script>

