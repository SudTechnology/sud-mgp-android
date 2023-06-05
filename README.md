## [不同版本SDK支持游戏及集成文档](https://docs.sud.tech/zh-CN/app/Client/StartUp.html)

## 怎么选择使用哪个版本SDK？
标准版本SDK支持更多游戏；Lite版本SDK只支持部分游戏. [详细支持游戏列表](https://docs.sud.tech/zh-CN/app/Client/StartUp.html)

## 安装方式：
### 1. 手动方式集成：
#### 下载 [sud-mgp-android](https://github.com/SudTechnology/sud-mgp-android/releases)
##### 标准版本SudMGP SDK: SudMGP-Android-v1.3.1.1127.zip
##### Lite版本SudMGP SDK: SudMGP-Android-v1.3.1.1127-lite.zip
##### 多语言语音识别扩展库(可选): SudASR-Android-v1.3.1.1127.zip

### 2. 通过Maven集成
#### 标准版本，依赖标准版本SudMGP SDK
```ruby
// 多语言语音识别扩展库(可选)
implementation 'tech.sud.mgp:SudASR:1.3.1.1127'
// 标准版本SudMGP SDK
implementation 'tech.sud.mgp:SudMGP:1.3.1.1127'

```
#### Lite版本，依赖Lite版SudMGP SDK
```ruby
// 多语言语音识别扩展库(可选)
implementation 'tech.sud.mgp:SudASR:1.3.1.1127'
// Lite版本SudMGP SDK
implementation 'tech.sud.mgp:SudMGP-lite:1.3.1.1127'

```

## 说明：  
1. 多语言语音识别扩展库，可识别英语、德语、阿拉伯语等等多语言，如需此功能，可选择集成此扩展库   
2. 如需上架Google Play，请联系Sud获取静态SDK（so库打在aar包里）
