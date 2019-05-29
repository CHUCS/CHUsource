---
title: Alyona and Mex
date: 2019-05-05 22:00:45
tags:
    - 簡單
    - sortings

---
Alyona's mother wants to present an array of n non-negative integers to Alyona. The array should be special.

Alyona is a capricious girl so after she gets the array, she inspects m of its subarrays. Subarray is a set of some subsequent elements of the array. The i-th subarray is described with two integers l<sub>i</sub> and r<sub>i</sub>, and its elements are a\[l<sub>i</sub>], a[l<sub>i</sub> + 1], ..., a\[r<sub>i</sub>].

Alyona is going to find mex for each of the chosen subarrays. Among these m mexes the girl is going to find the smallest. She wants this minimum mex to be as large as possible.

You are to find an array a of n elements so that the minimum mex among those chosen by Alyona subarrays is as large as possible.

The mex of a set S is a minimum possible non-negative integer that is not in S.
<!-- more -->
#### Input:
The first line contains two integers n and m (1 ≤ n, m ≤ 10<sup>5</sup>).

The next m lines contain information about the subarrays chosen by Alyona. The i-th of these lines contains two integers l<sub>i</sub> and r<sub>i</sub> (1 ≤ l<sub>i</sub> ≤ r<sub>i</sub> ≤ n), that describe the subarray a\[l<sub>i</sub>], a[l<sub>i</sub> + 1], ..., a\[r<sub>i</sub>].
#### Output:
In the first line print single integer — the maximum possible minimum mex.

In the second line print n integers — the array a. All the elements in a should be between 0 and 10<sup>9</sup>.

It is guaranteed that there is an optimal answer in which all the elements in a are between 0 and 10<sup>9</sup>.

If there are multiple solutions, print any of them.
#### 範例:
input:
```
5 3
1 3
2 5
4 5
```
output:
```
2
1 0 2 1 0
```
input:
```
4 2
1 4
2 4
```
output:
```
3
5 2 0 1
```

#### Note:
The first example: the mex of the subarray (1, 3) is equal to 3, the mex of the subarray (2, 5) is equal to 3, the mex of the subarray (4, 5) is equal to 2 as well, thus the minumal mex among the subarrays chosen by Alyona is equal to 2.
#### 題意:
給你一個陣列，現在可以對每一個元素分別將他變小，最後選出沒在陣列中出現過的正數中最小的，問你這個數值的最大值是多少？

#### 思路:
輸入完後從小排到大，先將答案設為1，然後跑整個陣列，若是當前數字大於等於答案，則表示這個數字能變成答案，那就表示可以將沒出現的數字(答案)加1，跑完陣列後輸出答案即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/64e67f626854df2b130243b23d4b678f.js"></script>
[題目網址](https://codeforces.com/problemset/problem/739/A)