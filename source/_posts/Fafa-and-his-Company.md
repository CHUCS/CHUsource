---
title: Codeforces 935A
date: 2019-03-26 13:23:48
tags:
    - CHU Training
    - CodeForces
    - math
    - implementation
    - 新手
---
[Fafa and his Company](https://codeforces.com/problemset/problem/935/A)

Fafa owns a company that works on huge projects. There are n employees in Fafa's company. Whenever the company has a new project to start working on, Fafa has to divide the tasks of this project among all the employees.
<!-- more -->
Fafa finds doing this every time is very tiring for him. So, he decided to choose the best l employees in his company as team leaders. Whenever there is a new project, Fafa will divide the tasks among only the team leaders and each team leader will be responsible of some positive number of employees to give them the tasks. To make this process fair for the team leaders, each one of them should be responsible for the same number of employees. Moreover, every employee, who is not a team leader, has to be under the responsibility of exactly one team leader, and no team leader is responsible for another team leader.

Given the number of employees n, find in how many ways Fafa could choose the number of team leaders l in such a way that it is possible to divide employees between them evenly.

#### Input:
The input consists of a single line containing a positive integer n (2 ≤ n ≤ 10<sup>5</sup>) — the number of employees in Fafa's company.

#### Output:
Print a single integer representing the answer to the problem.

#### 範例:

input:
```
2
```
output:
```
1
```
input:
```
10
```
output:
```
3
```

#### Note:
In the second sample Fafa has 3 ways:

>>● choose only 1 employee as a team leader with 9 employees under his responsibility.
>>● choose 2 employees as team leaders with 4 employees under the responsibility of each of them.
>>● choose 5 employees as team leaders with 1 employee under the responsibility of each of them. 
#### 題意:
現在有n個員工，要被分成小組，一個小組一定要有1個組長和1個以上的組員，而且每一組的人數必須一樣，問現在有幾種分法？

#### 思路:
題目等同於問n有幾個2以上的因數，1不行不用管；n一定是，先加1；從2開始，能整除就加2，因為因數是成對出現的，這樣可以只檢查到平方根就好；例外的平方根要注意，平方根能整除也只加1。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/dec4d3138b5eb87b0df108f844503fcb.js"></script>

