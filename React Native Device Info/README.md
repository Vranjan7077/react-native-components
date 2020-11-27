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
| [getCarrier()](#getcarrier)                                       | `Promise<string>`   |  ✅  |   ✅    |   ❌    | ❌ |
| [getCodename()](#getcodename)                                     | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getDevice()](#getdevice)                                         | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getDeviceId()](#getdeviceid)                                     | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getDeviceType()](#getDeviceType)                                 | `string`            |  ✅  |   ✅    |   ❌    | ❌ |
| [getDisplay()](#getdisplay)                                       | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getDeviceName()](#getdevicename)                                 | `Promise<string>`   |  ✅  |   ✅    |   ✅    | ❌ |
| [getDeviceToken()](#getdevicetoken)                               | `Promise<string>`   |  ✅  |   ❌    |   ❌    | ❌ |
| [getFirstInstallTime()](#getfirstinstalltime)                     | `Promise<number>`   |  ❌  |   ✅    |   ✅    | ❌ |
| [getFingerprint()](#getfingerprint)                               | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getFontScale()](#getfontscale)                                   | `Promise<number>`   |  ✅  |   ✅    |   ❌    | ❌ |
| [getFreeDiskStorage()](#getfreediskstorage)                       | `Promise<number>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getFreeDiskStorageOld()](#getfreediskstorageold)                 | `Promise<number>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getHardware()](#gethardware)                                     | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getHost()](#gethost)                                             | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getIpAddress()](#getipaddress)                                   | `Promise<string>`   |  ✅  |   ✅    |   ✅    | ❌ |
| [getIncremental()](#getincremental)                               | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getInstallerPackageName()](#getinstallerpackagename)             | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getInstallReferrer()](#getinstallreferrer)                       | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ✅ |
| [getInstanceId()](#getinstanceid)                                 | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getLastUpdateTime()](#getlastupdatetime)                         | `Promise<number>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getMacAddress()](#getmacaddress)                                 | `Promise<string>`   |  ✅  |   ✅    |   ❌    | ❌ |
| [getManufacturer()](#getmanufacturer)                             | `Promise<string>`   |  ✅  |   ✅    |   ✅    | ❌ |
| [getMaxMemory()](#getmaxmemory)                                   | `Promise<number>`   |  ❌  |   ✅    |   ✅    | ✅ |
| [getModel()](#getmodel)                                           | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getPhoneNumber()](#getphonenumber)                               | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getPowerState()](#getpowerstate)                                 | `Promise<object>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getProduct()](#getproduct)                                       | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getPreviewSdkInt()](#getPreviewSdkInt)                           | `Promise<number>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getReadableVersion()](#getreadableversion)                       | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getSerialNumber()](#getserialnumber)                             | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getSecurityPatch()](#getsecuritypatch)                           | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getSystemAvailableFeatures()](#getSystemAvailableFeatures)       | `Promise<string[]>` |  ❌  |   ✅    |   ❌    | ❌ |
| [getSystemName()](#getsystemname)                                 | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getSystemVersion()](#getsystemversion)                           | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getTags()](#gettags)                                             | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getType()](#gettype)                                             | `Promise<string>`   |  ❌  |   ✅    |   ❌    | ❌ |
| [getTotalDiskCapacity()](#gettotaldiskcapacity)                   | `Promise<number>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getTotalDiskCapacityOld()](#gettotaldiskcapacityold)             | `Promise<number>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getTotalMemory()](#gettotalmemory)                               | `Promise<number>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getUniqueId()](#getuniqueid)                                     | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [getUsedMemory()](#getusedmemory)                                 | `Promise<number>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getUserAgent()](#getuseragent)                                   | `Promise<string>`   |  ✅  |   ✅    |   ❌    | ✅ |
| [getVersion()](#getversion)                                       | `string`            |  ✅  |   ✅    |   ✅    | ❌ |
| [hasGms()](#hasGms)                                               | `boolean`           |  ❌  |   ✅    |   ❌    | ❌ |
| [hasHms()](#hasHms)                                               | `boolean`           |  ❌  |   ✅    |   ❌    | ❌ |
| [hasNotch()](#hasNotch)                                           | `boolean`           |  ✅  |   ✅    |   ✅    | ❌ |
| [hasSystemFeature()](#hassystemfeaturefeature)                    | `Promise<boolean>`  |  ❌  |   ✅    |   ❌    | ❌ |
| [isAirplaneMode()](#isairplanemode)                               | `Promise<boolean>`  |  ❌  |   ✅    |   ❌    | ✅ |
| [isBatteryCharging()](#isbatterycharging)                         | `Promise<boolean>`  |  ✅  |   ✅    |   ❌    | ✅ |
| [isEmulator()](#isemulator)                                       | `Promise<boolean>`  |  ✅  |   ✅    |   ✅    | ❌ |
| [isLandscape()](#isLandscape)                                     | `Promise<boolean>`  |  ✅  |   ✅    |   ✅    | ❌ |
| [isLocationEnabled()](#isLocationEnabled)                         | `Promise<boolean>`  |  ✅  |   ✅    |   ❌    | ✅ |
| [isHeadphonesConnected()](#isHeadphonesConnected)                 | `Promise<boolean>`  |  ✅  |   ✅    |   ❌    | ❌ |
| [isPinOrFingerprintSet()](#ispinorfingerprintset)                 | `Promise<boolean>`  |  ✅  |   ✅    |   ✅    | ❌ |
| [isTablet()](#istablet)                                           | `boolean`           |  ✅  |   ✅    |   ✅    | ❌ |
| [supported32BitAbis()](#supported32BitAbis)                       | `Promise<string[]>` |  ❌  |   ✅    |   ❌    | ❌ |
| [supported64BitAbis()](#supported64BitAbis)                       | `Promise<string[]>` |  ❌  |   ✅    |   ❌    | ❌ |
| [supportedAbis()](#supportedAbis)                                 | `Promise<string[]>` |  ✅  |   ✅    |   ❌    | ❌ |
| [syncUniqueId()](#syncuniqueid)                                   | `Promise<string>`   |  ✅  |   ❌    |   ❌    | ❌ |

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
Share your reusable components between projects using Bit [Github]https://github.com/teambit/bit)

Bit makes it simple to share, document, and reuse independent components between projects. Use it to maximize code reuse, keep a consistent design, collaborate as a team, speed delivery, and build apps that scale.

Bit supports Node, React Native, React, Vue, Angular, and more.

