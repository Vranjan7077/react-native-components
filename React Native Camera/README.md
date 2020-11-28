This library is the most popular library for using the mobile device camera. One of the reasons for its popularity is its a very stable product with many features that’s very easy to use. this open-source library has over 8k stars on [GitHub](https://github.com/react-native-camera/react-native-camera)

One of the important native features of mobile development is using the device’s camera for taking a photo or video. 

When creating React Native apps, you can simply use the react-native camera library to access the functionality of using the device’s camera.

This library performs these actions by communicating with the device’s native operating system through some helper methods.

This library allows developers to store video recordings in the same directory where photos are saved.

You can also integrate Google’s camera view into your app directly using this react-native-camera library.

## Installation

Using npm:

```shell
npm i react-native-camera
```

## How to use

To access the camera, you need to write a code sample similar to the following.

```shell
class App extends Component {
  render() {
    return (
      <View style={styles.container}>
        <RNCamera
          style={{ flex: 1, alignItems: 'center' }}
          ref={ref => {
            this.camera = ref
          }}
        />
      </View>
    )
  }
}
 
const styles = StyleSheet.create({
  container: {
    flex: 1,
    flexDirection: 'column',
    backgroundColor: 'black'
  }
})
 
export default App;
```
![gif](https://github.com/Vranjan7077/react-native-components/blob/main/React%20Native%20Device%20Info/gif.gif?raw=true)