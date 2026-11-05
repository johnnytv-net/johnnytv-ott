# JohnnyTV OTT

A second, lightweight JohnnyTV app for Android TV and Firestick. It opens the
web player at johnnytv.net/simple.html full screen. Installs alongside the main
JohnnyTV app (different package: net.johnnytv.ott).

Every push to main builds a signed APK and publishes it as a release tagged with
the versionName from app/build.gradle.kts. The APK is at
releases/download/<tag>/app-release.apk.

Keystore: the workflow makes one on first run. To keep updates installable over
the top, add the generated ott.jks as the KEYSTORE_B64 secret (base64) after the
first build - or every build signs with a fresh key and the box refuses the update.
