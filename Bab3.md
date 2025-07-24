# 📦 Bab 3: Menghubungkan Git Lokal dan GitHub
Setelah kalian belajar dasar-dasar perintah Git dan telah memahami cara kerja Git secara lokal pada komputer kalian, kini saatnya untuk melangkah lebih jauh, yaitu menghubungkan Git ke Github.
GitHub adalah layanan hosting repositori Git berbasis cloud yang memungkinkan kalian untuk:
- Menyimpan repositori secara online
- Berbagi kode ke orang lain
- Berkolaborasi dengan tim
- Mengamankan cadangan proyek kalian

## 🔧 3.1 Membuat Akun dan Repositori di GitHub
### 1. Buat Akun  
Kunjungi https://github.com dan buat akun GitHub jika kalian belum memilikinya.
### 2. Buat repositori baru  
- Klik tombol `New` pada menu repositori github kalian
```
Nanti masukin gambar github_repo1
```
- Isi nama repositori kalian, misalnya `belajar-git`, kalian juga bisa menambahkan deskripsi singkat pada kolom deskripsi nya (opsional)
- Lalu kalian bisa memilih opsi public (semua orang dapat melihat repositori nya, tetapi pemilik repositori yang menentukan siapa yang bisa commit) atau private (pemilik repositori dapat mengatur siapa yang bisa melihat dan melakukan commit pada repositori nya)
```
Nanti masukin gambar github_repo2
```
- Jangan centang opsi `Initialize this repository with a README file`.
```
Nanti masukin gambar github_repo3
```
- Jika sudah tidak ada yang diatur lagi, Klik tombol “Create repository”.

## 🌐 3.2 Menghubungkan Git Lokal ke GitHub
Setelah membuat repositori di github, Github akan memberikan kalian tampilan awal seperti berikut:
```
Nanti masukin gambar github_repo4
```
Langkah selanjutnya yang akan kalian lakukan adalah menyambungkannya dengan repositori Git Lokal yang pernah kalian buat sebelumnya pada komputer kalian.

### 🔍 Kondisi Awal  
Yang sudah kalian punya yaitu:
1. Repositori Git lokal yang berada di dalam folder atau direktori proyek kalian, serta sudah melakukan git init dan melakukan commit
2. Repositori Github kosong yang baru selesai kalian buat dan belum berisi apapun

Sekarang kita akan menghubungkan dua repositori tersebut, agar nanti setiap perubahan yang kalian lakukan dari komputer lokal bisa dikirim (push) ke Github.

### 🔗 Langkah-langkah Menyambungkan
#### 1. Salin URL Repositori Github
Setelah membuat repositori github, salin alamat URL-nya seperti contoh berikut:
```
https://github.com/AndromedaRZ/belajar-git.git
```
Nama user nya akan secara otomatis menggunakan nama kalian.

#### 2. Tambahkan remote Github ke repositori lokal
Buka folder atau direktori proyek kalian menggunakan terminal, lalu ketik perintah berikut:
```
git remote add origin https://github.com/AndromedaRZ/belajar-git.git
```
Penjelasan perintah di atas:
- git remote add: perintah untuk menambahkan remote jarak jauh dari lokal agar terhubung ke Github kalian
- origin: nama alias default untuk repositori github (kalian juga bisa menggunakan nama yang kalian inginkan)
- URL: alamat repositori github kalian

Untuk memastikan apakah remote nya sudah terhubung atau belum, kalian bisa menggunakan perintah berikut:
```
git remote -v
```
Jika sudah terhubung, maka akan muncul keterangan seperti berikut:
```
Nanti masukin gambar git_remote_-v
```

#### 3. Push ke Github
Setelah repositori sudah terhubung, kalian bisa kirim perubahan (commit) dari repositori lokal kalian ke Github dengan perintah berikut:
```
git push -u origin master
```
Perintah di atas berguna untuk menyamakan perubahan yang ada di Repositori Github agar sama dengan Git Lokal kalian pada remote origin dengan branch master.

Setelah menyambungkannya dengan remote origin branch master, pada perubahan yang ada di Git Lokal berikutnya kalian hanya perlu mengetik perintah berikut:
```
git push
```
Maka otomatis Repositori yang ada di Github akan berubah.

