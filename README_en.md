## How do I choose which version of the SDK to use? 
The standard version of the SDK supports all games, while the Lite version of the SDK only supports some games. For a detailed list of supported games, please refer to the [Supported Games List](https://docs.sud.tech/zh-CN/app/Client/StartUp.html). 
 
## Installation Methods: 
### 1. Manual Integration of SudMGP SDK 
#### Download [SudMGP](https://github.com/SudTechnology/sud-mgp-android/releases) 
##### Lite Version SDK: SudMGP-Android-v1.5.4.1247-lite.zip 
##### Standard Version SDK: SudMGP-Android-v1.5.4.1247.zip 
##### Multilingual Speech Recognition Extension Library (Optional): SudMGP-Android-v1.5.4.1247.zip 
###### For detailed steps on manual integration, please refer to the [QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md). 
### 2. Integration of SudMGP SDK via Maven 
#### Dependency on the Lite Version of SudMGP SDK
```ruby
// Lite Version SudMGP SDK
// To publish on Google Play, you need to replace it with this dependency：api 'tech.sud.mgp:SudMGP-lite-static:1.5.4.1247'
api 'tech.sud.mgp:SudMGP-lite:1.5.4.1247'

// Multilingual Speech Recognition Extension Library (Optional)
api 'tech.sud.mgp:SudASR:1.5.4.1247'
```

#### Dependency on the Standard Version of SudMGP SDK
```ruby
// Standard Version SudMGP SDK
// To publish on Google Play, you need to replace it with this dependency：api 'tech.sud.mgp:SudMGP-static:1.5.4.1247'
api 'tech.sud.mgp:SudMGP:1.5.4.1247'

// Multilingual Speech Recognition Extension Library (Optional)
api 'tech.sud.mgp:SudASR:1.5.4.1247'
```

## Notes:   
1. The Multilingual Speech Recognition Extension Library can recognize multiple languages such as English, German, and Arabic. If you need this feature, you can choose to integrate this extension library.   
2. Please use SudMGPWrapper to integrate the SDK, see QuickStart. 
 
## Integration Demo 
[QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md)
