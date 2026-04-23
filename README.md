  | NAMA | NIM | KELAS |
| :--- | :--- | :--- |
| MORENO FERDINAND FARHANTINO | 2409116097 | C`24 |

---
## 📂 WEBSITE PORTOFOLIO
Website ini adalah proyek aplikasi web portofolio statis yang dibangun untuk memenuhi kriteria profesionalisme, estetika modern, dan responsivitas. Menggunakan kombinasi Framework CSS dan JavaScript untuk memberikan pengalaman pengguna yang optimal.

---
## 💻 Teknologi yang Digunakan
Proyek ini mengintegrasikan beberapa teknologi utama untuk mencapai hasil maksimal:
- HTML5: Sebagai fondasi struktur konten website yang semantik.
- CSS3 Custom: Untuk memberikan sentuhan personal seperti gradasi warna (linear-gradient) dan animasi transisi.

### Nilai Tambah
- Bootstrap 5: Digunakan untuk sistem tata letak (Grid System), komponen Card, Navbar, Progress Bar, serta memastikan website sepenuhnya responsif di berbagai perangkat.

- Vue JS 3 (CDN): Digunakan untuk fitur interaktif seperti Data Binding dan Directives (v-for, v-bind), sehingga manajemen data konten menjadi lebih bersih dan terpusat.
---

## 🖥️ Tampilan Setiap Section/Fitur
Website ini terdiri dari beberapa fitur utama yang dirancang:

#### Konfigurasi Head & Meta
* Bagian ini mengatur identitas website, responsivitas layar, serta menghubungkan semua file eksternal

Kode:
```bash
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portofolio | Moreno Ferdinand Farhantino</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="style.css">
```
#### Fitur Navbar
* Menu navigasi yang tetap berada di atas saat layar digulir, memudahkan perpindahan antar section dengan efek bayangan halus.

Kode:
```bash
<nav class="navbar navbar-expand-lg navbar-light bg-white sticky-top shadow-sm">
    <div class="container">
        <a class="navbar-brand fw-bold" href="#">Moreno<span class="text-primary">Porto.</span></a>
        </div>
</nav>
```

#### Section Home
* Area perkenalan utama dengan teks sambutan yang menggunakan gradasi warna dan foto profil yang berukuran besar.

Kode:
```bash
<h1 class="display-3 fw-800 text-dark">Halo, Saya <br>
    <span class="text-gradient">{{ name }}</span>
</h1>
<img :src="profilePic" alt="Foto Profil Moreno" class="img-fluid custom-hero-img shadow-lg">
```

#### Fitur Pengalaman
* Daftar riwayat organisasi yang ditampilkan secara vertikal dengan aksen garis berwarna (border-start) di sisi kiri.

Kode:
```bash
<div v-for="exp in experiences" :key="exp.title" class="experience-item p-3 mb-3 border-start border-4 border-primary bg-white shadow-sm rounded">
    <h6 class="fw-bold mb-1 text-dark">{{ exp.year }}</h6>
    <p class="mb-0 small text-secondary">{{ exp.title }}</p>
</div>
```

#### Fitur My Skills
* Visualisasi keahlian menggunakan bilah progres yang lebarnya bergerak secara dinamis berdasarkan nilai data.

Kode:
```bash
<div class="progress" style="height: 12px;">
    <div class="progress-bar bg-primary-gradient" role="progressbar" 
         :style="{ width: skill.value + '%' }"></div>
</div>
```

#### Footer
* Bagian akhir website yang menampilkan informasi hak cipta.

Kode:
```bash
<footer class="bg-dark text-white py-5 text-center">
    <h5 class="fw-bold mb-3">{{ name }}</h5>
    <p class="small opacity-75 mb-0">&copy; 2026. Dibuat oleh Moreno Ferdinand Farhantino.</p>
</footer>
```

### Nilai Tambah
#### Section About Me
* Berisi deskripsi profil diri yang dipanggil secara reaktif menggunakan Vue JS.

Kode:
```bash
<div class="col-md-6">
    <h3 class="h4 fw-bold mb-3"><i class="fas fa-user-circle text-primary me-2"></i>Siapa Saya?</h3>
    <p class="text-secondary text-justify">{{ aboutMeText }}</p>
</div>
```
#### Section Certificates
* Galeri sertifikat yang disusun rapi dalam sistem grid Bootstrap 3 kolom.

Kode:
```bash
<div class="col-md-4" v-for="(cert, index) in certificates" :key="index">
    <div class="card h-100 border-0 shadow-sm custom-card">
        <img :src="cert.image" class="card-img-top">
        <div class="card-body text-center">
            <h5 class="card-title fw-bold text-primary">{{ cert.title }}</h5>
        </div>
    </div>
</div>
```
#### Konfigurasi Vue JS (Script)
* Logika utama untuk mengatur semua data teks dan gambar agar website bersifat statis namun mudah dikelola.

Kode:
```bash
createApp({
    data() {
        return {
            name: 'Moreno Ferdinand Farhantino',
            experiences: [...],
            skills: [...],
            certificates: [...]
        }
    }
}).mount('#app')
```

## Lampiran
* Tampilan Home:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dbbd0adc-a8fd-4386-8ff5-9a9386a189fc" />

* Tampilan About Me:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/58cb8fb5-2371-46ef-9f8f-fc96fd9bf904" />

* Tampilan Certificates:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a8194fde-84e3-4a1c-8b5e-5a707f4c3d2b" />


