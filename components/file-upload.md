# GEMS Design System — File Upload Guidelines

## 1. Purpose

File Upload merupakan komponen yang digunakan untuk memilih, mengunggah, dan memantau proses unggahan file dalam aplikasi GEMS.

Komponen ini digunakan untuk kebutuhan dokumen, foto, lampiran, bukti pendukung, dan file lain sesuai persyaratan bisnis.

**Core Principle:**

> AI MUST menggunakan komponen File Upload resmi GEMS Design System. AI MUST memilih konfigurasi `Files queued`, `Type`, dan `Breakpoint` yang tersedia, mempertahankan struktur visual resmi, serta mengikuti aturan validasi dan pengelolaan file dari HSD/BRD.

### 1.1 Mandatory Design System Compliance

AI MUST:

1. Menggunakan instance File Upload resmi GEMS.
2. Memilih konfigurasi resmi berdasarkan kondisi file.
3. Menggunakan `Progress bar` atau `Progress fill` sesuai pattern yang disetujui.
4. Menggunakan breakpoint Desktop atau Mobile yang tersedia.
5. Mempertahankan typography, warna, spacing, border, radius, ikon, dan layout resmi.
6. Menggunakan Button, Alert, dan komponen pendukung resmi GEMS.
7. Mengikuti persyaratan jenis file, ukuran, jumlah, dan kewajiban unggahan dari HSD/BRD.
8. Menampilkan feedback yang sesuai dengan proses unggahan.
9. Memastikan file yang berhasil diunggah dapat dikenali pengguna.

AI MUST NOT:

1. Membuat File Upload custom jika komponen resmi tersedia.
2. Menggunakan upload widget dari library lain.
3. Mengganti instance resmi dengan Frame manual.
4. Membuat visual variant baru.
5. Mengubah warna, ukuran, atau progress indicator secara manual.
6. Mengarang aturan format, ukuran, atau jumlah file.
7. Menyatakan file berhasil diunggah sebelum sistem mengonfirmasinya.
8. Menghapus file tanpa mengikuti ketentuan aplikasi.

---

## 2. Official File Upload Variants

### 2.1 Verified Component Properties

Berdasarkan metadata Figma, terdapat tiga properties resmi.

| Property | Available Values |
|---|---|
| Files queued | True, False |
| Type | Progress bar, Progress fill |
| Breakpoint | Desktop, Mobile |

Total terdapat delapan konfigurasi.

### 2.2 Official Configuration Matrix

| Files queued | Type | Breakpoint |
|---|---|---|
| False | Progress bar | Desktop |
| True | Progress bar | Desktop |
| False | Progress fill | Desktop |
| True | Progress fill | Desktop |
| False | Progress bar | Mobile |
| True | Progress bar | Mobile |
| False | Progress fill | Mobile |
| True | Progress fill | Mobile |

### 2.3 Files Queued Property

**`Files queued=False`**

Digunakan ketika belum ada file dalam antrean unggahan komponen.

**`Files queued=True`**

Digunakan ketika terdapat file yang telah dipilih dan masuk dalam antrean unggahan.

**Rules:**

- MUST menggunakan konfigurasi sesuai kondisi antrean.
- MUST memperbarui konfigurasi ketika antrean berubah.
- MUST NOT menganggap `Files queued=True` berarti semua file sudah berhasil diunggah.
- MUST NOT menampilkan file yang belum dipilih.
- MUST NOT mengubah property hanya untuk keperluan estetika.

### 2.4 Type Property

**`Type=Progress bar`**

Menggunakan konfigurasi indikator progres berbentuk bar.

**`Type=Progress fill`**

Menggunakan konfigurasi indikator progres fill.

**Rules:**

- MUST menggunakan salah satu Type resmi.
- MUST mengikuti pattern yang ditetapkan aplikasi.
- MUST mempertahankan visual progress indicator resmi.
- MUST NOT membuat jenis progress indicator baru.
- MUST NOT mengganti Type secara otomatis tanpa kebutuhan.

