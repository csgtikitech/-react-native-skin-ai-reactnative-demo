# Install

```
yarn add react-native-skin-ai

# RN >= 0.60
cd ios && pod install

```

⚠️ You need install dependencies
```
    "react-native-camera": "3.15.1",
    "react-native-device-info": "^6.0.2",
    "react-native-image-picker": "2.0.0",
    "react-native-image-resizer": "1.1.0",
    "react-native-linear-gradient": "^2.5.6",
    "react-native-permissions": "2.0.9",
    "rn-fetch-blob": "^0.12.0"

```

## Post-install Steps

### iOS

For iOS 10+:

Add the `NSCameraUsageDescription`, `NSPhotoLibraryUsageDescription`, `NSCameraUsageDescription`, `NSPhotoLibraryAddUsageDescription` and `NSMicrophoneUsageDescription` (if allowing video) keys to your `Info.plist` with strings describing why your app needs these permissions.

**Note: You will get a SIGABRT crash if you don't complete this step**

```xml
<plist version="1.0">
  <dict>
    ...
  	<key>NSCameraUsageDescription</key>
    <string>Your own description of the purpose</string>
    <key>NSPhotoLibraryUsageDescription</key>
    <string>$(PRODUCT_NAME) would like access to your photo gallery</string>
    <key>NSCameraUsageDescription</key>
    <string>$(PRODUCT_NAME) would like to use your camera</string>
    <key>NSPhotoLibraryAddUsageDescription</key>
    <string>$(PRODUCT_NAME) would like to save photos to your photo gallery</string>
    <key>NSMicrophoneUsageDescription</key>
    <string>$(PRODUCT_NAME) would like to use your microphone (for videos)</string>
  </dict>
</plist>
```

⚠️ If you are planning on submitting your application to app store:

To be compliant with Guideline 5.1.1 - Legal - Privacy - Data Collection and Storage, the permission request alert should specify how your app will use this feature to help users understand why your app is requesting access to their personal data.

```
$(PRODUCT_NAME) would like access to your photo gallery to change your profile picture
```


### Android

Add the required permissions in `AndroidManifest.xml`:

```xml
 	<uses-permission android:name="android.permission.CAMERA" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.DOWNLOAD_WITHOUT_NOTIFICATION" />
```

### Android (Optional)

In folder android/app/build.gradle : add three line
```
 defaultConfig {
        .....
        missingDimensionStrategy 'react-native-camera', 'general'
        renderscriptSupportModeEnabled true
        multiDexEnabled true
        ......
    }
```

7. Refer to [Post-install Steps](Install.md#post-install-steps).
