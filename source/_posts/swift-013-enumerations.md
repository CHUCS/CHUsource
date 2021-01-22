---
title: Swift 013 Enumerations
keywords: swift 013 enumerations
date: 2021-01-22 13:30:56
categories: Swift tutorials
tags:
    - swift
---
# Enum
在使用一些函式的時候，我們有時會會不小心給錯輸入的值而產生粗心的錯誤，有可能大小寫不對、全形半形導致錯誤找了很久才找到，為了避免這個錯誤我們可以使用`enum`先定義好這個輸入的型態，如果在這個型態之外我們就會產生警告，以下是還未使用`enum`時的寫法。
<!-- more -->
```swift
func getStatusNoEnum(weather: String) -> String? {
    if weather == "sunny" {
        return "Good"
    }else {
        return nil
    }
}
```
使用`enum`後將可以完全的避免掉粗心的錯誤。

```swift
func getStatus(weather: WeatherType) -> String? {
    if weather == WeatherType.sun {
        return "Good"
    }else {
        return nil
    }
}

getHaterStatus(weather: WeatherType.cloud)
```


你還可以將輸入化簡，讓程式碼簡潔乾淨。


```swift
func getStatusSwitch(weather: WeatherType) -> String? {
    switch weather {
    case .sun:
        return "Sun!"
    case .cloud:
        return "Cloud"
    default:
        return nil
    }
}

getStatusSwitch(weather: .cloud)
```

當然如果你有需要你可以在enum中定義參數的型態，在調用時將會出現你所定義的變數名稱，。
```swift
enum speedType {
    case one
    case two
    case three(speed: Int)
}

func getStatusSpeed(speed: speedType) -> String? {
    switch speed {
    case .one:
        return "one!"
    case .two:
        return "two!"
    case .three(let speed) where speed > 10:
        return "three > 10"
    case .three(let speed) where speed < 10:
        return "three < 10"
    default:
        return nil
    }
}


getStatusSpeed(speed: .three(speed: 11))
```