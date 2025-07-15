# 📘 Bab 2: Dasar-Dasar Perintah Git
Di Bab ini, kalian akan mulai menggunakan git secara langsung di komputer kalian, materi yang akan kalian pelajari dimulai dari membuat repositori git kalian, mencatat perubahan yang kalian lakukan (commit), dan melihat riwayat perubahan dengan perintah di terminal kalian. Git tidak akan langsung menyimpan perubahan yang kalian lakukan secara otomatis, ada beberapa perintah yang dapat kalian gunakan untuk melakukan hal tersebut. Oleh karena itu, mari kita pelajari secara bertahap.

## 🧩 2.1 Membuat Repositori Git
### 🔸 Apa Itu Repositori? 
Repositori adalah tempat Git menyimpan semua riwayat perubahan dari file yang ada di dalam sebuah folder atau direktori proyek kalian. Repositori bisa bersifat lokal (disimpan dalam komputer kalian) atau remote (disimpan di platform bernama github, nanti akan dibahas di bab berikutnya).
### 🔸 Cara Membuat Repositori Git Lokal
Sebelum membuat repositori lokal di dalam komputer kalian, pertama-tama kalian harus membuat sebuah folder atau direktori terlebih dahulu untuk tempat kalian menyimpan file proyek kalian. Jika kalian sudah membuat folder atau direktori nya, buka folder atau direktori tersebut menggunakan terminal, lalu ketik:
```
git init
```
Setelah menjalankan perintah `git init`. Git akan membuat folder tersembunyi bernama '.git', folder tersebut akan menyimpan dan mencatat seluruh perubahan yang kalian lakukan pada proyek kalian.  
📌 Catatan penting: Folder ini tidak boleh dihapus, karena berisi semua data penting Git.

## 🧠 2.2 Memahami Alur Kerja Git
Sebelum kita melakukan perubahan pada proyek milik kita, kita harus memahami alur kerja git terlebih dahulu. Untuk lebih jelasnya, area kerja pada repositori git terbagi menjadi 3:
### 🔸 Working Directory 
Adalah lokasi folder atau direktori tempat kalian membuat repositori, ini adalah folder proyek kalian yang berisi file-file yang bisa kalian lihat dan edit. Jika kalian melakukan tindakan seperti membuat sebuah file baru, mengedit file, atau menghapus file proyek kalian, berarti kalian masih berada di dalam area Working Directory, dan status file yang kalian edit akan menjadi modified.
### 🔸 Staging Area
Adalah area sementara di saat kalian sedang melakukan perubahan di dalam folder atau direktori proyek kalian, tetapi kita belum memutuskan untuk commit atau mengonfirmasi perubahan tersebut. Jika kalan sering belanja online melalui aplikasi belanja, maka staging area ini seperti saat kalian memasukkan barang yang ingin kalian beli ke dalam keranjang dan belum memutuskan untuk melakukan checkout barang tersebut. Jika kalian sudah selesai mengedit file proyek kalian, kalian bisa menggunakan perintah `git add`, maka file yang sudah kalian edit tadi akan masuk ke area yang namanya staging area.

📌 File yang sudah berada di staging area tidak akan berubah jika kalian mengeditnya lagi sebelum commit, kalian perlu menggunakan perintah `git add` lagi jika ingin mengedit ulang filenya.
### 🔸 Repository (Commit History)
Dalam Git, repositori adalah tempat di mana seluruh riwayat proyek kamu disimpan secara permanen. Setiap perubahan yang kamu simpan dengan perintah `git commit` akan masuk ke dalam repository, dan Git akan menyimpannya sebagai snapshot, atau salinan kondisi proyek pada saat commit tersebut dilakukan.
### 🧾 Apa Itu Commit?
Commit adalah langkah menyimpan perubahan ke repository. Commit bersifat permanen, artinya Git akan mencatatnya dan kamu bisa kembali ke commit itu kapan saja. Setiap commit berisi commit hash (code commitnya), nama dan email pembuatnya, waktu dan tanggal commitnya, daftar perubahan, serta pesan commit jika kalian menambahkan pesan singkat saat melakukan commitnya.
### 📸 Apa Itu Snapshot?
Snapshot dalam Git adalah salinan lengkap kondisi proyek kalian pada saat tertentu, biasanya setiap kali kalian melakukan `git commit`. Git menyimpan proyek kalian dalam bentuk snapshot, bukan hanya perubahan baris demi baris seperti sistem kontrol versi tradisional. Ini adalah inti dari cara kerja git. Snapshot adalah kondisi seluruh file proyek saat commit dilakukan.

