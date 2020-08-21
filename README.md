# rn-notifications
An example React native app to explore best practices for integrating remote notifications

Just building this with whatever's currently installed on my personal dev MacBook Pro running Mojave 10.14.6.

```
$ node --version
v13.10.1
$ yarn --version
1.22.4
$ pod --version
1.9.1
$ /Applications/Xcode.app/Contents/Developer/usr/bin/xcodebuild -version
Xcode 11.3.1
Build version 11C504
```

I'll get some Android info after I have iOS up and running.

## The Recipe
```
$ npx react-native init NotifyApp
$ cd NotifyApp
$ yarn add react-native-notifications
$ pod install --project-directory=ios/
```

Open `ios/NotifyApp.xcworkspace` in Xcode and do the following:

1. Change the bundle id to `com.heynow.NotifyApp` (was `org.reactjs.native.example.NotifyApp`)
2. Assign the team to 'Heynow Software'
3. Add the 'Push Notifications' Capability and the 'Background Modes' Cabality with the 'Remote notifications' checked
