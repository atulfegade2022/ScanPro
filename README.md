# ScanPro PDF — Smart Scanner & PDF Tools

STATUS: Phase 1 written. NOT compiled or run (authoring sandbox had no Android SDK or network).

## Build (on your machine)
1. Open this folder in Android Studio (Koala or newer); sync will create the Gradle wrapper.
2. Debug APK: `./gradlew assembleDebug` -> app/build/outputs/apk/debug/app-debug.apk
3. Unit tests: `./gradlew testDebugUnitTest`

## Done in Phase 1
Gradle Kotlin DSL + version catalog, Material 3 theme (crimson/orange, dark mode), 5-tab navigation,
Home screen UI, original adaptive icon, one unit test.

## Not yet implemented (marked in-app)
Scanner, PDF tools, document manager, Room, Testing Dashboard, Billing, settings.

## Phase 2 (written, NOT compiled)
Scan button is now a large hero button. It opens the Google ML Kit Document Scanner
(live camera, automatic edge detection and perspective crop, clean-up filters, multi-page, gallery import).
The PDF is copied to app storage (files/scans/ScanPro_<time>.pdf) and shown under Recent Documents.
Notes: needs Google Play services on the device; the library version (16.0.0-beta1) should be checked
for a newer stable release; the "AI" part is ML Kit's on-device processing, not a cloud service.
