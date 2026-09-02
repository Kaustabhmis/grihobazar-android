# Grihobazar Android App - Build & Run Guide

This project is a native Android WebView wrapper for **[www.grihobazar.in](https://www.grihobazar.in)** with support for:
- Full Web App rendering with hardware acceleration & DOM storage
- Pull-to-refresh via `SwipeRefreshLayout`
- Real-time page load progress indicator
- Offline fallback screen with dynamic retry button
- File upload & camera selector via `WebChromeClient.onShowFileChooser`
- External intent handlers for WhatsApp chat (`wa.me`), Phone dialer (`tel:`), Mail composer (`mailto:`), and Google Maps (`geo:`)
- Geolocation permission bridging
- Native back navigation dispatcher

---

## 🛠️ Requirements
- Android Studio Iguana / Hedgehog / Jellyfish or newer
- JDK 17 or JDK 21 (bundled with Android Studio)
- Android SDK Platform 34 (Android 14)
- Minimum supported Android version: Android 7.0 (API 24)

---

## 🚀 How to Build & Run in Android Studio

1. **Download & Extract ZIP**:
   Click the **"Download Project (.ZIP)"** button in the top navigation bar. Extract the `GrihobazarApp` folder.

2. **Open in Android Studio**:
   - Open Android Studio.
   - Click **File** > **Open...**
   - Select the extracted `GrihobazarApp` directory and click **OK**.
   - Wait for Gradle Sync to complete automatically.

3. **Run on Device or Emulator**:
   - Connect an Android phone with USB Debugging enabled, OR select an Android Virtual Device (AVD).
   - Click the green **Run (▶)** button or press `Shift + F10`.

4. **Generate Release APK / AAB (for Play Store)**:
   - Go to **Build** > **Generate Signed Bundle / APK...**
   - Select **Android App Bundle** (for Google Play) or **APK** (for direct distribution).
   - Select or create your Keystore (.jks).
   - Choose **release** build variant and click **Finish**.
   - Your output will be located in `app/release/app-release.apk`.

---

## 💻 Building via Command Line (CLI)

```bash
# For Linux/macOS
./gradlew assembleDebug

# For Windows
gradlew.bat assembleDebug

# Output APK will be at:
# app/build/outputs/apk/debug/app-debug.apk
```

---

## 📱 Features

### WebView Configuration
- **URL**: https://www.grihobazar.in
- **Hardware Acceleration**: Enabled for smooth rendering
- **DOM Storage**: Enabled for local data persistence
- **JavaScript**: Enabled with secure access
- **User Agent**: Custom user agent for property portal

### User Experience
- **Pull-to-Refresh**: Swipe down to reload the webpage
- **Loading Progress**: Progress bar shows page load status
- **Offline Handling**: Shows fallback screen when offline with retry button
- **File Upload**: Full support for property image uploads and file selection
- **Camera Access**: Direct camera integration for property photos

### External Intents
- **WhatsApp**: `wa.me` links open WhatsApp
- **Phone**: `tel:` links open dialer
- **Email**: `mailto:` links open mail composer
- **Maps**: `geo:` links open Google Maps

### Permissions
- Internet access
- Camera (for property photo uploads)
- File storage (for uploads)
- Geolocation (for property searches by location)

---

## 🔧 Configuration

### Change Website URL
Edit `app/src/main/java/com/grihobazar/MainActivity.kt`:
```kotlin
private val WEB_URL = "https://www.grihobazar.in"
```

### App Name & Icon
- **App Name**: Change in `app/src/main/res/values/strings.xml`
- **App Icon**: Replace in `app/src/main/res/mipmap-*/ic_launcher.png`

---

## 📦 Release Build

### Sign APK for Play Store
```bash
./gradlew bundleRelease
```

Output: `app/release/app-release.aab`

### Install Signed APK to Device
```bash
adb install -r app/release/app-release.apk
```

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Gradle sync fails | File > Invalidate Caches > Restart |
| WebView content not loading | Check internet permissions in manifest |
| White screen on launch | Verify `WEB_URL` is correct and reachable |
| Camera not working | Grant camera permission when prompted |
| File upload fails | Check storage permissions and upload size limits |

---

## 📝 License

This project is licensed under the MIT License.

---

## 👨‍💻 Developer Info

Created with ❤️ for Grihobazar Property Portal
- Repository: https://github.com/Kaustabhmis/grihobazar-android
- Website: https://www.grihobazar.in
