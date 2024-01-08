## How do I choose which version of the SDK to use? 
The standard version of the SDK supports all games, while the Lite version of the SDK only supports some games. For a detailed list of supported games, please refer to the [Supported Games List](https://docs.sud.tech/zh-CN/app/Client/StartUp.html). 
 
## Installation Methods: 
### 1. Manual Integration of SudMGP SDK 
#### Download [SudMGP](https://github.com/SudTechnology/sud-mgp-android/releases) 
##### Standard Version SDK: SudMGP-Android-v1.3.6.1181.zip 
##### Lite Version SDK: SudMGP-Android-v1.3.6.1181-lite.zip 
##### Multilingual Speech Recognition Extension Library (Optional): SudMGP-Android-v1.3.6.1181.zip 
###### For detailed steps on manual integration, please refer to the [QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md). 
### 2. Integration of SudMGP SDK via Maven 
#### Dependency on the Standard Version of SudMGP SDK
```ruby
// Standard Version SudMGP SDK
implementation 'tech.sud.mgp:SudMGP:1.3.6.1181'

// Multilingual Speech Recognition Extension Library (Optional)
implementation 'tech.sud.mgp:SudASR:1.3.6.1181'
```
#### Dependency on the Lite Version of SudMGP SDK
```ruby
// Lite Version SudMGP SDK
implementation 'tech.sud.mgp:SudMGP-lite:1.3.6.1181'

// Multilingual Speech Recognition Extension Library (Optional)
implementation 'tech.sud.mgp:SudASR:1.3.6.1181'
```
## Notes:   
1. The Multilingual Speech Recognition Extension Library can recognize multiple languages such as English, German, and Arabic. If you need this feature, you can choose to integrate this extension library.    
2. If you need to publish on Google Play, please contact Sud to obtain the static SDK (the so library is packed in the aar package).    
3. Please use SudMGPWrapper to integrate the SDK, see QuickStart. 
 
## Integration Demo 
[QuickStart](https://github.com/SudTechnology/hello-sud-plus-android/blob/master/project/QuickStart/README.md)
