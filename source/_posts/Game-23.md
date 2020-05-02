---
title: Codeforces 1141A Game 23
date: 2019-05-05 22:00:09
tags:
    - 新手
    - implementation
    - math
---
[Codeforces 1141A](https://codeforces.com/problemset/problem/1141/A)
<!-- more -->
Polycarp plays "Game 23". Initially he has a number n and his goal is to transform it to m. In one move, he can multiply n by 2 or multiply n by 3. He can perform any number of moves.

Print the number of moves needed to transform n
to m. Print -1 if it is impossible to do so.

It is easy to prove that any way to transform n to m contains the same number of moves (i.e. number of moves doesn't depend on the way of transformation).

#### Input:
The only line of the input contains two integers n and m (1≤n≤m≤5⋅108).

#### Output:
Print the number of moves to transform n to m, or -1 if there is no solution.

#### 範例:
input:
```
120 51840
```
output:
```
7
```
input:
```
42 42
```
output:
```
0
```
input:
```
48 72
```
output:
```
-1
```
#### Note:
In the first example, the possible sequence of moves is: 120→240→720→1440→4320→12960→25920→51840. The are 7 steps in total.

In the second example, no moves are needed. Thus, the answer is 0.

In the third example, it is impossible to transform 48 to 72.
#### 題意:
輸入n、m，你現在每一步可以將n乘以2或3，問你需要幾步可以將n變成m？不能的話輸出-1。

#### 思路:
先判斷能不能n整除m，不能就輸出-1，可以的話直接除，然後將商質因數分解，看有幾個2跟3，有2跟3以外的因數就輸出-1，不然個數加起來就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/55eb8af27dbbcb1e6383f0c1fbe38cf1.js"></script>
