# Build ScamShield APK (no Android Studio needed on your own PC if using GitHub Actions)

This source project is configured to build a debug APK using GitHub Actions.

## Build online
1. Create a new repository on GitHub.
2. Extract this ZIP and upload the *contents* of this folder to the repository root (so `.github`, `app`, `build.gradle`, and `settings.gradle` are at the top level).
3. Open the repository's **Actions** tab and enable Actions if prompted.
4. Select **Build APK** → **Run workflow** (or push to the `main` branch).
5. Open the completed workflow run. Under **Artifacts**, download `ScamShield-debug-apk`.
6. Extract the downloaded artifact ZIP; it contains `app-debug.apk`.
7. Transfer `app-debug.apk` to your Android phone and open it to install. If prompted, allow installation from that source. Only install APKs you built or trust.

## Local build
Use Android Studio with JDK 17, Android SDK Platform 35, and Gradle 8.9. Then run `npm test` and `gradle assembleDebug`. The APK is generated at `app/build/outputs/apk/debug/app-debug.apk`.

This is a debug/demo build, not a Play Store release. The app's recipient profiles, risk signals, reports, and points are simulated; it does not verify real bank accounts or transfer money.
