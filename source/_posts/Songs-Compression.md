---
title: Codeforces 1015C
date: 2019-03-26 13:24:53
tags:
    - CHU Training
    - CodeForces
    - sortings
    - greedy
    - 簡單
---
# Codeforces 1015C - Songs Compression
[Songs Compression](https://codeforces.com/problemset/problem/1015/C)

Ivan has n songs on his phone. The size of the i-th song is a<sub>i</sub> bytes. Ivan also has a flash drive which can hold at most m bytes in total. Initially, his flash drive is empty.
<!-- more -->
Ivan wants to copy all n songs to the flash drive. He can compress the songs. If he compresses the i-th song, the size of the i-th song reduces from a<sub>i</sub> to b<sub>i</sub> bytes (b<sub>i</sub> < a<sub>i</sub>).

Ivan can compress any subset of the songs (possibly empty) and copy all the songs to his flash drive if the sum of their sizes is at most m. He can compress any subset of the songs (not necessarily contiguous).

Ivan wants to find the minimum number of songs he needs to compress in such a way that all his songs fit on the drive (i.e. the sum of their sizes is less than or equal to m).

If it is impossible to copy all the songs (even if Ivan compresses all the songs), print "-1". Otherwise print the minimum number of songs Ivan needs to compress.

#### Input:
The first line of the input contains two integers n and m (1≤n≤10<sup>5</sup>,1≤m≤10<sup>9</sup>) — the number of the songs on Ivan's phone and the capacity of Ivan's flash drive.

The next n lines contain two integers each: the i-th line contains two integers ai and bi (1≤a<sub>i</sub>,b<sub>i</sub>≤10<sup>9</sup>, a<sub>i</sub>>b<sub>i</sub>) — the initial size of the i-th song and the size of the i-th song after compression.

#### Output:
If it is impossible to compress a subset of the songs in such a way that all songs fit on the flash drive, print "-1". Otherwise print the minimum number of the songs to compress.

#### 範例:
input:
```
4 21
10 8
7 4
3 1
5 4
```
output:
```
2
```
input:
```
4 16
10 8
7 4
3 1
5 4
```
output:
```
-1
```

#### Note:
In the first example Ivan can compress the first and the third songs so after these moves the sum of sizes will be equal to 8+7+1+5=21≤21. Also Ivan can compress the first and the second songs, then the sum of sizes will be equal 8+4+3+5=20≤21. Note that compressing any single song is not sufficient to copy all the songs on the flash drive (for example, after compressing the second song the sum of sizes will be equal to 10+4+3+5=22>21).

In the second example even if Ivan compresses all the songs the sum of sizes will be equal 8+4+1+4=17>16
.
#### 題意:
現在有n首歌，要放進容量為m的隨身碟裡，考慮到容量問題，歌可以進行壓縮，從原本的容量ai壓縮成bi，現在問你最少要壓縮幾首歌才能將歌全部塞進隨身碟中，或是不可能塞進去？

#### 思路:
先將a加總，得到未壓縮的總容量max；將b加總，得到全壓縮的總容量min。當max<=m時無須壓縮；當min>m時不可能；剩下的情況將每1首歌的壓縮容量差距記起來，依差距從大排到小，從差距大的開始壓縮，壓縮到容量可以後停止就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/d228c2a19a77b9da421e25e87cd3e3d9.js"></script>

