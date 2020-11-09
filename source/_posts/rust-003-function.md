---
title: Rust 003 Function
keywords: rust-003-function
date: 2020-11-09 20:21:48
categories: Rust tutorials
tags:
---
# Rust 函式

我們可以在src下創建一個新的檔案`print.rs`，編寫一下程式。

```rust=
pub fn run(){
    println!("Hello print.rs run!!")
}
```
<!-- more -->
然後我們回到主程式來引用我們寫得函式。


```rust=
mod print;

fn main() {
    print::run();
}

```

接著執行就可以看到我們的結果了。

![](iMTn529.png)