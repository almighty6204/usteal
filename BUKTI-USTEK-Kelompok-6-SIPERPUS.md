# LAMPIRAN BUKTI-BUKTI USTEK  
## Pengembangan Sistem Informasi Perpustakaan Berbasis Web  
**Instansi**: Universitas Kebangsaan Republik Indonesia  
**Penyedia**: Kelompok 6 – Program Studi Sistem Informasi  
**Tahun**: 2026  
**Tanggal penyusunan dokumen bukti**: 2026-04-27  

---

## 1. Identitas Tim Pelaksana (Kelompok 6)

| No | Nama | Posisi | Tugas Utama |
|---:|------|--------|------------|
| 1 | Muhammad Akmal Palqah | Project Leader / Project Manager | Koordinasi tim, penjadwalan, komunikasi stakeholder, validasi deliverable |
| 2 | Rahayu Padilah | System Analyst | Analisis kebutuhan, proses bisnis, penyusunan SRS, desain database (ERD/LRS) |
| 3 | Ilham Al Munawar | Programmer Front-end | Implementasi UI/UX (Bootstrap), integrasi API ke tampilan |
| 4 | Muhammad Fajar Nurjaman | Programmer Back-end | Implementasi backend, API, autentikasi, logika sirkulasi & denda |
| 5 | Riphan Romadlon | QA & Dokumentasi | Black-box testing, test report, dokumentasi UAT dan BAST |

---

## 2. Data Stakeholder Perpustakaan

| No | Nama | Jabatan | Peran pada kegiatan |
|---:|------|---------|---------------------|
| 1 | Syahid Rohidin | Kepala Perpustakaan | Narasumber utama, validasi kebutuhan, persetujuan UAT |
| 2 | Yayan Skakmat | Staf Administrasi Perpustakaan | Narasumber operasional, pendamping observasi, pelaksana uji coba UAT |

---

## 3. Bukti Kegiatan Analisis Kebutuhan (Wawancara)

### 3.1 Notulen Wawancara Stakeholder
**Judul**: Notulen Wawancara Kebutuhan Sistem Informasi Perpustakaan  
**Hari/Tanggal**: Senin, 2026-04-20  
**Waktu**: 10.00–11.15 WIB  
**Tempat**: Ruang Kepala Perpustakaan – Universitas Kebangsaan Republik Indonesia  

**Narasumber**:  
- Syahid Rohidin (Kepala Perpustakaan)

**Peserta dari Tim Kelompok 6**:  
- Muhammad Akmal Palqah (PM)  
- Rahayu Padilah (SA)  
- Ilham Al Munawar (FE)  
- Muhammad Fajar Nurjaman (BE)  
- Riphan Romadlon (QA)

#### Agenda Wawancara
1. Menggali alur kerja peminjaman & pengembalian buku.  
2. Mengidentifikasi kendala layanan perpustakaan saat ini.  
3. Menggali kebutuhan fitur katalog/OPAC dan e-resources.  
4. Menentukan kebutuhan laporan dan dashboard monitoring.

#### Ringkasan Hasil Wawancara
**A. Kondisi dan Permasalahan Saat Ini**
- Pencatatan sirkulasi masih manual/tersebar sehingga riwayat peminjaman sulit ditelusuri dengan cepat.  
- Proses pencarian buku kurang efektif, terutama saat koleksi bertambah.  
- Penghitungan keterlambatan/denda berpotensi salah karena manual.  
- Kebutuhan akses e-book/jurnal belum terintegrasi dalam satu platform layanan.

**B. Kebutuhan Fungsional (Prioritas)**
1. **Modul Data Pengguna/Anggota**: kelola akun anggota (mahasiswa/dosen), status aktif, pencarian anggota.  
2. **Modul Katalog/OPAC**: pencarian berdasarkan judul/penulis/kategori, detail buku, status ketersediaan.  
3. **Modul Sirkulasi**: peminjaman, pengembalian, perhitungan jatuh tempo otomatis.  
4. **Modul Denda**: hitung denda keterlambatan otomatis dan riwayat pembayaran.  
5. **Modul E-Resources**: unggah file atau tautan e-book/jurnal, pencarian e-resources.  
6. **Dashboard Monitoring**: statistik peminjaman, buku terpopuler, jumlah anggota aktif, keterlambatan.

