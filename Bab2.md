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



