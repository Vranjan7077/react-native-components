React Native Permission library lets you make these requests in an easy, fast, and reliable way. This library consists of a unified permissions package and an API for React Native on iOS and Android, which makes the coding part shorter.

React Native Permissions is also an open-source library with over 2k stars on [GitHub](https://github.com/zoontek/react-native-permissions).

## Installation

Using npm:

```shell
npm install — save react-native-permissions
```

or using yarn:

```shell
yarn add react-native-permissions
```

# Commonly used permissions from this library.

```shell
PERMISSIONS.ANDROID.CALL_PHONE;
```
```shell
PERMISSIONS.ANDROID.CAMERA;
```
```shell
PERMISSIONS.ANDROID.READ_CALL_LOG;
```
```shell
PERMISSIONS.ANDROID.READ_SMS;
```
```shell
PERMISSIONS.ANDROID.READ_CONTACTS;
```

### These permission requests can have one of the following outcomes.
```shell
RESULTS.UNAVAILABLE
```
```shell
RESULTS.DENIED
```
```shell
RESULTS.GRANTED
```
```shell
RESULTS.BLOCKED
```

#### let’s see how to check and continue with the permission requests.
```shell
import {check, PERMISSIONS, RESULTS} from 'react-native-permissions';
 
check(PERMISSIONS.IOS.CAMERA)
  .then((result) => {
    switch (result) {
      case RESULTS.UNAVAILABLE:
        console.log(
          'feature is not available',
        );
        break;
      case RESULTS.DENIED:
        console.log('permission has not been requested / is denied but requestable',);
        break;
      case RESULTS.GRANTED:
        console.log('The permission is granted');
        break;
      case RESULTS.BLOCKED:
        console.log('The permission is denied and not requestable anymore');
        break;
    }
  })
  .catch((error) => {
    // …
  });
```
![Permissions](https://github.com/Vranjan7077/react-native-components/blob/main/React%20Native%20Permissions/img1.png?raw=true)
