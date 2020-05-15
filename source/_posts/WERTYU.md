---
title: UVA 10082
date: 2019-11-17 10:21:35
tags:
- implementation
---
# UVA 10082 - WERTYU
[WERTYU](https://onlinejudge.org/external/100/10082.pdf)


#### 題意:
他請你幫他解密，規則是他敲的鍵盤左邊那個才是原本的答案，例如他敲O你要輸出I這樣。
<!-- more -->
#### 思路:
我們可以先建一個鍵盤的表，然後逐一搜尋，找到一樣的我就取他左邊那個，空白的話就直接印。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/13b38d45451133452556dd4e7fd5cdaa.js"></script>