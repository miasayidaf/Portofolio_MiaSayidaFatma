# MobileAutomation_MiaSayidaFatma — Login Eraspace

## Automation Script Mobile

Proyek automation testing untuk fitur **Login pada aplikasi Eraspace Android**, menggunakan pendekatan yang sama seperti proyek `WebAutomation_MiaSayidaFatma`:

- **Bahasa Pemrograman:** JavaScript (CommonJS)
- **Automation Framework:** WebdriverIO
- **BDD Framework:** Cucumber BDD/Gherkin
- **Design Pattern:** Page Object Model (POM)
- **Step Definitions:** Implementasi langkah-langkah pengujian
- **Assertion:** Node.js `assert`
- **Test Reporter:** Spec Reporter
- **Mobile Automation:** Appium + UiAutomator2

Automation mobile menggunakan **Appium dan UiAutomator2** pada Android, bukan automation browser Chrome.

## Test Cases

| TC ID | Tipe | Test Scenario | Expected Result |
|---|---|---|---|
| 1.1 | Negative | Login menggunakan username dan password tidak valid, kemudian klik Login | Login gagal dan sistem menampilkan pesan error |
| 1.2 | Positive | Login menggunakan username dan password valid, kemudian klik Login | Login berhasil; halaman utama, daftar menu, nama akun, dan jumlah poin ditampilkan |

**Lokasi Feature File:** `features/eraspace/login.feature`

## Persiapan (Windows)

1. Install Node.js, Android Studio/Android SDK Platform Tools, Java JDK, dan Appium 2.
2. Jalankan Android Emulator atau hubungkan perangkat Android dengan USB Debugging aktif. Periksa menggunakan `adb devices`.
3. Install Eraspace dari Google Play Store atau gunakan APK yang diperoleh secara sah. Proyek ini ditujukan untuk Android, bukan iOS.
4. Siapkan akun pengujian resmi dengan kredensial valid dan pastikan aplikasi dalam kondisi logout.
5. Gunakan **Appium Inspector** untuk mengidentifikasi `resource-id` atau `accessibility ID` pada halaman Login dan setelah login. Selector UI belum dapat diverifikasi dari proyek automation web atau screenshot.

## Instalasi

Jalankan perintah berikut di terminal folder proyek:

```bash
npm install
npx appium driver install uiautomator2
cp .env.example .env
```

Edit file `.env` dengan mengisi:

- `APP_PACKAGE`: Package ID Eraspace yang terpasang, **atau**
- `APP_PATH`: Lokasi file APK Eraspace.
- `VALID_USERNAME`: Username akun pengujian yang valid.
- `VALID_PASSWORD`: Password akun pengujian yang valid.

Untuk mencari package ID aplikasi terpasang:

```bash
adb shell pm list packages
```

## Cara Menjalankan Automation Testing

Buka **dua terminal** dari folder proyek di Visual Studio Code.

### Terminal 1 — Appium Server

```bash
npm run appium
```

### Terminal 2 — Eksekusi Pengujian

Periksa konfigurasi dan perangkat:

```bash
npm run doctor
```

Jalankan Negative Login:

```bash
npm run test:login:negative
```

Jalankan Positive Login:

```bash
npm run test:login:positive
```

Jalankan kedua skenario:

```bash
npm run test:login
```

## Struktur Folder Project

```text
MobileAutomation_MiaSayidaFatma/
├── features/
│   ├── eraspace/login.feature
│   ├── pageobjects/eraspace.page.js
│   └── step-definitions/eraspace.steps.js
├── config/locators.json
├── config/locators.example.json
├── scripts/check-setup.js
├── evidence/
├── .env.example
├── .gitignore
├── wdio.conf.js
└── package.json
```
