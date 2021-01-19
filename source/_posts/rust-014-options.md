---
title: Rust 013 Options
keywords: rust 013 options
date: 2021-01-19 14:03:44
categories: Rust tutorials
tags:
    - rust
---
# Options
利用Options回傳一個直來判斷函式中有沒有錯誤，如果有錯誤就可以為傳None否則回傳Some，而在Some裡面的直就是回傳變數的值。我們可以利用下面的程式碼來判斷y是不是為零，如果是零就回傳None否則回傳相除。
<!-- more -->
```rust=
fn div(x: f64, y: f64) -> Option<f64> {
    if y == 0.0 {
        None
    } else {
        Some(x / y)
    }
}

fn main() {
    let res = div(5.0, 7.0);
    match res {
        Some(x) => println!("{:.3}", x),
        None => println!("y == 0"),
    }
}
```
