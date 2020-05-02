---
title: UVA 10340 All in All
date: 2019-11-17 10:28:54
tags:
- implementation
---
[UVA10340](https://onlinejudge.org/external/103/10340.pdf)
<!-- more -->

#### 題意:
幫他找出A字串在不再B字串裡面，沒有連續沒關西。

#### 思路:
逐一檢查有沒有匹配到相同的字，如果有就換下一個字直到然後次數加一，最後檢查相同的次數等不等於原本的長度，就可以知道答案了。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/8f601b9d5c30cf3a6bd30a1c93650b31.js"></script>