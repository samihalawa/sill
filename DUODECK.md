# DuoDeck for iPhone Duo

DuoDeck turns the lower half of a half-folded iPhone Duo into an adjustable Mac trackpad and control surface, while keeping the Mac video above the fold. Based on the Apache-2.0 open-source [Sill](https://github.com/Saffsanity/sill) remote Mac streaming engine.

## Use the controls

1. Pair DuoDeck with [Sill for Mac](https://getsill.app/download) and open your iPhone Duo halfway.
2. Open the **Trackpad** menu and choose **Small**, **Medium**, or **Full**.
3. Open **Shortcuts** and tap a command to send it to the Mac. Use **Preset** in the same menu to switch between **Editing**, **Browsing**, **Windows**, and **Code**.

DuoDeck remembers your size and preset. Shortcuts remain available with a Full trackpad. Small and Medium can also show buttons beside the pad when there is enough room at the current text size. Some shortcuts depend on the frontmost Mac app or its keyboard settings.

## Requirements
An iPhone Duo with iOS 27.1 or later for fold-aware laptop layout, plus a Mac running the compatible Sill companion. On ordinary iPhones and iPads, the inherited Sill layouts remain available.

## Build
On a Mac with Xcode 27.1 or newer:

```sh
xcodebuild -project iOSClient/Sill.xcodeproj -scheme Sill -configuration Debug \
  -destination 'generic/platform=iOS Simulator' CODE_SIGNING_ALLOWED=NO build
```

For code signing, use your own Apple Developer account and unique bundle identifier. The current DuoDeck bundle identifier is com.agentsai.duodeck (Agents AI Ltd.).

The open-source license is Apache 2.0; please retain the upstream attribution and notices when redistributing.
