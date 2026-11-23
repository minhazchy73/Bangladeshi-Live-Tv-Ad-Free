# Bangladesh Live TV - Android project

A lightweight Android WebView app that wraps the supplied Bangladeshi YouTube live channel list. Includes Android fullscreen video handling and back-button behavior.


## Build an APK

1. Install Android Studio (current stable) on a Windows/Mac/Linux computer.
2. Open Android Studio > **Open** > select this `BangladeshLiveTV` project folder.
3. Let Gradle sync and download the Android Gradle plugin/dependencies.
4. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK is normally located at `app/build/outputs/apk/debug/app-debug.apk`.
6. Copy that APK to your Android phone, tap it, and allow installation from that source if Android asks.

For a release APK, choose **Build > Generate Signed Bundle / APK > APK** and create a signing key.

## Playback note

Live feeds are embedded YouTube streams. Some channel streams may block embedded playback or require YouTube's own app/site; the web page includes an **Open on YouTube** option for that case. This project is a personal-use client and does not host or redistribute the channel video.

## Lightweight Ad/Tracker Blocking

This build includes a WebView request filter for common third-party ad and tracking domains. It can reduce some banner ads, tracking requests, and ad network traffic inside the app. It is **not a full ad blocker** and does not reliably block YouTube's own ads; attempting to filter YouTube's shared delivery domains can break live video.

The blocklist is embedded in `MainActivity.java` and can be extended by adding domains to `BLOCKED_HOSTS`.
