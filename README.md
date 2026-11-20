# Bravia Remote – Android app

## Easiest: build the APK online (no Android Studio)
1. Create a free GitHub repo and upload everything in this folder (keep the `.github` folder).
2. Open the repo's **Actions** tab, wait for "Build APK" to finish (~5 min).
3. Open the finished run, download the **BraviaRemote-apk** artifact, unzip it, install `app-debug.apk` on your phone (allow "install unknown apps").

## Or build locally
npm install && npx cap add android
# add android:usesCleartextTraffic="true" to <application> in android/app/src/main/AndroidManifest.xml
npx cap sync android && npx cap open android   # then Build > Build APK

## TV settings
Settings > Network > Home network > IP control: set Authentication to
"Normal and Pre-Shared Key", set a Pre-Shared Key, and turn on Simple IP control.
Phone and TV must be on the same Wi-Fi. Enter the TV IP + key in the app's Link tab.