## 📦 3.3 Menghubungkan GitHub ke Git Lokal
Untuk mengubungkan repositori Github ke Git Lokal, kalian bisa menggunakan perintah `git clone`.  
  
### 🔍 Apa itu git clone?
`git clone` adalah perintah Git yang digunakan untuk menyalin (menduplikasi) seluruh isi repositori dari GitHub (atau repositori remote lainnya) ke komputer lokal. Saat kita menjalankan git clone, kita tidak hanya menyalin file proyek, tapi juga seluruh riwayat perubahan (commit history), konfigurasi Git, dan hubungan dengan repositori asal (remote origin).
  
📂 Ibaratnya seperti ini:  
"Mendownload satu proyek lengkap dari GitHub ke komputer, beserta riwayat revisinya dan siap untuk dikerjakan."  

Caranya hampir sama yaitu kita membuat akun github dan membuat repositori seperti sebelumnya.
Tetapi pada menu pembuatan repositori, kita beri centang pada opsi `Add a README file`.
```
Nanti masukkin gambar github_repo5.png
```
Lalu klik tombol "Create repository".  

Nanti hasilnya akan memiliki tampilan yang berbeda seperti ini:
```
Nanti masukkin gambar github_repo6.png
```

### 🔗 Langkah-langkah Menyambungkan
#### 1. Salin URL Repositori Github
Setelah membuat repositori github, salin alamat URL-nya seperti contoh berikut:
```
https://github.com/AndromedaRZ/belajar-git.git
```
Nama user nya akan secara otomatis menggunakan nama kalian.

#### 2. Kloning repositori Github ke Git Lokal
Buka folder atau direktori proyek kalian menggunakan terminal, lalu ketik perintah berikut:
```
git clone https://github.com/AndromedaRZ/panduan-github.git
```
Penjelasan perintah di atas:
- `git clone` digunakan untuk menduplikasikan proyek ke dalam komputer kita (lokal).
- URL ditempatkan setelah `git clone` berasal dari alamat repositori yang ada di Github yang ingin kita ambil.

Nantinya juga Git akan:
- Membuat folder baru bernama panduan-github
- Mendownload seluruh isi repositori Github ke dalam folder tersebut
- Menghubungkan folder lokal dengan remote repositori (Github) secara otomatis
Sisanya kalian bisa masuk ke folder tersebut lalu mulai melanjutkan proyek sebelumnya seperti mengedit file, commit, push, pull dan sebagainya.

Untuk memastikan apakah remote nya sudah terhubung atau belum, kalian bisa menggunakan perintah berikut di dalam folder tempat kalian menjalankan `git clone`:
```
git remote -v
```
Jika sudah terhubung, maka akan muncul keterangan seperti berikut:
```
Nanti masukin gambar git_remote_-v
```
  
#### 3. Push ke Github
Setelah repositori sudah terhubung, kalian bisa kirim perubahan (commit) dari repositori lokal kalian ke Github dengan perintah berikut:
```
git push -u origin master
```
Perintah di atas berguna untuk menyamakan perubahan yang ada di Repositori Github agar sama dengan Git Lokal kalian pada remote origin dengan branch master.

Setelah menyambungkannya dengan remote origin branch master, pada perubahan yang ada di Git Lokal berikutnya kalian hanya perlu mengetik perintah berikut:
```
git push
```
Maka otomatis Repositori yang ada di Github akan berubah.

#### 4. Pull dari Github
Jika repositori yang ada di Github mengalami perubahan (misalnya mengubah file atau menambahkan dan menghapus file).  
Kalian bisa menggunakan perintah:
```
git pull origin master
```
Berguna untuk menarik perubahan tersebut agar Git Lokal kalian bisa menyamakan perubahan yang ada di Github dengan branch Master.  
Jadi, kita tidak perlu melakukan semua perubahan yang ada di Git Lokal secara otomatis.  
Sama halnya dengan `git push` tadi, setelah menyambungkannya dengan origin branch master.  
Kalian cukup mengetikkan perintah berikut:
```
git pull
```
Maka otomatis Repositori yang ada di Git Lokal akan berubah.
