# @threls/expo-pusher-beams

This is an attempt of updating @threls/expo-pusher-beams / Pusher Beams client implementation for Expo.
This is not an official library and this is deprecated / not maintained.

# Deprecated
I forked this library to upgrade the Gradle version from 7.6.4 to 8.6 and be able to run it on a Java 17 environment. 
You have to install this library using `npx expo install @jonathancaspar/JonathanCaspar/expo-pusher-beams`, add this plugin in your `app.json` file, reinstall the native dependencies (using `npx expo prebuild --clean`) then create the android build (using `npx expo run:android`).

I managed to make it work using Java 17 and Gradle 8.6, however I gave up on it for several reasons:
- nobody is actively maintaining this library
- this library has a really poor API / documentation and is lacking core functionalities that the native Pusher Beams library offer (such as background message handling)
- this library is not up-to-date

In the end, I opted for directly using Firebase Messaging instead of Pusher Beams.
It requires us to change our backend to use Firebase Messaging and on the frontend we are simply installing the Firebase React Native SDK. Doing this resolved all our problems and we now run on an up-to-date stack.