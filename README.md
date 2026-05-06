<h1 align="center">KELOMPOK PEMROGRAMAN WEB</h1>

Anggota Kelompok:

Muhammad Dwi Firmansyah_202412012

Nabil

Yovitha Gracia Tavares_202412044


A. Code dan hasil awal bug 1

<img width="1589" height="318" alt="codinganawal png" src="https://github.com/user-attachments/assets/8e201eff-8a32-4607-a794-b1a0d014ecd9" />
<img width="1884" height="545" alt="output" src="https://github.com/user-attachments/assets/0d25ef58-dd5b-4cfd-b923-4461bea509b4" />
Penjelasan bug : Radio button terpisah dari labelnya — di output, label teks ("Pria", "Wanita") muncul di baris terpisah dan tidak sejajar dengan radio button-nya. Radio button malah muncul di tengah halaman (terlalu ke kanan), sedangkan teks labelnya ada di kiri bawah. Tidak ada <br> atau pemisah antar setiap radio button
Teks label ditulis langsung setelah tag input (bukan dibungkus <label>)
Karena tidak ada struktur pembungkus, browser merender semuanya dalam satu baris panjang yang overflow dan berantakan

Solusi atau perbaikan :


