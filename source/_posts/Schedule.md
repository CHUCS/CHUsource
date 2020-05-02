---
title: Codeforces 31C Schedule
date: 2020-04-27 17:02:28
tags:
    - implementation
---
[Codeforces 31C](https://codeforces.com/problemset/problem/31/c)
<!-- more -->

#### 題意:
給你n個課程的開始及結束時間，問你能不能只刪掉一個就讓所有課程的時間不重疊？

#### 思路:
紀錄每個時間的開始及結束，排序，找同時有兩堂課重疊的最早及最晚，檢查有沒有課程比這個時間範圍大的，有的話該課程符合條件；沒有兩堂課重疊的話，所有課程都是答案；有三堂課同時重疊的話，沒有答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/397506b1a3517cded062fec9603cbfd6.js"></script>