---
title: Codeforces 129B
keywords: Codeforces Students and Shoelaces, Codeforces 129B
date: 2020-05-31 17:18:06
categories: Codeforces
tags:
    - brute force
    - dfs and similar
    - graphs
    - implementation
    - 1200
---
# Codeforces 129B - Students and Shoelaces
[題目網址](https://codeforces.com/problemset/problem/129/B)


#### 題意:
Anna和Maria想要訓斥表現不好的n位學生，因此買了m條鞋帶，每個鞋帶將兩位學生綁在一起，然後會訓斥剛好只有被綁一個鞋帶的所有學生，將這些學生分為一組並且這些學生會將鞋帶帶走，重複找相同狀況的學生直到不符條件。請問學生共被分為幾組訓斥?
<!-- more -->
#### 思路:
用一個二位陣列存鞋帶綁了哪些學生，鞋帶是雙向的所以如果綁了i跟j，那陣列中[i][j]與[j][i]都要記為1，並記錄每一位學生被綁了幾條鞋帶，之後找只有被綁一條的學生，將學生與跟他綁在一起的學生的被綁數-1，並把關係移除，完成一輪就是一組，重複到沒有學生是指綁一條鞋帶為止。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/bef4680413ec760112edf8aba7fe9b1b.js"></script>