**Important:** Kedua Type merupakan alternatif visual. Metadata Figma tidak menetapkan bahwa salah satunya wajib untuk foto atau dokumen.

### 2.5 Breakpoint Property

**`Breakpoint=Desktop`**

Digunakan pada layout desktop.

**`Breakpoint=Mobile`**

Digunakan pada layout mobile.

AI MUST menggunakan konfigurasi yang sesuai target layar.

AI MUST NOT membuat responsive variant baru ketika konfigurasi resmi sudah tersedia.

---

## 3. When to Use File Upload

### 3.1 Recommended Usage

File Upload SHOULD digunakan ketika pengguna perlu:

1. Mengunggah dokumen.
2. Menambahkan foto bukti atau evidence.
3. Mengunggah lampiran formulir.
4. Menambahkan dokumen pendukung pengajuan.
5. Mengunggah bukti pembayaran atau transaksi.
6. Menambahkan file laporan.
7. Mengunggah tiket atau dokumen perjalanan.
8. Melampirkan file untuk proses verifikasi.
9. Memperbarui file yang sebelumnya diunggah.

### 3.2 Usage Matrix

| Context | Example | Recommendation |
|---|---|---|
| Document Form | Lampiran dokumen | Use File Upload |
| Evidence Submission | Foto bukti kegiatan | Use File Upload |
| Travel Form | Tiket perjalanan | Use File Upload |
| Report Form | Dokumen laporan | Use File Upload |
| Profile Form | Foto profil | Use jika pattern resmi mendukung |
| Data Import | Unggah Excel/CSV | Use jika alur impor mendukung |
| Read-only Detail | Melihat file yang sudah ada | Gunakan display pattern resmi yang sesuai |
| File Download | Mengunduh dokumen | Gunakan Download Action |

### 3.3 Mandatory Usage Conditions

AI MUST menggunakan File Upload resmi ketika:

- HSD/BRD meminta input file.
- Form membutuhkan dokumen pendukung.
- Pengguna harus melampirkan foto atau evidence.
- Existing application menggunakan GEMS File Upload.
- Pengguna membutuhkan feedback progres unggahan.

---

## 4. When NOT to Use File Upload

File Upload MUST NOT digunakan untuk:

1. Input teks.
2. Input angka.
3. Input tanggal.
4. Pemilihan data dari Dropdown.
5. Menampilkan file tanpa kebutuhan unggahan.
6. Mengunduh file.
7. Menampilkan gambar dekoratif.
8. Mengganti Avatar apabila tersedia komponen khusus yang lebih sesuai.

AI MUST menggunakan komponen GEMS lain berdasarkan fungsi sebenarnya.

---

## 5. File Upload Component Anatomy

### 5.1 Component Structure

AI MUST mempertahankan struktur sesuai instance resmi GEMS.

Elemen yang perlu diperiksa:

| Element | Purpose |
|---|---|
| Upload Area | Area pemilihan file |
| Upload Instruction | Menjelaskan cara memilih file |
| File Information | Menampilkan informasi file |
| File Queue | Menampilkan file dalam antrean |
| Progress Indicator | Menunjukkan progres unggahan |
| File Action | Tindakan terhadap file jika tersedia |
| Supporting Text | Menjelaskan persyaratan file |
| Validation Feedback | Menjelaskan kesalahan input jika terjadi |

Daftar ini merupakan checklist implementasi. Keberadaan dan susunan masing-masing elemen harus mengikuti instance resmi.

### 5.2 Upload Area Rules

AI MUST:

- Menggunakan area unggah resmi.
- Mempertahankan visual GEMS.
- Menggunakan interaksi yang didukung.
- Memastikan area unggah dapat digunakan.
- Menggunakan instruksi yang jelas.

AI MUST NOT:

