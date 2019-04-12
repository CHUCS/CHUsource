---
title: Teams Forming
date: 2019-03-26 13:24:41
tags:
    - CHU Training
    - CodeForces
    - sortings
    - greedy
    - 簡單
---
One day n students come to the stadium. They want to play football, and for that they need to split into teams, the teams must have an equal number of people.

We know that this group of people has archenemies. Each student has at most two archenemies. Besides, if student A is an archenemy to student B, then student B is an archenemy to student A.

The students want to split so as no two archenemies were in one team. If splitting in the required manner is impossible, some students will have to sit on the bench.

Determine the minimum number of students you will have to send to the bench in order to form the two teams in the described manner and begin the game at last.
<!-- more -->
#### Input:
The first line contains two integers n and m (2 ≤ n ≤ 100, 1 ≤ m ≤ 100) — the number of students and the number of pairs of archenemies correspondingly.

Next m lines describe enmity between students. Each enmity is described as two numbers ai and bi (1 ≤ a<sub>i</sub>, b<sub>i</sub> ≤ n, a<sub>i</sub> ≠ b<sub>i</sub>) — the indexes of the students who are enemies to each other. Each enmity occurs in the list exactly once. It is guaranteed that each student has no more than two archenemies.

#### Output:
Print a single integer — the minimum number of students you will have to send to the bench in order to start the game.

#### 範例:
input:
```
5 4
1 2
2 4
5 3
1 4
```
output:
```
1
```
input:
```
6 2
1 4
3 4
```
output:
```
0
```
input:
```
6 6
1 2
2 3
3 1
4 5
5 6
6 4
```
output:
```
2
```

#### 題意:
n個學生要分成n/2組，每1組保證正好2個人，每個人都有各自的程式技能等級ai，你可以挑1個人來解掉1題題目讓他的程式技能等級提升1級，現在問你最少要讓學生總共解掉多少題目來使得每一組的2個人間彼此的程式技能等級都是一樣的？

#### 思路:
把所有人依技能等級從大到小排序，兩兩一組，把低的拉到跟高的一樣，加總差距就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/bc6568329876e43c5ddbf19948035b6f.js"></script>

[題目網址](https://codeforces.com/problemset/problem/216/B)