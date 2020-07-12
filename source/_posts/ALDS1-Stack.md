---
title: AOJ ALDS1_3_A
keywords: ALDS1 Stack
date: 2020-07-12 17:29:12
categories:
tags:
    - implementation
---
# AOJ ALDS1_3_A - Stack
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_3_A)

#### 題意:
Reverse Polish表示法是每個運算符都遵循其所有操作數的一種表示法。例如，正常符號中的表達式（1 + 2）*（5 + 4）可以用Reverse Polish表示為1 2 + 5 4 + *。Reverse Polish的優點之一是它沒有括號。

編寫一個程序，該程序以"Reverse Polish"符號讀取表達式並打印計算結果。
<!-- more -->
#### 思路:
利用stack先進後出的規則存取每個數字，遇到＋,-,*就把上面兩個數字排出並作運算，算完後再放入stack中。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/c3b0db7392bc501256200706688ca8bc.js"></script>