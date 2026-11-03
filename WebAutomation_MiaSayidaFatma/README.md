# CURA Healthcare — Web Automation

Project Web Automation menggunakan **WebdriverIO 10 + Cucumber + JavaScript (CommonJS) + Page Object Model (POM)**.

## Cara Menjalankan Automation (Git Bash di VS Code)

1. Extract file ZIP, kemudian buka folder `WebAutomation_MiaSayidaFatma_Ready` menggunakan Visual Studio Code.
2. Buka **Terminal > New Terminal** dan pilih **Git Bash**.
3. Jalankan `npm i` untuk menginstal seluruh dependencies (membutuhkan koneksi internet).
4. Jalankan `npm run test` + copy relative path untuk mengeksekusi salah satu feature yang ingin dijalankan.
5. Jalankan `npm run test:login` untuk mengeksekusi 2 skenario Login (Positive & Negative).
6. Jalankan `npm run test:appointment` untuk mengeksekusi 2 skenario Make Appointment (Positive & Negative).
7. Jalankan `npm run test:curaHealthcare` untuk mengeksekusi seluruh 4 skenario pengujian atau 1 folder curaHealthcare.

**Website yang diuji:**  
https://katalon-demo-cura.herokuapp.com/profile.php#login

## Recording Hasil Automation Testing

Saya juga telah menyediakan **screen recording** yang menampilkan hasil eksekusi automation testing beserta langkah-langkah menjalankan pengujian melalui Visual Studio Code.

**Nama file:** `webAutomation_MiaSayidaFatma_Recording.webm`

File recording tersebut tersedia di dalam folder **`curaHealthcare`**.

Silakan mengunduh dan membuka file recording untuk melihat hasil running automation serta panduan menjalankan pengujian secara langsung.
