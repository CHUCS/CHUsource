---
title: UVA 900
date: 2019-12-13 16:52:19
link: Brick-Wall-Patterns
keywords: UVA 900, UVA Brick Wall Patterns
tags:
    - 新手
    - dp
---
# UVA 900 - Brick Wall Patterns
[Brick Wall Patterns](https://onlinejudge.org/external/9/900.pdf)


#### 題意:
給你N個磚頭，問你有幾種排列方式。
<!-- more -->
#### 思路:
仔細觀察數列時會發現有規律，1的時候1、2的時候2、3的時候3、4的時候5....，第三項會是前兩項的和，因此我們可以先建一個表將所有答案算出來，之後利用查表來輸出答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/d3dd936f31d55be2205f5f8be4576bff.js"></script>