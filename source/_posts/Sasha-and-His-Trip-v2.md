---
title: Codeforces 1113A (dp)
keywords: Codeforces Sasha and His Trip, Codeforces 1113A
date: 2020-05-30 19:05:06
categories: Codeforces
tags:
    - dp
    - greedy
    - math
---
# Codeforces 1113A - Sasha and His Trip (dp)
[題目網址](https://codeforces.com/problemset/problem/1113/A)

#### 題意:
Sasha喜歡到處旅行，在Sasha的國家裡有n座城市，這n座城市是連成一直線的且每座城市間距離相同，每去一座城市需要1公升的汽油，Sasha想要去這n座城市，Sasha有一台能裝v公升汽油的車，但這台車現在沒有汽油，每座城市都有加油站，第i座城市每一公升需要i的價錢，Sasha希望能花最少的錢完成這趟旅行，請問Sasha「最少」需要花多少錢來完成這趟旅行?
<!-- more -->
#### 思路:
由於不能有加超過油箱v，所以要花最少錢加油的話越早加油越好，所以我們可以先建一個油表來表示到那裡要花多少錢，如果n-m>=1代表油不夠，我們就看差多少距離查油表。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/32811888fa30e8313d3acf0936359d83.js"></script>