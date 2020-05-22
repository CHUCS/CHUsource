---
title: CodeForces 148A
date: 2019-03-07 19:45:56
keywords: Codeforces 148A, Codeforces Insomnia cure
categories: Codeforces
tags:
	- CodeForces
	- sortings
	- 簡單
---
# CodeForces 148A - Insomnia cure
[Insomnia cure](https://codeforces.com/problemset/problem/148/A)

«One dragon. Two dragon. Three dragon», — the princess was counting. She had trouble falling asleep, and she got bored of counting lambs when she was nine.
<!-- more -->
However, just counting dragons was boring as well, so she entertained herself at best she could. Tonight she imagined that all dragons were here to steal her, and she was fighting them off. Every k-th dragon got punched in the face with a frying pan. Every l-th dragon got his tail shut into the balcony door. Every m-th dragon got his paws trampled with sharp heels. Finally, she threatened every n-th dragon to call her mom, and he withdrew in panic.

How many imaginary dragons suffered moral or physical damage tonight, if the princess counted a total of d dragons?

#### Input:
Input data contains integer numbers k, l, m, n and d, each number in a separate line (1 ≤ k, l, m, n ≤ 10, 1 ≤ d ≤ 10<sup>5</sup>).

#### Output:
Output the number of damaged dragons.

#### 範例:
input:
```
1
2
3
4
12
```
output:
```
12
```
input:
```
2
3
4
5
24
```
output:
```
17
```
#### Note:
In the first case every first dragon got punched with a frying pan. Some of the dragons suffered from other reasons as well, but the pan alone would be enough.

In the second case dragons 1, 7, 11, 13, 17, 19 and 23 escaped unharmed.

#### 題意:
計算龍的攻擊。

#### 思路:
Every k-th dragon got punched in the face with a frying pan: 每K隻龍就攻擊一遍
Every l-th dragon got his tail shut into the balcony door. 
Every m-th dragon got his paws trampled with sharp heels. 
Finally, she threatened every n-th dragon to call her mom, and he withdrew in panic.

依此類推每??隻龍就攻擊(k ,l ,m ,n)
解法是開一個陣列去紀錄哪一些龍被攻擊了，最後再用一個for迴圈去統計有多少隻龍受到傷害
```
	ex:
		 Every k-th dragon got punched in the face with a frying pan ,k = 2 (有12隻龍)
		 
		 開一個陣列: □ □ □ □ □ □ □ □ □ □ □ □ (12個) 
		 
		 因為是每兩隻龍就攻擊一次所以陣列每數到2就標記一次:
		 
		 1 2 1 2 1 2 1 2 1 2 1 2
		 □ ■ □ ■ □ ■ □ ■ □ ■ □ ■
		 
		 最後做統計，有標記的就是被攻擊過的:
		 
		   1   2   3   4   5   6
		 □ ■ □ ■ □ ■ □ ■ □ ■ □ ■
		 
		 所以被攻擊過的龍就是6隻。
```
題目有 k ,l ,m ,n依此類推都是這樣去標記，最後在做一次統計

#### 程式碼:
<script src="https://gist.github.com/Daviswww/0cd0e5027094ec5738df365d8f2b38cc.js"></script>