- Membuat dropzone custom.
- Mengubah border menjadi dashed secara manual jika tidak sesuai komponen.
- Membuat ikon upload custom.
- Mengubah ukuran area secara sembarangan.

### 5.3 Supporting Text Rules

Supporting text SHOULD menjelaskan persyaratan file yang relevan.

Contoh:

- Format yang didukung: PDF, JPG, PNG.
- Maksimal ukuran file: sesuai ketentuan sistem.
- Maksimal jumlah file: sesuai ketentuan sistem.

Contoh format di atas hanya ilustrasi. AI MUST menggunakan persyaratan sebenarnya dari HSD/BRD.

AI MUST NOT mengarang batas ukuran atau jumlah file.

---

## 6. File Upload States

### 6.1 Official Component Configuration States

Konfigurasi yang sudah terverifikasi:

- Files queued=False.
- Files queued=True.
- Progress bar.
- Progress fill.
- Desktop.
- Mobile.

### 6.2 Functional State Matrix

| State | Trigger | Expected Behavior |
|---|---|---|
| Empty | Belum ada file dipilih | Menampilkan area unggah |
| Files Queued | File telah dipilih | Menampilkan antrean file |
| Validating | File sedang diperiksa | Memeriksa persyaratan file |
| Uploading | File sedang dikirim | Menampilkan progres jika tersedia |
| Success | Upload dikonfirmasi berhasil | Menampilkan status berhasil |
| Error | Upload gagal | Menampilkan feedback kesalahan |
| Invalid File | File tidak memenuhi syarat | Menampilkan alasan penolakan |
| Removing | Penghapusan sedang diproses | Menampilkan feedback jika diperlukan |
| Removed | File berhasil dihapus | Memperbarui daftar file |

State fungsional tersebut bukan otomatis nama variant Figma.

### 6.3 Empty State

**Condition:** Belum ada file yang dipilih.

**Rules:**

- MUST menggunakan `Files queued=False`.
- MUST menampilkan instruksi unggah sesuai komponen.
- MUST mengikuti Type dan Breakpoint yang dipilih.
- MUST NOT menampilkan file fiktif.

### 6.4 Files Queued State

**Condition:** Pengguna telah memilih satu atau lebih file.

**Rules:**

- MUST menggunakan `Files queued=True`.
- MUST menampilkan file sesuai data yang dipilih.
- MUST mempertahankan informasi antrean.
- MUST membedakan file yang belum diunggah dari file yang berhasil diunggah.
- MUST NOT menganggap seluruh file telah berhasil disimpan.

### 6.5 Validating State

**Condition:** Sistem sedang memeriksa file.

**Validation may include:**

- Format file.
- Ukuran file.
- Jumlah file.
- Kewajiban unggahan.
- Validitas file sesuai ketentuan sistem.

**Rules:**

- MUST menggunakan aturan validasi HSD/BRD.
- MUST memberikan feedback jika file tidak valid.
- MUST NOT mengarang persyaratan.
- MUST NOT menampilkan Success sebelum validasi selesai.

### 6.6 Uploading State

**Condition:** Proses unggahan sedang berlangsung.

**Rules:**

- MUST menggunakan indikator progres resmi jika didukung.
- MUST menampilkan progres berdasarkan data aktual.
- MUST NOT membuat persentase dummy.
- MUST NOT menampilkan 100% jika proses belum selesai.
- MUST NOT mengizinkan tindakan yang menyebabkan konflik data jika tidak didukung sistem.

### 6.7 Success State

**Condition:** Sistem mengonfirmasi unggahan berhasil.

**Rules:**

- MUST memberikan feedback keberhasilan sesuai pattern GEMS.
- MUST mempertahankan informasi file yang berhasil diunggah.
- MUST memperbarui status file.
- MUST NOT menampilkan Success sebelum menerima hasil sistem.
- MUST NOT membuat visual Success custom.

### 6.8 Error State

