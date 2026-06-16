# Product Requirements Document (PRD)

## 1. Ringkasan Produk
FloTest adalah aplikasi web untuk mengelola tes dan soal, serta membantu pengguna mengerjakan tes secara online.

Project menggunakan dummy data dan tidak menggunakan PHP, JavaScript, backend, maupun database.
---

## 2. User

Siapa yang menggunakan produk?

### Admin
Mengelola seluruh:
- Pengguna
- Tes
- Soal

### Mentor
Mengelola:
- Tes miliknya
- Soal pada tes miliknya

### Menti
Mengerjakan tes dan melihat hasil.

---

## 3. Fitur

### Authentication

* Login

### Admin

* Melihat daftar pengguna
* Membuat pengguna
* Mengubah pengguna
* Menghapus pengguna
* Melihat daftar tes
* Membuat tes
* Mengubah tes
* Menghapus tes
* Melihat daftar soal
* Membuat soal
* Mengubah soal
* Menghapus soal

### Mentor

* Melihat daftar tes
* Membuat tes
* Mengubah tes
* Menghapus tes
* Melihat daftar soal
* Membuat soal
* Mengubah soal
* Menghapus soal

### Menti

* Mengerjakan tes
* Melihat hasil

---

## 4. Relationship

- User hanya dapat memiliki 1 role dari Admin, Mentor, atau Menti.
- Mentor memiliki Test.
- Test memiliki Question.
- Menti mengerjakan Test.
- Test menghasilkan Result milik Menti.

---

## 5. Acceptance Criteria

Project dianggap selesai jika:

- Navigasi antar halaman berfungsi
- Setiap fitur user dapat ditampilkan
- Data dummy tampil sesuai kebutuhan halaman
- Form memiliki field sesuai kebutuhan fitur
- Tidak ada halaman kosong