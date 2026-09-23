# BenivalApp

A minimal iOS app (SwiftUI + WKWebView) that opens **https://beniwal.me**.
Full-screen web view, back/forward swipe gestures, custom app icon.

## What you need

- A Mac with **Xcode 15 or later**
- An Apple ID (free works for installing on your own iPhone; a paid
  Apple Developer Program membership is only needed for App Store distribution)

## Build & run

1. Unzip and open `BenivalApp.xcodeproj` in Xcode.
2. Select the **BenivalApp** target → **Signing & Capabilities** → pick your
   Team. (Change the Bundle Identifier `com.beniwal.app` if it collides.)
3. Connect your iPhone (or pick a simulator), press **Run** (⌘R).

## Files

- `BenivalApp/BenivalAppApp.swift` — app entry point
- `BenivalApp/ContentView.swift` — root view
- `BenivalApp/WebView.swift` — WKWebView wrapper (change the URL here)
- `BenivalApp/Assets.xcassets` — app icon & accent color

## Notes

- To point the app at a different site, edit the URL in `ContentView.swift`.
- `NSAppTransportSecurity` isn't needed: the site is served over HTTPS.
- Web-view-only apps can face extra scrutiny in App Store review
  (guideline 4.2, minimum functionality), so this is best for personal /
  TestFlight use unless the site offers app-like functionality.
