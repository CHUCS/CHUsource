---
title: AOJ ALDS1_7_B - Binary Tree
keywords: ALDS1_7_B Binary Tree
date: 2020-07-18 15:53:01
categories: AOJ
tags:
    - implementation
---
# 二元樹
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_7_B)

#### 題意:
有根的二叉樹是具有根節點的樹，其中每個節點最多有兩個子節點。

您的任務是編寫一個程序，該程序讀取有根的二叉樹T並為T的每個節點u打印以下信息：
node ID of u (節點編號)
parent of u (節點父親)
sibling of u (節點兄弟)
the number of children of u (節點小孩數目)
depth of u (節點深度)
height of u (節點高)
node type (root, internal node or leaf) (節點狀態)
<!-- more -->
#### 思路:
##### sibling 兄弟
如果左節點跟右節點都不為-1就代表有兄弟。
```C++
if(tree[id].left != -1 && tree[id].right != -1) {
    tree[left].sibling = right;
    tree[right].sibling = left;
}
```
##### degree ＆ children parent 子節點個數與子節點父親
計算子節點數並順便將子節點的父親標記。
```C++
if(left != -1) {
    tree[id].degree++;
    tree[left].parent = id;
}
if(right != -1) {
    tree[id].degree++;
    tree[right].parent = id;
}
```

##### height 節點高度
一直往下找然後比較最大的深度回傳。
```C++
int dfs(Node *tree, int key) 
{ 
    if (tree[key].left == -1 && tree[key].right == -1) {
        return 0;
    }
    if (tree[key].left == -1) {
        return dfs(tree, tree[key].right) + 1; 
    }
    if (tree[key].right == -1) {
        return dfs(tree, tree[key].left) + 1; 
    }
    
    return max(dfs(tree, tree[key].left), dfs(tree, tree[key].right)) + 1; 
} 
```

##### depth 深度
從根往下並沿路標記深度，深度則是由父親的深度加一就可以得到自己的深度。
```C++
void depth(Node *tree, int key){
    if(tree[key].parent != -1){ 
        tree[key].depth = tree[tree[key].parent].depth + 1;
    }
    if(tree[key].left != -1){
        depth(tree, tree[key].left);
    }
    if(tree[key].right != -1){
        
        depth(tree, tree[key].right);
    }
    return;
}
```

#### 程式碼:
<script src="https://gist.github.com/Daviswww/400e539d787926ef7fc0ef89f881f4a5.js"></script>