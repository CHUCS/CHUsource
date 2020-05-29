---
title: Codeforces 313B
keywords: Codeforces Ilya and Queries, Codeforces 313B
date: 2020-05-29 00:57:33
categories: Codeforces
tags:
    - Dynamic programming
    - dp
    - 動態規劃
---
# Codeforces 313B - Ilya and Queries
[題目網址](https://codeforces.com/problemset/problem/313/B)


#### 題意:
給你一個字串s，由字元"."和"#"組成，共有m個查詢，每個查詢為一組數字(l,r)，代表字串中的位置從左邊l到右邊r，查出此區段間有多少符合s[i] = s[i+1]。
(依題意，長度為n的字串，其字元對應位置為1~n)。
<!-- more -->
#### 思路:
對每個字元s[i]紀錄從第一個字元s[1]到s[i]符合條件的數量，區間l ~ r的答案就會是1 ~ r的答案減掉1~l的答案。 

#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/d2ee5f0909948e0231308c62bbcd921e.js"></script>