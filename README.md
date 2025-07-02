# Aplikasi Pendaftaran Mahasiswa Baru - Tech Edition

Aplikasi web untuk pendaftaran mahasiswa baru dengan tampilan modern teknologis. Aplikasi ini menggunakan **Python Flask** sebagai backend dan **MySQL** sebagai database.

## 📸 Screenshot Aplikasi


Form Pendaftaran
![image](https://github.com/user-attachments/assets/d8009b4d-f100-460e-bef5-2ef4a611a339)

Halaman Sukses
![image](https://github.com/user-attachments/assets/4a40fa50-4d33-4d34-bb8b-983ff6f5b28a)

Daftar Siswa
![image](https://github.com/user-attachments/assets/1ca94cf0-2027-4275-a75c-4089ddf68c62)

![Panel Admin]
![image](https://github.com/user-attachments/assets/1f772332-c30c-479d-abf9-373c03964392)

## 🚀 Teknologi yang Digunakan

- **Backend:** Python 3 dengan framework Flask
- **Database:** MySQL
- **Frontend:** HTML5, CSS3
- **Font:** Google Fonts (Outfit, Rajdhani)
- **Efek Visual:** CSS Animations, Gradients, Glassmorphism
- **File Upload:** Handling dan penyimpanan foto profil mahasiswa

## 📋 Prasyarat

Sebelum menjalankan aplikasi, pastikan Anda memiliki:

1. Python 3.7+ terinstall
2. MySQL Server (bisa melalui XAMPP, WAMP, atau instalasi langsung)
3. Pip (Python package manager)

## 💻 Instalasi

### 1. Clone atau Download Repository

```bash
git clone [url-repository] 
# atau download ZIP dan ekstrak
```

### 2. Setup Database

1. Jalankan MySQL Server
2. Buka phpMyAdmin atau MySQL CLI
3. Import file SQL dari folder database:

```bash
mysql -u root -p < database/setup.sql
```

Atau melalui phpMyAdmin:
- Buka http://localhost/phpmyadmin
- Buat database baru bernama `db_pendaftaran_maba`
- Import file `database/setup.sql`

### 3. Setup Virtual Environment

```bash
# Buat virtual environment
python -m venv venv

# Aktifkan virtual environment
# Untuk Windows
venv\Scripts\activate
# Untuk MacOS/Linux
source venv/bin/activate

# Install dependensi
pip install -r requirements.txt
```

### 4. Konfigurasi Database

Edit file `config/database.py` sesuai dengan konfigurasi MySQL Anda:

```python
DB_CONFIG = {
    'host': 'localhost',
    'database': 'db_pendaftaran_maba',
    'user': 'root',  # Sesuaikan dengan username MySQL Anda
    'password': ''   # Sesuaikan dengan password MySQL Anda
}
```

### 5. Siapkan Folder Upload

Aplikasi memerlukan folder untuk menyimpan foto yang diunggah:

```bash
# Pastikan folder uploads sudah ada
mkdir -p static/uploads

# Letakkan gambar default.jpg di folder uploads
# Atau aplikasi akan membuat file default secara otomatis
```

## 🔧 Menjalankan Aplikasi

1. Pastikan virtual environment aktif
2. Pastikan MySQL server berjalan
3. Jalankan aplikasi:

```bash
python app.py
```

4. Buka browser dan akses:
   - Form Pendaftaran: http://localhost:5000/
   - Daftar Siswa: http://localhost:5000/daftar-siswa
   - Panel Admin: http://localhost:5000/admin/pendaftar

## 📁 Struktur Proyek

```
/project-root
│
├── /app                # Folder utama aplikasi
│   ├── __init__.py     # File inisialisasi aplikasi
│   ├── config.py       # Konfigurasi aplikasi
│   ├── models.py       # Definisi model database
│   ├── routes.py       # Definisi route/endpoint
│   └── templates/      # Folder untuk file HTML
│
├── /static             # Folder untuk file statis
│   ├── /css             # File CSS
│   ├── /js              # File JavaScript
│   └── /images          # Gambar
│
├── /database            # Folder untuk file database
│   └── setup.sql       # Script untuk setup database
│
├── requirements.txt     # Daftar dependensi Python
└── run.py              # File untuk menjalankan aplikasi
```



