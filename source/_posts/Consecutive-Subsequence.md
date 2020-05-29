---
title: Codeforces 977F
keywords: Codeforces Consecutive Subsequence, Codeforces 977F
date: 2020-05-29 00:55:42
categories: Codeforces
tags:
    - Dynamic programming
    - dp
    - 動態規劃
    - 普通
---
# Codeforces 977F - Consecutive Subsequence
[題目網址](https://codeforces.com/problemset/problem/977/F)

#### 題意:
輸入長度為n的數字序列，希望找出一個「最長為k」的子序列為[x, x+1,...,x+k-1]並印出「最長長度k」及相符的「元素位置」，如有多個答案印出任一個。
<!-- more -->
一個序列中可刪除任一或多個元素形成子序列，也可以不刪除任何元素，例如:序列[5,3,1,2,4]的子序列可以為[3],[5,3,1,2,4],[5,1,4],[3,1,4]等，但[1,2,3]不是子序列。
#### 思路:
因為子序列數字是連續的，所以數字x可能的最長長度會是x-1的最長長度+1，例如:
假設發現某位置x=6有最長長度k=4，代表序列中有其中一個6，他的前面就會有3,4,5，若從此位置往下找發現7，則x=7的最長長度就會是k=5。
因此利用map來記錄所有數字的最長長度，找出其中長度最長的數字就可以了。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/d3a06af1beaac5bfe4cf1d7493466a11.js"></script>
