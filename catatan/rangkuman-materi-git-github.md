# Rangkuman Lengkap Materi Workshop: From AI to GitHub
**Kegiatan**: Workshop EXPECTIK 2026 — Day 1 (Proyek Workshop-26)  
**Pemateri**: Nugi Farhan (*Senior Product Designer & UX Advisor*)  
**Judul Modul**: *Building with AI, Managing Change with GitHub*  
**Sumber Berkas**: `Git & Github.pdf`

---

## Capaian & Objektif Pembelajaran
1. Mampu menjelaskan bagaimana perancangan *prompt AI* yang spesifik dan berkonteks menghasilkan luaran kode/aplikasi yang jauh lebih baik.
2. Mampu mengidentifikasi dan memahami konsep *repository*, *commit*, *branch*, dan *pull request*.
3. Mampu membedakan secara jelas antara **Git** (alat lokal) dan **GitHub** (platform *cloud* kolaborasi).
4. Mampu mempraktikkan alur kerja *version controlling* secara mandiri.

---

## BAGIAN 1: MEMBUAT & MENGEMBANGKAN (PROMPT ENGINEERING)

### 1. Definisi Prompt Engineering
* **Prompt**: Instruksi, konteks, atau masukan yang diberikan pengguna kepada model AI (seperti ChatGPT, Claude, Antigravity) untuk menghasilkan keluaran tertentu.
* Bentuk prompt beragam: mulai dari pertanyaan sederhana, kata kunci teknis, instruksi bertingkat, hingga potongan kode.
* **Prompt Engineering**: Seni dan teknik merancang instruksi secara terstruktur agar AI menghasilkan jawaban yang tepat, relevan, berkualitas tinggi, dan langsung layak digunakan (*production-ready*).

### 2. Pentingnya Konteks (*Context is Key*)
* **Tanpa Konteks**:
  ```text
  Create student task planner
  ```
  *(Hasil cenderung generik, tidak terarah, dan belum tentu sesuai kebutuhan).*
* **Dengan Konteks**:
  Menyertakan peran (*role*), tujuan spesifik (*goal*), batasan teknologi (*constraints*), serta format output yang diinginkan.

### 3. Struktur Prompt yang Baik (*Good Prompt Structure*)
Struktur standar prompt profesional terdiri dari 4 pilar utama:
1. **Role (Peran)**: Menetapkan peran/identitas AI.  
   *Contoh*: *"You are helping me build a beginner-friendly student task planner as a simple web application."*
2. **Task / Goal (Tugas Utama)**: Menentukan tujuan utama yang ingin dicapai.  
   *Contoh*: *"Create a task planner that helps first-year university students keep track of assignments and deadlines."*
3. **Context & Constraints (Konteks & Batasan)**:
   * **Requirements**: Fitur daftar tugas, tanggal pengumpulan (*due date*), status penyelesaian, tombol filter (*all, pending, completed*), tampilan responsif.
   * **Constraints**: Bahasa yang digunakan (HTML, CSS, Vanilla JavaScript murni tanpa pustaka/library eksternal berlebihan), struktur kode rapi, dan mudah dipelajari pemula.
4. **Format & Output (Bentuk Keluaran)**:
   * Menentukan format berkas, penjelasan cara menjalankan aplikasi, panduan pengujian interaksi, dan instruksi verifikasi (*"Do not claim that the application works until you have verified its behavior"*).

### 4. Taktik Prompting Efektif (Berdasarkan Panduan Google Cloud)
* **Gunakan kata kerja aksi (*Action Verbs*)**: Menentukan tindakan yang diharapkan secara tegas (misal: *Write, Compose, Analyze, Summarize*).
* **Tentukan panjang dan format luaran**: Misalnya daftar poin (*bullet points*), esai 500 kata, atau tabel.
* **Spesifikasikan target audiens**: Misalnya audiens pemula (*non-technical*) atau mahasiswa tingkat pertama.
* **Sertakan data dan fakta relevan**.
* **Rujuk dokumen atau sumber spesifik**.
* **Definisikan istilah dan konsep kunci**.

### 5. Keuntungan Prompt Engineering
* Meningkatkan performa dan akurasi model AI.
* Meminimalkan bias, kesalahan (*hallucination*), dan respon yang tidak diinginkan.
* Memberikan kendali penuh dan kepastian hasil (*predictability*).
* Menghadirkan pengalaman pengembangan perangkat lunak yang jauh lebih cepat dan efisien.

---

## BAGIAN 2: MANAJEMEN PERUBAHAN & KOLABORASI (GIT & GITHUB)

### 1. Apa itu Git?
* **Git** adalah sistem pengontrol versi terdistribusi (*Distributed Version Control System / DVCS*) yang diciptakan oleh **Linus Torvalds** pada tahun 2005.
* Git berfungsi untuk merekam dan melacak riwayat perubahan pada berkas proyek: **siapa** yang mengubah, **kapan** diubah, dan **apa saja** baris yang dimodifikasi.

### 2. Perbedaan Mendasar: Git vs GitHub

| Karakteristik | Git | GitHub |
| :--- | :--- | :--- |
| **Kategori** | Software / Alat CLI lokal (*DVCS*) | Layanan / Platform berbasis web (*Cloud Hosting*) |
| **Lokasi Operasi** | Komputer lokal pengguna (tanpa internet) | Server *cloud* internet |
| **Fungsi Utama** | Melacak dan mengelola riwayat perubahan berkas | Menyimpan repositori daring, kolaborasi tim, dan portofolio |
| **Pencipta / Pemilik** | Linus Torvalds (Open Source) | Microsoft GitHub |

