---
title: AOJ ALDS1_7_C - Tree Walk
keywords: AOJ ALDS1_7_C Tree Walk
date: 2020-08-11 12:55:23
categories: AOJ
tags:
    - implementation
---
# 樹遍歷
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_7_C)

#### 題意:
您的任務是編寫一個程序，該程序根據以下算法執行樹遍歷（系統遍歷樹中的所有例程）：

1. 根、左子樹和右子樹(preorder)。
2. 左子樹、根子樹和右子樹(inorder)。
3. 左子樹、右子樹和根(postorder)。

<!-- more -->
#### 思路:
創建一個結構left代表左子樹，right代表右子樹，pr代表父節點用於檢查是否為跟節點。

創建一個帶有結構的陣列依序填入所有值。
```C++
for(int i = 0; i < n; i++){
    cin >> key >> left >> right;
    
    tree[key].left = left;
    tree[key].right = right;
    tree[left].pr = key;
    tree[right].pr = key;
    node[i] = key;
}
```

接著尋找父節點，輸入的所有節點檢查pr為-1就是父節點。
```C++
int getRoot(Node* tree, int *node, int n){
    int root = 0;
    for(int i = 0; i < n; i++){
        if(tree[node[i]].pr == -1){
            root = node[i];
        }
    }
    return root;
}
```
最後利用題目上敘的規則遞迴輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b95063f99f1a85b8b827f35fe13c2c35.js"></script>