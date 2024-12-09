# React Native Dimensions Inaccuracy After Keyboard Hide on Android

This repository demonstrates a bug in React Native where `Dimensions.get('window').height` returns an incorrect value on Android after the keyboard is shown and then hidden.  The height often remains smaller than the actual screen height.

## Bug Description

The `Dimensions` API in React Native is used to get the screen dimensions. However, on Android, after the keyboard is dismissed, the height returned by `Dimensions.get('window').height` may not reflect the correct screen height.  This leads to layout issues and incorrect calculations.

## How to Reproduce

1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Observe the console output after the keyboard is shown and then hidden.  The reported height will likely be incorrect.

## Solution

The provided solution uses `onLayout` to correctly determine height after keyboard is dismissed.

## Technology Used

* React Native