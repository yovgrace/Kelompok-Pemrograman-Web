<h1 align="center">KELOMPOK PEMROGRAMAN WEB</h1>

Anggota Kelompok:

-Muhammad Dwi Firmansyah_202412012

-Nabil

-Yovitha Gracia Tavares_202412044

![Hasil Progam](contoheror.png)
       }
        input, textarea, select {
            width: 100%;
            padding: 8px;
            margin: 5px 0 15px;
            box-sizing: border-box; /* Tambahan agar padding tidak merusak lebar 100% */
            ========================================================
            ghytfrters
            ========================================================
        }

        /* Khusus untuk textarea agar tidak bisa diubah ukurannya */
        textarea {
            resize: none;
            height: 80px; /* Menentukan tinggi kotak alamat */
            ========================================================

            ========================================================
        }

        .icon-aksi {
            width: 20px;       /* Atur lebar gambar */
            height: 20px;      /* Atur tinggi gambar */
            object-fit: cover; /* Agar gambar tidak gepeng */
            vertical-align: middle;
            ========================================================

            ========================================================
        }

        .aksi a {
            display: inline-block;
            padding: 2px;
            ========================================================

            ========================================================

        }
    <label>Jenis Kelamin</label><br>
    <input type="radio" name="jk" value="Pria"> Pria
    <input type="radio" name="jk" value="Wanita"> Wanita
    <br><br>
    =====================================================

    =====================================================

<script>
    const form = document.getElementById("formMahasiswa");
    const tableBody = document.getElementById("tableBody");

    // ===== DROPDOWN TANGGAL =====
    function isiTanggal(max = 31) {
        const tgl = document.getElementById("tanggal");
        tgl.innerHTML = "";
        for (let i = 1; i <= max; i++) {
            // PERBAIKAN: Gunakan backtick (`)
            tgl.innerHTML += `<option value="${i}">${i}</option>`;
          =============================================================

          =============================================================
            
        }
    }

    isiTanggal();

    document.getElementById("bulan").addEventListener("change", function() {
        const bulan = this.value;
        let maxHari = 31;

        if (["04","06","09","11"].includes(bulan)) maxHari = 30;
        if (bulan === "02") maxHari = 28;

        isiTanggal(maxHari);
      ==========================================================

      ==========================================================
    });

    // ===== DROPDOWN TAHUN =====
    const currentYear = new Date().getFullYear();
    for (let i = 1990; i <= currentYear; i++) {
        // PERBAIKAN: Gunakan backtick (`)
        document.getElementById("tahun").innerHTML += `<option value="${i}">${i}</option>`;
      ============================================================

      ============================================================
    }

    // ===== LOAD DATA =====
    window.onload = function() {
        const data = JSON.parse(localStorage.getItem("mahasiswa")) || [];
        data.forEach(d => tambahBaris(d));
      =============================================================

      =============================================================
    };

    // ===== SUBMIT =====
    form.addEventListener("submit", function(e) {
        e.preventDefault();

        const nim = document.getElementById("nim").value.trim();
        const nama = document.getElementById("nama").value.trim();
        const alamat = document.getElementById("alamat").value;
      ============================================================

      ============================================================                    

        // VALIDASI NIM DUPLIKAT
        const rows = tableBody.querySelectorAll("tr");
        for (let r of rows) {
            if (r.children[0].innerText === nim) {
                alert("NIM sudah ada!");
                return;
        =========================================================

        =========================================================
            }
        }

        // VALIDASI JENIS KELAMIN
        const selectedJK = document.querySelector('input[name="jk"]:checked');
        if (!selectedJK) {
            alert("Silakan pilih jenis kelamin!");
            return;
        }
        const jk = selectedJK.value;

        let tanggal = document.getElementById("tanggal").value;
        const bulan = document.getElementById("bulan").value;
        const tahun = document.getElementById("tahun").value;

        tanggal = tanggal.padStart(2, "0");
        ===========================================================

        ===========================================================
        // PERBAIKAN: Gunakan backtick (`)
        const ttl = `${tanggal}-${bulan}-${tahun}`;

        const password = document.getElementById("password").value;

        const dataBaru = { nim, nama, alamat, jk, ttl, password };

        tambahBaris(dataBaru);
        ========================================================

        ========================================================

        // SIMPAN KE LOCALSTORAGE
        let data = JSON.parse(localStorage.getItem("mahasiswa")) || [];
        data.push(dataBaru);
        localStorage.setItem("mahasiswa", JSON.stringify(data));

        form.reset();
        =========================================================

        =========================================================
    });

    function tambahBaris(d) {
        const row = document.createElement("tr");
      ============================================

      ============================================

        row.innerHTML = `
            <td>${d.nim}</td>
            <td>${d.nama}</td>
            <td>${d.alamat}</td>
            <td>${d.jk}</td>
            <td>${d.ttl}</td>
            <td>${d.password}</td>
            <td>
                <a href="#" onclick="editRow(this)">
                    <img src="pensil.png" width="20">
                </a>
                <a href="#" onclick="deleteRow(this)">
                    <img src="garbage.png" width="20">
                </a>
            </td>
        `;

        tableBody.appendChild(row);
      ===========================================

      ===========================================
    }

    function deleteRow(el) {
        if(!confirm("Hapus data ini?")) return;
        
        const row = el.parentElement.parentElement;
        const nim = row.children[0].innerText;
      ==============================================

      ==============================================

        row.remove();

        let data = JSON.parse(localStorage.getItem("mahasiswa")) || [];
        data = data.filter(d => d.nim !== nim);
        localStorage.setItem("mahasiswa", JSON.stringify(data));
    }

    function editRow(el) {
        const row = el.parentElement.parentElement;
        const cells = row.children;

        // Pindahkan data ke form
        document.getElementById("nim").value = cells[0].innerText;
        document.getElementById("nama").value = cells[1].innerText;
        document.getElementById("alamat").value = cells[2].innerText;
        document.getElementById("password").value = cells[5].innerText;
      =================================================================

      =================================================================

        // Hapus data lama dari tabel dan localStorage agar saat di-submit dianggap data baru/update
        const nimLama = cells[0].innerText;
        row.remove();
      ================================================================

      ================================================================
        
        let data = JSON.parse(localStorage.getItem("mahasiswa")) || [];
        data = data.filter(d => d.nim !== nimLama);
        localStorage.setItem("mahasiswa", JSON.stringify(data));
      ===============================================================

      ===============================================================
    }
</script>

</body>
</html>/*
