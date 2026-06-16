# Architecture

# FloTest (HTML & CSS MVP)

## 1. Scope

Menggunakan:
* HTML
* CSS
* Dummy Data

Tidak menggunakan:
* PHP
* JavaScript
* Backend
* Database

---

## 2. Struktur Folder

Folder dipisahkan berdasarkan role pengguna.
Question merupakan bagian dari Test.

```text
flotest/
│
├── index.html
│
├── admin/
│   ├── dashboard.html
│   │
│   ├── users/
│   │   ├── index.html
│   │   ├── create.html
│   │   └── edit.html
│   │
│   ├── tests/
│   │   ├── index.html
│   │   ├── create.html
│   │   ├── edit.html
│   │   └── questions/
│   │       ├── index.html
│   │       ├── create.html
│   │       └── edit.html
│
├── mentor/
│   ├── dashboard.html
│   │
│   └── tests/
│       ├── index.html
│       ├── create.html
│       ├── edit.html
│       └── questions/
│           ├── index.html
│           ├── create.html
│           └── edit.html
│
├── menti/
│   ├── dashboard.html
│   ├── take-test.html
│   └── result.html
│
└── assets/
    ├── css/
    │   └── style.css
    └── images/
```

### Sitemap

```text
Login
├── Dashboard Admin
│   ├── Users
│   └── Tests
│       └── Questions
├── Dashboard Mentor
│   └── Tests
│       └── Questions
└── Dashboard Menti
```

---

## 3. Layout

Semua halaman menggunakan layout yang konsisten.

```html
<header>
    <nav></nav>
</header>

<main>
    <section></section>
</main>

<footer></footer>
```

---

## 4. CSS Structure

```text
style.css
├── Reset
├── Global
├── Layout
├── Components
└── Utilities
```

## 5. Naming Convention

File:
- lowercase
- gunakan tanda hubung (-)

Contoh:
dashboard.html
create-test.html

CSS:
Gunakan nama class yang deskriptif.

Contoh:
.card
.btn-primary
.form-group

---

## 6. Definition of Done

Architecture dianggap selesai jika:

* Struktur folder final
* Struktur halaman final
* Relationship antar resource terdefinisi
* Layout global terdefinisi
* Struktur CSS terdefinisi
* Siap masuk ke tahap implementation
