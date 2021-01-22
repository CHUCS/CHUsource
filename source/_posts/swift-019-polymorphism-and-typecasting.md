---
title: Swift 019 Polymorphism and Typecasting
keywords: swift 019 polymorphism and typecasting
date: 2021-01-22 13:32:51
categories: Swift tutorials
tags:
    - swift
---
# 類別繼承
我們可以先創造一個專輯的類別來定義最基本的屬性，之後我們可以將其他各種專輯繼承專輯這個類別，而當我們創建完後，由於都是屬於專輯的類別，因此可以完美且快速的定義在一起。
<!-- more -->
```swift
class Album {
    var name: String
    
    init(name: String) {
        self.name = name
    }
}

class StudioAlbum: Album {
    var studio: String
    
    init(name: String, studio: String) {
        self.studio = studio
        super.init(name: name)
    }
}

class LiveAlbum: Album {
    var location: String
    
    init(name: String, location: String) {
        self.location = location
        super.init(name: name)
    }
}


var apple = StudioAlbum(name: "Apple", studio: "Pie")
var banana = StudioAlbum(name: "Banana", studio: "ship")
var pear = LiveAlbum(name: "Pear", location: "taiwan")
var allAlbums: [Album] = [apple, banana, pear]
```

我們可以透過定義getPerformance之後再使用override進行修改，之後我們可以快速的將所有的getPerformance快速的列印出來。

```swift
class AlbumGod {
    var name: String
    
    init(name: String) {
        self.name = name
    }
    
    func getPerformance() -> String {
        return "The album is \(name)"
    }
}

class StudioAlbumGod: AlbumGod {
    var studio: String
    
    init(name: String, studio: String) {
        self.studio = studio
        super.init(name: name)
    }
    
    override func getPerformance() -> String {
        return "The studio album is \(name)"
    }
}

class LiveAlbumGod: AlbumGod {
    var location: String
    
    init(name: String, location: String) {
        self.location = location
        super.init(name: name)
    }
    
    override func getPerformance() -> String {
        return "The live album is \(name)"
    }
}


var appleGod = StudioAlbumGod(name: "Apple", studio: "Pie")
var bananaGod = StudioAlbumGod(name: "Banana", studio: "ship")
var pearGod = LiveAlbumGod(name: "Pear", location: "taiwan")
var allAlbumGods: [AlbumGod] = [appleGod, bananaGod, pearGod]

for albumGod in allAlbumGods {
    print(albumGod.getPerformance())
}
```