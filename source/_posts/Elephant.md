---
title: Elephant
date: 2019-03-14 10:01:20
tags:
    - CHU Training
    - CodeForces
---
An elephant decided to visit his friend. It turned out that the elephant's house is located at point 0 and his friend's house is located at point x(x > 0) of the coordinate line. In one step the elephant can move 1, 2, 3, 4 or 5 positions forward. Determine, what is the minimum number of steps he need to make in order to get to his friend's house.
<!-- more -->
#### Input:
The first line of the input contains an integer x (1 ≤ x ≤ 1 000 000) — The coordinate of the friend's house.

#### Output:
Print the minimum number of steps that elephant needs to make to get from point 0 to point x.

#### 範例:
input:
```
5
```
output:
```
1
```
input:
```
12
```
output:
```
3
```

#### Note:
In the first sample the elephant needs to make one step of length 5 to reach the point x.

In the second sample the elephant can get to point x if he moves by 3, 5 and 4. There are other ways to get the optimal answer but the elephant cannot reach x in less than three moves.

#### 題意:
字串中有H、Q、9時印出指定的內容，+增加內部數值。給你一串字串，問你這串字串會不會讓你印出東西？

#### 思路:
因為只有HQ9會印出東西，所以把字串全部跑一次，有HQ9其中一個字出現就是YES，否則就是NO。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a3c788a465878f6d9badc51d1728422a.js"></script>

[題目網址](https://codeforces.com/problemset/problem/617/A)