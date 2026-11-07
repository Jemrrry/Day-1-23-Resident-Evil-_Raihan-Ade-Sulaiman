# 📚 Dokumentasi Kegiatan Workshop - EXPECTIK 2026
### Jurusan Teknik Informatika dan Komputer (TIK) — Politeknik Negeri Jakarta

![GitHub repo size](https://img.shields.io/github/repo-size/Jemrrry/Day-1-23-Resident-Evil-_Raihan-Ade-Sulaiman?color=blue&style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/Jemrrry/Day-1-23-Resident-Evil-_Raihan-Ade-Sulaiman?style=flat-square)
![Visibility Public](https://img.shields.io/badge/Visibility-Public-green?style=flat-square)

---

## 👤 Identitas Peserta

| Keterangan | Data Peserta |
| :--- | :--- |
| **Nama Lengkap** | Raihan Ade Sulaiman |
| **NIM** | 2607441044 |
| **Program Studi** | Rekayasa Keamanan Siber |
| **Kelompok** | Kelompok 23 - Resident Evil |
| **Mentor Kelompok** | Kak Awa & Bang Nizar |
| **Akun GitHub** | [@Jemrrry](https://github.com/Jemrrry) |
| **Tautan Repositori** | [https://github.com/Jemrrry/Day-1-23-Resident-Evil-_Raihan-Ade-Sulaiman](https://github.com/Jemrrry/Day-1-23-Resident-Evil-_Raihan-Ade-Sulaiman) |

---

## 📖 Deskripsi Singkat Repository

Repository ini dibuat sebagai media penyimpanan publik (*public repository*) dan pusat dokumentasi resmi selama mengikuti kegiatan **Workshop EXPECTIK 2026: Day 1 - Proyek Workshop** yang diselenggarakan oleh Himpunan Mahasiswa Informatika dan Komputer (HIMATIK) Politeknik Negeri Jakarta.

Repositori ini memuat rangkuman materi dari modul **"Building with AI, Managing Change with GitHub" (From AI to GitHub)** yang dibawakan oleh Kak **Nugi Farhan** (*Senior Product Designer & UX Advisor*), catatan pembelajaran, implementasi pembuatan aplikasi berbasis AI (*Student Task Planner*), serta bukti praktik pengelolaan kode menggunakan Git dan GitHub.

---

## 🎯 Tujuan & Kegunaan Repository

Berdasarkan ketentuan Misi Proyek Workshop EXPECTIK 2026, repository ini memiliki tujuan sebagai berikut:

1. **Sarana Penyimpanan & Pengelolaan Daring**: Memanfaatkan platform GitHub sebagai media penyimpanan berbasis *cloud* dan pengelolaan dokumentasi proyek secara daring.
2. **Pengelolaan Repository Public**: Melatih kemampuan membuat, mengonfigurasi, dan mengelola repository dengan visibilitas *Public* agar dapat diakses serta dinilai secara transparan.
3. **Membiasakan Dokumentasi Teknis**: Membiasakan peserta untuk selalu mencatat dan mendokumentasikan setiap materi pembelajaran, sintaks teknis, dan proses pembuatan proyek.
4. **Manajemen Berkas Terstruktur**: Meningkatkan keahlian dalam menyusun file, aset materi, dan catatan kegiatan secara rapi dan hierarkis.
5. **Pemanfaatan `README.md`**: Mengasah keterampilan dalam menyusun berkas `README.md` dengan format Markdown yang profesional dan informatif sebagai halaman utama dokumentasi.

---

## ℹ️ Informasi Kegiatan Workshop

- **Nama Misi**: Day 1 - Proyek Workshop-26 (Week 1)
- **Topik Workshop**: *From AI to GitHub: Building with AI, Managing Change with GitHub*
- **Pemateri**: Kak Nugi Farhan (*Senior Product Designer / UX Advisor*)
- **Penyelenggara**: Himpunan Mahasiswa Informatika dan Komputer (HIMATIK) PNJ
- **Waktu Pelaksanaan**: Sabtu, 7 November 2026
- **Tenggat Pengumpulan**: Sabtu, 7 November 2026, Pukul 23.59 WIB
- **Platform Pengumpulan**: Website Resmi EXPECTIK HIMATIK PNJ

---

## 📝 Dokumentasi Kegiatan & Rangkuman Materi Workshop

> *Catatan mendalam dan rincian teknis dapat dibaca pada berkas: [catatan/rangkuman-materi-git-github.md](catatan/rangkuman-materi-git-github.md)*

### 1. Topik & Materi yang Disampaikan
Materi workshop terbagi menjadi dua pilar utama:
1. **Building with AI (Prompt Engineering)**:
   - Konsep dasar prompt dan pentingnya konteks dalam instruksi (*Context is Key*).
   - Struktur prompt efektif: **Role**, **Task/Goal**, **Context/Constraints**, dan **Format/Output**.
   - Taktik *prompting* profesional berdasarkan standar Google Cloud (kata kerja aksi, target audiens, fakta/data, batasan teknologi).
2. **Managing Change with GitHub (Git & GitHub)**:
   - Konsep Version Control System (VCS) dan sejarah Git oleh Linus Torvalds (2005).
   - Perbedaan mendasar antara Git (alat lokal DVCS) dan GitHub (platform kolaborasi awan).
   - Alur kerja 3 area Git: *Working Directory*, *Staging Area (Index)*, dan *Git Directory (Repository)*.
   - Konfigurasi identitas, koneksi keamanan berbasis SSH Key (Ed25519), dan perintah esensial (`git init`, `git add`, `git commit`, `git remote`, `git push`, `git pull`).
   - Praktik pembuatan aplikasi web pemula: **Student Task Planner**.

---

### 2. Catatan & Rangkuman Materi Pembelajaran

#### A. Alur Kerja Git (Git Workflow)
```
+---------------------+      git add      +------------------+     git commit     +-------------------+
|  Working Directory  |  ==============>  |   Staging Area   |  ===============>  |   Git Directory   |
| (File lokal diedit) |                   | (Index sementara)|                    |   (.git / Repo)   |
+---------------------+                   +------------------+                    +-------------------+
                                                                                            ||
                                                                                 git push   ||   git pull
                                                                                            \/
                                                                                  +-------------------+
                                                                                  |  GitHub (Remote)  |
                                                                                  +-------------------+
```

#### B. Cheatsheet Perintah Esensial
```bash
# 1. Konfigurasi identitas pengguna
git config --global user.name "Nama Lengkap"
git config --global user.email "email@mahasiswa.pnj.ac.id"

# 2. Inisialisasi repositori Git baru
git init

# 3. Memindahkan seluruh perubahan ke Staging Area
git add .

# 4. Menyimpan snapshot perubahan dengan pesan deskriptif
git commit -m "feat: inisialisasi repositori dokumentasi workshop expectik 2026"

# 5. Mengatur branch utama ke 'main'
git branch -M main

# 6. Menghubungkan ke remote repository GitHub
git remote add origin https://github.com/[username]/[nama-repo].git

# 7. Mengunggah commit ke GitHub
git push -u origin main
```

---

### 3. Poin-Poin Penting & Pengetahuan Baru yang Dipelajari

* **Prompt yang Presisi Menghasilkan Kode Berkualitas**: AI seperti ChatGPT, Claude, atau Antigravity membutuhkan konteks spesifik (*Role, Goal, Constraints, Output*) agar tidak menghasilkan kode yang salah atau terlalu rumit (*overengineered*).
* **Pemisahan Peran Git vs GitHub**: Git bekerja sepenuhnya secara lokal di komputer tanpa koneksi internet untuk merekam setiap perubahan, sedangkan GitHub adalah media kolaborasi dan publikasi kode berbasis cloud.
* **Keamanan SSH Key Ed25519**: Memahami keunggulan kurva Edwards-curve Digital Signature Algorithm (Ed25519) rancangan Daniel J. Bernstein dibanding RSA lama dalam hal performa dan ketahanan kriptografi.
* **Pentingnya Visibilitas Publik**: Memastikan repositori berstatus **Public** agar dapat diakses panitia penilai tanpa kendala otorisasi, sekaligus memulai rekam jejak portofolio digital mahasiswa baru TIK PNJ.

---

## 📁 Struktur Direktori Repository

```text
.
├── README.md                           # Berkas dokumentasi utama repository
├── Git & Github.pdf                    # Modul materi workshop: From AI to GitHub
├── catatan/
│   ├── rangkuman-materi-git-github.md  # Rangkuman lengkap materi slide deck
│   └── catatan-workshop.md             # Catatan pembelajaran & evaluasi harian
├── materi/
│   └── README.md                       # Tempat penyimpanan file materi pendukung
└── dokumentasi/
    └── README.md                       # Tempat screenshot bukti kehadiran & praktik
```

---

## 📷 Dokumentasi Visual / Bukti Pelaksanaan

> *Tambahkan foto tangkapan layar (screenshot) sesi workshop dan hasil praktik Git/GitHub di bawah ini:*

| Bukti Kehadiran Workshop | Bukti Praktik Git & GitHub |
| :---: | :---: |
| *<img width="900" height="1600" alt="WhatsApp Image 2026-11-07 at 18 07 49" src="https://github.com/user-attachments/assets/f504d3fd-1df4-4383-933f-662d397b2f7d" />* | *<img width="960" height="1280" alt="WhatsApp Image 2026-11-07 at 17 30 05" src="https://github.com/user-attachments/assets/eef74cf4-5261-4e9b-a77a-69d2a2acea90" />* |

---
