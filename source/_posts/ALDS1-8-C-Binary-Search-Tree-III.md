---
title: AOJ ALDS1_8_C - Binary Search Tree III
keywords: ALDS1_8_C Binary Search Tree III
date: 2020-08-24 13:45:44
categories: AOJ
tags:
    - implementation
---
# 二元樹搜索 - 刪除
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_8_C)

#### 題意:
編程一個擁有新增、查詢、刪除功能的二元樹，在每次新增點時，如果key大於node->key，就新增在node->right，否則新增在node->left。最後輸出Preorder與Inorder。
<!-- more -->

#### 程式碼:
<script src="https://gist.github.com/Daviswww/e5a835cfa1a3f511e096388e9697423c.js"></script>