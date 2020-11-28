Using this library, developers can update the device UI after an outgoing call that has started while integrating other device hardware like speakers. React-Native-callkeep is also an open-source library on [Github](https://github.com/react-native-webrtc/react-native-callkeep#troubleshooting)


The react-native-callkeep is a well-known library among native developers that allows handling essential actions that are relevant to phone calls in cross-platform mobile applications. 

This library contains the iOS CallKit framework and Android ConnectionService for coordinating the calling services with the system and other apps. 

These calling services are integrated into the built-in phone app for calling. 

Followings are some interesting services that you can have in a lot more easy way than using other libraries.

```shell
1. Receiving incoming calls
2. Making outgoing calls (VoIP or otherwise)
3. Call blocking and identification
4. Mark calls as active or not
5. End and Reject calls
6. Mute and hold calls
```

## Installation

Using npm:

```shell
npm i react-native-callkeep
```

### Some of the methods available in this library like:

```shell
1. setAvailable — the device is ready to make outgoing calls. It’s available only on Android.
2. setCurrentCallActive — Mark the current call as active. for example when call is answered.
3. displayIncomingCall — Display Incoming calls
4. answerIncomingCall — tell the sdk if a user has answered the call
5. endcall — it’s called if the user has ended the call
6. rejectCall — it’s called when a call is rejected
```
