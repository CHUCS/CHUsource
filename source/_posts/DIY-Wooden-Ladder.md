---
title: Codeforces 1197A DIY Wooden Ladder
date: 2019-09-19 16:04:52
tags:
- greedy
- sortings
- math
---
[Codeforces 1197A](http://codeforces.com/problemset/problem/1197/A)
<!-- more -->
Let's denote a k-step ladder as the following structure: exactly k+2 wooden planks, of which

● two planks of length at least k+1 — the base of the ladder;
● k planks of length at least 1 — the steps of the ladder;

Note that neither the base planks, nor the steps planks are required to be equal.

For example, ladders 1 and 3 are correct 2-step ladders and ladder 2 is a correct 1-step ladder. On the first picture the lengths of planks are [3,3] for the base and [1] for the step. On the second picture lengths are [3,3] for the base and [2] for the step. On the third picture lengths are [3,4] for the base and [2,3] for the steps.

![A](A.PNG)
You have n planks. The length of the i-th planks is a<sub>i</sub>. You don't have a saw, so you can't cut the planks you have. Though you have a hammer and nails, so you can assemble the improvised "ladder" from the planks.

The question is: what is the maximum number k such that you can choose some subset of the given planks and assemble a k-step ladder using them?
#### Input:
The first line contains a single integer T (1≤T≤100) — the number of queries. The queries are independent.

Each query consists of two lines. The first line contains a single integer n (2≤n≤10<sup>5</sup>) — the number of planks you have.

The second line contains n integers a<sub>1</sub>,a<sub>2</sub>,…,a<sub>n</sub> (1≤a<sub>i</sub>≤10<sup>5</sup>) — the lengths of the corresponding planks.

It's guaranteed that the total number of planks from all queries doesn't exceed 105.
#### Output:
Print T integers — one per query. The i-th integer is the maximum number k, such that you can choose some subset of the planks given in the i-th query and assemble a k-step ladder using them.

Print 0 if you can't make even 1-step ladder from the given set of planks.
#### 範例:
input:
```
4
4
1 3 1 3
3
3 3 2
5
2 3 3 4 2
3
1 1 2
```
output:
```
2
1
2
0
```

#### Note:

#### 題意:
第一個輸入為T個木梯
第二個輸入為N個木條
接著輸入a<sub>1</sub>....a<sub>n</sub>個木條長度

題目問你他要請你幫他隨便造出一個木梯，但是因為沒有工具，所以木頭不行切割，利用這些木頭可以造出幾個階梯的木梯?(木頭間格距離為1)
#### 思路:
在輸入的過程中尋找第一長的木條max1與第二長的木條max2，將第二長的木條長度減去1，因為最上面木梯不能建階梯，接著我們把第二長木條長度和剩餘的木條數相比,如果木條數較小,代表他無法把階梯建造完全,會在中途用光木條數,此時木條數就是最多可以造出幾個階梯數,如果木條數大於第二常木條長度,表示他可以完全建造完畢,所以此時第二長的木條長度-1即是可以造出的階梯數.

#### 程式碼:
<script src="https://gist.github.com/Daviswww/6b5a155e8e6747f7dd817d186437a46c.js"></script>

