# To-Do List Kelompok

Aplikasi web **To-Do List** sederhana: pengguna mengetik tugas, menekan tombol **Tambah**, lalu tugas muncul di daftar. Proyek ini dibuat dalam satu sprint Scrum (45 menit) pada praktikum Rekayasa Perangkat Lunak (RPL) tentang **Scrum dengan Git & GitHub**.

Aplikasi dibangun dengan HTML, CSS, dan JavaScript murni (tanpa framework) agar fokus praktikum tetap pada proses Scrum dan kolaborasi Git.

## Fitur

- Menambahkan tugas lewat kotak isian dan tombol **Tambah** (tugas kosong diabaikan)
- Menandai tugas selesai dengan sekali klik (teks tercoret)
- Menghapus tugas dengan klik dua kali
- Menampilkan jumlah tugas secara otomatis
- Tampilan sederhana dan rapi

## Cara Menjalankan

Tidak perlu instalasi apa pun.

1. Clone repository ini:
   ```bash
   git clone https://github.com/<username-SM>/todo-kelompok-<nomor>.git
   cd todo-kelompok-<nomor>
   ```
2. Buka file `index.html` di browser (klik dua kali atau seret ke jendela browser).
3. Ketik tugas, lalu klik **Tambah**.

## Cara Penggunaan

| Aksi | Hasil |
|------|-------|
| Ketik tugas lalu klik **Tambah** | Tugas masuk ke daftar |
| Klik satu kali pada tugas | Tugas ditandai selesai (tercoret) |
| Klik dua kali pada tugas | Tugas dihapus dari daftar |

## Struktur Proyek

```
todo-kelompok-<nomor>/
├── index.html   # Halaman utama (US-1)
├── script.js    # Tambah tugas & tandai selesai (US-2)
├── style.css    # Tampilan (US-3)
├── hapus.js     # Hapus tugas dengan klik dua kali (US-5)
├── hitung.js    # Menghitung jumlah tugas (US-6)
└── README.md    # Dokumentasi proyek (US-4)
```

### ID Elemen HTML yang Dipakai Bersama

| ID | Fungsi |
|----|--------|
| `inputTugas` | Kotak isian tugas |
| `btnTambah` | Tombol Tambah |
| `daftarTugas` | Daftar tugas (`<ul>`) |
| `jumlahTugas` | Teks jumlah tugas |

## Anggota Tim dan Peran

Kelompok: **<nama kelompok>** · Kelas: **<kelas>**

| Peran | Nama | Tugas (User Story) | Branch |
|-------|------|--------------------|--------|
| Product Owner | <nama> | US-4: `README.md` | `fitur/us-4-readme` |
| Scrum Master | <nama> | US-1: `index.html` | `fitur/us-1-halaman` |
| Developer 1 | <nama> | US-2: `script.js` | `fitur/us-2-tambah-tugas` |
| Developer 2 | <nama> | US-3: `style.css` | `fitur/us-3-tampilan` |
| Developer 3 | <nama> | US-5: `hapus.js` | `fitur/us-5-hapus-tugas` |
| Developer 4 | <nama> | US-6: `hitung.js` | `fitur/us-6-jumlah-tugas` |

## Product Backlog

| ID | User Story | Status |
|----|------------|--------|
| US-1 | Sebagai pengguna, saya ingin melihat halaman berisi judul, kotak isian, dan tombol Tambah, agar bisa menulis tugas. | ✅ |
| US-2 | Sebagai pengguna, saya ingin menambahkan tugas ke daftar dan menandainya selesai, agar bisa mencatat pekerjaan. | ✅ |
| US-3 | Sebagai pengguna, saya ingin tampilan yang rapi dan tugas selesai tercoret, agar nyaman dibaca. | ✅ |
| US-4 | Sebagai pengembang, saya ingin README yang menjelaskan aplikasi dan anggota tim, agar proyek mudah dipahami orang lain. | ✅ |
| US-5 | Sebagai pengguna, saya ingin menghapus tugas dengan klik dua kali, agar daftar tidak penuh tugas lama. | ✅ |
| US-6 | Sebagai pengguna, saya ingin melihat jumlah tugas di daftar, agar tahu berapa banyak pekerjaan saya. | ✅ |

> Ganti ☐ dengan ✅ untuk user story yang dinyatakan **selesai** saat Sprint Review.

## Definition of Done

Sebuah user story dianggap selesai jika memenuhi poin berikut:

- [ ] Aplikasi bisa dibuka di browser
- [ ] Tugas bisa ditambahkan
- [ ] Tugas yang diklik tercoret
- [ ] Tugas bisa dihapus dengan klik dua kali
- [ ] Jumlah tugas tampil
- [ ] Tampilan rapi
- [ ] README menjelaskan aplikasi

## Alur Kerja Git

Setiap anggota bekerja di branch sendiri dan **tidak boleh langsung push ke `main`**.

```bash
# 1. Buat branch sesuai user story
git checkout -b fitur/us-2-tambah-tugas

# 2. Simpan perubahan
git add .
git commit -m "US-2: menambahkan fitur tambah tugas"

# 3. Kirim ke GitHub
git push -u origin fitur/us-2-tambah-tugas
```

Setelah itu:

1. Buka repository di GitHub, klik **Compare & pull request**.
2. Beri judul sesuai user story (contoh: `US-2 Tambah tugas`) dan pilih satu teman sebagai Reviewer.
3. Reviewer memeriksa tab **Files changed**, lalu memberi komentar atau **Approve**.
4. Scrum Master melakukan **Merge pull request** dengan urutan: US-1, US-3, US-2, US-5, US-6, US-4.
5. Semua anggota memperbarui salinan lokal:
   ```bash
   git checkout main
   git pull origin main
   ```

**Pasangan reviewer:** Scrum Master ↔ Product Owner, Developer 1 ↔ Developer 3, Developer 2 ↔ Developer 4.

## Proses Scrum (1 Sprint = 45 Menit)

| Menit | Tahap |
|-------|-------|
| 0–5 | Sprint Planning |
| 5–10 | Persiapan repository |
| 10–30 | Sprint (coding, commit, push, pull request) |
| 20 | Daily Scrum |
| 30–38 | Integrasi (review dan merge) |
| 38–42 | Sprint Review |
| 42–45 | Retrospektif |

## Teknologi

- HTML5
- CSS3
- JavaScript (vanilla)
- Git & GitHub

## Pengembangan Lanjutan

- Tombol **Hapus Semua** (tantangan tambahan)
- Memindahkan backlog ke GitHub Issues dan GitHub Projects

---

Dibuat untuk praktikum Rekayasa Perangkat Lunak (RPL) · Materi: Agile/Scrum dan kolaborasi dengan Git & GitHub.
