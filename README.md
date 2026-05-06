<h1 align="center">KELOMPOK PEMROGRAMAN WEB</h1>

Anggota Kelompok:

Muhammad Dwi Firmansyah_202412012

Nabil

Yovitha Gracia Tavares_202412044


1. Code dan hasil awal bug 1

<img width="1589" height="318" alt="codinganawal png" src="https://github.com/user-attachments/assets/8e201eff-8a32-4607-a794-b1a0d014ecd9" />
<img width="1884" height="545" alt="output" src="https://github.com/user-attachments/assets/0d25ef58-dd5b-4cfd-b923-4461bea509b4" />

Penjelasan bug : 
Radio button terpisah dari labelnya — di output, label teks ("Pria", "Wanita") muncul di baris terpisah dan tidak sejajar dengan radio buttonnya. Radio button malah muncul di tengah halaman (terlalu ke kanan), sedangkan teks labelnya ada di kiri bawah. Tidak ada <br> atau pemisah antar setiap radio button Teks label ditulis langsung setelah tag input (bukan dibungkus <label>) Karena tidak ada struktur pembungkus, browser merender semuanya dalam satu baris panjang yang overflow dan berantakan.


Solusi atau perbaikan
<img width="1575" height="335" alt="Perbaikan" src="https://github.com/user-attachments/assets/bfbae3c2-a9b4-44cf-a62b-51d5fb85d8ea" />
<img width="1885" height="601" alt="output perbaikan" src="https://github.com/user-attachments/assets/7df0de91-100c-4734-aa63-7aeee23167c1" />

Penjelasan perbaikan :
Pada kode perbaikan ini, terdapat beberapa perubahan yang dilakukan untuk menyempurnakan tampilan form. Perubahan pertama yang cukup terlihat adalah penambahan atribut placeholder pada setiap field input. Pada field NIM ditambahkan placeholder "Masukkan NIM", pada field Nama ditambahkan placeholder "Masukkan Nama Lengkap", dan pada textarea Alamat ditambahkan placeholder "Masukkan Alamat Lengkap". Tujuan dari penambahan placeholder ini adalah untuk memberikan petunjuk kepada pengguna tentang data apa yang harus diisi pada masing-masing kolom, sehingga form menjadi lebih informatif dan mudah dipahami. Selain itu, pada field textarea Alamat juga ditambahkan atribut required, sama seperti field NIM dan Nama. Hal ini bertujuan agar pengguna tidak bisa mengosongkan field Alamat saat mengisi form, sehingga semua data penting wajib diisi sebelum form dapat dikirimkan.


2. Code dan hasil bug 2


   


