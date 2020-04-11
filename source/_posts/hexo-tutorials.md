---
title: 社團網站維護指南
date: 2020-04-11 22:25:27
tags:
    - tutorials
    - hexo
---
# HEXO Documentation

### ＃什麼是 Hexo？
Hexo 是一個快速、簡單且強大的網誌框架。Hexo 使用 Markdown（或其他標記語言）解析您的文章，並在幾秒鐘內，透過漂亮的主題產生靜態檔案。
<!-- more -->
### 安裝需求
安裝 Hexo 相當簡單；然而，在安裝前您必須先檢查下列您的電腦是否已經安裝下列軟體：
● Node.js
● Git

#### 安裝 Git
● Windows：下載並安裝 git.
● Mac：使用 Homebrew, MacPorts 或 安裝程式 安裝。
● Linux (Ubuntu, Debian)：sudo apt-get install git-core
● Linux (Fedora, Red Hat, CentOS)：sudo yum install git-core

#### 安裝 Node.js
[Node.js](https://nodejs.org/en/)

#### 安裝 Hexo 套件
[CHUCS Packages](https://github.com/CHUCS/CHUsource/packages/180164)
```
npm install @chucs/hexo-site@0.0.0
```

### ＃指令

#### 創建一個頁面
```
$ hexo new [layout] <title>
```
範例：hexo new "Codeforces12345"

可以在資料夾內的sources/_posts找到你生成的頁面，上面分別會寫著你的標題、時間和標記你可以隨意更改，而下面空白處則是妳網頁顯示的內容，可以參考[Markdown](https://chucs.github.io/Markdown/4)語法或其他的psot檔撰寫。
```
---
title: 我是留言板
date: 2019-03-02 10:51:33
tags:
    - 留言板
---
```

#### 生成頁面
生成你所撰寫的網頁使你可以瀏覽。
```
$ hexo g
```

#### 啟動本地伺服器
你可以瀏覽你所創建的頁面是否與你想要的一樣。
```
$ hexo s
```

#### 發布到網站
將撰寫完的內容發佈至組織裡使網站更新。
```
$ hexo deploy
```

##### note:
首先你必須擁有一個[Github](https://github.com/)帳號，然後由管理員邀請至社團組織內[CHUCS](https://github.com/CHUCS)，更改為管理員才可以發布。