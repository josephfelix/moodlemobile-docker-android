# Moodle Mobile Android

```
## Extra helper command
If you want to run or build the ionic project in computer but doesn't have Android Studio, Android SDK or Ionic Framework and this computer installed Docker. You can use helper command  

- Restore npm package
```
docker run --rm -v $(pwd):/ionicapp josephfelix/moodlemobile-android npm install
```
- Preview Ionic web app in your web browser
```
docker run --rm -v $(pwd):/ionicapp -p 8100:8100 josephfelix/moodlemobile-android ionic serve
```
- Build android apk output file
```
docker run --rm -v $(pwd):/ionicapp josephfelix/moodlemobile-android ionic cordova build android
```

## ADB Support
You can use adb (Android debug bridge) in this docker image follow this command.
```
docker run --privileged -v /dev/bus/usb:/dev/bus/usb -P -v $(pwd):/ionicapp josephfelix/moodlemobile-android /opt/android-sdk/platform-tools/adb devices
```
