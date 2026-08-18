## How to Choose an SDK Version?

The **Pro SDK** supports all games, while the **Standard SDK** supports only selected games.

For the full list of supported games, see [Supported Game List](https://docs.sud.tech/en-US/app/Client/StartUp.html).

---

## Installation

### 1. Integrate the SudGIP SDK Manually

#### Download [SudGIP](https://github.com/SudTechnology/sud-mgp-android/releases)

##### Standard SDK: `SudGIP-Android-v1.6.8.1299.zip`

##### Pro SDK: `SudGIP-Android-v1.6.8.1299-pro.zip`

##### Multilingual Speech Recognition Extension (Optional): `SudASR-Android-v1.6.8.1299.zip`

After downloading, unzip the package to obtain the `.aar` file. Copy the `.aar` file into your project and add it as a dependency.

### 2. Integrate the SudGIP SDK via Maven

#### Add the Standard SudGIP SDK Dependency

```gradle
// Standard SudGIP SDK
// For publishing to Google Play, replace this dependency with:
// api 'tech.sud.gip:SudGIP-static:1.6.8.1299'
api 'tech.sud.gip:SudGIP:1.6.8.1299'
```

#### Add the Pro SudGIP SDK Dependency

```gradle
// Pro SudGIP SDK
// For publishing to Google Play, replace this dependency with:
// api 'tech.sud.gip:SudGIP-pro-static:1.6.8.1299'
api 'tech.sud.gip:SudGIP-pro:1.6.8.1299'
```

#### Add the SudASR SDK Dependency (Optional)

```gradle
// Multilingual speech recognition extension.
// Supports English, German, Arabic, and other languages.
// Add this dependency only if multilingual speech recognition is required.
api 'tech.sud.gip:SudASR:1.6.8.1299'
```

---

## APK Size Impact

> [!NOTE]
> The size values below are approximate and are intended only for dependency selection and APK size estimation.

- Actual APK size changes may vary depending on build configuration, code shrinking, resource compression, native library compression, ABI configuration, and APK/AAB packaging settings.
- The “Approximate Total Size / Increase” column represents the estimated size when all ABI architectures are included. It does not represent the final size increase of a single-ABI APK.
- If your APK includes only one ABI, it usually contains only the corresponding native libraries, so the actual APK size increase will be smaller.
- If your APK includes multiple ABIs, the native libraries for all included architectures will be packaged into the APK, and their sizes will accumulate.
- The dependency names below do not include version numbers. Please use the appropriate version when integrating.

### Package Size Overview

| Dependency | Includes Native `.so` Files | Approximate Total Size / Increase | Description |
| --- | :---: | ---: | --- |
| `tech.sud.gip:SudGIP` | No | Less than **1 MB** | Recommended. Adds minimal APK size. |
| `tech.sud.gip:SudGIP-static` | Yes | About **28.9 MB** | Includes native `.so` files for four ABI architectures. |
| `tech.sud.gip:SudGIP-pro` | No | About **7.3 MB** | Pro dynamic-library artifact; does not include native `.so` files. |
| `tech.sud.gip:SudGIP-pro-static` | Yes | About **133.3 MB** | Includes native `.so` files for four ABI architectures. |
| `tech.sud.gip:SudASR` | Yes | About **12.5 MB** | Multilingual speech recognition extension, including native `.so` files for four ABI architectures. |

### Native Library Size by ABI

| Dependency | x86 | x86_64 | arm64-v8a | armeabi-v7a |
| --- | ---: | ---: | ---: | ---: |
| `SudGIP-static` | About 7.4 MB | About 7.4 MB | About 7.1 MB | About 6.1 MB |
| `SudGIP-pro-static` | About 34.7 MB | About 33.3 MB | About 31.5 MB | About 29.4 MB |
| `SudASR` | About 215 KB | About 4.3 MB | About 4.2 MB | About 3.5 MB |

---

## Android Version Requirements

Different SDK artifacts have different minimum Android version requirements. Configure the appropriate `minSdk` value in your project.

| Dependency | Minimum Android Version |
| --- | ---: |
| `tech.sud.gip:SudGIP` | Android 5.0 (API 21) |
| `tech.sud.gip:SudGIP-static` | Android 5.0 (API 21) |
| `tech.sud.gip:SudGIP-pro` | Android 5.1 (API 22) |
| `tech.sud.gip:SudGIP-pro-static` | Android 5.1 (API 22) |
| `tech.sud.gip:SudASR` | Android 5.0 (API 21) |

## Integration Demo

[QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README_en.md)
