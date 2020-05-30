---
title: Codeforces 1020B
keywords: Codeforces Badge, Codeforces 1020B
date: 2020-05-30 20:49:45
categories: Codeforces
tags:
    - brute force
    - dfs and similar
    - graphs
    - 1000
---
# Codeforces 1020B - Badge
[題目網址](https://codeforces.com/problemset/problem/1020/b)

#### 題意:
老師要在調皮的學生的徽章上打洞，有n位調皮的學生，每位學生都會回答另一位同學才是，過程持續了一段時間，老師最後遇到已經有被打洞的學生，老師最後在徽章上打了第二次洞，並結束這個過程。
你不知道第一位被打洞得學生是誰，但你知道每一位學生指誰是下一位，你的任務是，當每一位學生是第一位時，找出最後會是誰被打兩次洞。
<!-- more -->
#### 思路:
用一個陣列存學生被選中的次數，第一個出現第二次就是答案。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/a5a9bbcaa6db979e131db5bbeefc11b5.js"></script>