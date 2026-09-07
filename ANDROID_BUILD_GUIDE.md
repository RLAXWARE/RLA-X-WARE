# RLA X WARE — Android Build Guide

Source ini adalah aplikasi Expo/React Native yang siap dipindahkan ke lingkungan
build Android. Preview Replit menggunakan Expo Go; untuk menghasilkan aplikasi
native, gunakan Android Studio atau layanan build Expo yang sudah terhubung ke
akunmu.

## Persiapan

- Node.js 20 atau lebih baru
- pnpm
- Java 17
- Android Studio dan Android SDK jika build dilakukan lokal

## Menjalankan source

```bash
pnpm install
pnpm --filter @workspace/rla-x-ware run typecheck
pnpm --filter @workspace/rla-x-ware run dev
```

## Build native

Buka folder `artifacts/rla-x-ware` di lingkungan build Android pilihanmu,
gunakan konfigurasi dari `app.json`, lalu hasilkan APK untuk pengujian atau AAB
untuk Google Play. Nama aplikasi dan package Android sudah disetel sebagai:

- Nama: `RLA X WARE`
- Package: `com.rla.xware`
- Orientasi: portrait

## Catatan keamanan

Aplikasi ini hanya membuka pengaturan Android resmi dan launcher game resmi.
Aplikasi tidak membypass login, menyuntikkan kode ke game, memodifikasi file
game, atau membuat overlay/crosshair untuk keuntungan tidak adil. Izin
`WRITE_SETTINGS` bersifat terbatas dan tetap bergantung pada dukungan perangkat.