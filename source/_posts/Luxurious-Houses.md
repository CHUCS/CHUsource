---
title: Codeforces 581B
date: 2019-05-05 22:00:19
link: Luxurious-Houses
keywords: Codeforces 581B, Codeforces Luxurious Houses
tags:
    - 簡單
    - implementation
---
# Codeforces 581B - Luxurious Houses
[Luxurious Houses](https://codeforces.com/problemset/problem/581/B)

The capital of Berland has n multifloor buildings. The architect who built up the capital was very creative, so all the houses were built in one row.
<!-- more -->
Let's enumerate all the houses from left to right, starting with one. A house is considered to be luxurious if the number of floors in it is strictly greater than in all the houses with larger numbers. In other words, a house is luxurious if the number of floors in it is strictly greater than in all the houses, which are located to the right from it. In this task it is assumed that the heights of floors in the houses are the same.

The new architect is interested in n questions, i-th of them is about the following: "how many floors should be added to the i-th house to make it luxurious?" (for all i from 1 to n, inclusive). You need to help him cope with this task.

Note that all these questions are independent from each other — the answer to the question for house i does not affect other answers (i.e., the floors to the houses are not actually added).

#### Input:
The first line of the input contains a single number n (1 ≤ n ≤ 10<sup>5</sup>) — the number of houses in the capital of Berland.

The second line contains n space-separated positive integers h<sub>i (1 ≤ h<sub>i</sub> ≤ 10<sup>9</sup>), where hi equals the number of floors in the i-th house. 

#### Output:
Print n integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub>, where number a<sub>i</sub> is the number of floors that need to be added to the house number i to make it luxurious. If the house is already luxurious and nothing needs to be added to it, then a<sub>i</sub> should be equal to zero.

All houses are numbered from left to right, starting from one.

#### 範例:
input:
```
5
1 2 3 1 2
```
output:
```
3 2 0 2 0 
```
input:
```
4
3 2 1 4
```
output:
```
2 3 4 0 
```
#### 題意:
給你N間房子的高度，從左到右。一間房子若是比他右邊所有的房子都要高的話就能稱為奢華，問你每一間房子各自若要變的奢華的話還要再增高多少？

#### 思路:
從最右邊開始，記錄到目前為止最高的高度，然後若是自己比最高的高度還矮或是一樣，就加高，不然不用加。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/50eceb9a682e44901b10ccabb961c6a8.js"></script>
