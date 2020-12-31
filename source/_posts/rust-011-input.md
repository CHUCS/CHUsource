---
title: Rust 011 Input
keywords: rust-011-input
date: 2020-12-31 14:46:07
categories: Rust tutorials
tags:
    - rust
---
# Rust 輸入
### 單一輸入
利用rust的標準輸入法輸入一行字串，`std::io::stdin()`
```rust=
fn main() {
    let mut s = String::new();
    std::io::stdin().read_line(&mut s).expect("err read");
        println!("{}", s);
}
```
<!-- more -->

如果使用一個loop在這裡輸入時你會發現你的輸入會一直連續下去，跟其他語言不同他並不會取代掉原本的輸入，只要不重新new原本的變數的話輸入是會一直連續下去的，因此輸入後可以對字串進行切割等處理。

```rust=
fn main() {
    let mut s = String::new();

    loop{
        std::io::stdin().read_line(&mut s).expect("err read");
        println!("{}", s);
    }

}
```
![](vHHdK7O.png)


### 重新產生避免連續
又或者我們可以寫成一個函式讓他每次都重新產生一次。

```rust=
fn main() {
    let input = single_input();
    println!("{}", input);
}

fn single_input() -> String {
    let mut s = String::new();
    std::io::stdin().read_line(&mut s).expect("err read");
    return s;
}
```

![](SZeE6yq.png)

### 輸入型態轉換
接著我們來將依行輸入轉成其他的型態，由下面來看關鍵的就是我們將上面return的`String`改成`i32`，接著最重要的一行就是我們將字串轉成其他的型態`s.trim().parse::<i32>().unwrap();`，我們來將它分解開來逐一介紹。

`trim()`的意思是會把字串前後不重要的符號都移除 (例如空白跟換行符號)。  

`parse::<T>()`是可以解析成其他的型態，只要在角括號裡改成想要的型態就可以了。  

`unwrap()`很多情況下 function 吐回來的東西是 Result，Result 的意思是他除了是你想要的東西之外，也有可能是一個錯誤一般情況下應該要處理這個錯誤，如果對 Result 做 unwrap() 代表忽略錯誤的情況真的發生錯誤時就直接讓程式終止。

```rust=
fn main() {
    let input: i32 = single_input();
    println!("Output: {}", input);
}

fn single_input() -> i32 {
    let mut s = String::new();
    std::io::stdin().read_line(&mut s).expect("err read");
    return s.trim().parse::<i32>().unwrap();
}
```
![](T8IzkIC.png)

### 輸入後存進vector
如果你的輸入是輸入一個換一行的話，你可以將每次的輸入都`push`進一個vec內，這樣所有的值都可以存在你所創的vec內。
```rust=
fn main() {
    let mut vec = Vec::new();
    
    for i in 0..3 {
        let input: i32 = single_input();
        vec.push(input);
    }
    
    for i in vec {
        println!("{}", i);
    }
}

fn single_input() -> i32 {
    let mut s = String::new();
    std::io::stdin().read_line(&mut s).expect("err read");
    return s.trim().parse::<i32>().unwrap();
}
```
![](x64eg4b.png)
