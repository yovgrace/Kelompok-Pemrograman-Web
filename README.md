<h1 align="center">KELOMPOK PEMROGRAMAN WEB</h1>

Anggota Kelompok:

Muhammad Dwi Firmansyah_202412012

Muhammad Nabil Abdillah_202412053

Yovitha Gracia Tavares_202412044


1. Code dan hasil bug 1
   
   NIM hanya berisi angka
   <img width="381" height="117" alt=" bug 1" src="https://github.com/user-attachments/assets/570ebbc2-1e31-41a2-a9c9-59d3e609ba06" />
   <img width="642" height="215" alt="output bug 1" src="https://github.com/user-attachments/assets/f9ffb069-afb6-4610-b938-c6f315e97048" />

Penjelasan bug : 
Kode tersebut menggunakan Regular Expression (Regex) /^\d+$/ untuk memastikan bahwa data yang dimasukkan ke dalam variabel nim adalah angka murni. Simbol ^ menandakan awal baris, \d+ berarti harus terdapat satu atau lebih karakter angka, dan $ menandakan akhir baris, sehingga jika pengguna memasukkan karakter selain angka (seperti huruf atau spasi), metode .test(nim) akan menghasilkan nilai false. Karena terdapat operator negasi ! di depan Regex tersebut, maka kondisi if akan bernilai true saat input salah, yang kemudian memicu munculnya pesan alert("NIM harus berupa angka!") dan perintah return untuk menghentikan proses eksekusi kode selanjutnya (seperti pengiriman data ke database).


Solusi atau perbaikan
<img width="1575" height="335" alt="Perbaikan" src="https://github.com/user-attachments/assets/bfbae3c2-a9b4-44cf-a62b-51d5fb85d8ea" />
<img width="712" height="183" alt="perbaikan bug 1" src="https://github.com/user-attachments/assets/4789540d-c66f-4db8-9719-b29fecd50215" />

Penjelasan perbaikan :
Pada kode perbaikan ini, terdapat beberapa perubahan yang dilakukan untuk menyempurnakan tampilan form. Perubahan pertama yang cukup terlihat adalah penambahan atribut placeholder pada setiap field input. Pada field NIM ditambahkan placeholder "Masukkan NIM", pada field Nama ditambahkan placeholder "Masukkan Nama Lengkap", dan pada textarea Alamat ditambahkan placeholder "Masukkan Alamat Lengkap". Tujuan dari penambahan placeholder ini adalah untuk memberikan petunjuk kepada pengguna tentang data apa yang harus diisi pada masing-masing kolom, sehingga form menjadi lebih informatif dan mudah dipahami. Selain itu, pada field textarea Alamat juga ditambahkan atribut required, sama seperti field NIM dan Nama. Hal ini bertujuan agar pengguna tidak bisa mengosongkan field Alamat saat mengisi form, sehingga semua data penting wajib diisi sebelum form dapat dikirimkan.


2. Code dan hasil bug 2

<img width="1724" height="198" alt="bug 2" src="https://github.com/user-attachments/assets/dd27eac5-21fd-43f5-96e9-4c26690a16e2" />
<img width="1895" height="232" alt="output bag 2" src="https://github.com/user-attachments/assets/59a76d5e-9953-47ba-a7e5-08ab29cf0539" />

Penjelasan bug :
Berdasarkan kode dan output di atas, dropdown tanggal dan tahun sudah berhasil terisi dengan menggunakan perulangan for loop pada JavaScript, dimana tanggal diisi dari 1 sampai 31 dan tahun diisi dari 1990 sampai 2025 menggunakan innerHTML. Namun error yang masih terjadi adalah ketiga dropdown yaitu tanggal, bulan, dan tahun masih tampil secara vertikal ke bawah dan memenuhi lebar penuh layar seperti yang terlihat pada output, padahal seharusnya ketiganya tampil sejajar dalam satu baris. Hal ini terjadi karena pada kode HTML sebelumnya tidak terdapat pembungkus <div style="display: flex; gap: 10px;"> yang berfungsi untuk mengelompokkan ketiga dropdown tersebut agar tampil secara horizontal dalam satu baris.