**Condition:** Proses unggahan gagal.

**Rules:**

- MUST menampilkan feedback yang menjelaskan kegagalan.
- MUST menggunakan Alert, Notification, atau komponen resmi yang sesuai.
- SHOULD menyediakan Retry jika sistem mendukung.
- MUST NOT menghapus file yang masih dapat dicoba ulang tanpa kebutuhan.
- MUST NOT menampilkan Success.

### 6.9 Invalid File State

**Condition:** File tidak memenuhi persyaratan.

**Rules:**

- MUST menjelaskan alasan file ditolak.
- MUST menggunakan validasi sesuai sistem.
- MUST membedakan invalid format, ukuran, dan jumlah jika informasi tersedia.
- MUST NOT menggunakan pesan error generik jika penyebab diketahui.

### 6.10 Removed State

**Condition:** File berhasil dihapus dari antrean atau penyimpanan.

**Rules:**

- MUST memperbarui daftar file.
- MUST memperbarui jumlah file.
- MUST kembali ke `Files queued=False` jika antrean kosong.
- MUST membedakan menghapus file dari antrean dengan menghapus file yang sudah tersimpan.
- MUST mengikuti aturan konfirmasi jika penghapusan bersifat permanen.

---

## 7. File Selection & Upload Interaction

### 7.1 Select File

Ketika pengguna memilih file:

1. Sistem membuka mekanisme pemilihan file yang didukung.
2. Pengguna memilih file.
3. Sistem membaca informasi file.
4. Sistem melakukan validasi.
5. File valid dimasukkan ke antrean atau diproses sesuai alur aplikasi.
6. Komponen memperbarui kondisi Files queued.

AI MUST mengikuti alur unggahan yang ditetapkan aplikasi.

### 7.2 Drag & Drop

Jika komponen dan implementasi mendukung drag-and-drop:

- MUST menggunakan interaction pattern resmi.
- MUST memvalidasi file yang dijatuhkan.
- MUST mempertahankan feedback resmi.
- MUST NOT membuat dropzone custom.

Jika drag-and-drop tidak didukung, AI MUST NOT menambahkannya berdasarkan asumsi.

### 7.3 Multiple Files

Jika HSD/BRD mengizinkan beberapa file:

- MUST mengikuti jumlah maksimum.
- MUST menampilkan antrean sesuai kemampuan komponen.
- MUST memvalidasi setiap file.
- MUST menjaga status setiap file.
- MUST NOT menerima file melebihi batas yang ditentukan.

Jika hanya satu file diizinkan, AI MUST mengikuti single-file behavior aplikasi.

### 7.4 Remove File

Jika pengguna menghapus file:

- MUST memastikan target file benar.
- MUST mengikuti aturan aplikasi.
- MUST memperbarui antrean.
- MUST menggunakan komponen konfirmasi resmi jika diperlukan.
- MUST NOT menghapus file lain.

### 7.5 Replace File

Jika pengguna mengganti file:

- MUST mengikuti replace behavior aplikasi.
- MUST memvalidasi file baru.
- MUST memperbarui informasi file setelah proses berhasil.
- MUST NOT menghapus file lama secara permanen sebelum kondisi penggantian yang diwajibkan sistem terpenuhi.

---

## 8. File Validation Rules

### 8.1 Required Validation

AI MUST membaca persyaratan file dari HSD/BRD.

| Validation | Requirement |
|---|---|
| File Type | Sesuai format yang diizinkan |
| File Size | Sesuai batas ukuran |
| File Count | Sesuai jumlah maksimum |
| Required Upload | Sesuai kewajiban field |
| File Integrity | Sesuai validasi sistem |
| Permission | Sesuai role access |

### 8.2 Required Field

Jika unggahan wajib:

- MUST menggunakan indikator required resmi pada label field.
- MUST mencegah submit jika persyaratan belum terpenuhi.
- MUST menampilkan validation feedback resmi.
- MUST menjelaskan bahwa file wajib dilampirkan.

