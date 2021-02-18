# React-Native Environment Building Steps
## iOS

### 1. Install homebrew
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

### 2. Install git
    brew install git

### 3. [Install node.js](https://nodejs.org/dist/v14.15.4/node-v14.15.4.pkg)

### 4. [Install vscode (stable version)](https://code.visualstudio.com/docs/?dv=osx)

### 5. Install watchman
    brew install watchman

### 6. Install cocoapods
    brew cleanup -d -v 
    brew install cocoapods 

### 7. [Install Xcode](https://developer.apple.com/services-account/download?path=/Developer_Tools/Xcode_12.3/Xcode_12.3.xip)

### 8. Install iOS simulator
-   open Xcode -> Create Empty Project  -> Perference -> Components -> install iOS 13.4 simulator

### 9. Chose Xcode Command Line Tools Version
-   open Xcode -> Select Empty Project -> Perference -> Location -> Command Line Tools -> chose Xcode 12.3 (12C33)
npm run ios


## Android

### 1. Install JDK
    brew install --cask adoptopenjdk/openjdk/adoptopenjdk8

### 2. [Install Android Studio](https://developer.android.com/studio)

-   Use standard install
Android Studio -> Preferences | Appearance & Behavior → System Settings open → Android SDK.

-   Select the "SDK Platforms" tab from within the SDK Manager, then check the box next to "Show Package Details" in the bottom right corner. 

-   Look for and expand the Android 10 (Q) entry, then make sure the following items are checked: Android SDK Platform 29 and Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image.

-   Next, select the "SDK Tools" tab and check the box next to "Show Package Details" here as well.

-   Look for and expand the "Android SDK Build-Tools" entry, then make sure that 29.0.2 is selected.

-   Finally, click "Apply" to download and install the Android SDK and related build tools.


### 3. Add PATH to ~/.zshrc

```sh
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

### 4. launch app in Android simulator
    npm run android
Notice: You need to run "npm run ios" first.


## Register Apple ID Steps

### 1. Get the Apple ID.
### 2. [Login Apple Developer](https://developer.apple.com/account)
### 3. Generating a Provision Profile
-   You need to register at least one iPhone for generating a iOS APP development Provision Profile.
-   You can register the iPhone in "Devices" in Apple Developer website.
-   Except upper step, you also need to upload your Mac certificate to "Certificates".
-   Using Mac's "Keychain Access" to create Certificate Signing Request (CSR) file and upload to "Certificates".
-   From now, you can set "Identifiers" to your apps.
-   Congratulation!

