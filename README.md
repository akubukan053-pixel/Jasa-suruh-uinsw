# Jasa Suruh UINSW — Android APK

Project Android native sederhana yang menampilkan aplikasi kalkulator HPP dari `app/src/main/assets/index.html` melalui Android WebView.

## Membuat APK tanpa Android Studio

1. Buat repository baru di GitHub, misalnya `jasa-suruh-uinsw`.
2. Ekstrak ZIP project ini di HP/komputer.
3. Upload **seluruh isi folder project** ke repository GitHub (termasuk folder tersembunyi `.github`). Pastikan `build.gradle`, `settings.gradle`, `app/`, dan `.github/` berada di tingkat teratas repository.
4. Buka tab **Actions** di repository. Jika diminta, pilih **I understand my workflows, go ahead and enable them**.
5. Workflow **Build APK Android** akan berjalan otomatis setelah file di-push. Bisa juga jalankan manual melalui Actions → Build APK Android → Run workflow.
6. Tunggu sampai proses berstatus hijau **Success**.
7. Buka hasil run workflow, gulir ke bagian **Artifacts**, lalu unduh `JasaSuruh-UINSW-APK`.
8. Ekstrak ZIP artifact dan buka `app-debug.apk` di Android. Izinkan pemasangan dari sumber ini jika Android memintanya.

## Persyaratan build

GitHub Actions memasang Java 17, Android SDK, dan Gradle 8.9 secara otomatis. Android Gradle Plugin 8.7.3 digunakan oleh project ini. Android Studio tidak diperlukan.

## Catatan aplikasi

- Application ID: `id.uinsw.jasasuruh`
- Versi: `1.0.0` (versionCode 1)
- Minimum Android: Android 6.0 (API 23)
- Data order dan pengaturan disimpan lokal pada perangkat melalui WebView localStorage. Belum tersinkron ke cloud/Supabase.
- File APK debug cocok untuk instalasi dan pengujian. Untuk distribusi publik/Play Store, buat APK/AAB release dengan signing key sendiri dan simpan secret dengan aman di GitHub.