Jika unggahan opsional:

- MUST NOT menampilkan required indicator.
- MUST NOT memblokir submit hanya karena file belum dipilih.

### 8.3 File Type Validation

AI MUST:

- Menggunakan daftar format yang ditentukan.
- Menolak format yang tidak didukung sesuai sistem.
- Menampilkan pesan kesalahan yang jelas.
- Tidak mengarang format yang diperbolehkan.

### 8.4 File Size Validation

AI MUST:

- Menggunakan batas ukuran resmi.
- Memvalidasi ukuran setiap file sesuai aturan.
- Menampilkan pesan jika file terlalu besar.
- Tidak mengarang batas ukuran.

### 8.5 File Count Validation

AI MUST:

- Mengikuti jumlah maksimum file.
- Menampilkan feedback jika batas terlampaui.
- Mempertahankan file yang valid sesuai behavior sistem.
- Tidak menambah kapasitas upload secara manual.

---

## 9. File Upload in Forms

### 9.1 Create Form

Ketika File Upload digunakan pada form tambah data:

- MUST menggunakan komponen resmi.
- MUST mengikuti urutan field dari HSD/BRD.
- MUST menampilkan label yang jelas.
- MUST menerapkan required validation jika diperlukan.
- MUST menjaga file yang telah dipilih selama proses pengisian sesuai kebijakan aplikasi.

### 9.2 Edit Form

Ketika digunakan pada form edit:

- MUST menampilkan file existing sesuai kebutuhan.
- MUST membedakan file existing dan file baru jika alur memerlukannya.
- MUST mengikuti aturan replace/remove.
- MUST NOT menghapus file existing secara otomatis.
- MUST mempertahankan data sampai perubahan dikonfirmasi sesuai alur aplikasi.

### 9.3 Form Submission

Sebelum submit, AI MUST memastikan:

1. Required file terpenuhi.
2. File memenuhi format.
3. File memenuhi batas ukuran.
4. File memenuhi batas jumlah.
5. Status unggahan sesuai persyaratan sistem.
6. Tidak ada proses yang belum selesai jika submit mensyaratkan upload selesai.

AI MUST NOT menganggap file tersimpan hanya karena sudah dipilih.

---

## 10. Progress Indicator Guidelines

### 10.1 Progress Bar

**Property:** `Type=Progress bar`

AI MUST:

- Menggunakan variant resmi.
- Menampilkan progres berdasarkan nilai aktual jika tersedia.
- Mempertahankan visual styling.
- Menggunakan feedback sesuai status file.

AI MUST NOT:

- Membuat progress bar custom.
- Mengubah warna progres secara manual.
- Membuat animasi custom tanpa acuan.
- Menggunakan nilai progres palsu.

### 10.2 Progress Fill

**Property:** `Type=Progress fill`

AI MUST:

- Menggunakan variant resmi.
- Mengikuti visual progress fill GEMS.
- Menggunakan data progres aktual jika tersedia.
- Mempertahankan ukuran dan styling.

AI MUST NOT:

- Membuat progress fill custom.
- Mengubah fill color di luar GEMS.
- Mengubah layout progres secara manual.

### 10.3 Progress Selection

AI MUST menentukan Type berdasarkan:

1. Approved design.
2. Existing application pattern.
3. Component usage guideline resmi.
4. Kebutuhan presentasi progres yang didukung komponen.

Jika tidak ada aturan pemilihan yang dapat diverifikasi, AI MUST meminta klarifikasi sebelum menetapkan standar baru.

---

## 11. File Upload UX Writing

### 11.1 General Rules

AI MUST:

- Menggunakan bahasa yang jelas.
- Mengikuti terminologi HSD/BRD.
- Menjelaskan persyaratan file.
- Memberikan feedback sesuai kondisi.
- Menghindari pesan yang ambigu.