Agar kalian bisa memahami lebih jelas mengenai area dalam git, kalian dapat melihat gambar berikut:
NANTI KASIH GAMBAR DIAGRAMNYA COY

## ✏️ 2.3 Menambahkan dan Menyimpan Perubahan
### 🔹 1. Buat File Baru
Pertama-tama, cobalah membuat sebuah file baru pada folder atau direktori proyek kalian, bukalah folder atau direktori proyek kalian, lalu jalankan terminal dan ketikkan perintah berikut:
```
echo "Belajar git"> catatan.txt
```
Perintah di atas berfungsi untuk membuat sebuah file txt baru bernama 'catatan.txt', lalu memasukkan kalimat "Belajar git" di dalam isi file tersebut.
### 🔹 2. Cek Status File
Lihatlah status file kalian dengan perintah berikut:
```
git status
```
Git akan menampilkan file yang sudah kalian edit tadi, perlu diketahui dalam tahap ini, kalian masih berada di area working directory.
### 🔹 3. Tambahkan File ke Staging Area
Sebelum menyimpan perubahan, kalian perlu memilih file mana yang ingin dicatat perubahannya, gunakan perintah berikut untuk menyimpan perubahan dari file secara spesifik:
```
git add catatan.txt
```
Atau jika kalian melakukan perubahan pada banyak file, menggunakan perintah spesifik satu persatu pasti akan memakan waktu yang cukup lama, maka gunakan perintah berikut untuk menyimpan perubahan dari semua file yang kalian edit.
```
git add .
```
Perintah di atas akan menambahkan semua file yang kalian ubah ke area yang namanya staging area. Jika kalian ingin memastikan bahwa file yang kalian ubah sudah tersimpan perubahannya atau sudah ditambahkan ke staging area, kalian dapat menggunakan perintah `git status`, maka akan muncul keterangan seperti berikut:

### 🔹 4. Simpan Perubahan dengan Commit
Gunakan perintah berikut untuk menyimpan perubahan file proyek kalian saat ini ke dalam riwayat git.
```
git commit -m "Menambahkan file catatan.txt"
```
File yang sudah di-commit akan tersimpan perubahannya ke dalam area repository (commit history)

## 🔍 Melihat Isi Repositori (Riwayat Commit)
Setelah kalian melaukan beberapa kali commit atau perubahan, kalian bisa melihat daftar riwayat commit kalian menggunakan perintah pada terminal seperti berikut:
```
git log
```
Maka contoh riwayat commitnya akan muncul seperti berikut:
```
Jangan lupa masukin gambar git log nya
```
Dalam hasil git log di atas, diperlihatkan informasi dari log atau riwayat commit kalian. Seperti siapa yang melakukan perubahan atau commit tersebut, lalu kapan waktu dan tanggal commit tersebut dibuat, dan isi dari pesan commit yang kalian buat.

## 2.4 🌿 Bekerja dengan Branch (Cabang)
### 📌 Apa Itu Branch?
Branch (Cabang) adalah salah satu fitur di Git yang berfungsi untuk membuat jalur pengembangan atau jalur proyek yang terpisah dari jalur utama (biasanya jalur utama disebut `main` atau `master`)  
Branch memungkinkan kita untuk:
1. Mencoba fitur baru tanpa merusak atau merubah kode utama
2. Memperbaiki bug secara terpisah
3. Mengembangkan beberapa ide atau fitur sekaligus

Setelah selesai, hasil pekerjaan di branch lain bisa digabungkan (merge) kembali ke branch utama (main/master)

### 💡 Analogi Branch
Bayangkan proyek kita seperti sebuah pohon besar yang batangnya memiliki beberapa cabang dahan
- Batang utama = branch `main/master` tempat kode stabil berada
- Cabang-cabang lain = branch baru untuk mengembangkan fitur tertentu secara terpisah

Jika nanti cabang yang lain sudah selesai dikerjakan, kita bisa menggabungkan fiturnya kembali ke cabang utama `main/master`

### 🔧 Membuat branch baru

Pertama-tama kita perlu mengetahui aturan untuk memberi nama pada branch terlebih dahulu:
1. Jangan gunakan spasi jika lebih dari 1 kata, gunakan `-` sebagai alternatif.
2. Hindari karakter aneh, seperti `#`, `@`, `!`, `%`.
3. Gunakanlah nama yang pendek dan mudah dimengerti, contohnya:
   - `fitur-login`
   - `fitur-redirect`
   - `bug-v1.2`

