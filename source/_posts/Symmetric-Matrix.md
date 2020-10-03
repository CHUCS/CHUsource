---
title: Codeforces 1426B
keywords: Codeforces Symmetric Matrix, Codeforces 1426B
date: 2020-10-03 15:09:56
categories: Codeforces
tags:
    - implementation
    - 900
---
# Codeforces 1426B - Symmetric Matrix
[題目網址](https://codeforces.com/problemset/problem/1426/B)

#### 題意:
Masha有n種類型2x2大小的磁磚，磁磚上每格各有一個數字，Masha想利用這幾種磁磚組成mxm的矩形(可用任意種類與任意數量組成)，然後Masha希望這個矩形上的數字是對稱的--對任一對位置(i,j)要符合s[i][j] = s[j][i]，請問Masha有辦法組成他想要的矩形嗎?
<!-- more -->
#### 思路:
當m為奇數就不可能用2x2組成，觀察後可以發現當磁磚右上與左下數字相同必能符合對稱條件，反之則不符合對稱條件，因此在n種磁磚中有一種右上左下數字相同就能組成。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/bded1c9c1f388bf6a4f1a331a2a08147.js"></script>