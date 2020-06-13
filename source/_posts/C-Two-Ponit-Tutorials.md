---
title: Two Ponit Tutorials
date: 2020-04-15 13:49:35
keywords: C++ Two Ponit Tutorials
categories: C++ tutorials
tags:
    - tutorials
    - cpp
---
# C++ Two Ponit Tutorials
### #雙指標
+ 用來從陣列中搜尋特定區間
+ 耗時為O(N)，比暴力法(O(N^2))快
+ 需要在搜尋的區間跟區間長度有關時才能使用
+ 使用兩個index作為左邊界跟右邊界
+ 根據條件，需縮減區間時，左邊界右移
+ 根據條件，需擴增區間時，右邊界右移
+ 透過動態的區間內容搜尋所有可能

<!-- more -->

### #範例

以1133C為範例，此題目給你一組數列，要 求你將他們分組，並滿足每組中最大的減最小的差在5以內，問你最多人的一組可以是多少人。
>先將數列排序，然後依照雙指標的作法
>> 區間最右邊(最大值)減區間最左邊(最小值)的差在5以內，滿足分組條件，嘗試擴充區間，右邊界右移。

>> 差不在5以內，不滿足分組條件，縮減編組，左邊界右移。

<script src="https://gist.github.com/Daviswww/46a2a0419fe4afda45a71ffe94337635.js"></script>