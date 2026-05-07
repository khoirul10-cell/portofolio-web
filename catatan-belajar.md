📚 Buku Saku (Cheat Sheet) Front-End Web Fase 11. Struktur & Fondasi HTMLIni adalah kerangka dasar yang wajib ada di setiap file HTML:HTML<!DOCTYPE html> <!-- Memberitahu browser bahwa ini adalah HTML5 -->
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Judul Halaman Web</title>
    <!-- Tag penghubung ke file CSS -->
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <!-- Semua konten visual web ditaruh di sini -->
</body>
</html>
Tag HTML EsensialTag HTMLNama / FungsiContoh Penggunaan<header>Bagian atas web (biasanya untuk Logo & Navbar).<header> ... </header><main>Pembungkus konten utama web.<main> ... </main><section>Bagian/segmen spesifik dalam halaman.<section class="profil"> ... </section><h1> - <h6>Judul (Heading). <h1> paling besar/utama.<h1>Target Belajar</h1><p>Paragraf biasa.<p>Ini teks deskripsi.</p><a>Tautan (Link). Atribut target="_blank" buka tab baru.<a href="[https://github.com](https://github.com)">Buka GitHub</a><img>Menampilkan gambar. Wajib pakai src dan alt.<img src="foto.jpg" alt="Foto Profil"><ul> / <ol>Daftar. <ul> (titik/bullet), <ol> (angka 1,2,3).<ul> <li>Item 1</li> </ul>Form Input DasarTag FormFungsiContoh Penggunaan<form>Pembungkus seluruh elemen input.<form> ... </form><label>Teks keterangan untuk kotak input.<label for="nama">Nama:</label><input>Kotak isian.<input type="text" id="nama" name="namaUser"><button>Tombol aksi.<button type="submit">Simpan</button>2. CSS & Visual DesainAturan Emas CSS: Penamaan class itu Case-Sensitive (bedakan huruf besar & kecil)!Properti DasarCSS.nama-class {
    color: #333333; /* Mengubah warna teks */
    background-color: #f4f4f9; /* Mengubah warna latar belakang */
    font-size: 16px; /* Mengubah ukuran huruf */
    font-weight: bold; /* Menebalkan huruf */
    text-align: center; /* Meratakan teks ke tengah */
    border-radius: 8px; /* Melengkungkan sudut kotak */
    box-shadow: 0 4px 8px rgba(0,0,0,0.2); /* Memberi efek bayangan */
}
CSS Box Model (Model Kotak)Browser melihat semua elemen sebagai kotak.padding: Jarak ke dalam (jarak antara teks dengan garis pinggir kardus).margin: Jarak ke luar (jarak kardusmu dengan kardus orang lain).border: Garis pinggir kotaknya (contoh: border: 2px solid blue;).width: Lebar kotak (contoh: width: 100%; untuk lebar penuh).Efek Interaktif (Hover & Focus)CSS/* Efek saat tombol disorot mouse */
button:hover {
    background-color: #2980b9;
    transform: translateY(-3px); /* Tombol seolah naik ke atas (efek 3D) */
    transition: all 0.3s ease; /* Membuat gerakannya mulus, tidak kaku */
}

/* Efek saat kotak input diklik/sedang diketik */
input:focus {
    outline: none;
    border-color: #3498db; /* Garis kotak berubah biru */
}
3. CSS Flexbox (Tata Letak Modern)Digunakan untuk menjajarkan elemen agar rapi tanpa harus menggunakan <br>. Perintah selalu diberikan kepada Bapak Pembungkusnya (Container).CSS.bapak-flexbox {
    display: flex; /* MENGAKTIFKAN SIHIR FLEXBOX */
    
    /* 1. Mengatur Arah Barisan */
    flex-direction: row; /* (Default) Anak berbaris ke samping */
    /* flex-direction: column; -> Anak berbaris dari atas ke bawah */

    /* 2. Mengatur Posisi Horizontal (Kiri-Kanan) */
    justify-content: space-between; /* Disebar rata (mentok kiri & kanan) */
    /* Pilihan lain: center, flex-start, flex-end, space-around */

    /* 3. Mengatur Posisi Vertikal (Atas-Bawah) */
    align-items: center; /* Membuat semua anak sejajar di tengah secara vertikal */

    /* 4. Mengatur Jarak Antar Anak */
    gap: 20px; /* Pengganti margin yang jauh lebih rapi */

    /* 5. Mengizinkan Anak Turun Baris Jika Sempit */
    flex-wrap: wrap; 
}
4. Media Queries (Responsivitas HP)Digunakan untuk menimpa aturan CSS utama ketika layar pengguna mengecil (misalnya dibuka di HP). Kode ini biasanya diletakkan di baris paling bawah pada file style.css.CSS/* Aturan di bawah ini HANYA aktif jika lebar layar maksimal 600px */
@media (max-width: 600px) {
    
    /* Memaksa elemen yang tadinya ke samping, menjadi ke bawah */
    .bapak-flexbox {
        flex-direction: column;
    }

    /* Mengecilkan huruf agar lebih nyaman dibaca di layar kecil */
    h1 {
        font-size: 24px;
    }
}