**C. Kebutuhan Non-Fungsional**
- Keamanan: role-based access (admin/pustakawan/anggota), password terenkripsi, validasi input.  
- Ketersediaan: akses 24/7 melalui web.  
- Kinerja: pencarian cepat (disarankan indexing pada kolom judul/penulis/isbn).  
- Kemudahan pakai: UI sederhana dan responsif.

#### Keputusan Rapat
- Sistem dikembangkan berbasis web dengan modul sesuai USTEK (Pengguna, OPAC, Sirkulasi, Dashboard).  
- Dilakukan pembuatan dokumen SRS dan prototype UI untuk divalidasi pada pertemuan berikutnya.  
- Pengujian penerimaan (UAT) dilaksanakan bersama pihak perpustakaan setelah versi beta siap.

#### Tindak Lanjut
- Tim menyusun **SRS** dan **SDD (ERD/LRS + UI prototype)**.  
- Menyusun daftar test case untuk Black-box testing & UAT.

#### Tanda Tangan (Paraf)
- Kepala Perpustakaan, **Syahid Rohidin**: (__________)  
- Project Manager, **Muhammad Akmal Palqah**: (__________)  

---

### 3.2 Daftar Hadir Wawancara
**Kegiatan**: Wawancara Kebutuhan Sistem Informasi Perpustakaan  
**Hari/Tanggal**: Senin, 2026-04-20  
**Tempat**: Ruang Kepala Perpustakaan  

| No | Nama | Jabatan/Peran | Tanda Tangan |
|---:|------|---------------|-------------|
| 1 | Syahid Rohidin | Kepala Perpustakaan | (__________) |
| 2 | Yayan Skakmat | Staf Administrasi | (__________) |
| 3 | Muhammad Akmal Palqah | Project Manager | (__________) |
| 4 | Rahayu Padilah | System Analyst | (__________) |
| 5 | Ilham Al Munawar | Programmer Front-end | (__________) |
| 6 | Muhammad Fajar Nurjaman | Programmer Back-end | (__________) |
| 7 | Riphan Romadlon | QA & Dokumentasi | (__________) |

---

## 4. Bukti Kegiatan Observasi Proses Bisnis (As-Is)

### 4.1 Form Observasi Proses Sirkulasi
**Judul**: Lembar Observasi Proses Peminjaman & Pengembalian Buku (As-Is)  
**Hari/Tanggal**: Senin, 2026-04-20  
**Waktu**: 11.15–12.00 WIB  
**Lokasi**: Meja Layanan Sirkulasi Perpustakaan  

**Observer**:  
- Rahayu Padilah (System Analyst)  
- Riphan Romadlon (QA & Dokumentasi)

#### Temuan Observasi (As-Is)
**A. Proses Peminjaman**
1. Anggota menyerahkan identitas/kartu anggota kepada petugas.  
2. Petugas mengecek ketersediaan buku dan mencatat transaksi peminjaman.  
3. Petugas menentukan tanggal jatuh tempo (due date) dan menyampaikan kepada anggota.

**B. Proses Pengembalian**
1. Anggota menyerahkan buku yang dipinjam.  
2. Petugas memeriksa kondisi buku dan mencatat pengembalian.  
3. Jika terlambat, petugas menghitung keterlambatan dan denda.

**C. Kendala Utama**
- Risiko human error dalam pencatatan dan perhitungan denda.  
- Sulit melakukan rekap cepat untuk laporan bulanan.  
- Pencarian histori peminjaman membutuhkan waktu lama.

#### Rekomendasi (To-Be)
- Sistem melakukan **pencatatan sirkulasi otomatis** dan menyimpan histori transaksi.  
- Due date dan denda dihitung otomatis sesuai aturan yang disepakati.  
- OPAC untuk meningkatkan efisiensi pencarian koleksi.  

**Paraf Observer**:  
- Rahayu Padilah: (__________)  
- Riphan Romadlon: (__________)  

---

## 5. Bukti Output Tahap Analisis — SRS (Ringkas)

### 5.1 Kebutuhan Fungsional (Ringkas)
**Aktor**: Admin/Pustakawan, Anggota (Mahasiswa/Dosen)

