# More on React Native

1.**What does React Native do when it builds your application?**
Assuming we have Node.js and Watchman installed, when it builds our application, it will provide us with us with the Starter React native app is in `index.ios.js` for iOS and also `index.android.js` for Android.in React Native, there is no DOM rather, there are Native Components which are provided by platforms such as iOS and Android.  

2.**Can you simply deploy a react web app to the phone?**
No, we are not able to simply deploy a web-app to a phone. Phones have a web browser for web apps, or apps that are standalone. We can't install a web page.


**New Vocabulary to Learn**

1. **Eject:**
Ejecting lets us turn an Expo project into a pure React Native app, just as if it had been created with the react-native init command. [levelup.gitconnected.com](https://levelup.gitconnected.com/expo-vs-react-native-cli-a-guide-to-bootstrapping-new-react-native-apps-6f0fcafee58f) says, "When a project is ejected, all of the Native code is unpacked into ios and android folders, and the App.js file is split into App.js and index.js, exposing the code that mounts the root React Native component." Basically, if we are building a project using Expo and then later find out that some dependencies don't work with Expo, we can eject and then use ExpoKit to have all of the Expo dependencies still work.

1. **Android avd:** This is an Android Virtual Device (AVD) and it is a configuration that defines the characteristics of an Android phone, tablet, or other Android devices that you want to simulate in the Android Emulator.
2. **Expo:** 
Expo CLI is one of the fastest ways to get started using React Native. Expo is a set of tools built around React Native and helps us to start writing a React Native app quickly. We only need a recent version of Node.js and a phone or emulator. 