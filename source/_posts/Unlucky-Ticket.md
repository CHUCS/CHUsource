---
title: Codeforces 160B
date: 2020-04-14 13:05:42
keywords: Codeforces 160B, Codeforces Unlucky Ticket
categories: Codeforces
tags:
    - greedy
    - sortings
    - 簡單
---
# Codeforces 160B - Unlucky Ticket
[Unlucky Ticket](https://codeforces.com/problemset/problem/160/B)


#### 題意:
一張票券上的序號會由偶數個數字組成，如果前半的每個數字，都能不重複地找到一個後半的數字比它大；或是前半的每個數字，都能不重複地找到一個後半的數字比它小，則稱這張票券為不幸運票券。現在輸入票券序號，問你它是否是不幸運票券？
<!-- more -->
#### 思路:
將前半及後半各自排序，然後比對是否每個數字都比較大或每個數字比較小。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/807796ebbf46f2126719277a42631a32.js"></script>