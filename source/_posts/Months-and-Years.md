---
title: Codeforces 899B
date: 2019-04-20 18:50:27
tags:
    - implementation
    - 簡單
---
# Codeforces 899B - Months and Years
[Months and Years](https://codeforces.com/problemset/problem/899/B)

Everybody in Russia uses Gregorian calendar. In this calendar there are 31 days in January, 28 or 29 days in February (depending on whether the year is leap or not), 31 days in March, 30 days in April, 31 days in May, 30 in June, 31 in July, 31 in August, 30 in September, 31 in October, 30 in November, 31 in December.
<!-- more -->
A year is leap in one of two cases: either its number is divisible by 4, but not divisible by 100, or is divisible by 400. For example, the following years are leap: 2000, 2004, but years 1900 and 2018 are not leap.

In this problem you are given n (1 ≤ n ≤ 24) integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub>, and you have to check if these integers could be durations in days of n consecutive months, according to Gregorian calendar. Note that these months could belong to several consecutive years. In other words, check if there is a month in some year, such that its duration is a<sub>1</sub> days, duration of the next month is a<sub>2</sub> days, and so on.

#### Input:
The first line contains single integer n (1 ≤ n ≤ 24) — the number of integers.

The second line contains n integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> (28 ≤ a<sub>i</sub> ≤ 31) — the numbers you are to check.

#### Output:
If there are several consecutive months that fit the sequence, print "YES" (without quotes). Otherwise, print "NO" (without quotes).

You can print each letter in arbitrary case (small or large).

#### 範例:
input:
```
4
31 31 30 31
```
output:
```
Yes
```
input:
```
2
30 30
```
output:
```
No
```
input:
```
5
29 31 30 31 30
```
output:
```
Yes
```
input:
```
3
31 28 30
```
output:
```
No
```
input:
```
3
31 31 28
```
output:
```
Yes
```
#### Note:
In the first example the integers can denote months July, August, September and October.

In the second example the answer is no, because there are no two consecutive months each having 30 days.

In the third example the months are: February (leap year) — March — April – May — June.

In the fourth example the number of days in the second month is 28, so this is February. March follows February and has 31 days, but not 30, so the answer is NO.

In the fifth example the months are: December — January — February (non-leap year).

#### 題意:
給你一個連續的月份天數，問你這個連續的月份有沒有可能出現？

#### 思路:
先創一個正常年份的天數陣列，接著是閏年的2月處理，因為只輸入最多24個月(2年)，因此不可能出現兩個閏年，因此紀錄29天的次數，超過1次就不可能。其他情況可以把閏年順移到平年，因此直接把29當28處理，接著將所有月份當起點試試能不能滿足輸入即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a21f1a4f07f6179796e9e9878219b838.js"></script>
