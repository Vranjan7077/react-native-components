React-native-contacts might be the best library to access the device contact list when making React Native apps. It allows you to do many in-app operations regarding to contacts. 

Some of the actions you can perform with it are as follows:
```shell
1. Adding Contacts
2. Open Contact Form
3. Updating Contacts
4. Add numbers to an existing contact
5. Delete Contacts
```

This is a database intensive process, it may take a certain time period to complete the action, depending on the size of the contacts list and the performance of the device. 

Because of this, it is better to get all the contacts via the getAll method in the API before it is needed, and you can store the full list inside cache memories for future use.

React-Native-contacts is a 100% open-source library on [GitHub](https://github.com/morenoh149/react-native-contacts)


## Installation

Using npm:

```shell
npm install react-native-contacts — save
```

or using yarn:

```shell
yarn add react-native-contacts
```

### How to use

```shell
import { PermissionsAndroid } from 'react-native';
import Contacts from 'react-native-contacts';
 
PermissionsAndroid.request(
  PermissionsAndroid.PERMISSIONS.READ_CONTACTS,
  {
    'title': 'Contacts',
    'message': 'Let us us access your contacts',
    'buttonPositive': 'Please accept'
  }
)
.then(Contacts.getAll)
.then(contacts => {
  ...
})
```

