---
title: Codeforces 1143C
keywords: Codeforces Queen, Codeforces 1143C
date: 2020-06-11 00:56:44
categories: Codeforces
tags:
    - dfs and similar
    - trees
    - 1400
---
# Codeforces 1143C - Queen
[題目網址](https://codeforces.com/problemset/problem/1143/C)


#### 題意:
給你一棵有根樹，有1~n個頂點，沒有循環圖出現，有一個特殊的點叫做根，根的父級p<sub>i</sub>為-1。
有些點會尊敬長輩，有些不會，c<sub>i</sub> = 1表示不尊敬任何長輩，c<sub>i</sub> = 0表示尊敬所有長輩。
你必須一步步刪除一個非根的點，這的點被刪除的條件為不尊敬父母跟不被所有這個點的小孩尊敬，若一次動作中有多個點可以刪除，從「編號最小」的開始刪除，當這個點被刪除後，他的所有小孩會連接到他的父母。
當沒有點可以刪除後，照順序印出你刪除的點。
<!-- more -->
#### 思路:
思考如果本身是尊敬長輩的，那自己跟父母就不會被刪除，被刪除的點改變連接狀態，但不會影響結果，所以會被刪掉的點找出來後從編號小的點開始輸出。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/4f39d918e9e2586f63f31405ee11f1a1.js"></script>