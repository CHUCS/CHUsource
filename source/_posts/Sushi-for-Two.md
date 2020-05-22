---
title: Codeforces 1138A
date: 2019-03-26 13:25:21
keywords: Codeforces 1138A, Codeforces Sushi for Two
categories: Codeforces
tags:
    - CodeForces
    - binary search
    - two pointers
    - 普通
---
# Codeforces 1138A - Sushi for Two
[Sushi for Two](https://codeforces.com/problemset/problem/1138/A)

Arkady invited Anna for a dinner to a sushi restaurant. The restaurant is a bit unusual: it offers n pieces of sushi aligned in a row, and a customer has to choose a continuous subsegment of these sushi to buy.
<!-- more -->
The pieces of sushi are of two types: either with tuna or with eel. Let's denote the type of the i-th from the left sushi as t<sub>i</sub>, where t<sub>i</sub>=1 means it is with tuna, and t<sub>i</sub>=2 means it is with eel.

Arkady does not like tuna, Anna does not like eel. Arkady wants to choose such a continuous subsegment of sushi that it has equal number of sushi of each type and each half of the subsegment has only sushi of one type. For example, subsegment [2,2,2,1,1,1] is valid, but subsegment [1,2,1,2,1,2] is not, because both halves contain both types of sushi.

Find the length of the longest continuous subsegment of sushi Arkady can buy.

#### Input:
The first line contains a single integer n (2≤n≤100000) — the number of pieces of sushi.

The second line contains nintegers t<sub>1</sub>, t<sub>2</sub>, ..., t<sub>n</sub> (t<sub>i</sub>=1, denoting a sushi with tuna or t<sub>i</sub>=2, denoting a sushi with eel), representing the types of sushi from left to right.

It is guaranteed that there is at least one piece of sushi of each type. Note that it means that there is at least one valid continuous segment.
#### Output:
Print a single integer — the maximum length of a valid continuous segment.

#### 範例:
input:
```
7
2 2 2 1 1 2 2
```
output:
```
4
```
input:
```
6
1 2 1 2 1 2
```
output:
```
2
```
input:
```
9
2 2 1 1 1 2 2 2 2
```
output:
```
6
```
#### Note:
In the first example Arkady can choose the subsegment [2,2,1,1] or the subsegment [1,1,2,2] with length 4.

In the second example there is no way but to choose one of the subsegments [2,1] or [1,2] with length 2.

In the third example Arkady's best choice is the subsegment [1,1,1,2,2,2].

#### 題意:
2個人去吃壽司，台上只有一排n個的壽司，有鮪魚和鰻魚兩種，壽司店只願意賣連續的一組壽司。其中一個人只想吃鮪魚，另一個人只想吃鰻魚，而且還希望能剛好每個半邊都是一樣的壽司方便分配，問你他們可以買的壽司最長是幾個？

#### 思路:
用二分搜尋法搜尋寬度，要注意的是長度必須是偶數，因此先將搜尋上限調整至大於等於n的2的冪次方較方便。確定可不可以的時候使用雙指標的方法搜尋較為快速。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/88d3e3247eccead6d05d0232156e110e.js"></script>

