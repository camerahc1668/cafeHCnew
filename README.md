# ☕ POS HC — GitHub Actions Build

Tự động build **APK Android** và **IPA iOS** trên GitHub (miễn phí).

## 📁 Cấu trúc
```
.github/
  workflows/
    build-android.yml   ← Build APK Android
    build-ios.yml       ← Build IPA iOS
www/
  index.html            ← App POS HC
android-resources/
  network_security_config.xml
ios-resources/
  ExportOptions.plist
capacitor.config.json
package.json
```

## 🚀 Cách dùng

1. Upload thư mục này lên GitHub repository
2. Vào tab **Actions** → chờ build (~5–10 phút)
3. Tải file về trong phần **Artifacts**:
   - `POS-HC-Android-APK` → file `.apk` cài trên Android
   - `POS-HC-iOS-IPA` → file `.ipa` cài trên iPhone

## ⚠️ Lưu ý iOS

File `.ipa` build ra là **unsigned** (chưa ký) vì không có Apple Developer Account.

Để cài lên iPhone, dùng một trong các cách:
- **AltStore** — cài IPA không cần jailbreak, miễn phí
- **Sideloadly** — tool cài IPA qua USB
- **Apple Developer Account** ($99/năm) — để ký và phát hành App Store

## 🔄 Cập nhật app

Chỉ cần sửa `www/index.html` rồi commit → GitHub tự build lại!