Berikut adalah perintah untuk membuat branch baru:
```
git branch <nama branch>
```
Jika kita ingin membuat branch baru bernama `fitur-login`, jalankan perintah:
```
git branch fitur-login
```
*Ini hanya membuat branch, tapi kita belum berpindah ke branch tersebut

### 🚀 Berpindah ke branch
Cara berpindah branch, cukup ketikkan `git switch` beserta nama branch yang ingin kita tuju:
```
git swtich <nama branch>
```
Agar kita bisa pindah dan menggunakan branch `fitur-login`, jalankan perintah:
```
git switch fitur-login
```
Setelah ini, semua perubahan dan commit kita akan masuk ke branch `fitur-login`, dan tidak akan mengganggu progress di branch utama (`main/master`)  
Kamu juga bisa langsung membuat branch dan berpindah ke branch yang kamu buat sekaligus dengan perintah:
```
git switch -c fitur-login
```

### 🔄 Kembali ke Branch Utama
Kalau mau kembali bekerja di branch utama `main`, jalankan:
```
git switch main
```
Atau jika nama branch utamanya adalah `master`, maka jalankan:
```
git switch master
```

### 🔍 Melihat Daftar Branch
Untuk melihat semua branch yang ada, gunakan perintah:
```
git branch
```
Hasilnya, misalnya:  
```
<Nanti masukkin gambar 'git_branch.png'>
```
Pada gambar diatas, ada 3 cabang yang muncul yaitu `bug-v1`, `fitur-login`, dan `master`.  
Pada branch `master` terdapat simbol `*` di depannya yang berarti kita sedang berada di branch tersebut, hal yang sama berlaku pada branch lainnya ketika kita pindah branch

### 📃 Note
Perlu diketahui, ketika kita membuat branch baru maka branch tersebut akan membuat jalur baru dari branch dan commit yang kita tempati.  
Misalnya ketika kita berada di branch `master` dan berada di commit ke-3, lalu kita membuat branch baru bernama `fitur-login`, maka branch `fitur-login` akan membuat jalur baru yang berasal dari branch `master` commit ke-3. Nantinya ke-2 branch tersebut akan menampilkan hasil pengerjaan atau commit yang sama, tetapi akan menjadi berbeda ketika salah satu branch melakukan commit.
Setelah itu kita melakukan commit pada branch `fitur-login` sehingga itu menjadi commit ke-4nya. Progress yang ada di branch `master` tidak akan terganggu dan hasilnya akan tetap menampilkan commit ke-3.
  
Lalu ketika kita sedang berada di branch `fitur-login` dan membuat branch baru bernama `bug-v1`, maka branch `bug-v1` akan membuat jalur baru yang berasal dari branch `fitur-login` dan bukan berasal dari branch `master`. Karena branch `fitur-login` sudah membuat jalur terpisah dari branch `master`, maka branch `bug-v1` adalah hasil percabangan dari commit ke-4 pada branch `fitur-login`.
  
Pada awalnya akan terasa sulit jika kalian mencoba memahami fungsi branch ini untuk pertama kalinya, tetapi nantinya kalian akan terbiasa ketika sering menggunakan fungsi branch ini. Karena branch ini akan sangat membantu ketika kita sedang mengerjakan proyek secara berkelompok ataupun berkolaborasi dengan tim lain.

Karena fungsi yang menunjukkan percabangan, di bawah ini adalah contoh bagaimana cara melihat alur perkembangan commit setiap branch yang terjadi, dengan cara mengetik perintah:
```
git log --all --graph
```
Hasilnya akan seperti ini:
```
Masukkin gambar "git_log_all_graph.png"
```
  
Cara keluar dari git lognya adalah cara menekan tombol 'q'.
  
Jika kelihatannya terlalu panjang dan membingungkan, kalian bisa mempermudahnya dengan menambahkan perintah `--oneline` seperti ini:
```
git log --all --graph --oneline
```
Hasilnya:
```
Masukkin gambar "git_log_all_graph_oneline.png"
```
Dari kedua gambar tersebut, nantinya akan terlihat perkembangan setiap commit dari setiap branch yang berbeda, dan dengan perintah tersebut juga akan memunculkan sebuah garis yang menjelaskan grafik perkembangannya yang bercabang-cabang.

