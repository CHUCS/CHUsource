---
title: Magnets
date: 2019-04-20 18:05:29
tags:
    - implementation
    - 新手
---
Mad scientist Mike entertains himself by arranging rows of dominoes. He doesn't need dominoes, though: he uses rectangular magnets instead. Each magnet has two poles, positive (a "plus") and negative (a "minus"). If two magnets are put together at a close distance, then the like poles will repel each other and the opposite poles will attract each other.

Mike starts by laying one magnet horizontally on the table. During each following step Mike adds one more magnet horizontally to the right end of the row. Depending on how Mike puts the magnet on the table, it is either attracted to the previous one (forming a group of multiple magnets linked together) or repelled by it (then Mike lays this magnet at some distance to the right from the previous one). We assume that a sole magnet not linked to others forms a group of its own.
![A](A.PNG)
Mike arranged multiple magnets in a row. Determine the number of groups that the magnets formed.
<!-- more -->
#### Input:
The first line of the input contains an integer n (1 ≤ n ≤ 100000) — the number of magnets. Then n lines follow. The i-th line (1 ≤ i ≤ n) contains either characters "01", if Mike put the i-th magnet in the "plus-minus" position, or characters "10", if Mike put the magnet in the "minus-plus" position.

#### Output:
On the single line of the output print the number of groups of magnets.

#### 範例:
input:
```
6
10
10
10
01
10
10
```
output:
```
3
```
input:
```
4
01
01
10
10
```
output:
```
2
```
#### Note:
The first testcase corresponds to the figure. The testcase has three groups consisting of three, one and two magnets.

The second testcase has two groups, each consisting of two magnets.

#### 題意:
輸入N段的磁鐵，相連的可能會吸引在一起，問最後排成一列的磁鐵有幾段？

#### 思路:
輸入時判斷跟前一個是否一樣，不一樣的不會吸在一起，段數加1。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/7a91611f2f7f3efad84d67e8014ab433.js"></script>

[題目網址](https://codeforces.com/problemset/problem/344/A)