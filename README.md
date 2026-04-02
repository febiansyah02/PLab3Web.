# Praktikum 3: View Layout dan View Cell

Repository ini merupakan kelanjutan dari tugas pemrograman web menggunakan CodeIgniter 4. Fokus pada praktikum kali ini adalah implementasi View Layout untuk templating yang efisien dan View Cell untuk komponen UI yang modular.

*Perubahan Utama dari Praktikum 2*

  Pada praktikum sebelumnya, kita menggunakan konsep parsial (menggunakan include untuk header dan footer). Di Praktikum 3 
  ini, kita beralih ke:

1. View Layout: Menggunakan satu template induk (main.php) sebagai kerangka utama.

2. View Cell: Membuat komponen mandiri untuk menampilkan "Artikel Terkini" di sidebar tanpa harus menulis logika di setiap Controller.

*Langkah-Langkah Praktikum*

1. Membuat Layout Utama

    Membuat file template induk di app/Views/layout/main.php. File ini berisi struktur HTML dasar, navigasi, dan sidebar. Bagian konten utama menggunakan fungsi renderSection('content') agar bisa diisi secara dinamis oleh halaman lain.

3. Implementasi View Cell (Artikel Terkini)

   Langkah ini bertujuan agar daftar artikel di sidebar dapat dipanggil secara otomatis:

    - Logic: Membuat class ArtikelTerkini di app/Cells/.
 
   - View: Membuat tampilan komponen di app/Views/components/artikel_terkini.php.

   - Database: Menambahkan kolom created_at pada tabel artikel untuk mengurutkan postingan terbaru.
  
4. Menghubungkan Halaman ke Layout

   Mengubah file home.php (atau index.php) agar menggunakan template induk dengan perintah.

# Pertanyaan Tugas

1. Apa manfaat utama penggunaan View Layout?

   *JAWAB:* Memudahkan pengelolaan tampilan. Jika ada perubahan pada navigasi atau footer, kita cukup mengubah satu file layout saja, dan seluruh halaman website akan otomatis berubah.

2. Jelaskan perbedaan antara View Cell dan View biasa!

   *JAWAB:*

   - View Biasa: Hanya berisi kode tampilan dan datanya harus dikirim manual dari Controller.
  
   - View Cell: Komponen modular yang memiliki logika sendiri (seperti mini-controller). Ia bisa mengambil data dari model secara mandiri sehingga bisa diletakkan di halaman mana saja tanpa mengubah kode Controller utama.
  
# Screenshot Hasil
<img width="1905" height="1079" alt="Cuplikan layar 2026-04-02 141223" src="https://github.com/user-attachments/assets/b5ed7cbc-e4ec-49f2-a337-9a70e5eb0a74" />
