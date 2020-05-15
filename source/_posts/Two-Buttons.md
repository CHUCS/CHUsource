---
title: Codeforces 520B
date: 2019-10-26 11:52:34
tags:
    - dfs and similar
    - graphs
    - greedy
    - implementation
    - math
    - shortest paths
---
# Codeforces 520B - Two Buttons
[Two Buttons](https://codeforces.com/problemset/problem/520/B)

Vasya has found a strange device. On the front panel of a device there are: a red button, a blue button and a display showing some positive integer. 
<!-- more -->

After clicking the red button, device multiplies the displayed number by two. After clicking the blue button, device subtracts one from the number on the display. 

If at some point the number stops being positive, the device breaks down. The display can show arbitrarily large numbers. Initially, the display shows number n.

#### Input:
The first and the only line of the input contains two distinct integers n and m (1 ≤ n, m ≤ 10<sup>4</sup>), separated by a space .

#### Output:
Print a single number — the minimum number of times one needs to push the button required to get the number m out of number n.

#### 範例:
input:
```
4 6
```
output:
```
2
```
input:
```
10 1
```
output:
```
9
```

#### Note:
In the first example you need to push the blue button once, and then push the red button once.

In the second example, doubling the number is unnecessary, so we need to push the blue button nine times.

#### 題意:
它給你兩個按鈕和一個數值n，一個做數值*2的動作，另一個則做數值-1的動作，試問最少需要案幾次按鈕才能到達目標值n。

#### 思路:
2(2((2n)+1)) = m  -->  n = (((m/2)-1)/2)/2
使用類似反矩陣的概念，去讓m接近n，因為在n做運算時必定為整數則反之亦然，所以m做運算時絕對不能出現小數點，意思是m做除以2的運算時必須為偶數。

#### 程式碼:

<script src="https://gist.github.com/89snnfk561/775e4e0b3a627e88d921dea99c9d424a.js"></script>

