## How to Choose Which Version of the SDK to Use?

The **Pro version SDK** supports all games;
The **Standard version SDK** only supports a subset of games.
[Detailed supported game list](https://docs.sud.tech/zh-CN/app/Client/StartUp.html)

## Installation Methods:

### 1. Manual Integration of the SudGIP SDK

#### Download from [SudGIP](https://github.com/SudTechnology/sud-mgp-android/releases)

* **Standard SDK version**: SudGIP-Android-v1.6.4.1266-beta.zip
* **Pro SDK version**: SudGIP-Android-v1.6.4.1266-beta-pro.zip
* **Multilingual Speech Recognition Extension Library (optional)**: SudASR-Android-v1.6.4.1266-beta.zip

Unzip the downloaded zip file, extract the `.aar` files, copy them into your project, and add them as dependencies.

### 2. Integration via Maven

#### Depend on the Standard SudGIP SDK

```ruby
// Standard SudGIP SDK
// Use this dependency when publishing to Google Play:
api 'tech.sud.gip:SudGIP-static:1.6.4.1266-beta'

api 'tech.sud.gip:SudGIP:1.6.4.1266-beta'

// Multilingual Speech Recognition Extension Library (optional)
api 'tech.sud.gip:SudASR:1.6.4.1266-beta'
```

#### Depend on the Pro SudGIP SDK

```ruby
// Pro SudGIP SDK
// Use this dependency when publishing to Google Play:
api 'tech.sud.gip:SudGIP-pro-static:1.6.4.1266-beta'

api 'tech.sud.gip:SudGIP-pro:1.6.4.1266-beta'

// Multilingual Speech Recognition Extension Library (optional)
api 'tech.sud.gip:SudASR:1.6.4.1266-beta'
```

## Notes:

1. The multilingual speech recognition extension library supports recognition in English, German, Arabic, and other languages. If you need this feature, you can integrate this extension library.
2. Please integrate the SDK through `SudGIPWrapper`. See QuickStart for details.

## Integration Demo

[QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md)

---

Let me know if you need this translated into Markdown or a different format.
