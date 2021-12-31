---
title: AOJ ITP1_7_A Grading
keywords: ITP1_7_A Grading
categories: AOJ
tags:
  - implementation
date: 2020-06-14 09:43:47
---
# AOJ ITP1_7_A - Grading
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_7_A)

#### 題意:
輸入三個數字分別為期中考期末考與補考-1代表缺考。
按照規則幫學生打分數：
● 如果學生不參加期中考試或期末考試，則其成績應為F。
● 如果期中和期末考試的總分大於或等於80，則學生的成績應為A。
● 如果期中考試和期末考試的總分大於或等於65且小於80，則學生的成績應為B。
● 如果期中考試和期末考試的總分大於或等於50且小於65，則學生的成績應為C。
● 如果期中和期末考試的總分大於或等於30且小於50，則該學生的成績為D。但是，如
● 果補考的分數大於或等於50，則該成績為C。
● 如果期中和期末考試的總分小於30，則學生的成績應為F。
<!-- more -->
#### 思路:
按照規則寫。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/9cc4ed69e10fe8eedc5fcd80245a19ac.js"></script>