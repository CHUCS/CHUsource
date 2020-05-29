---
title: Codeforces 732B
keywords: Codeforces Cormen — The Best Friend Of a Man, Codeforces 732B
date: 2020-05-29 18:59:16
categories: Codeforces
tags:
    - Dynamic programming
    - dp
    - greedy
    - 動態規劃
    - 貪婪
---
# Codeforces 732B - Cormen — The Best Friend Of a Man
[題目網址](https://codeforces.com/problemset/problem/732/B)


#### 題意:
Polycarp養了一隻狗叫Cormen，但Polycarp有個麻煩，Cormen喜歡散步，Cormen在「連續兩天」中至少要散步k次才會開心，如果k=5，而昨天Polycarp帶著Cormen散步2次，那今天必須至少散步3次，再隔一天則至少要散步2次。
Polycarp分析有n天，n天中每天Polycarp帶著Cormen散步a次，請幫Polycarp確定這n天中每天還需要「最少」多散步幾次Cormen才會開心。
<!-- more -->
共增加幾次，並把增加後每天需要散步幾次的結果都印出來。
#### 思路:
從第二天開始都要計算與前一天共散步幾次，不夠的話就補上並更改當天次數。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/441fd43738a5b291154d61494bcaaba5.js"></script>