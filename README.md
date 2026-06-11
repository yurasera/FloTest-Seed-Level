# Product Requirements Document (PRD)

# FloTest (HTML & CSS MVP)

## 1. Ringkasan Produk

FloTest adalah aplikasi web untuk membantu mentor membuat tes dan membantu menti mengerjakan tes secara online.

Project ini dibuat untuk mempelajari HTML dan CSS. Seluruh data masih berupa data statis (dummy data) dan belum menggunakan backend maupun database.

---

## 2. Tujuan Pembelajaran

Mentee diharapkan memahami:

* Struktur HTML
* Semantic HTML
* Layouting
* Navigation
* Form
* Table
* Card Component
* Styling menggunakan CSS
* Struktur folder project

---

## 3. User

### Admin

Mengelola pengguna dan memantau seluruh tes.

### Mentor

Membuat dan mengelola tes.

### Menti

Mengerjakan tes dan melihat hasil.

---

## 4. Sitemap

```text
Login
│
├── Dashboard Admin
│
├── Dashboard Mentor
│   ├── Daftar Tes Mentor
│   └── Form Buat Tes
│
└── Dashboard Menti
    ├── Kerjakan Tes
    └── Hasil Tes
```

---

## 5. Halaman yang Harus Dibuat

### 1. Login Page

Menampilkan:

* Logo FloTest
* Input Email
* Input Password
* Tombol Login

---

### 2. Dashboard Admin

Menampilkan:

* Total Mentor
* Total Menti
* Total Tes

Menu:

* Mentor
* Menti
* Tes

---

### 3. Dashboard Mentor

Menampilkan:

* Jumlah Tes
* Jumlah Soal

Menu:

* Daftar Tes
* Buat Tes

---

### 4. Daftar Tes Mentor

Menampilkan tabel:

| Judul Tes | Status | Jumlah Soal |
| --------- | ------ | ----------- |

Status:

* Draft
* Published
* Archived

Contoh data:

| Judul Tes              | Status    | Jumlah Soal |
| ---------------------- | --------- | ----------- |
| HTML Basic Test        | Published | 10          |
| CSS Basic Test         | Draft     | 8           |
| Responsive Design Test | Archived  | 15          |

---

### 5. Form Buat Tes

Field:

* Judul Tes
* Deskripsi Tes
* Status

Pilihan Status:

* Draft
* Published
* Archived

Tombol:

* Simpan

---

### 6. Dashboard Menti

Menampilkan:

* Tes Tersedia
* Tes Selesai

Menu:

* Kerjakan Tes
* Hasil Tes

---

### 7. Halaman Kerjakan Tes

Menampilkan:

Nama Tes:

```text
HTML Basic Test
```

Pertanyaan:

```text
Apa fungsi HTML?
```

Pilihan:

```text
( ) A. HyperText Markup Language
( ) B. HyperText Markdown Language
( ) C. HighText Machine Language
( ) D. Home Tool Markup Language
```

Tombol:

* Sebelumnya
* Selanjutnya
* Submit

---

### 8. Halaman Hasil Tes

Menampilkan:

```text
Nilai: 80
```

Daftar soal:

```text
✓ Jawaban Anda: A
✓ Jawaban Benar: A
```

---

## 6. Data Dummy

### User

* 1 Admin
* 2 Mentor
* 5 Menti

### Tes

* HTML Basic Test
* CSS Basic Test
* Responsive Design Test

### Status Tes

* Draft
* Published
* Archived

---

## 7. Batasan Project

* Tidak menggunakan PHP
* Tidak menggunakan Database
* Tidak menggunakan JavaScript
* Tidak ada autentikasi sungguhan
* Tidak ada penyimpanan data
* Tidak ada perhitungan nilai otomatis
* Semua data menggunakan dummy data

---

## 8. Deliverables

Mentee berhasil membuat:

* 8 halaman HTML
* CSS eksternal
* Navigasi antar halaman
* Struktur folder yang rapi
* Dummy data yang konsisten

---

## 9. Acceptance Criteria

Project dianggap selesai jika:

* Semua halaman dapat dibuka
* Semua navigasi antar halaman berfungsi
* Menggunakan semantic HTML
* Menggunakan CSS eksternal
* Tidak menggunakan inline CSS
* Struktur folder project rapi
* Seluruh halaman menggunakan dummy data yang konsisten

---

## 10. Struktur Folder

```text
flotest/
│
├── index.html
│
├── admin/
│   └── dashboard.html
│
├── mentor/
│   ├── dashboard.html
│   ├── tests.html
│   └── create-test.html
│
├── menti/
│   ├── dashboard.html
│   ├── take-test.html
│   └── result.html
│
└── assets/
│   ├── css/style.css
    └── images/
```