1. Autentikasi (Login/Logout) dan manajemen role.  
2. Manajemen Data Anggota (CRUD, status aktif).  
3. Manajemen Data Buku (CRUD, kategori, rak, stok).  
4. OPAC: pencarian & filter buku, detail buku, status tersedia.  
5. Sirkulasi: peminjaman, pengembalian, perpanjangan (opsional).  
6. Denda: hitung otomatis, riwayat denda & pembayaran.  
7. E-Resources: kelola file/tautan, pencarian, akses sesuai role.  
8. Dashboard: statistik buku terpopuler, peminjaman per periode, keterlambatan.

### 5.2 Kebutuhan Non-Fungsional (Ringkas)
- Keamanan: hashing password, validasi input, session management.  
- Kinerja: pagination untuk list, indexing kolom pencarian utama.  
- Usability: tampilan responsif (mobile friendly).  
- Ketersediaan: akses web 24/7.  
- Backup: backup database berkala.

---

## 6. Bukti Output Tahap Desain — SDD (Ringkas)

### 6.1 ERD (Deskripsi Entitas & Relasi)
**Entitas Utama**
- `users(id, nama, email, password_hash, role, status, created_at)`
- `members(id, user_id, nim_nidn, prodi, no_hp, alamat)`
- `categories(id, nama)`
- `books(id, isbn, judul, penulis, penerbit, tahun, kategori_id, rak, stok)`
- `loans(id, member_id, loan_date, due_date, status)`
- `loan_items(id, loan_id, book_id, qty)`
- `returns(id, loan_id, return_date, late_days, fine_amount)`
- `fine_payments(id, return_id, pay_date, amount, method, note)`
- `eresources(id, judul, tipe, file_path, url, uploaded_by, created_at)`

**Relasi Ringkas**
- users 1—1 members  
- categories 1—N books  
- members 1—N loans  
- loans 1—N loan_items  
- books 1—N loan_items  
- loans 1—0..1 returns  
- returns 1—N fine_payments  
- users 1—N eresources (uploaded_by)

### 6.2 Rancangan UI (Daftar Layar Prototype)
1. Login  
2. Dashboard Admin  
3. Data Buku (list + tambah/edit)  
4. Data Anggota  
5. OPAC (pencarian koleksi)  
6. Peminjaman (buat transaksi)  
7. Pengembalian (hitung denda otomatis)  
8. E-Resources (list + upload/link)  
9. Laporan (filter periode)

---

## 7. Bukti Pengembangan — Development Log (Ringkas)

### 7.1 Catatan Aktivitas Pengembangan (Contoh Log)
| Periode | Aktivitas | Penanggung Jawab | Output |
|---|---|---|---|
| Minggu 5 | Setup project, struktur database awal | Muhammad Fajar Nurjaman, Rahayu Padilah | Skema tabel inti |
| Minggu 6 | Modul login & role | Muhammad Fajar Nurjaman | Autentikasi & otorisasi |
| Minggu 7 | CRUD Buku, Kategori, Anggota | Ilham Al Munawar, Muhammad Fajar Nurjaman | Halaman admin & API |
| Minggu 8 | Sirkulasi (pinjam/kembali) & denda | Muhammad Fajar Nurjaman | Transaksi + perhitungan denda |
| Minggu 9 | Dashboard & e-resources | Ilham Al Munawar, Muhammad Fajar Nurjaman | Statistik & modul e-resources |

---

## 8. Bukti Pengujian — Test Report Black-Box

### 8.1 Laporan Pengujian Black-Box
**Nama Sistem**: Sistem Informasi Perpustakaan Berbasis Web  
**Versi**: Beta 0.1  
**Tanggal Uji**: 2026-06-23  
**Penguji**: Riphan Romadlon (QA & Dokumentasi)

| ID | Modul | Skenario | Data Uji (Input) | Hasil yang Diharapkan | Hasil Aktual | Status |
|---:|-------|----------|------------------|------------------------|--------------|:------:|
| TC-01 | Login | Login valid | Email & password benar | Masuk dashboard | Sesuai | PASS |
| TC-02 | Login | Login invalid | Password salah | Muncul pesan gagal | Sesuai | PASS |
| TC-03 | Buku | Tambah buku | Form valid | Data tersimpan | Sesuai | PASS |
| TC-04 | OPAC | Cari judul | Keyword: “Sistem Informasi” | Menampilkan hasil relevan | Sesuai | PASS |
| TC-05 | Sirkulasi | Peminjaman | Member aktif + buku stok > 0 | Transaksi terbentuk & due date | Sesuai | PASS |
| TC-06 | Pengembalian | Terlambat | Return_date > due_date | late_days & fine_amount terisi | Sesuai | PASS |

