# 📦 Bab 3: Menghubungkan Git Lokal ke GitHub
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
- Jangan centang opsi `Initialize this repository with a README file`
```
Nanti masukin gambar github_repo3
```
- Jika sudah tidak ada yang diatur lagi, Klik tombol “Create repository”

## 🌐 3.2 Menyambungkan Git Lokal ke GitHub
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
Nama user nya akan secara otomatis menggunakan nama kalian

#### 2. Tambahkan remote Github ke repositori lokal
Buka folder atau direktori proyek kalian menggunakan terminal, lalu ketik perintah berikut:
```
git remote add origin https://github.com/AndromedaRZ/belajar-git.git
```
Penjelasan perintah di atas:
- git remote add: perintah untuk menambahkan remote jarak jauh dari lokal agar terhubung ke Github kalian
- origin: nama alias default untuk repositori github
- URL: alamat repositori github kalian

#### 3. Push ke Github
Setelah repositori sudah terhubung, kalian bisa kirim perubahan (commit) dari repositori lokal kalian ke Github
```
git push -u origin master
```
Perintah di atas akan membantu kalian jika di masa depan nanti kalian ingin melakukan push atau menyamakan perubahan di repositori Github agar sama dengan repositori lokal kalian, kalian hanya perlu menggunakan perintah `git push`. Arti dari perintah di atas yaitu mendorong perubahan dari repositori lokal ke repositori Github kalian pada remote origin dengan branch master.

Jika sudah selesai melakukan push, kalian bisa periksa kembali repositori Github yang tadi kalian buat. Jika berhasil, maka kalian bisa melihat semua file dan commit yang kalian lakukan sebelumnya di lokal kini sudah muncul di Github kalian.