## 🌳 2.6 Menggabungkan Branch (Merge)
### 📌 Apa Itu Merge?
Setelah kita memahami apa itu branch, berikutnya adalah merge. Setelah kamu selesai mengerjakan sebuah fitur atau perbaikan bug di branch terpisah, kamu pasti ingin menggabungkan hasil pekerjaan itu ke branch utama (`main/master`).  
Itulah fungsi `merge` di Git
- `git merge` akan menggabungkan riwayat commit dari satu branch ke branch tempat dan commit tempat kita berada sekarang.
- Hal ini bertujuan untuk memastikan semua perubahan dari branch lain masuk ke branch aktif, sehingga perkembangan proyek tetap terintegrasi.

### 💡 Analogi Merge
Bayangkan ketika kita sedang membangun rumah:
- branch `main/master` = rancangan utama rumah
- branch `fitur-taman` = rencana menambahkan taman kecil di samping rumah
Saat taman sudah selesai dibuat di blueprint terpisah (`branch`), kita ingin menggabungkannya ke rancangan utama.
Proses pembangunan itu adalah `merge`.

### 🛠️ Cara Menggunakan `git merge`
#### 1️⃣ Pindah ke branch yang ingin menerima hasil merge
Biasanya kita menggunakan branch utama yaitu `main/master`.
```
git switch master
```
#### 2️⃣ Jalankan perintah merge
Misalnya kamu ingin menggabungkan branch `fitur-taman` ke `master`.
```
git merge fitur-taman
```
Git akan mengambil semua commit di branch `fitur-taman` yang belum ada di `master`, lalu menyatukannya dengan branch `master`

### ✅ Hasil Merge
- Jika tidak ada file yang diubah di kedua branch pada bagian yang sama, Git akan langsung berhasil merge otomatis.
- Kalau ada file yang diubah di kedua branch pada bagian yang sama, Git akan mendeteksi konflik. Dan kalian harus menyelesaikan konflik itu secara manual.

### ⚠️ Apa Itu Konflik Merge?
Konflik saat merge atau penggabungan branch terjadi apabila Git menemukan perubahan yang bertabrakan antara branch yang satu dengan yang lainnya.
Contoh:  
- Di branch `main/master`, baris ke-5 file index.html ditulis "Halo Dunia".
- Di branch `fitur-taman`, baris ke-5 file yang sama juga ditulis "Hello World".
Git tidak tahu mana yang harus diambil, jadi dia meminta kalian untuk menyelesaikan konflik tersebut secara manual.

### 🔍 Tips Setelah Merge
- Gunakan git log --oneline --graph --all untuk melihat bagaimana branch-branch sudah digabung.
- Gunakan git status untuk memastikan tidak ada konflik tersisa.

Dengan `git merge`, kalian bisa menggabungkan hasil pekerjaan dari branch terpisah ke branch utama. Fitur ini sangat berguna ketika kalian sedang mengerjakan sebuah proyek bersama teman-teman kalian, kalian dapat menjaga alur pengembangan proyek kalian tetap rapi dan terstruktur dan menjaga kerja sama saat kalian sedang mengembangkan proyek kalian.

## 2.7 🗑️ Menghapus Branch Setelah Merge
### 📌 Kenapa branch dihapus?
Setelah kalian selesai menggabungkan branch fitur (misalnya `git merge`) ke branch utama (`main/master`), branch fitur itu biasanya sudah tidak diperlukan lagi.  
Menghapus branch yang sudah selesai kalian kerjakan bisa berguna untuk:
1. Menjaga repositori tetap bersih dan rapi
2. Menghindari kebingungan (misalnya tidak sengaja kerja di branch lama)

### 🧹 Cara Menghapus Branch di Git
Misalnya kalian sudah sudah merge branch `fitur-login` ke branch `master`, dan ingin menghapus branch `fitur-login`:
```
git branch -d fitur-login
```
perintah `-d` artinya:
- Delete (menghapus) branch hanya jika branch sudah digabung (merged) ke branch lain
- Jika branch tersebut belum melakukan merge, Git akan menolak menghapusnya, supaya progress di branch tersebut tidak hilang

Jika kalian sudah yakin ingin menghapus branch yang belum di-merge (misalnya branch eksperimen yang gagal), maka gunakan:
```
git branch -D fitur-login
```
Perintah dari `-D` adalah `--delete --force` atau hapus paksa.  
Hal ini juga perlu diperhatikan karena akan langsung menghapus branch tanpa mengecek apakah sudah di-merge atau belum.
