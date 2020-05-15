---
title: Codeforces 1251A
date: 2020-04-15 13:18:14
tags:
    - brute force
    - strings
    - two pointers
    - 普通
---
# Codeforces 1251A - Broken Keyboard
[Broken Keyboard](https://codeforces.com/problemset/problem/1251/A)


#### 題意:
現在有一個只會輸入26個英文小寫字母的鍵盤，有些鍵是正常的，有些是壞掉的，壞掉的鍵按一次會輸入兩個字，輸入過程中保證按鍵的好壞狀態不會改變。現在給你一些輸入完的字串，問你根據這個字串能保證是好的鍵有哪些，沒有就輸出空字串，有的話要依照字母順序輸出？
<!-- more -->
#### 思路:
從最前面開始看所有字連續出現的次數，有曾經出現連續奇數次的話就能保證是正常的，記錄起來後輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a3439ebfaa877a471d3723c30ef9d54b.js"></script>