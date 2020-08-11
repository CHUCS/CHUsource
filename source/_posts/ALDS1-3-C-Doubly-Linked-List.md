---
title: AOJ ALDS1_3_C - Doubly Linked List
keywords: ALDS1 Doubly Linked List
date: 2020-07-13 13:06:41
categories: AOJ
tags:
    - implementation
---
# 雙向鏈結串列
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_3_C)

#### 題意:
寫一個具備以下功能的Doubly Linked List:
insert x: 加入一個元素x在list的最前面.
delete x: 刪除一個元素x. 如果沒有找到，不必做任何動作.
deleteFirst: 刪除list第一個元素.
deleteLast: 刪除list最後一個元素.
<!-- more -->
#### 思路:

##### 節點
```
struct Node{
	int data;
    // 上一個節點
	Node* prev;
    // 下一個節點
	Node* next;
};
```
首先我們要先宣告一個結構分別為資料,上個節點和下一個節點。

##### 新增數字
```
void insertNode(int x){
    Node* tmpNode = motherNode->next;
    motherNode->next = new Node();
    motherNode->next->data = x;
    motherNode->next->next = tmpNode;
    motherNode->next->prev = motherNode;
    tmpNode->prev = motherNode->next;
};
```
先新增一個新節點然後將資料放入後，與主節點做連接。

##### 刪除數字
```
void deleteNode(int x){
    Node* tmpNode = motherNode->next;
    while(tmpNode != motherNode && tmpNode->data != x){
        tmpNode = tmpNode->next;
    }
    if(tmpNode != motherNode){	
        tmpNode->prev->next = tmpNode->next;
        tmpNode->next->prev = tmpNode->prev;
        delete tmpNode;
    }
};
```
逐一檢查節點資料是否為x，如果找到了就將next與prev的節點換成下一個位置的，然後刪除節點。

##### 刪除最前面的
```
void deleteFirst(){
    Node* tmpNode = motherNode->next;
    motherNode->next = motherNode->next->next;
    motherNode->next->prev = motherNode;
    delete tmpNode;	
};
```
將最前面的節點交換後與主節點連接，然後再將他刪除。
##### 刪除最後面的
```
void deleteLast(){
    Node* tmpNode = motherNode->prev;
    motherNode->prev = motherNode->prev->prev;
    motherNode->prev->next = motherNode;
    delete tmpNode; 
};
```
將最後面的節點交換後與主節點連接，然後再將他刪除。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b9f0ee48e8f8965c9b8b30ecaeee9afe.js"></script>