# 📚 Perpustakaan Digital: Manajemen Koleksi Buku Modern 🚀

![Perpustakaan Digital Banner](https://placehold.co/1200x400/282c34/ffffff?text=Perpustakaan+Digital+Modern)

Sebuah aplikasi web *full-stack* yang dirancang dengan indah dan fungsional untuk mengelola koleksi buku dan data penulis Anda secara efisien. Proyek ini dibangun di atas arsitektur yang modular dan skalabel, memanfaatkan kekuatan React.js untuk antarmuka pengguna yang dinamis, Pyramid (Python) untuk logika bisnis yang kokoh, dan PostgreSQL sebagai tulang punggung basis data yang andal.

---

## 📖 Daftar Isi

1.  [✨ Sekilas Proyek](#-sekilas-proyek)
2.  [🚀 Fitur Unggulan](#-fitur-unggulan)
3.  [🛠️ Teknologi yang Digunakan](#-teknologi-yang-digunakan)
4.  [🏗️ Arsitektur Sistem](#-arsitektur-sistem)
5.  [⚙️ Penyiapan & Menjalankan Aplikasi](#-penyiapan-menjalankan-aplikasi)
    * [✅ Prasyarat](#-prasyarat)
    * [🐘 Penyiapan Database PostgreSQL](#-penyiapan-database-postgresql)
    * [🐍 Penyiapan Backend (Pyramid)](#-penyiapan-backend-pyramid)
    * [⚛️ Penyiapan Frontend (React JS)](#-penyiapan-frontend-react-js)
6.  [💡 Cara Menggunakan Aplikasi](#-cara-menggunakan-aplikasi)
    * [Autentikasi (Login)](#autentikasi-login)
7.  [📈 Pengembangan Lebih Lanjut](#-pengembangan-lebih-lanjut)

---

## 1. ✨ Sekilas Proyek

"Perpustakaan Digital" adalah aplikasi web interaktif yang merevolusi cara Anda mengelola koleksi buku dan informasi detail penulis. Dengan antarmuka yang intuitif, aplikasi ini memungkinkan Anda untuk melakukan operasi **CRUD (Create, Read, Update, Delete)** dengan mudah pada entitas buku dan penulis. Baik untuk koleksi pribadi, perpustakaan kecil, atau sebagai fondasi proyek yang lebih besar, aplikasi ini menawarkan solusi manajemen data yang terorganisir, efisien, dan modern. Ini juga merupakan showcase kemampuan pengembangan *full-stack* menggunakan teknologi terkini.

---

## 2. 🚀 Fitur Unggulan

Aplikasi ini dilengkapi dengan serangkaian fitur inti yang dirancang untuk manajemen data yang komprehensif dan pengalaman pengguna yang optimal:

* ### **Manajemen Buku:**
    * **Daftar Koleksi:** Lihat daftar lengkap semua buku Anda, lengkap dengan judul, ISBN, tahun publikasi, dan nama penulis.
    * **Tambah Buku Baru:** Masukkan detail buku baru dengan mudah melalui formulir yang ramah pengguna. Anda dapat memilih penulis yang sudah ada atau menambahkan penulis baru secara langsung.
    * **Edit Detail Buku:** Perbarui informasi buku yang ada, seperti judul, ISBN, tahun, atau kaitkan dengan penulis yang berbeda.
    * **Hapus Buku:** Hapus buku dari koleksi Anda, menjaga daftar tetap relevan dan terkini.

* ### **Manajemen Penulis:**
    * **Daftar Penulis:** Jelajahi daftar semua penulis yang terdaftar dalam sistem, dengan nama dan biografi singkat.
    * **Tambah Penulis Baru:** Tambahkan data penulis baru dengan cepat, termasuk nama dan biografi.
    * **Edit Detail Penulis:** Perbarui informasi penulis yang ada kapan saja.
    * **Hapus Penulis:** Hapus data penulis dari sistem. (Catatan: Penghapusan mungkin dibatasi jika ada buku yang masih terkait).

* ### **Antarmuka Responsif:**
    * Dirancang dengan prinsip *responsive design* untuk memastikan tampilan dan fungsionalitas yang mulus di berbagai perangkat: desktop 🖥️, tablet 📱, dan ponsel 🤳.

* ### **API RESTful:**
    * Komunikasi yang bersih dan efisien antara *frontend* dan *backend* melalui *endpoint* API RESTful, memungkinkan pengembangan independen dan fleksibilitas.

* ### **Autentikasi Dasar (JWT):**
    * Sistem login dasar menggunakan **JSON Web Tokens (JWT)** untuk mengamankan akses ke fitur manajemen data. Hanya pengguna terautentikasi yang dapat melakukan operasi CRUD, memberikan lapisan keamanan awal.

## 3. 🛠️ Teknologi yang Digunakan

Proyek ini dibangun di atas fondasi teknologi *open-source* yang kuat dan teruji:

### **Frontend:**
* **React.js**: Library JavaScript terkemuka untuk membangun antarmuka pengguna berbasis komponen yang dinamis dan reaktif.
* **Tailwind CSS**: *Utility-first CSS framework* yang mempercepat *styling* dan memungkinkan kustomisasi desain yang sangat fleksibel.
* **React Router DOM**: Untuk manajemen *routing* di sisi klien, memastikan navigasi antar halaman yang mulus.
* **Axios**: Klien HTTP berbasis *Promise* untuk *request* API yang efisien dan penanganan *interceptor* yang berguna.
* **Font Awesome**: Koleksi ikon vektor yang dapat diskalakan untuk estetika UI yang lebih baik.

### **Backend:**
* **Python**: Bahasa pemrograman utama, dipilih karena keserbagunaan, keterbacaan, dan ekosistem *library* yang kaya.
* **Pyramid**: *Framework* web Python yang fleksibel dan minimalis, memungkinkan pembangunan aplikasi *scalable* dengan komponen yang dipilih.
* **SQLAlchemy**: *Object Relational Mapper* (ORM) yang kuat, menyediakan cara elegan untuk berinteraksi dengan database menggunakan objek Python.
* **PostgreSQL**: Sistem manajemen basis data relasional *open-source* yang sangat andal, *powerful*, dan *scalable* untuk integritas data.
* **JWT (PyJWT)**: *Library* Python untuk implementasi *JSON Web Tokens* guna mengamankan komunikasi API dan mengelola sesi pengguna secara *stateless*.
* **Passlib**: *Library* komprehensif untuk *hashing password* yang aman, memastikan *password* pengguna tersimpan terenkripsi.
* **Waitress**: *WSGI server* yang ringan dan *production-ready* untuk Python, digunakan untuk menjalankan aplikasi Pyramid.

## 4. 🏗️ Arsitektur Sistem

Aplikasi ini mengadopsi arsitektur *Client-Server* yang terpisah (*decoupled*), di mana *frontend* dan *backend* beroperasi sebagai entitas yang independen namun saling berkomunikasi secara harmonis:

* **Frontend (React.js):**
    * Berfungsi sebagai lapisan *client-side* yang berjalan di *browser* pengguna.
    * Bertanggung jawab untuk rendering antarmuka pengguna (UI) dan semua interaksi visual.
    * Memuat data dari *backend* dan menampilkannya secara dinamis.

* **Backend (Pyramid/Python):**
    * Berjalan sebagai *server* aplikasi.
    * Menangani semua logika bisnis inti, termasuk validasi data, pemrosesan permintaan, dan manajemen sesi (melalui JWT).
    * Mengekspos *endpoint* API RESTful yang dapat diakses oleh *frontend*.

* **API RESTful:**
    * Jembatan komunikasi antara *frontend* dan *backend*.
    * *Frontend* mengirimkan permintaan HTTP (GET, POST, PUT, DELETE) ke *endpoint* API di *backend*.
    * *Backend* merespons dengan data dalam format JSON.
    * Pemisahan ini memungkinkan pengembangan paralel dan *deployment* yang fleksibel.

* **PostgreSQL:**
    * Database relasional yang berfungsi sebagai penyimpanan data persisten untuk seluruh aplikasi.
    * *Backend* berinteraksi dengan PostgreSQL menggunakan SQLAlchemy ORM untuk menyimpan dan mengambil data buku, penulis, dan pengguna.

[Image of Diagram Arsitektur Sistem]

*Diagram di atas menggambarkan aliran data dan interaksi antar komponen dalam arsitektur sistem ini.*

## 5. ⚙️ Penyiapan & Menjalankan Aplikasi

Ikuti langkah-langkah detail di bawah ini untuk menyiapkan dan menjalankan aplikasi di lingkungan lokal Anda.

### ✅ Prasyarat

Pastikan Anda telah menginstal *software* berikut di sistem Anda:

* **Python 3.8+**: Unduh dari [python.org](https://www.python.org/downloads/).
* **Node.js & npm** (atau yarn): Unduh dari [nodejs.org](https://nodejs.org/en/download/). `npm` (Node Package Manager) akan terinstal bersama Node.js.
* **PostgreSQL**: Unduh dari [postgresql.org/download/](https://www.postgresql.org/download/). Pastikan server PostgreSQL berjalan di `localhost:5432`.

### 🐘 Penyiapan Database PostgreSQL

1.  **Buat Database dan Pengguna:**
    Buka terminal PostgreSQL (misalnya `psql` atau melalui `pgAdmin`) dan jalankan perintah SQL berikut untuk membuat database dan pengguna baru yang akan digunakan oleh aplikasi Anda:

    ```sql
    CREATE DATABASE library_db;
    CREATE USER myuser WITH PASSWORD 'mypassword'; -- ⚠️ Ganti 'myuser' dan 'mypassword' dengan kredensial yang KUAT dan UNIK.
    GRANT ALL PRIVILEGES ON DATABASE library_db TO myuser;
    ```

    **PENTING:** Pastikan kredensial (`myuser`, `mypassword`) yang Anda buat ini sesuai dengan yang akan Anda konfigurasi di file `backend/development.ini`.

### 🐍 Penyiapan Backend (Pyramid)

1.  **Kloning Repositori:**
    Jika Anda belum mengkloning proyek, lakukan ini. Kemudian navigasikan ke direktori `backend`:

    ```bash
    git clone <URL_REPOSITORI_ANDA> # ➡️ Ganti dengan URL repositori GitHub Anda
    cd perpustakaan-digital/backend
    ```

2.  **Buat dan Aktifkan Lingkungan Virtual:**
    Sangat disarankan untuk menggunakan *virtual environment* untuk mengisolasi dependensi proyek:

    ```bash
    python -m venv venv
    # 🐧 Di Linux/macOS
    source venv/bin/activate
    # 🪟 Di Windows
    venv\Scripts\activate
    ```

3.  **Instal Dependensi Python:**
    Instal semua *library* Python yang dibutuhkan oleh *backend* dari `requirements.txt`:

    ```bash
    pip install -r requirements.txt
    ```

4.  **Konfigurasi Database:**
    Buka file `backend/development.ini` dengan editor teks Anda. Perbarui baris `sqlalchemy.url` agar sesuai dengan kredensial PostgreSQL yang Anda buat sebelumnya:

    ```ini
    sqlalchemy.url = postgresql+pg8000://myuser:mypassword@localhost:5432/library_db
    ```

    (Pastikan Anda mengganti `myuser` dan `mypassword` dengan kredensial aktual Anda).

5.  **Inisialisasi Database (Membuat Tabel dan Pengguna Admin Default):**
    Jalankan *script* `create_tables.py` untuk membuat skema database (tabel `books`, `authors`, `users`) dan menambahkan pengguna `admin` default:

    ```bash
    python create_tables.py
    ```

    * Anda akan melihat pesan konfirmasi di terminal bahwa tabel telah dibuat dan pengguna 'admin' telah ditambahkan dengan *password* default 'admin_password_kuat'.
    * **PENTING:** Demi keamanan, sangat disarankan untuk mengganti *password* ini setelah login pertama kali di aplikasi Anda.

6.  **Jalankan Server Backend:**
    Setelah semua dependensi terinstal dan database terinisialisasi, Anda dapat menjalankan server *backend* Pyramid:

    ```bash
    pserve development.ini
    ```
    _Backend_ akan berjalan dan mendengarkan permintaan di `http://localhost:6543`. Biarkan terminal ini tetap terbuka dan berjalan.

### ⚛️ Penyiapan Frontend (React JS)

1.  **Navigasi ke Folder Frontend:**
    Buka terminal baru (terpisah dari terminal _backend_) dan navigasi ke folder `frontend` proyek Anda:

    ```bash
    cd ../frontend
    ```

2.  **Instal Dependensi Node.js:**
    Instal semua *library* JavaScript yang dibutuhkan oleh _frontend_ dari `package.json`:

    ```bash
    npm install
    ```

3.  **Jalankan Aplikasi Frontend:**
    Setelah dependensi terinstal, jalankan aplikasi _frontend_ React:

    ```bash
    npm start
    ```
    _Frontend_ akan berjalan di `http://localhost:3000` (atau port lain jika 3000 sudah digunakan). _Browser_ Anda seharusnya akan otomatis terbuka ke alamat ini.

---

## 6. 💡 Cara Menggunakan Aplikasi

Setelah kedua server (*backend* dan *frontend*) berhasil berjalan:

1.  Buka _browser_ web Anda dan navigasi ke: `http://localhost:3000`

2.  Anda akan melihat halaman login. Gunakan kredensial default yang dibuat oleh `create_tables.py`:

### Autentikasi (Login)

Untuk mengakses fitur manajemen buku dan penulis, Anda perlu login.

* **Username Default:** `admin`
* **Password Default:** `admin_password_kuat` (atau *password* yang Anda tentukan jika Anda mengubahnya di _script_ `create_tables.py`)

3.  Setelah login berhasil, Anda dapat menavigasi ke halaman "Buku" atau "Penulis" melalui _navbar_ untuk mulai mengelola data koleksi Anda.

---

## 7. 📈 Pengembangan Lebih Lanjut

Proyek ini menyediakan fondasi yang kuat dan dapat diperluas. Beberapa ide untuk pengembangan dan peningkatan di masa mendatang meliputi:

* **Autentikasi yang Lebih Kuat:** Implementasi fitur *refresh token* untuk memperpanjang sesi tanpa login ulang, *token blacklisting* untuk membatalkan *token* yang dicuri, atau integrasi dengan penyedia identitas eksternal menggunakan OAuth/OpenID Connect.

* **Validasi Input yang Komprehensif:** Menambahkan validasi yang lebih ketat di sisi _backend_ dan _frontend_ untuk semua _input_ pengguna, termasuk validasi format (misal: ISBN), panjang karakter, dan tipe data, untuk meningkatkan integritas data dan keamanan.

* **Penanganan Error yang Lebih Baik:** Mengimplementasikan tampilan _error_ yang lebih ramah pengguna di _frontend_ (misal: modal _error_ yang informatif) dan sistem _logging error_ yang lebih canggih di _backend_ untuk memudahkan _debugging_ di lingkungan produksi.

* **Unit Testing yang Menyeluruh:** Menulis lebih banyak _unit test_ untuk _backend_ (Pyramid) dan _frontend_ (React) untuk mencapai cakupan kode yang lebih tinggi, memastikan keandalan dan mempermudah _refactoring_.

* **Peningkatan UI/UX:** Peningkatan tampilan dan rasa aplikasi dengan desain yang lebih kompleks, animasi, dan interaksi yang lebih halus untuk pengalaman pengguna yang lebih menyenangkan.

* **Paginasian & Pencarian:** Mengimplementasikan fitur paginasi untuk mengelola daftar buku/penulis yang sangat besar secara efisien, serta fitur pencarian dan _filtering_ yang kuat untuk memudahkan penemuan data.

* **Deployment:** Mengembangkan strategi _deployment_ yang robust untuk membawa aplikasi dari lingkungan pengembangan ke server produksi (misal: menggunakan Docker, Nginx/Gunicorn, atau layanan _cloud_).

* **Fitur Peminjaman/Pengembalian:** Menambahkan entitas dan logika baru untuk melacak status peminjaman dan pengembalian buku, termasuk tanggal peminjaman, tanggal jatuh tempo, dan peminjam.

* **Relasi Antar Entitas:** Jika ada entitas lain yang ingin ditambahkan (misal: Kategori, Peminjam), pastikan relasinya ditangani dengan baik di model database dan logika aplikasi.
