# Nativescript Coding Project
https://github.com/cgoboncan-ebsi/nativescript-code-project

## Prompt
This project scaffolds a plain nativescript-vue project that uses 
the nativescript carousel plugin.

The goal of this coding project is to determine the root cause
for why the ListView's tap event handler is not invoked on iOS.

The listView tap event handler does work on Android.

## Deliverable
Prepare a presentation that describes
 - The thought process to isolate the issue
 - Tools used
 - Recommendations
 - Final thoughts

## Background
This project was created using:
1. npm install -g @vue/cli @vue/cli-init
2. vue init nativescript-vue/vue-cli-template nativescript-coding-project
3. tns plugin add nativescript-carousel

## System Setup
The setup instructions for Nativescript can be found here for macOS [https://docs.nativescript.org/start/ns-setup-os-x](https://docs.nativescript.org/start/ns-setup-os-x)
The instructions are a bit outdated, but give the general steps.

1. Install homebrew `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
2. brew update
3. Install node v10+ (we use nvm to manage node).

### Xcode
4. Install Xcode via the App Store
5. Verify `Command Line Tools for Xcode` are installed

### Ruby
6. sudo gem install xcodeproj
7. sudo gem install cocoapods
8. pods setup

### Python
9. pip install six

### Nativescript
10. npm i -g nativescript
11. tns doctor (you can ignore any android/java related issues).

## Usage
``` bash
npm install
tns prepare ios
tns debug ios --no-hmr
```
