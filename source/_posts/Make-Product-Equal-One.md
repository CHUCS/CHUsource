---
title: Codeforces 1206B
keywords: Codeforces Make Product Equal One, Codeforces 1206B
date: 2020-05-29 00:56:52
categories: Codeforces
tags:
    - dp
    - implementation
    - 900
---
# Codeforces 1206B - Make Product Equal One
[題目網址](https://codeforces.com/problemset/problem/1206/B)

#### 題意:
給你n個數字，你可以對每個數字進行+1或-1的操作，每次操作就是一次動作，希望最後將所有數字相乘結果為1，請問需要「最少」幾次動作能使所有數字相乘結果為1?
<!-- more -->
#### 思路:
相乘為1就代表n個數字都必須調整成+1或-1，並且-1不能是奇數個，要最少動作，所以正數一定調整成1，負數一定調整成-1，零分開計算，如果有零就不需調整正負值，如果沒有零則最後答案+2(-1變+1是2動作)
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/f403062a1e75f40fb75f6bc72444807f.js"></script>