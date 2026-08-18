[English](README_en.md)
## 怎么选择使用哪个版本SDK？
pro版本SDK支持全部游戏；标准版本SDK只支持部分游戏. [详细支持游戏列表](https://docs.sud.tech/zh-CN/app/Client/StartUp.html)

---

## 安装方式：
### 1. 手动方式集成SudGIP SDK
#### 下载 [SudGIP](https://github.com/SudTechnology/sud-mgp-android/releases)
##### 标准版本SDK: SudGIP-Android-v1.6.8.1299.zip
##### pro版本SDK: SudGIP-Android-v1.6.8.1299-pro.zip
##### 多语言语音识别扩展库(可选): SudASR-Android-v1.6.8.1299.zip
##### 解压zip包拿到解压后的aar包，将aar包拷贝到项目中，并且在项目中依赖该aar包

### 2. 通过Maven集成SudGIP SDK
#### 依赖标准版本SudGIP SDK
```ruby
// 标准版本SudGIP SDK
// 上架Google Play需要替换成此依赖：api 'tech.sud.gip:SudGIP-static:1.6.8.1299'
api 'tech.sud.gip:SudGIP:1.6.8.1299'
```

#### 依赖pro版本SudGIP SDK
```ruby
// pro版本SudGIP SDK
// 上架Google Play需要替换成此依赖：api 'tech.sud.gip:SudGIP-pro-static:1.6.8.1299'
api 'tech.sud.gip:SudGIP-pro:1.6.8.1299'
```

### 依赖SudASR SDK（可选）
```ruby
// 多语言语音识别扩展库，可识别英语、德语、阿拉伯语等等多语言，如需此功能，可选择集成此扩展库
api 'tech.sud.gip:SudASR:1.6.8.1299'
```

---

## 包体增量说明

> [!NOTE]
> 以下体积数据均为近似值，用于依赖选型和 APK 包体评估。

- 实际 APK 体积增量会受到构建配置、代码混淆、资源压缩、So 压缩方式、ABI 配置以及 APK/AAB 打包方式等因素影响。
- 下表中的“近似总体积/增量”指包含全部 ABI 架构时的估算值，不代表单一 ABI APK 的最终体积。
- 若 APK 仅保留单一 ABI，通常仅会包含对应架构的 So 文件，实际包体增量会相应减少。
- 若 APK 同时包含多个 ABI，各架构的 So 文件会同时打入 APK，相关体积将累计。
- 以下依赖名称未携带具体版本号，实际接入时请使用对应版本号。

### 产物体积概览

| 依赖产物 | 是否包含 So | 近似总体积 / 增量 | 说明 |
| --- | :---: | ---: | --- |
| `tech.sud.gip:SudGIP` | 否 | 小于 **1 MB** | 推荐使用，APK 包体增量较小 |
| `tech.sud.gip:SudGIP-static` | 是 | 约 **28.9 MB** | 包含四种 ABI 架构的 So 文件 |
| `tech.sud.gip:SudGIP-pro` | 否 | 约 **7.3 MB** | Pro 版动态库产物，不包含 So 文件 |
| `tech.sud.gip:SudGIP-pro-static` | 是 | 约 **133.3 MB** | 包含四种 ABI 架构的 So 文件 |
| `tech.sud.gip:SudASR` | 是 | 约 **12.5 MB** | 多语言语音识别扩展库，包含四种 ABI 架构的 So 文件 |

### 各 ABI So 体积参考

| 依赖产物 | x86 | x86_64 | arm64-v8a | armeabi-v7a |
| --- | ---: | ---: | ---: | ---: |
| `SudGIP-static` | 约 7.4 MB | 约 7.4 MB | 约 7.1 MB | 约 6.1 MB |
| `SudGIP-pro-static` | 约 34.7 MB | 约 33.3 MB | 约 31.5 MB | 约 29.4 MB |
| `SudASR` | 约 215 KB | 约 4.3 MB | 约 4.2 MB | 约 3.5 MB |

---

## 系统版本要求

不同 SDK 产物对 Android 系统最低版本要求不同，请在项目中配置对应的 `minSdk`。

| 依赖产物 | 最低 Android 版本 |
| --- | ---: |
| `tech.sud.gip:SudGIP` | Android 5.0 (API 21) |
| `tech.sud.gip:SudGIP-static` | Android 5.0 (API 21) |
| `tech.sud.gip:SudGIP-pro` | Android 5.1 (API 22) |
| `tech.sud.gip:SudGIP-pro-static` | Android 5.1 (API 22) |
| `tech.sud.gip:SudASR` | Android 5.0 (API 21) |

## 集成Demo

[QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md)