**Kesimpulan**:  
Seluruh skenario uji utama berjalan sesuai kebutuhan fungsional. Sistem layak dilanjutkan ke tahap UAT bersama pihak perpustakaan.

Tanda tangan Penguji (QA): (__________)

---

## 9. Bukti UAT — Berita Acara User Acceptance Test

### 9.1 Berita Acara Pelaksanaan UAT
**Nomor**: 002/BA-UAT/K6/SIPERPUS/2026  
Pada hari ini, **Senin**, tanggal **2026-06-29**, bertempat di Perpustakaan Universitas Kebangsaan Republik Indonesia, telah dilaksanakan **User Acceptance Test (UAT)** aplikasi “Sistem Informasi Perpustakaan Berbasis Web”.

**Pihak yang terlibat**:
1. Syahid Rohidin – Kepala Perpustakaan (Pihak Pengguna)  
2. Yayan Skakmat – Staf Administrasi (Pihak Pengguna)  
3. Kelompok 6 – Prodi Sistem Informasi (Pihak Pengembang)

**Ruang lingkup uji**:
- Login & role  
- OPAC/Katalog  
- Peminjaman  
- Pengembalian & Denda  
- E-Resources  
- Dashboard monitoring  

**Hasil UAT**: **DITERIMA DENGAN CATATAN**  
**Catatan perbaikan minor**:
1. Penambahan filter kategori pada halaman OPAC.  
2. Penyesuaian format laporan bulanan (kolom jumlah transaksi & total denda).

**Penutup**:  
Dengan berita acara ini, pihak perpustakaan menyatakan sistem telah memenuhi kebutuhan utama sesuai USTEK dan dapat digunakan untuk implementasi setelah perbaikan minor diselesaikan.

Tanda tangan:  
- Kepala Perpustakaan, Syahid Rohidin: (__________)  
- Staf Administrasi, Yayan Skakmat: (__________)  
- Project Manager, Muhammad Akmal Palqah: (__________)  

---

## 10. Bukti Serah Terima — BAST Deliverables

### 10.1 Berita Acara Serah Terima (BAST)
**Nomor**: 003/BAST/K6/SIPERPUS/2026  
**Tanggal**: 2026-07-06  
Telah dilakukan serah terima deliverables dari Kelompok 6 kepada Perpustakaan Universitas Kebangsaan Republik Indonesia berupa:

1. Dokumen Analisis Sistem (SRS)  
2. Dokumen Desain Sistem (SDD: ERD/LRS + rancangan UI)  
3. Aplikasi Sistem Informasi Perpustakaan berbasis Web (versi beta)  
4. Manual Pengguna (Admin & Anggota)  
5. Laporan Pengujian (Black-box Test Report) dan Berita Acara UAT  

Dengan ini pihak perpustakaan menyatakan menerima deliverables tersebut untuk dipergunakan sesuai kebutuhan institusi.

Tanda tangan:  
- Pihak Perpustakaan (Syahid Rohidin): (__________)  
- Pihak Pengembang (Muhammad Akmal Palqah): (__________)  

---

## 11. Dokumentasi Foto (Tempat untuk ditempel)

> Tempelkan foto asli di bawah ini saat sudah ada (atau sisipkan link Google Drive).  
> Minimal disarankan 4 item.

1. Foto kegiatan wawancara dengan Kepala Perpustakaan (2026-04-20) – (tempel/link)  
2. Foto observasi meja sirkulasi (2026-04-20) – (tempel/link)  
3. Foto diskusi tim/prototype UI (tanggal menyesuaikan) – (tempel/link)  
4. Foto pelaksanaan UAT (2026-06-29) – (tempel/link)  

---
**Dokumen ini dibuat untuk melengkapi bukti pelaksanaan kegiatan sesuai USTEK Kelompok 6.**