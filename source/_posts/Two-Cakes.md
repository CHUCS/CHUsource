---
title: Codeforces 911B
date: 2019-04-20 18:51:03
link: Two-Cakes
keywords: Codeforces 911B, Codeforces Two Cakes
tags:
    - binary search 
    - implementation
    - 普通
---
# Codeforces 911B - Two Cakes
[Two Cakes](https://codeforces.com/problemset/problem/911/B)

It's New Year's Eve soon, so Ivan decided it's high time he started setting the table. Ivan has bought two cakes and cut them into pieces: the first cake has been cut into a pieces, and the second one — into b pieces.
<!-- more -->
Ivan knows that there will be n people at the celebration (including himself), so Ivan has set n plates for the cakes. Now he is thinking about how to distribute the cakes between the plates. Ivan wants to do it in such a way that all following conditions are met:

>>1. Each piece of each cake is put on some plate;
>>2. Each plate contains at least one piece of cake;
>>3. No plate contains pieces of both cakes.

To make his guests happy, Ivan wants to distribute the cakes in such a way that the minimum number of pieces on the plate is maximized. Formally, Ivan wants to know the maximum possible number x such that he can distribute the cakes according to the aforementioned conditions, and each plate will contain at least x pieces of cake.

Help Ivan to calculate this number x!

#### Input:
The first line contains three integers n, a and b (1 ≤ a, b ≤ 100, 2 ≤ n ≤ a + b) — the number of plates, the number of pieces of the first cake, and the number of pieces of the second cake, respectively.

#### Output:
Print the maximum possible number x such that Ivan can distribute the cake in such a way that each plate will contain at least x pieces of cake.

#### 範例:
input:
```
5 2 3
```
output:
```
1
```
input:
```
4 7 10
```
output:
```
3
```
#### Note:
In the first example there is only one way to distribute cakes to plates, all of them will have 1 cake on it.

In the second example you can have two plates with 3 and 4 pieces of the first cake and two plates both with 5 pieces of the second cake. Minimal number of pieces is 3.

#### 題意:
現在有兩大塊蛋糕各自分成a片和b片，要分給n個人，有3個條件，(1)每片蛋糕都要分出去；(2)每個人至少有1片蛋糕；(3)一個人只能有一種蛋糕。問你被分到最少片蛋糕的那個人，他最多能拿到幾片蛋糕？

#### 思路:
因為一塊蛋糕最多分成100片，因此用二分搜尋找1~100，記住最大值輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/514ffd6016100eaa0ee60e4e42edc292.js"></script>
