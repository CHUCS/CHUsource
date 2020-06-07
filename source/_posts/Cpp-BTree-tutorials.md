---
title: Build the Binary Tree tutorials
keywords: Binary tree
date: 2020-06-07 16:40:37
categories: C++ tutorials
tags: 
    - tutorials
    - cpp
---
# Binary Tree tutorials

## 介紹
二元樹是一種樹的資料結構，其中每個節點最多具有兩個子節點，分別稱為左節點和右節點。

## 完整代碼:
<script src="https://gist.github.com/Daviswww/057b8a423219e1bbdcd14b2d1f25cf0d.js"></script>

### 結構
所以我們必須先建造一個結構包含父節點與左右兩個子結點。

```
struct Node{
    int key;
    Node *left;
    Node *right;
};
```
### 創建一個新節點
生成一個新的節點並設定它的父節點為key。
```
Node* createNode(int key){
    Node* node = new Node();
    node->key = key;
    node->left = NULL;
    node->right = NULL;
    return node;
}
```
### 搜索節點(BFS)
將節點放入queue後檢查左節點與右節點使否為空，如果不為空就將他放繼續放入queue中直到找到索引為止。

舉例：
```
    1
   / \
  2   3
 / \
4   5
```
q: 1
檢查1左節點是否為NULL，放入
q: 2
檢查1右節點是否為NULL，放入
q: 2 3
檢查2左節點是否為NULL，放入
q: 3 4
檢查2右節點是否為NULL，放入
q: 3 4 5
檢查3左節點是否為NULL，放入
q: 4 5
檢查3右節點是否為NULL，不放入
q: 4 5
.
.
.
檢查5右節點是否為NULL，不放入
q: 5
```
Node* search(Node* root, int key){
    queue<Node*> q;
    q.push(root);

    while(!q.empty()){
        Node *temp = q.front();
        q.pop();
        if(temp->key == key) return temp;
        if(temp->left != NULL) q.push(temp->left);
        if(temp->right != NULL) q.push(temp->right);
    }
    return NULL;
}
```

### 插入
先創建一個新的節點，在利用剛剛寫好的查詢功能搜尋父節點，接著插入空的子節點位置完成新增。
```
void insert(Node *root, int parent, int key){
    Node *nodeToInsert = createNode(key); 
    Node *node = search(root, parent);
    if(node->left == NULL) {
        node->left = nodeToInsert;
        return;
    }
    if(node->right == NULL) {
        node->right = nodeToInsert;
        return;
    }
}
```