### 11.2 Recommended Wording

| Condition | Example Message |
|---|---|
| Empty | Unggah File |
| Supporting Text | Pilih file sesuai format dan ukuran yang ditentukan. |
| Required | File wajib diunggah. |
| Invalid Format | Format file tidak didukung. |
| Invalid Size | Ukuran file melebihi batas yang diizinkan. |
| Maximum Files | Jumlah file melebihi batas maksimum. |
| Uploading | File sedang diunggah. |
| Success | File berhasil diunggah. |
| Error | File gagal diunggah. Silakan coba kembali. |
| Removed | File berhasil dihapus. |

### 11.3 Contextual Labels

| Context | Recommended Label |
|---|---|
| Travel | Unggah Tiket Perjalanan |
| Evidence | Unggah Foto Bukti |
| Document | Unggah Dokumen |
| Report | Unggah Lampiran Laporan |
| Profile | Unggah Foto Profil |

Label harus disesuaikan dengan fitur dan persyaratan bisnis.

---

## 12. Responsive Behavior

### 12.1 Desktop

AI MUST:

- Menggunakan `Breakpoint=Desktop`.
- Menggunakan ukuran dan layout resmi.
- Mempertahankan visual file queue.
- Memastikan teks dan tindakan terbaca.
- Mengikuti responsive behavior GEMS.

### 12.2 Mobile

AI MUST:

- Menggunakan `Breakpoint=Mobile`.
- Mempertahankan struktur resmi.
- Memastikan file queue tetap dapat digunakan.
- Memastikan tindakan upload dan remove dapat diakses.
- Menggunakan typography dan spacing GEMS.

### 12.3 Responsive Restrictions

AI MUST NOT:

1. Menggunakan Desktop variant untuk Mobile tanpa acuan.
2. Membuat Mobile upload widget custom.
3. Mengubah ukuran secara manual.
4. Membuat breakpoint baru.
5. Menghilangkan informasi file yang penting.

---

## 13. Accessibility

AI MUST:

1. Menyediakan label field yang jelas.
2. Mendukung keyboard interaction.
3. Menggunakan focus indicator resmi.
4. Menyediakan accessible name untuk tombol upload dan remove.
5. Mengomunikasikan progres unggahan secara aksesibel.
6. Mengomunikasikan keberhasilan dan kegagalan.
7. Tidak hanya mengandalkan warna untuk menyampaikan status.
8. Mengikuti standar aksesibilitas proyek.

AI MUST NOT:

- Membuat kontrol yang hanya dapat digunakan dengan mouse.
- Menghilangkan focus indicator.
- Menggunakan ikon tanpa accessible label.
- Mengandalkan progress bar visual tanpa informasi status yang dapat dipahami.

---

## 14. AI Decision Logic

AI MUST mengikuti proses berikut.

### Step 1 — Identify Upload Requirement

Baca HSD/BRD untuk menentukan:

- Jenis file.
- Ukuran maksimum.
- Jumlah maksimum.
- Required atau Optional.
- Single atau Multiple.
- Upload behavior.
- Remove atau Replace behavior.

### Step 2 — Retrieve Official Component

AI MUST mengakses File Upload resmi GEMS.

### Step 3 — Determine Breakpoint

Pilih:

- Desktop.
- Mobile.

### Step 4 — Determine Progress Type

Pilih:

- Progress bar.
- Progress fill.

Pemilihan mengikuti pattern resmi atau approved design.

### Step 5 — Determine Files Queued

Jika antrean kosong:

`Files queued=False`

Jika antrean berisi file:

`Files queued=True`

### Step 6 — Configure Upload Content

Sesuaikan:

- Field Label.
- Supporting Text.
- File Requirements.
- File Queue Data.
- Progress Information.
- Available Actions.

### Step 7 — Apply Validation

Gunakan persyaratan dari HSD/BRD.

### Step 8 — Apply Functional States

