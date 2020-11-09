---
title: Rust 001 Install
keywords: rust-001-install
date: 2020-11-09 20:13:19
categories: Rust tutorials
tags:
    - rust
---
# RUST 介紹與安裝
## 優點

安全：Rust 擁有豐富類型系統和所有權模型，保證了內存安全性和線程安全性。

並發：Rust 可讓程序在編譯時並發執行，也就是多個事件在同一時間間隔執行，並且將安全與並發完美統一。

高效：Rust 快且節省內存。

<!-- more -->
## 安裝 RUST
到[RUST](https://www.rust-lang.org/)的官網按下`get started`然後你會看到下載畫面，選擇你的作業系統下載對應的下載檔案，通常他會先替你選好。

![](E2SfgQY.png)

打開你下載好的`rustup-init`檔案，打開後你會看到他所幫你安裝的路徑等資訊，接著在終端機內輸入1使用預設的安裝。

![](MOrVY0n.png)

  
安裝完後可以在終端機輸入`rustc --version`和`cargo --version`查看你所安裝版本。


接下來下載`Visual Studio Code`，打開後點擊左邊第四個選項來新增RUST套件，新增完後重新載入`Visual Studio Code`，然後右下角會跳出安裝RUST提醒就直接`install`。
![](Dt3OZKz.png)

新建一個`hello.rs`然後打開檔案將以下程式碼寫入。

```rust=
fn main() {
    println!("Hello, world!");
}
```

完成後打開終端機到檔案下的目錄執行下面的指令。
```bash=
$ rustc hello.rs
$ ./hello
```