---
title: Rust 007 Struct and Methods
keywords: Rust 007 Struct and Methods
date: 2020-11-11 20:45:13
categories: Rust tutorials
tags:
    - rust
---
# Rust 結構與模塊
Struct是自定義的數據類型，因此我們可以自行定義，而他也使我們能夠根據自己的需求調整數據的結構。Methods是將你所有的函式包裝再一起，而當你可以在這個模組下找到相關的函式。
<!-- more -->
## Struct
我們利用Struct定義我們結構，他就像一個物件一樣包含了所有你所定義的東西，當你需要取得值時你只需要`name.a`或是`name.b`就可以輕鬆地取得。

```rust=
struct Object{
    width: u32,
    height: u32,
}
```

接著我們創建一個函式來計算面積，傳進去的東西就是我們剛剛所宣告的物件。

```rust=
fn area(obj: Object) -> u32 {
    return obj.width * obj.height;
}
```

在這邊我們利用我們所創的結構將整個物件傳入函式，你可以在Object裡面拿到你所定義的值，當你的值越多時，他可以讓你的程式碼更加得清楚，使用起來更加方便。

```rust=
struct Object{
    width: u32,
    height: u32,
}

fn area(obj: Object) -> u32 {
    return obj.width * obj.height;
}

fn run() {
    let o = Object {
        width: 10,
        height: 5,
    };

    println!("{}", area(o));
}

fn main() {
    run();
}
```

# Impl

impl關鍵字被主要用於對類型限定的方式，而`impl`中定義的功能可以是獨立的，這意味著將其稱為`hello::world()`。這有點類似於`hello.world()`的概念。  

在使用`impl`時我們一樣先創建一個`struct`來定義我們所需要的數據。
```rust=
struct Object{
    width: u32,
    height: u32,
}
```
創建完後將`impl`與創建得`struct`名稱宣告成一樣的，這將會使他綁定再一起的感覺，你可以在裡面使用你所宣告的數據。`self`得用意是引用當前模塊和標記方法的接收者，這就是為什麼下面還有一個`new`的函式，我將直傳進去後在當前的模塊中，`self`就可以拿到我所須要的數據，而這邊有一個很特別的點是，`new`裡面的`Object`可以不用寫成`width:width`，因為在rust中只要他定義的名字是一樣的就會動傳到裡面去。

```
struct Object{
    width: u32,
    height: u32,
}

impl Object {
    fn area(&self) -> u32 {
        return self.width * self.height;
    }
    
    fn new(width: u32, height: u32) -> Object {
        Object {
            width,
            height,
        }
    }
}

fn run() {
    let obj = Object::new(10, 3);

    println!("{}", obj.area());
}

fn main() {
    run();
}
```
如果你想要把它拆的細一點，你也可以把`new`和`area`拆開寫也是可以的。

```rust=
impl Object {
    fn area(&self) -> u32 {
        return self.width * self.height;
    }
}

impl Object{
    fn new(width: u32, height: u32) -> Object {
        Object {
            width,
            height,
        }
    }
}
```