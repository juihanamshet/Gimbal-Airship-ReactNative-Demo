# React Native Gimbal Demo

## Getting Started
In https://manager.gimbal.com/apps create two Gimbal Applications, one each for Android and iOS.
For Android, enter `com.rngimbaldemo` as the package ID; for iOS, enter `org.reactjs.native.example.RNGimbalDemo` as the bundle ID.
Note the respective API keys for Android and iOS; they will be used in the sections below.

Clone the React Native Gimbal SDK library: `github.com/PaeDae/react-native-gimbal-sdk`.

Then, install the SDK from the demo app folder, as well as React Native Permissions:
* `yarn add ../react-native-gimbal-sdk` <path to the cloned `react-native-gimbal-sdk`>
* `yarn add react-native-permissions`

### Android:
Set your Android API Key in `MainApplication.java`:
* `private static final String GIMBAL_APP_API_KEY = "YOUR GIMBAL API KEY FOR ANDROID";`

### iOS:
Set your iOS API Key `AppDelegate.m`:
* In the method `didFinishLaunchingWithOptions`:  
        `[Gimbal setAPIKey:@"YOUR GIMBAL API KEY FOR iOS" options:nil];`  
  
If using React Native v0.60+, please also run the following from a terminal:  
`cd ios && pod install && cd ..`  

## Running the App and Starting the SDK:
* For Android, run `yarn react-native run-android` or `npx react-native run-android`
* For iOS run `yarn react-native run-ios` or `npx react-native run-ios`
* While the app is running, press the `Start` button in the `RNGimbal Demo` section of the interface.