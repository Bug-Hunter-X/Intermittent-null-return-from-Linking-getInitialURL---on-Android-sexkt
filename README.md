# Expo Linking.getInitialURL() - Intermittent null return on Android

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API where it intermittently returns `null` on Android devices, even when a deep link has been successfully opened.  This can lead to unexpected application behavior and data loss.

## Reproduction

1. Clone this repository.
2. Run the app on an Android emulator or device.
3. Open a deep link targeting the app.  (Instructions for setting this up in the respective files)
4. Observe that `getInitialURL` sometimes returns null despite the link being successfully opened.

## Solution

The provided solution uses a combination of techniques to mitigate this issue. It involves a retry mechanism and error handling to improve the reliability of retrieving the initial URL.