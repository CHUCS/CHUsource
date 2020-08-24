---
title: AOJ ALDS1_8_A Binary Search Tree I
keywords: ALDS1_8_A Binary Search Tree I
date: 2020-08-24 13:45:19
categories: AOJ
tags:
    - implementation
---
# 二元樹搜索 - 新增
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_8_A)

#### 題意:
編程一個擁有新增功能的二元樹，在每次新增點時，如果key大於node->key，就新增在node->right，否則新增在node->left。最後輸出Preorder與Inorder。

<!-- more -->

#### 程式碼:
<script src="https://gist.github.com/Daviswww/f392df5b2c8130b6eeff6a0b8c1b82bb.js"></script>