#  📘 Bab 1: Instalasi dan Konfigurasi Dasar Git
Setelah memahami pengertian git dan github, sekarang saatnya kalian untuk menginstal git pada komputer kalian agar bisa langsung mulai menggunakannya.

Di bagian ini kalian akan belajar:
1. Cara menginstal git sesuai sistem operasi yang kalian gunakan
2. Memastikan Git sudah berhasil terinstal
3. Mengatur identitas (nama dan email) kalian di git

## 🖥️ 1.1 Cara Menginstal Git
### 🔹 Untuk Pengguna Windows
1. Buka situs resmi Git:
👉 https://git-scm.com/
2. Klik tombol Download for Windows.
3. Jalankan file .exe yang sudah diunduh.
4. Saat proses instalasi, kamu cukup klik Next terus.
Biarkan pengaturan default, lalu klik Install.
5. Setelah selesai, buka aplikasi Git Bash atau Command Prompt.

### 🔹 Untuk Pengguna macOS
Pastikan kamu sudah menginstal Homebrew (pengelola paket di Mac).  
Jika belum, lihat: https://brew.sh, lalu jalankan perintah berikut di Terminal:
```
brew install git
```
### 🔹 Untuk Pengguna Linux (Ubuntu/Debian)  
Buka terminal dan jalankan perintah berikut:
```
sudo apt update
sudo install git
```

## ✅ 2. Memeriksa Apakah Git Sudah Terpasang  
Setelah instalasi selesai, kamu bisa cek apakah Git sudah berhasil terpasang dengan buka terminal, lalu ketik:
```
git --version
```
Sebagai contoh. Jika kalian menggunakan sistem operasi windows, maka akan muncul versi git seperti berikut:
```
git version 2.50.0.windows.1
```
Kalau muncul pesan error atau tidak dikenali, ulangi proses instalasi dan pastikan terminal mengenali perintah 'git'.

## ⚙️ 3. Konfigurasi Git
Sekarang, kita akan mengatur nama dan email kita pada git. Sebelum menggunakan git, kalian perlu mengatur identitas kalian terlebih dahulu. Ini penting karena setiap perubahan yang kalian atau orang lain lakukan (commit). Git akan melacak dan mencatat identitas siapa yang melakukan perubahan tersebut.  
untuk menentukan identitas kalian dalam git, jalankan perintah berikut pada terminal komputer kalian:
```
git config --global user.name "Nama Kalian"
git config --global user.email "emailkalian@gmail.com"
```
contoh
```
git config --global user.name "Rizky"
git config --global user.email "rizkyricky859@gmail.com"
```
## ✅ Penjelasan:
1.) --global : berarti konfigurasi ini berlaku untuk semua proyek Git di komputer kalian, kalian dapat menggunakan identitas yang berbeda di setiap proyek git kalian dengan menghapus perintah '--global' saat menentukan identitas kalian.  
2.) "Nama kalian" dan "emailkalian@gmail.com" bisa kalian ganti sesuai identitas yang ingin kalian buat.

## 🔍 Cek Konfigurasi Git
Untuk memastikan apakah nama dan email kalian sudah tersimpan, gunakan:
```
git config user.name
git config user.email
```

Hasil yang muncul kira-kira seperti ini:
```
Rizky
rizkyricky859@gmail.com
```
🎉 Sekarang Git Kamu Siap Digunakan!  
Kamu sudah berhasil:

- Menginstal Git  
- Memastikan Git aktif di terminal  
- Mengatur identitas Git kamu

😎 Bagaimana belajarnya? apakah kalian sudah ada gambaran mengenai git tadi? untuk materi berikutnya, kalian akan belajar memahami perintah-perintah dasar di dalam git. Tunggu apa lagi?, klik link di bawah ini untuk menuju ke materi berikutnya 👇.
