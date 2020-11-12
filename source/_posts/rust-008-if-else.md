---
title: Rust 008 If Else
keywords: rust 008 if else
date: 2020-11-12 20:25:48
categories: Rust tutorials
tags: 
    - rust
---
# Rust 判斷句
在許多的程式語言中，我們可以看到幾乎都有一些比較的符號來判斷，例如`>=`, `<=`, `==`那比較特別的是不等於，在程式中的不等於是`!=`，介紹完這些候我們就可以來討論判斷句了。
<!-- more -->
## #if else
這裡我們要介紹`if`和`else`，如果n%2==0成立的話就印出`even`，否則就印出`odd`，就如字面上的意思一樣。

```rust=
fn if_else(n: u32){
    if (n % 2) == 0 {
        println!("even");
    }else{
        println!("odd");
    }
}

fn main() {
    if_else(5);
}
```

## #if, else if
這邊所要展示的是多個判斷，就是說如果A沒有達成，又如果B沒有達成的依此類推，你可以用此方法把他們寫在一起。

```rust=
fn if_else_if_else(n: u32){
    if n == 0 {
        println!("zero");
    }else if (n % 2) == 0{
        println!("even");
    }else {
        println!("odd");
    }
}

fn main() {
    if_else_if_else(5);
}
```
## #let a = if
我們也可以用if else來給予變數值，但是要注意這些變數綁定的類型必須相同，否則會有錯誤。
```rust=
fn if_else_var(go: bool){
    let k = if go {
        10
    } else {
        20
    };
    println!("{}", k);
}

fn main() {
    if_else_var(true);
}
```