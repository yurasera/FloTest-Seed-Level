# Mapping FloTest

Aplikasi web untuk membuat dan mengerjakan tes secara online.

## Tujuan

- Mentor membuat soal dan tes.
- Menti mengerjakan tes.
- Admin mengelola seluruh sistem.

---

# Level User

## 1. Admin

Mengelola seluruh sistem.

### Fitur

- Login
- Dashboard statistik
- Kelola Mentor
- Kelola Menti
- Reset Password User
- Melihat Semua Soal
- Melihat Semua Hasil Tes
- Menonaktifkan Akun
- Mengatur Kategori Soal

---

## 2. Mentor

Membuat dan mengelola tes.

### Fitur

- Login
- Dashboard Mentor
- Membuat Tes
- Edit Tes
- Hapus Tes
- Membuat Soal
- Edit Soal
- Hapus Soal
- Menentukan Durasi Tes
- Menentukan Nilai Kelulusan
- Melihat Hasil Menti
- Memberikan Feedback

---

## 3. Menti

Mengerjakan tes yang diberikan mentor.

### Fitur

- Login
- Dashboard Menti
- Melihat Daftar Tes
- Mengerjakan Tes
- Submit Jawaban
- Melihat Nilai
- Melihat Feedback Mentor
- Melihat Riwayat Tes

---

# Alur Sistem

## Mentor Membuat Tes

```text
Login
 ↓
Buat Tes
 ↓
Tambah Soal
 ↓
Publish Tes
```

### Contoh

```text
Tes: Laravel Basic

Soal:
Apa fungsi Migration pada Laravel?

A. Routing
B. Database Versioning
C. Middleware
D. Authentication
```

---

## Menti Mengerjakan Tes

```text
Login
 ↓
Pilih Tes
 ↓
Jawab Soal
 ↓
Submit
 ↓
Lihat Hasil
```

---

# Hak Akses (Role Permission)

| Fitur | Admin | Mentor | Menti |
|---------|---------|---------|---------|
| Login | ✅ | ✅ | ✅ |
| Kelola User | ✅ | ❌ | ❌ |
| Buat Tes | ❌ | ✅ | ❌ |
| Edit Tes | ❌ | ✅ | ❌ |
| Hapus Tes | ❌ | ✅ | ❌ |
| Buat Soal | ❌ | ✅ | ❌ |
| Edit Soal | ❌ | ✅ | ❌ |
| Hapus Soal | ❌ | ✅ | ❌ |
| Kerjakan Tes | ❌ | ❌ | ✅ |
| Lihat Nilai Sendiri | ❌ | ❌ | ✅ |
| Lihat Hasil Semua Menti | ✅ | ✅ | ❌ |
| Kelola Kategori Soal | ✅ | ❌ | ❌ |

---

# Struktur Database

## users

| Field | Type |
|---------|---------|
| id | bigint |
| name | varchar |
| email | varchar |
| password | varchar |
| role | enum |

### Role

```text
admin
mentor
menti
```

---

## tests

| Field | Type |
|---------|---------|
| id | bigint |
| title | varchar |
| description | text |
| mentor_id | bigint |
| duration | integer |
| passing_score | integer |
| status | enum |

---

## questions

| Field | Type |
|---------|---------|
| id | bigint |
| test_id | bigint |
| question | text |
| type | enum |

---

## options

| Field | Type |
|---------|---------|
| id | bigint |
| question_id | bigint |
| option_text | text |
| is_correct | boolean |

---

## submissions

| Field | Type |
|---------|---------|
| id | bigint |
| test_id | bigint |
| menti_id | bigint |
| score | integer |
| submitted_at | datetime |

---

## answers

| Field | Type |
|---------|---------|
| id | bigint |
| submission_id | bigint |
| question_id | bigint |
| selected_option_id | bigint |

---

# Dashboard

## Admin Dashboard

Menampilkan:

- Total Mentor
- Total Menti
- Total Tes
- Total Soal
- Total Submission

---

## Mentor Dashboard

Menampilkan:

- Jumlah Tes Dibuat
- Jumlah Soal Dibuat
- Jumlah Menti Mengikuti Tes
- Rata-rata Nilai Menti

---

## Menti Dashboard

Menampilkan:

- Tes Tersedia
- Tes Selesai
- Nilai Terbaik
- Riwayat Tes

---

# Arsitektur Sederhana

```text
Admin
   │
Mentor
   │
Menti
   │
Frontend (Web)
   │
Backend (Laravel)
   │
Database (MySQL)
```

---

# Konsep yang Dipelajari

Melalui FloTest, mentee dapat memahami:

- Authentication
- Authorization
- Role Based Access Control (RBAC)
- CRUD
- Relasi Database
- Client Server Architecture
- MVC Pattern
- REST API
- Dashboard dan Reporting