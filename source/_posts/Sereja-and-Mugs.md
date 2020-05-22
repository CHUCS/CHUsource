---
title: Codeforces 426A
date: 2019-03-26 13:24:03
keywords: Codeforces 426A, Codeforces Sereja and Mugs
categories: Codeforces
tags:
    - CodeForces
    - implementation
    - 新手 
---
# Codeforces 426A - Sereja and Mugs
[Sereja and Mugs](https://codeforces.com/problemset/problem/426/A)

Sereja showed an interesting game to his friends. The game goes like that. Initially, there is a table with an empty cup and n water mugs on it. Then all players take turns to move. During a move, a player takes a non-empty mug of water and pours all water from it into the cup. If the cup overfills, then we assume that this player lost.
<!-- more -->
As soon as Sereja's friends heard of the game, they wanted to play it. Sereja, on the other hand, wanted to find out whether his friends can play the game in such a way that there are no losers. You are given the volumes of all mugs and the cup. Also, you know that Sereja has (n - 1) friends. Determine if Sereja's friends can play the game so that nobody loses. 

#### Input:
The first line contains integers n and s (2 ≤ n ≤ 100; 1 ≤ s ≤ 1000) — the number of mugs and the volume of the cup. The next line contains n integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> (1 ≤ a<sub>i</sub> ≤ 10). Number ai means the volume of the i-th mug.

#### Output:
In a single line, print "YES" (without the quotes) if his friends can play in the described manner, and "NO" (without the quotes) otherwise.

#### 範例:

input:
```
3 4
1 1 1
```
output:
```
YES
```
input:
```
3 4
3 1 3
```
output:
```
YES
```
input:
```
3 4
4 4 4
```
output:
```
NO
```

#### 題意:
n個杯子，n-1個人各選一個，總容量要不超過s，問有可能達成嗎？

#### 思路:
只問有沒有可能，不是一定要，所以只要考慮n-1個數的最小值就好，因此把最大的拿掉後看看行不行就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/0df5bb1e098e637055883d57254a1812.js"></script>

