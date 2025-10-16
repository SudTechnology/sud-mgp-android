[English](README_en.md)
## 怎么选择使用哪个版本SDK？
pro版本SDK支持全部游戏；标准版本SDK只支持部分游戏. [详细支持游戏列表](https://docs.sud.tech/zh-CN/app/Client/StartUp.html)

## 安装方式：
### 1. 手动方式集成SudGIP SDK
#### 下载 [SudGIP](https://github.com/SudTechnology/sud-mgp-android/releases)
##### 标准版本SDK: SudGIP-Android-v1.6.5.1268.zip
##### pro版本SDK: SudGIP-Android-v1.6.5.1268-pro.zip
##### 多语言语音识别扩展库(可选): SudASR-Android-v1.6.5.1268.zip
##### 解压zip包拿到解压后的aar包，将aar包拷贝到项目中，并且在项目中依赖该aar包

### 2. 通过Maven集成SudGIP SDK
#### 依赖标准版本SudGIP SDK
```ruby
// 标准版本SudGIP SDK
// 上架Google Play需要替换成此依赖：api 'tech.sud.gip:SudGIP-static:1.6.5.1268'
api 'tech.sud.gip:SudGIP:1.6.5.1268'

// 多语言语音识别扩展库(可选)
api 'tech.sud.gip:SudASR:1.6.5.1268'
```

#### 依赖pro版本SudGIP SDK
```ruby
// pro版本SudGIP SDK
// 上架Google Play需要替换成此依赖：api 'tech.sud.gip:SudGIP-pro-static:1.6.5.1268'
api 'tech.sud.gip:SudGIP-pro:1.6.5.1268'

// 多语言语音识别扩展库(可选)
api 'tech.sud.gip:SudASR:1.6.5.1268'

```

## 说明：
1. 多语言语音识别扩展库，可识别英语、德语、阿拉伯语等等多语言，如需此功能，可选择集成此扩展库
2. 请通过SudGIPWrapper集成SDK, 见QuickStart

## 集成Demo
[QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md)