Tangani:

- Empty.
- Queued.
- Validating.
- Uploading.
- Success.
- Error.
- Invalid File.
- Removed.

Gunakan komponen GEMS untuk seluruh feedback visual.

### Step 9 — Validate Against GEMS

AI MUST memastikan:

1. Instance resmi digunakan.
2. Files queued sesuai.
3. Type sesuai.
4. Breakpoint sesuai.
5. Typography sesuai.
6. Colors sesuai.
7. Spacing sesuai.
8. Icons sesuai.
9. Progress indicator sesuai.
10. Validation benar.
11. File actions benar.
12. Tidak ada komponen custom.

### Step 10 — Request Human Approval

Jika kebutuhan tidak didukung komponen resmi, AI MUST meminta Human Approval sebelum membuat alternatif.

---

## 15. AI Restrictions

AI MUST NOT:

1. Membuat File Upload custom.
2. Menggunakan upload widget dari library lain.
3. Mengganti instance resmi dengan Frame manual.
4. Membuat variant baru.
5. Mengubah typography di luar GEMS.
6. Mengubah warna di luar GEMS.
7. Mengubah spacing di luar GEMS.
8. Membuat progress indicator custom.
9. Membuat upload icon custom.
10. Membuat drag-and-drop area custom.
11. Membuat responsive variant baru.
12. Mengarang format file.
13. Mengarang batas ukuran file.
14. Mengarang jumlah maksimum file.
15. Mengabaikan required validation.
16. Menampilkan Success sebelum proses selesai.
17. Menampilkan progress palsu.
18. Menghapus file tanpa aturan yang sesuai.
19. Menghapus file existing secara otomatis.
20. Membuat retry behavior yang tidak didukung.
21. Menggunakan Button custom.
22. Menggunakan Alert custom.
23. Mengabaikan role access.
24. Menggunakan File Upload untuk fungsi yang tidak sesuai.
25. Mengklaim desain sesuai GEMS tanpa verifikasi.

---

## 16. Official GEMS Design System Component

### 16.1 Component Reference

**Component Name:** File Upload  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=743-3089

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `743:3089`

### 16.2 Verified Component Configurations

**Files queued:**
- True
- False

**Type:**
- Progress bar
- Progress fill

**Breakpoint:**
- Desktop
- Mobile

**Total:** 8 configurations.

### 16.3 Mandatory Component Usage

AI MUST:

1. Mengakses komponen File Upload resmi.
2. Menggunakan instance resmi.
3. Memilih Files queued, Type, dan Breakpoint yang tersedia.
4. Mempertahankan visual properties resmi.
5. Mengikuti persyaratan file dari HSD/BRD.
6. Menggunakan komponen pendukung GEMS.
7. Menangani kondisi unggahan secara benar.
8. Memvalidasi hasil implementasi terhadap GEMS.

### 16.4 Verification Requirements

Sebelum implementasi, AI MUST memeriksa:

- Component Name.
- Available Configurations.
- Component Properties.
- File Queue Structure.
- Progress Indicator.
- Typography.
- Colors.
- Spacing.
- Icons.
- Supported Actions.
- Validation Feedback.
- Responsive Behavior.

Jika suatu property atau visual state tidak dapat diverifikasi, AI MUST NOT mengarang spesifikasinya.

### 16.5 Final AI Instruction

**AI MUST retrieve and reuse the official GEMS File Upload component from the specified Figma source whenever the integration supports it.**

AI MUST select a supported combination of `Files queued`, `Type`, and `Breakpoint`, preserve the official component structure, and configure upload behavior according to approved HSD/BRD requirements.

AI MUST use official GEMS components, tokens, and feedback patterns for all supporting elements.

AI MUST NOT recreate File Upload manually, invent unsupported variants, fabricate validation rules, or introduce custom styling without Human Approval.

**GEMS Design System is the single source of truth for all File Upload visual specifications.**
