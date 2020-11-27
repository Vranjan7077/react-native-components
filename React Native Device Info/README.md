React Native device info is an excellent open-source library to retrieve device information in a react native application.

This library has a long API that lets you retrieve application name, battery level, build number, device ID, device name etc.

Currently, the latest version of it is v7.0.2 and it owns 5k+ stars in [Github](https://github.com/react-native-device-info/react-native-device-info#usage)



## Installation

Using npm:

```shell
npm install --save react-native-device-info
```

or using yarn:

```shell
yarn add react-native-device-info
```

## How to use
To use the API, first, you need to import it like this.

```shell
import DeviceInfo from ‘react-native-device-info’;
import { getUniqueId, getManufacturer } from ‘react-native-device-info’;
```


## API

Note that many APIs are platform-specific. If there is no implementation for a platform, then the "default" return values you will receive are `"unknown"` for string, `-1` for number, and `false` for boolean. Arrays and Objects will be empty (`[]` and `{}` respectively).

Most APIs return a Promise but also have a corresponding API with `Sync` on the end that operates synchronously. For example, you may prefer to call `isCameraPresentSync()` during your app bootstrap to avoid async calls during the first parts of app startup.

| Method                                                            | Return Type         |  iOS | Android | Windows | Web |
| ----------------------------------------------------------------- | ------------------- | :--: | :-----: | :-----: | :-: |
| [getAndroidId()](#getandroidid)                                   | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getApiLevel()](#getapilevel)                                     | `Promise<number>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getApplicationName()](#getapplicationname)                       | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getAvailableLocationProviders()](#getAvailableLocationProviders) | `Promise<Object>`   |  ✅  |   ✅    |   ❌    | ❌ |
| [getBaseOs()](#getbaseOs)                                         | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ✅ |
| [getBuildId()](#getbuildid)                                       | `Promise<string>`   |  ✅  |   ✅    |   ❌    | ❌ |
| [getBatteryLevel()](#getbatterylevel)                             | `Promise<number>`   |  ✅  |   ✅    |   ✅    | ✅ |
| [getBootloader()](#getbootloader)                                 | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getBrand()](#getbrand)                                           | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getBuildNumber()](#getbuildnumber)                               | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getBundleId()](#getbundleid)                                     | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [isCameraPresent()](#iscamerapresent)                             | `Promise<boolean>`  |  ❌  |   ✅    |   ✅    | ✅ |


---

## Let’s see how to use a few methods of this library

#### getAndroidId()

Gets the ANDROID_ID. See [API documentation](https://developer.android.com/reference/android/provider/Settings.Secure#ANDROID_ID) for appropriate use.

#### Examples

```js
DeviceInfo.getAndroidId().then(androidId => {
  // androidId here
});
```
---
### getBatteryLevel()

Gets the battery level of the device as a float comprised between 0 and 1.

#### Examples

```js
DeviceInfo.getBatteryLevel().then(batteryLevel => {
  // 0.759999
});
```

### isCameraPresent()

Tells if the device have any camera now.

#### Examples

```js
DeviceInfo.isCameraPresent()
  .then(isCameraPresent => {
    // true or false
  })
  .catch(cameraAccessException => {
    // is thrown if a camera device could not be queried or opened by the CameraManager on Android
  });
```


## Tips: 
Share your reusable components between projects using Bit [Github](https://github.com/teambit/bit)

Bit makes it simple to share, document, and reuse independent components between projects. Use it to maximize code reuse, keep a consistent design, collaborate as a team, speed delivery, and build apps that scale.

[Bit](https://bit.dev/) supports Node, React Native, React, Vue, Angular, and more.
![Bit](https://github.com/Vranjan7077/react-native-components/blob/main/React%20Native%20Device%20Info/gif.gif?raw=true)


