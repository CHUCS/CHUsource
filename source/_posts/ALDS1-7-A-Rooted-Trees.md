---
title: AOJ ALDS1_7_A - Rooted Trees
keywords: AOJ ALDS1_7_A Rooted Trees
date: 2020-07-15 16:05:42
categories: AOJ
tags:
    - implementation
---
# 根樹
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_7_A)

#### 題意:
Rooted Trees是連接的，無環的，無向的圖。Rooted Trees是一種自由樹，其中一個頂點與另一個頂點是不同的。Rooted Trees的頂點稱為“節點”。
你的任務是編寫一個程序，為給定的根樹T的每個節點u報告以下信息：
node ID of u (節點編號)
parent of u (節點父親)
depth of u (節點深度)
node type (root, internal node or leaf)
a list of chidlren of u (列出節點小孩)
<!-- more -->
#### 思路:
先創立一個結構parent、depth、type和internalNode方便紀錄我們的資料，接下來我們輸入每筆資料的時候就把自己節點的父親深度加一，就可以得到自己節點的深度，然後在子節點裡面，我們也做一樣的事情然後順便紀錄子節點的父親。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/c3dfdc3026767577257e91a5902bae1d.js"></script>