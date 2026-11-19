# Plainshot

Plainshot takes the hidden information out of your photos as you take them: where you were, the date and
time, which phone you have. Tap Shoot, use the phone's own camera, and each shot is cleaned a few seconds
after you take it. It has no adverts, no accounts, no paid version and no internet access.

- Website: https://customgpter.github.io/plainshot/
- Latest app file: https://github.com/CustomGPTer/plainshot/releases/latest
- Privacy: https://customgpter.github.io/plainshot/privacy.html

## What it does

- Opens the phone's full camera and cleans each shot about three seconds after it is saved
- Takes out location, date and time, phone model, camera settings, thumbnail, Samsung's extras and the
  motion clip; each has a switch to keep it. The picture itself is copied byte for byte, never re-made
- Moves the clean copy to DCIM/Plainshot under a neutral name and deletes the original
- A gallery of every photo on the phone with a "Safe" pill on the ones that hold nothing beyond what the
  settings allow, decided by reading each file
- "Make safe" for photos already on the phone, "Share safe" in the share menu, "Always on" for every photo
- JPEG, HEIC, PNG and WebP photos; MP4 and MOV videos
- No internet permission

## Building

The app is in the `android` folder. It needs JDK 17 or newer and the Android SDK (platform 36).

    cd android
    ./gradlew testReleaseUnitTest assembleDebug

A release build needs your own signing key: make a `keys` folder beside `android/build.gradle.kts` holding
your keystore and a `signing.properties` file with `storeFile`, `storePassword`, `keyAlias` and `keyPassword`.

## Licence

© 2026 Jonathan Jackson. All rights reserved. The app's source code is not published; this repository holds the website and the app releases.