Solusi atau Perbaikan :
<img width="1708" height="296" alt="perbaikan bug 2" src="https://github.com/user-attachments/assets/333debc2-9717-4709-8a38-936ec1d37614" />
<img width="1408" height="477" alt="perbaikan bug 2 (2)" src="https://github.com/user-attachments/assets/40ffb37a-a3b5-4732-9614-2cf2fdfc7985" />

Penjelasan perbaikan :
Berdasarkan kode dan output di atas, perbaikan yang dilakukan adalah dengan membuat fungsi isiTanggal(max) yang mengisi dropdown tanggal secara dinamis sesuai jumlah hari maksimal pada bulan yang dipilih. Fungsi ini dipanggil pertama kali dengan nilai default 31 hari, kemudian ditambahkan addEventListener pada dropdown bulan sehingga ketika bulan berubah, jumlah hari akan menyesuaikan secara otomatis, dimana bulan April, Juni, September, dan November memiliki maksimal 30 hari dan bulan Februari memiliki maksimal 28 hari. Hasil perbaikan ini terlihat jelas pada output dimana ketiga dropdown tanggal, bulan, dan tahun kini sudah tampil sejajar dalam satu baris secara horizontal, dan pada tabel Data Mahasiswa kolom "JK" juga sudah berubah menjadi "Jenis Kelamin" yang lebih deskriptif dibandingkan sebelumnya.


3. Code dan hasil bug 3
   <img width="1532" height="136" alt="bug 3" src="https://github.com/user-attachments/assets/29d1649e-c670-4263-9de5-3510498ede33" />
   <img width="1232" height="97" alt="output bug 3" src="https://github.com/user-attachments/assets/65954ec7-e892-4322-bbff-1e7fdb536c6f" />
   
Penjelasan bug :
Bug pada kode tersebut terjadi karena elemen <form> tidak ditutup dengan tag penutup </form> di akhir baris, yang menyebabkan struktur HTML menjadi tidak valid dan berpotensi merusak tata letak atau fungsionalitas elemen setelahnya. Selain itu, berdasarkan gambar output yang hanya menampilkan kolom "Nama", terdapat indikasi bahwa elemen input "NIM" tertutup atau terdistorsi oleh pengaturan CSS (seperti width: 100% atau display: block) yang belum dikelola dengan baik dalam kontainer form tersebut, sehingga elemen-elemen formulir tidak tersusun secara rapi secara vertikal maupun horizontal.


Solusi atau perbaikan :
<img width="825" height="137" alt="perbaikan bug 3" src="https://github.com/user-attachments/assets/88a4b576-f5a8-466e-aeac-8fb2af45e86b" />
<img width="1286" height="96" alt="output bug 3 (2)" src="https://github.com/user-attachments/assets/a32bdd53-014c-4378-a15d-1d48a87dbd49" />

Penjelasan Perbaikan :
Potongan kode tersebut mendefinisikan struktur input untuk kolom Nama dalam sebuah formulir HTML. Penggunaan tag <label> berfungsi sebagai judul keterangan, sementara tag <input type="text"> dengan id="nama" digunakan sebagai area pengisian data oleh pengguna. Penambahan atribut required berperan sebagai validasi agar input tidak boleh kosong saat submit, dan atribut placeholder="Masukkan Nama Lengkap" memberikan petunjuk teks di dalam kotak input untuk meningkatkan aspek user experience. Pada tampilan output, terlihat bahwa input tersebut mengisi lebar kontainer secara penuh, yang menandakan adanya penerapan gaya CSS seperti width: 100% agar kolom input terlihat lebih jelas dan mudah diisi.


4. Code dan hasil bug 4
   <img width="821" height="48" alt="bug 4 (2)" src="https://github.com/user-attachments/assets/cba3be73-52c6-4c51-a259-6fe048d7247b" />
   <img width="487" height="142" alt="output bug 4" src="https://github.com/user-attachments/assets/4f5dd404-0104-45ba-9a7c-fce98ef417f3" />

