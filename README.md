# Expo Linking.getInitialURL() returns null on Android

This repository demonstrates a bug where `Linking.getInitialURL()` in Expo's `Linking` API inconsistently returns `null` on Android devices even when a deep link is used to launch the application.  This can lead to unexpected application behavior, particularly if the initial URL is crucial for setting up the application state.

## Problem Description

The core issue is that `Linking.getInitialURL()` doesn't reliably return the initial URL when opening the app via a deep link on Android.  In some cases, it returns `null`, making it impossible to handle the deep link as intended.  This is not consistent and seems to be dependent on various factors such as the device, Android version, or even the background processes.