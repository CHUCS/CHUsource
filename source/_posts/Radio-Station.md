---
title: Codeforces 918B
date: 2020-04-30 17:11:21
tags:
    - implementation
    - strings
    - 簡單
---
# Codeforces 918B - Radio Station
[Radio Station](https://codeforces.com/problemset/problem/918/B)

#### 題意:
給你n個伺服器名稱跟ip，再輸入m個命令跟目標ip，要你輸出每個命令跟目標ip加上伺服器名稱。
<!-- more -->
#### 思路:
把伺服器名稱跟ip都先存著，輸入命令時比對ip，並輸出對應伺服器名稱。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/bf0719749e1c4f9b2a5372f84e918992.js"></script>