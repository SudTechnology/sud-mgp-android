[English](README_en.md)
## 怎么选择使用哪个版本SDK？
标准版本SDK支持全部游戏；Lite版本SDK只支持部分游戏. [详细支持游戏列表](https://docs.sud.tech/zh-CN/app/Client/StartUp.html)

## 安装方式：
### 1. 手动方式集成SudMGP SDK
#### 下载 [SudMGP](https://github.com/SudTechnology/sud-mgp-android/releases)
##### Lite版本SDK: SudMGP-Android-v1.4.9.1231-lite.zip
##### 标准版本SDK: SudMGP-Android-v1.4.9.1231.zip
##### 多语言语音识别扩展库(可选): SudASR-Android-v1.4.9.1231.zip
###### 手动集成详细步骤请看 [QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md)
### 2. 通过Maven集成SudMGP SDK
#### 依赖Lite版本SudMGP SDK
```ruby
// Lite版本SudMGP SDK
// 上架Google Play需要替换成此依赖：api 'tech.sud.mgp:SudMGP-lite-static:1.4.9.1231'
api 'tech.sud.mgp:SudMGP-lite:1.4.9.1231'

// 多语言语音识别扩展库(可选)
api 'tech.sud.mgp:SudASR:1.4.9.1231'
```

#### 依赖标准版本SudMGP SDK
```ruby
// 标准版本SudMGP SDK
// 上架Google Play需要替换成此依赖：api 'tech.sud.mgp:SudMGP-static:1.4.9.1231'
api 'tech.sud.mgp:SudMGP:1.4.9.1231'

// 多语言语音识别扩展库(可选)
api 'tech.sud.mgp:SudASR:1.4.9.1231'

```

## 说明：
1. 多语言语音识别扩展库，可识别英语、德语、阿拉伯语等等多语言，如需此功能，可选择集成此扩展库
2. 请通过SudMGPWrapper集成SDK, 见QuickStart

## 集成Demo
[QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md)
