---
title: Codeforces 1113A
keywords: Codeforces Sasha and His Trip, Codeforces 1113A
date: 2020-05-29 19:05:06
categories: Codeforces
tags:
    - Dynamic programming
    - dp
    - greedy
    - math
    - 動態規劃
    - 貪婪
    - 數學
---
# Codeforces 1113A - Sasha and His Trip
[題目網址](https://codeforces.com/problemset/problem/1113/A)

#### 題意:
Sasha喜歡到處旅行，在Sasha的國家裡有n座城市，這n座城市是連成一直線的且每座城市間距離相同，每去一座城市需要1公升的汽油，Sasha想要去這n座城市，Sasha有一台能裝v公升汽油的車，但這台車現在沒有汽油，每座城市都有加油站，第i座城市每一公升需要i的價錢，Sasha希望能花最少的錢完成這趟旅行，請問Sasha「最少」需要花多少錢來完成這趟旅行?
<!-- more -->
#### 思路:
要花最少錢，則越早加油越好且不能有多餘的汽油，如果路的長度n-1比容量v還小，那n-1就是答案，如果n-1>v，紀錄會剩下多長的路(n-1-v)，從第二個城市開始每次都加一次油(錢)，最後加總就是答案。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/6dfa1886c95cd8ee5d58dfd7509ebbe6.js"></script>