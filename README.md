![alt text](https://d.top4top.io/p_3580bc5w91.png?raw=true)

Mass Admin Page Finder adalah sebuah tools keamanan siber yang digunakan untuk menemukan halaman admin/login pada banyak website sekaligus secara otomatis.

🔍 Cara Kerja
  - Membaca Daftar Domain - dari file list.txt
  - Membaca Daftar Path - dari file wordlist.txt
  - Menggabungkan Kombinasi - setiap domain dengan setiap path admin
  - Testing Otomatis - mencoba mengakses URL yang terbentuk
  - Filter Response - hanya menyimpan halaman yang terdeteksi sebagai admin page

📁 Fungsi Spesifik
  1. Load Domains (load_domains())
     - Membaca domain dari file list.txt
     - Format: satu domain per baris
     - Contoh: example.com, google.com, dll
  2. Load Wordlist (load_wordlist())
     - Membaca path admin dari file wordlist.txt
     - Format: path seperti /admin, /login, /wp-admin
     - Contoh: /admin, /administrator, /login.php
  3. Check Admin Page (check_admin_page())
     - Mencoba 4 variasi URL untuk setiap kombinasi:
        - HTTPS tanpa www
        - HTTP tanpa www
        - HTTPS dengan www
        - HTTP dengan www
     - Filter berdasarkan:
        - Status code 200 (OK)
        - Konten mengandung kata kunci: 'login', 'password', 'admin', dll
   4. Save Result (save_result())
      - Menyimpan URL yang ditemukan ke result.txt
      - Hanya URL tanpa status code

🎯 Kegunaan Praktis
1. Untuk Security Researcher
   - Penetration testing
   - Vulnerability assessment
   - Security auditing
2. Untuk Web Developer
   - Testing keamanan aplikasi
   - Memeriksa exposure halaman admin
   - Audit konfigurasi
3. Untuk Bug Bounty Hunter
   - Reconnaissance otomatis
   - Finding low-hanging fruits
   - Mass domain scanning
