---
title: K Dimensional Tree
keywords: k-dimensional tree, K-D tree
date: 2020-06-12 12:50:39
categories: C++ tutorials
tags: 
    - tutorials
    - cpp
---
# K-Dimensional Tree tutorials

## 介紹
K元樹是一種樹的資料結構，其中每個節點可以有很多的子節點。
<!-- more -->
## 完整代碼:
<script src="https://gist.github.com/Daviswww/bde0499460a088ad106e51154c6630f2.js"></script>

### 結構
所以我們必須先建造一個結構包含父節點與一個動態陣列以便於我們利用。

```
struct Node{
    int key;
    vector<Node *> child;
};
```
### 創建一個新節點
生成一個新的節點並設定它的父節點為key，而每一個key下面都有一個動態陣列。
```
Node* createNode(int key){
    Node* node = new Node();
    node->key = key;
    return node;
}
```
### 搜索節點(BFS)
將節點放入queue後檢查陣列是否為空，如果不為空就將他放繼續放入queue中直到找到索引為止。

舉例：
```
      1
   / / \ \
  7  2   3 6
 / \        \ \
4   5        8 9
```
q: vector(root)
檢查vector(root)[0]下面陣列是否為NULL，放入
q: vector(1)
檢查vector(1)[0]下面的陣列是否為空，放入
q: vector(7)
檢查vector(1)[1]下面的陣列是否為空，不放入
q: vector(7)
檢查vector(1)[2]下面的陣列是否為空，不放入
q: vector(7)
檢查vector(1)[3]下面的陣列是否為空，放入
q: vector(7), vector(6)
檢查vector(7)[0]下面的陣列是否為空，不放入
q: vector(6)
.
.
.
檢查vector(6)[1]下面的陣列是否為空，不放入
q:

```
Node* search(Node *root, int key){
    queue<Node*> q;
    q.push(root);
    if(root->key == key){
        return root;
    }else{
        while(!q.empty()){
            Node *temp = q.front();
            q.pop();
            for(int i = 0; i < temp->child.size(); i++){
                if(temp->child[i]->key == key){
                    return temp->child[i];
                }
                if(!temp->child[i]->child.empty()){
                    q.push(temp->child[i]);
                }
            }
        }
    }
    return NULL;
}
```

### 插入
先創建一個新的節點，在利用剛剛寫好的查詢功能搜尋父節點，接著放入動態陣列內的最後面，與queue的push一樣。
```
void insert(Node *root, int parent, int key){
    Node *nodeToInsert = createNode(key);
    Node *node = search(root, parent);
    if(node != NULL){
        (node->child).push_back(nodeToInsert);
    }else{
        cout << "No" << endl;
        return;
    }
}
```