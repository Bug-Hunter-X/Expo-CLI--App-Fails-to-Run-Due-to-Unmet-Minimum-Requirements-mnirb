# Expo CLI: App Fails to Run Due to Unmet Minimum Requirements

This repository demonstrates a common, yet often difficult-to-diagnose, error in Expo CLI projects. The app fails to run on devices or simulators due to unmet minimum requirements specified in `app.json` or `expo.json`. The error is usually not explicitly stated, manifesting as a blank screen or immediate crash.

## Problem

The core issue lies in discrepancies between your app's capabilities and the target device's capabilities. If your app requires features or system versions not present on the chosen device or simulator, it will fail to launch.

## Solution

The solution involves carefully reviewing the `app.json` or `expo.json` file's `expo.ios.supportsTablet`, `expo.android.minSdkVersion`, `expo.android.versionCode`, and `expo.web.config` sections to make sure that they are correctly aligned with the capabilities of the actual devices you intend to test with.  Ensure compatibility across platforms and adjust minimum requirements as needed. You can also update your device's software or choose a more compatible device.