---
title: Codeforces 246A Buggy Sorting
date: 2019-04-27 18:42:02
tags:
    - 簡單
    - sortings
---
[Codeforces 246A](https://codeforces.com/problemset/problem/246/A)
<!-- more -->
Little boy Valera studies an algorithm of sorting an integer array. After studying the theory, he went on to the practical tasks. As a result, he wrote a program that sorts an array of n integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> in the non-decreasing order. The pseudocode of the program, written by Valera, is given below. The input of the program gets number n and array a.

```
loop integer variable i from 1 to n - 1
    loop integer variable j from i to n - 1
        if (aj > aj + 1), then swap the values of elements aj and aj + 1
```
But Valera could have made a mistake, because he hasn't yet fully learned the sorting algorithm. If Valera made a mistake in his program, you need to give a counter-example that makes his program work improperly (that is, the example that makes the program sort the array not in the non-decreasing order). If such example for the given value of n doesn't exist, print -1.

#### Input:
You've got a single integer n (1 ≤ n ≤ 50) — the size of the sorted array.

#### Output:
Print n space-separated integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> (1 ≤ a<sub>i</sub> ≤ 100) — the counter-example, for which Valera's algorithm won't work correctly. If the counter-example that meets the described conditions is impossible to give, print -1.

If there are several counter-examples, consisting of n numbers, you are allowed to print any of them.
#### 範例:
input:
```
1
```
output:
```
-1
```

#### 題意:
給你一個排序法，目標是將陣列排序成非遞減的格式，但是這排序法有錯誤，現在輸入陣列長度，你是否能舉例出一個會排序錯誤的陣列？

#### 思路:
陣列從位置0排到最後，但是卻先移除位置0，因此長度在3以上時，最後一個一定移不到位置0，因此長度在3以上時將最後一個輸出最小的，其他情況輸出-1即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/bb7804303d64985fd6da2a32dcff7dfe.js"></script>