### 3. Alur Kerja Git (*Git Workflow*)
Git bekerja melalui 3 area utama di mesin lokal:
1. **Working Directory (Tree)**: Direktori tempat kita membuat, mengedit, dan memodifikasi file kerja secara nyata.
2. **Staging Area (Index)**: Area persiapan sementara untuk memilih perubahan berkas mana saja yang akan dimasukkan ke dalam commit berikutnya melalui perintah `git add`.
3. **Git Directory (Repository / `.git`)**: Jantung dari Git yang menyimpan metadata, basis data objek terkompresi, dan seluruh *snapshot* riwayat commit proyek.

```
+-------------------+       git add       +-------------------+      git commit      +-------------------+
| Working Directory |  ================>  |   Staging Area    |  =================>  |   Git Directory   |
|   (Edit Berkas)   |                     |      (Index)      |                      |   (.git / Repo)   |
+-------------------+                     +-------------------+                      +-------------------+
                                                                                               ||
                                                                                    git push   ||   git pull
                                                                                               \/
                                                                                     +-------------------+
                                                                                     |  Remote (GitHub)  |
                                                                                     +-------------------+
```

### 4. Perintah-Perintah Penting Git

#### A. Operasi Lokal Dasar
* `git init`  
  Menginisialisasi direktori saat ini menjadi repositori Git lokal baru (membuat folder tersembunyi `.git`).
* `git add .` atau `git add -A` / `git add --all`  
  Memindahkan seluruh perubahan berkas (baru, diedit, atau dihapus) ke *staging area*.  
  *(Catatan: `git add *` tidak mencatat file yang dihapus).*
* `git commit -m "pesan commit"`  
  Menyimpan snapshot perubahan dari staging area ke riwayat repositori lokal dengan pesan deskriptif.

#### B. Operasi Remote (GitHub)
* `git remote add origin <URL>`  
  Menghubungkan repositori lokal dengan repositori jarak jauh (*remote*) di GitHub.
* `git push -u origin main`  
  Mengunggah riwayat commit dari cabang (*branch*) lokal `main` ke repositori di GitHub.
* `git pull origin main`  
  Mengambil pembaruan terbaru dari GitHub sekaligus menggabungkannya ke branch lokal yang sedang aktif.
* `git clone <URL>`  
  Menyalin repositori lengkap dari GitHub ke komputer lokal.

---

## BAGIAN 3: PANDUAN SETUP LINGKUNGAN PENGEMBANGAN

### 1. Konfigurasi Identitas Git
Wajib diset agar riwayat commit tercatat atas nama mahasiswa yang bersangkutan:
```bash
git config --global user.name "Nama Lengkap Peserta"
git config --global user.email "email@mahasiswa.pnj.ac.id"
git config --global --list
```

### 2. Autentikasi Aman Menggunakan SSH Key (Ed25519)
Workshop menyarankan penggunaan algoritma kriptografi modern **Ed25519** (*Edwards-curve Digital Signature Algorithm* berdasarkan Curve25519 oleh Daniel J. Bernstein) karena memiliki performa tinggi dan keamanan superior:
```bash
# 1. Generate SSH Key baru
ssh-keygen -t ed25519 -C "email@domain.com"

# 2. Nyalakan SSH Agent di terminal
eval "$(ssh-agent -s)"

# 3. Masukkan SSH Key ke GitHub
# Buka GitHub -> Settings -> SSH and GPG Keys -> New SSH Key -> Tempel isi file id_ed25519.pub

# 4. Verifikasi koneksi ke GitHub
ssh -T git@github.com
# Respon sukses: "Hi username! You've successfully authenticated, but GitHub does not provide shell access."
```

### 3. Checklist Verifikasi Setup Komputer
Sebelum mulai bekerja, pastikan 4 hal ini sudah terpasang dan berfungsi baik:
1. `git --version` (Git terdeteksi)
2. `git config --global user.name` & `user.email` (Identitas tersetup)
3. `code --version` (VS Code CLI siap digunakan)
4. `ssh -T git@github.com` (Koneksi ke GitHub terautentikasi)

---

## BAGIAN 4: IMPLEMENTASI PRAKTIK (STUDENT TASK PLANNER)

Sesuai materi workshop, langkah alur praktik pengembangan proyek adalah:
1. **Pilih AI Assisted Platform**: Menggunakan platform bantuan AI (Claude, Antigravity, ChatGPT).
2. **Rancang Prompt Terstruktur**: Memasukkan prompt dengan 4 pilar (*Role, Goal, Constraints, Output*) untuk membuat aplikasi web **Student Task Planner**.
3. **Inisialisasi Repositori**: Jalankan `git init` di folder proyek.
4. **Tahap First Commit & Push**: `git add .`, `git commit -m "init"`, dan dorong ke GitHub.
5. **Melakukan Perubahan (*Iterasi*)**: Mengembangkan fitur baru atau memperbaiki tampilan.
6. **Commit & Push Pembaruan**: Merekam perubahan baru ke GitHub untuk membiasakan alur kerja version control.