Penjelasan bug   : 
Potongan kode JavaScript tersebut berfungsi untuk memproses data pendaftaran, di mana baris pertama menggabungkan variabel `tanggal`, `bulan`, dan `tahun` menjadi satu string format tanggal lahir (**ttl**) menggunakan *template literals*. Baris kedua mengambil nilai dari elemen input dengan ID `password` menggunakan perintah `document.getElementById("password").value` untuk disimpan ke dalam konstanta `password`. Masalah atau "bug" pada implementasi ini terlihat dari hasil *output*-nya, di mana nilai kata sandi tampil sebagai teks terbuka (**12345**) di dalam tabel; hal ini menunjukkan bahwa meskipun kodenya secara sintaksis benar, terdapat kesalahan pada tipe input di sisi HTML yang tidak menggunakan `type="password"`, sehingga data sensitif tersebut tidak terenkripsi atau tersembunyi saat ditampilkan kembali.


  Solusi atau perbaikan :
  <img width="762" height="40" alt="perbaikan bug 4" src="https://github.com/user-attachments/assets/b12fddbe-9834-40e7-8a97-d6051b43bd83" />
  <img width="377" height="167" alt="output perbaikan bug 4" src="https://github.com/user-attachments/assets/9f3677a6-c4d1-4cdb-9ba6-9b448f30b4ca" />


Penjelasan perbaikan :
Potongan kode perbaikan tersebut menggunakan teknik **masking** untuk menyembunyikan karakter asli kata sandi pada tampilan tabel demi keamanan data. Di dalam elemen `<td>`, variabel `${maskedPassword}` (yang berisi karakter sensor seperti asteris `*****`) ditampilkan secara visual kepada pengguna, sementara nilai aslinya tetap disimpan secara tersembunyi di dalam atribut kustom `data-real-pass="${d.password}"`. Pendekatan ini memastikan bahwa informasi sensitif tidak terbaca secara langsung di layar, namun tetap dapat diakses oleh sistem atau fungsi JavaScript lainnya melalui atribut data tersebut jika diperlukan untuk proses autentikasi atau logika aplikasi lebih lanjut.


5. Code dan hasil bug 5
   <img width="805" height="216" alt="bug 5 (2)" src="https://github.com/user-attachments/assets/af2c0095-58f5-426f-bebf-a2c12a3f6815" />
   <img width="226" height="152" alt="bug 5" src="https://github.com/user-attachments/assets/07668e14-a307-4aab-a1b2-4a52508be2db" />

Penjelasan bug :
Kode tersebut mengandung bug yang menyebabkan ikon pada kolom **Aksi** tidak muncul atau pecah (*broken image*), seperti yang terlihat pada gambar output. Secara teknis, masalah ini terjadi karena jalur file (*file path*) pada atribut `src="edit.png"` dan `src="trash.png"` tidak valid atau file gambar tersebut tidak ditemukan di direktori yang sama dengan file HTML/JS tersebut. Meskipun secara struktur kode HTML di dalam *template literal* sudah benar menggunakan tag `<a>` untuk fungsi `editRow` dan `deleteRow`, browser gagal memuat aset visualnya sehingga hanya menampilkan ikon *placeholder* gambar rusak.


Solusi atau perbaikan :
<img width="1605" height="264" alt="perbaikan bug 5" src="https://github.com/user-attachments/assets/cb6dc2a4-099f-40f5-b34a-52decc57026c" />
<img width="267" height="176" alt="output perbaikan bug 5" src="https://github.com/user-attachments/assets/f05d2050-0227-4ea3-a001-494e2ebdc32e" />


Penejelasan perbaikan :
Potongan kode perbaikan tersebut memperbarui elemen kolom **Aksi** dengan memastikan sumber gambar (`src`) merujuk pada file yang benar, yaitu `pensil.png` dan `garbage.png`, sehingga ikon dapat merender dengan sempurna pada tabel. Di dalam tag `<img>`, ditambahkan atribut `alt` sebagai teks alternatif untuk aksesibilitas dan `class="icon-aksi"` untuk standarisasi gaya visual melalui CSS. Secara fungsional, setiap ikon dibungkus oleh tag jangkar (`<a>`) yang menjalankan fungsi JavaScript `editRow(this)` dan `deleteRow(this)` ketika diklik, dan seluruh rangkaian baris tersebut akhirnya disisipkan ke dalam dokumen menggunakan perintah `tableBody.appendChild(row)`.




 


  

   


   


