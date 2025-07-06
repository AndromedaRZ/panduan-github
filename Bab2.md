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
Setelah menjalankan perintah 'git init'. Git akan membuat folder tersembunyi bernama '.git', folder tersebut akan menyimpan dan mencatat seluruh perubahan yang kalian lakukan pada proyek kalian.  
📌 Catatan penting: Folder ini tidak boleh dihapus, karena berisi semua data penting Git.

## 🧠 2.2 Memahami Alur Kerja Git
Sebelum kita melakukan perubahan pada proyek milik kita, kita harus memahami alur kerja git terlebih dahulu. Untuk lebih jelasnya, area kerja pada repositori git terbagi menjadi 3:
### 🔸 Working Directory 
Adalah lokasi folder atau direktori tempat kalian membuat repositori, ini adalah folder proyek kalian yang berisi file-file yang bisa kalian lihat dan edit. Jika kalian melakukan tindakan seperti membuat sebuah file baru, mengedit file, atau menghapus file proyek kalian, berarti kalian masih berada di dalam area Working Directory, dan status file yang kalian edit akan menjadi modified.
### 🔸 Staging Area
Adalah area sementara di saat kalian sedang melakukan perubahan di dalam folder atau direktori proyek kalian, tetapi kita belum memutuskan untuk commit atau mengonfirmasi perubahan tersebut. Jika kalan sering belanja online melalui aplikasi belanja, maka staging area ini seperti saat kalian memasukkan barang yang ingin kalian beli ke dalam keranjang dan belum memutuskan untuk melakukan checkout barang tersebut. Jika kalian sudah selesai mengedit file proyek kalian, kalian bisa menggunakan perintah 'git add', maka file yang sudah kalian edit tadi akan masuk ke area yang namanya staging area.

📌 File yang sudah berada di staging area tidak akan berubah jika kalian mengeditnya lagi sebelum commit, kalian perlu menggunakan perintah 'git add' lagi jika ingin mengedit ulang filenya.
### 🔸 Repository (Commit History)
