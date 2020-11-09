---
title: Rust 002 Project
keywords: rust-002-project
date: 2020-11-09 20:15:13
categories: Rust tutorials
tags:
    - rust
---
# Rust 第一個專案

安裝完RUST後我們可以開始寫我們第一個RUST得程式了，首先我們先下`cargo init`這將會替我們創建一些基本的檔案。

```bash=
$ cargo init
```
<!-- more -->
![](uMvHeRj.png)

目錄應該是長下面這樣，`Cargo.toml`裡面寫的是一些設定檔案，版本訊息等等，`main.rs`則是我們主要寫程式的地方。
```
.
|-- Cargo.toml
`-- src
    `-- main.rs
```

然後打開`main.rs`編寫我們第一個RUST程式。
```rust=
fn main() {
    println!("Hello, world!");
}
```

接著執行程式

```bash=
$ cargo run
```

![](J4JlXIU.png)

執行完後你會看到你剛剛寫的`Hello, world!`印在終端機上面。

如果你不想要執行程式的話可以輸入`build`就好。
```bash=
$ cargo build
```
![](vudWD4D.png)