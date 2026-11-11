# GEMS Design System — Alert Guidelines

## 1. Purpose & Core Principles

Alert merupakan komponen komunikasi visual yang digunakan untuk menyampaikan informasi penting, peringatan, kesalahan, hasil validasi, atau kondisi tertentu yang perlu diketahui pengguna dalam konteks halaman atau proses yang sedang dilakukan.

Alert membantu pengguna memahami kondisi sistem, dampaknya terhadap data atau proses, serta tindakan yang perlu dilakukan.

### 1.1 Primary Purposes

- Menampilkan informasi penting yang berkaitan dengan halaman.
- Memberikan peringatan sebelum pengguna melanjutkan proses.
- Menampilkan hasil validasi data.
- Menjelaskan kesalahan atau kegagalan proses.
- Menampilkan informasi keberhasilan yang perlu tetap terlihat.
- Memberikan instruksi untuk memperbaiki data atau menyelesaikan masalah.
- Menjelaskan dampak suatu kondisi terhadap proses bisnis.

### 1.2 Core Principles

1. Alert harus relevan dengan konteks pengguna.
2. Pesan Alert harus jelas, ringkas, dan dapat ditindaklanjuti jika diperlukan.
3. Alert harus menjelaskan kondisi aktual, bukan membuat asumsi.
4. Tingkat urgensi harus sesuai dengan makna pesan.
5. Alert tidak boleh mengganggu pengguna tanpa alasan.
6. Alert harus menggunakan komponen dan variant resmi GEMS.
7. Alert tidak boleh menggantikan Modal, Toast, atau validasi field ketika komponen tersebut lebih tepat.

### 1.3 AI Rules

- MUST menggunakan komponen Alert resmi GEMS.
- MUST menentukan isi pesan berdasarkan HSD/BRD dan kondisi sistem.
- MUST memilih warna sesuai tingkat urgensi dan makna informasi.
- MUST memastikan pesan mudah dipahami.
- MUST NOT membuat informasi, jumlah data, atau hasil proses yang tidak tersedia.
- MUST NOT menggunakan Alert untuk setiap feedback kecil.
- MUST NOT menggunakan Alert sebagai pengganti konfirmasi tindakan.

---

## 2. When to Use Alert

### 2.1 Recommended Usage

| Context | When to Use | Example |
|---|---|---|
| Validation Result | Menampilkan hasil validasi sebelum proses dilanjutkan | Hasil Validasi Data Impor |
| Incomplete Information | Menginformasikan data yang belum lengkap | Lengkapi informasi sebelum mengirim pengajuan |
| Warning | Menjelaskan kondisi yang perlu diperhatikan | Sebagian data tidak dapat diproses |
| Error | Menjelaskan kegagalan atau kesalahan sistem | Data gagal dimuat |
| Success | Menampilkan hasil berhasil yang perlu tetap terlihat | Data berhasil divalidasi |
| Informational | Menyampaikan informasi atau ketentuan | Perubahan data akan berlaku pada periode berikutnya |
| Process Impact | Menjelaskan dampak terhadap data atau workflow | Data tidak valid tidak akan diimpor |
| Requirement Notice | Menjelaskan persyaratan sebelum proses | Dokumen wajib dilengkapi sebelum pengajuan |

### 2.2 When NOT to Use Alert

| Requirement | Reason | Recommended Component |
|---|---|---|
| Feedback singkat setelah menyimpan | Bersifat sementara | Notification / Toast |
| Konfirmasi penghapusan | Membutuhkan keputusan eksplisit | Modal |
| Konfirmasi pengiriman | Membutuhkan keputusan pengguna | Modal |
| Kesalahan pada satu field | Lebih tepat ditampilkan dekat field | Input Validation |
| Menampilkan status pada tabel | Informasi ringkas | Badge |
| Menampilkan kondisi tanpa data | Membutuhkan tampilan khusus | Empty State |
| Menjalankan aksi utama | Alert bukan pengganti kontrol aksi | Button |
| Memilih atau mengubah nilai | Membutuhkan kontrol input | Input / Dropdown / Toggle |

### 2.3 Selection Rules

- MUST menggunakan Alert jika informasi perlu terlihat dalam konteks halaman.
- SHOULD menggunakan Alert untuk hasil validasi yang memiliki dampak terhadap proses.
- SHOULD menggunakan Alert untuk menjelaskan kesalahan yang memerlukan tindakan pengguna.
- MUST menggunakan Modal apabila pengguna harus mengonfirmasi tindakan sebelum sistem melanjutkan.
- SHOULD menggunakan Toast untuk feedback sementara yang tidak perlu tetap terlihat.
- MUST NOT menggunakan Alert hanya sebagai elemen dekoratif.

---

## 3. Alert Component Structure

GEMS Design System menyediakan komponen Alert dengan properti `Color`, `Size`, dan `Breakpoint`.

### 3.1 Official Properties

| Property | Available Values |
|---|---|
| `Color` | `Default`, `Brand`, `Gray`, `Error`, `Warning`, `Success` |
| `Size` | `Floating`, `Full-width` |
| `Breakpoint` | `Desktop`, `Mobile` |

### 3.2 Content Structure

Alert dapat memuat elemen berikut sesuai variant dan kebutuhan:

| Element | Description | Usage |
|---|---|---|
| Container | Area visual utama Alert | Required |
| Icon | Indikator visual sesuai konteks | Menguatkan makna pesan |
| Title | Judul atau ringkasan kondisi | Menjelaskan informasi utama |
| Description | Penjelasan kondisi, dampak, atau instruksi | Memberikan konteks |
| Close Icon | Kontrol untuk menutup Alert | Jika dismiss diizinkan |
| Action | Tindakan lanjutan | Jika didukung variant dan requirement |

Tidak semua elemen harus muncul pada setiap Alert. Gunakan struktur yang tersedia pada variant GEMS.

### 3.3 Component Rules

- MUST menggunakan property resmi GEMS.
- MUST mengikuti struktur dan styling komponen GEMS.
- MUST menggunakan kombinasi variant yang tersedia.
- MUST NOT membuat warna atau ukuran custom tanpa persetujuan.
- MUST NOT menambahkan tombol atau ikon yang tidak didukung variant tanpa validasi.
- SHOULD menggunakan Title dan Description jika informasi membutuhkan penjelasan.

---

## 4. Alert Colors & Semantic Meaning

### 4.1 Available Colors

| Color | Semantic Meaning | Recommended Usage |
|---|---|---|
| `Default` | Informasi umum | Pesan informatif standar |
| `Brand` | Informasi dengan penekanan brand | Pengumuman atau informasi penting yang relevan |
| `Gray` | Informasi netral | Keterangan atau ketentuan umum |
| `Error` | Kesalahan atau kegagalan | Proses gagal, data tidak dapat diproses |
| `Warning` | Peringatan atau kondisi berisiko | Validasi sebagian gagal, informasi perlu diperiksa |
| `Success` | Keberhasilan | Proses berhasil dan hasilnya perlu tetap terlihat |

### 4.2 Color Selection Rules

- MUST memilih warna berdasarkan makna pesan.
- MUST menggunakan `Error` untuk kondisi kesalahan atau kegagalan yang sesuai.
- SHOULD menggunakan `Warning` untuk kondisi yang membutuhkan perhatian tetapi tidak selalu merupakan kegagalan total.
- SHOULD menggunakan `Success` untuk kondisi keberhasilan.
- SHOULD menggunakan `Default` atau `Gray` untuk informasi netral.
- MUST NOT menggunakan `Error` untuk informasi biasa.
- MUST NOT menggunakan `Success` sebelum sistem mengonfirmasi keberhasilan.
- MUST NOT memilih warna hanya berdasarkan preferensi estetika.

### 4.3 Semantic Mapping Examples

| Condition | Recommended Color | Reason |
|---|---|---|
| Semua data valid | Success | Validasi berhasil |
| Sebagian data tidak valid | Warning | Pengguna perlu memeriksa hasil |
| Seluruh proses impor gagal | Error | Proses tidak berhasil |
| Persyaratan belum lengkap | Warning | Pengguna perlu melengkapi data |
| Informasi ketentuan pengajuan | Default / Gray | Informasi netral |
| Pengumuman penting | Brand | Penekanan informasi sesuai kebutuhan |

Pemetaan akhir harus sesuai dengan kondisi bisnis dan variant yang tersedia.

---

## 5. Alert Sizes & Breakpoints

### 5.1 Floating

**Description:**

Alert dengan layout yang tidak harus memenuhi seluruh lebar viewport.

**Recommended Usage:**

- Informasi pada area konten.
- Validasi pada card atau section.
- Pemberitahuan pada halaman detail.
- Pesan pada area yang memiliki batas lebar tertentu.

**AI Rules:**

- MUST menggunakan `Size=Floating` jika sesuai konteks.
- MUST mengikuti dimensi dan layout GEMS.
- MUST menjaga keterbacaan Title dan Description.
- MUST NOT menentukan lebar custom tanpa kebutuhan yang tervalidasi.

### 5.2 Full-width

**Description:**

Alert yang menggunakan pola lebar penuh sesuai area atau variant GEMS.

**Recommended Usage:**

- Informasi penting pada bagian atas halaman.
- Peringatan yang relevan untuk seluruh konten.
- Hasil validasi sebelum tabel atau proses lanjutan.
- Pesan yang membutuhkan perhatian pengguna dalam konteks halaman.

**AI Rules:**

- MUST menggunakan `Size=Full-width` sesuai variant GEMS.
- SHOULD ditempatkan dekat area atau proses yang relevan.
- MUST NOT menggunakan Full-width untuk seluruh pesan tanpa mempertimbangkan hierarki.

### 5.3 Desktop & Mobile

| Breakpoint | Usage |
|---|---|
| `Desktop` | Alert pada aplikasi web desktop |
| `Mobile` | Alert pada aplikasi mobile atau layout mobile |

**AI Rules:**

- MUST menggunakan Breakpoint sesuai target desain.
- MUST mengikuti struktur responsif GEMS.
- MUST memastikan teks tidak terpotong.
- MUST mempertahankan makna pesan pada seluruh breakpoint.
- MUST NOT menggunakan layout Desktop secara langsung pada Mobile tanpa penyesuaian.

---

## 6. Alert Content & Message Structure

### 6.1 Title

Title menjelaskan kondisi utama yang perlu diketahui pengguna.

**Guidelines:**

- MUST jelas dan spesifik.
- SHOULD singkat dan mudah dipindai.
- SHOULD menggunakan kalimat yang menjelaskan kondisi.
- MUST NOT menggunakan judul ambigu seperti "Perhatian" jika kondisi dapat dijelaskan lebih spesifik.
- MUST NOT menggunakan judul yang bertentangan dengan hasil proses.

**Examples:**

- Hasil Validasi Data Impor
- Informasi Belum Lengkap
- Data Gagal Dimuat
- Perubahan Berhasil Disimpan
- Sebagian Data Tidak Dapat Diproses

### 6.2 Description

Description memberikan informasi tambahan mengenai kondisi, dampak, atau langkah berikutnya.

**Guidelines:**

- MUST menjelaskan kondisi secara akurat.
- SHOULD menjelaskan dampak terhadap data atau proses.
- SHOULD memberikan instruksi jika pengguna perlu bertindak.
- MUST NOT menggunakan pesan teknis yang sulit dipahami pengguna.
- MUST NOT menampilkan informasi yang tidak didukung data sistem.

### 6.3 Message Formula

Untuk kondisi yang membutuhkan penjelasan, gunakan struktur:

**Condition → Impact → Next Action**

| Element | Purpose | Example |
|---|---|---|
| Condition | Apa yang terjadi | 20 data tidak valid |
| Impact | Apa dampaknya | Data tersebut tidak akan diimpor |
| Next Action | Apa yang perlu dilakukan | Periksa keterangan pada tabel |

### 6.4 Writing Rules

- MUST menggunakan bahasa yang sesuai dengan produk.
- MUST mempertahankan istilah bisnis yang benar.
- SHOULD menggunakan kalimat aktif dan langsung.
- SHOULD menghindari paragraf panjang.
- MUST NOT menyalahkan pengguna.
- MUST NOT menggunakan pesan seperti "Terjadi kesalahan" tanpa penjelasan jika informasi penyebab tersedia.
- MUST NOT memberikan instruksi yang tidak dapat dilakukan pengguna.

---

## 7. Validation Result Alert

### 7.1 Purpose

Validation Result Alert digunakan untuk menampilkan hasil pemeriksaan data sebelum pengguna melanjutkan proses, seperti impor, unggah, atau pengajuan.

Alert membantu pengguna mengetahui jumlah data yang valid, jumlah data yang bermasalah, serta dampaknya terhadap proses.

### 7.2 Example — Data Import Validation

**Title:**

Hasil Validasi Data Impor

**Description:**

180 data valid siap diimpor ke Daftar Registrasi Aset. 20 data tidak valid tidak akan diimpor. Periksa keterangan pada tabel untuk mengetahui penyebabnya.

**Recommended Configuration:**

| Property | Configuration |
|---|---|
| Component | Alert |
| Color | Warning |
| Size | Full-width |
| Breakpoint | Desktop |
| Title | Hasil Validasi Data Impor |
| Description | Ringkasan hasil validasi dan instruksi |
| Placement | Sebelum tabel hasil validasi |
| Close | Jika proses mengizinkan dismiss |

### 7.3 Validation Scenarios

| Scenario | Recommended Alert | Expected Information |
|---|---|---|
| Semua data valid | Success | Jumlah data valid dan proses berikutnya |
| Sebagian data tidak valid | Warning | Jumlah valid, tidak valid, dan dampaknya |
| Semua data tidak valid | Error / Warning sesuai kondisi | Alasan dan langkah perbaikan |
| Validasi gagal dijalankan | Error | Kegagalan validasi dan tindakan berikutnya |
| Validasi membutuhkan perhatian | Warning | Informasi yang perlu diperiksa |

### 7.4 AI Rules

- MUST menggunakan jumlah data aktual.
- MUST membedakan data valid dan tidak valid.
- MUST menjelaskan apakah data tidak valid akan dilewati atau memblokir seluruh proses.
- MUST NOT mengasumsikan semua data valid otomatis akan diimpor.
- MUST NOT mengasumsikan proses impor parsial selalu diperbolehkan.
- SHOULD menempatkan Alert sebelum tabel hasil validasi.
- SHOULD memberikan instruksi untuk memeriksa detail kesalahan.
- MUST NOT menampilkan hasil validasi yang belum dihitung sistem.

---

## 8. Incomplete Information Alert

### 8.1 Purpose

Incomplete Information Alert digunakan untuk memberitahukan bahwa terdapat informasi yang belum memenuhi persyaratan proses.

### 8.2 Recommended Context

- Form pengajuan belum lengkap.
- Dokumen wajib belum diunggah.
- Informasi perjalanan belum lengkap.
- Data registrasi belum memenuhi persyaratan.
- Informasi pendukung belum tersedia.

### 8.3 Example

**Title:**

Informasi Belum Lengkap

**Description:**

Lengkapi informasi yang wajib diisi sebelum mengirim pengajuan.

### 8.4 Behavior Rules

- MUST menampilkan informasi yang relevan dengan kondisi form.
- SHOULD membantu pengguna menemukan bagian yang belum lengkap.
- MUST menggunakan validasi field untuk menunjukkan kesalahan pada input terkait.
- MUST NOT menggantikan seluruh validasi field dengan satu Alert umum.
- MUST NOT mengizinkan proses berlanjut jika aturan bisnis menetapkan data wajib.
- SHOULD mempertahankan Alert selama kondisi belum terselesaikan jika informasi masih relevan.

---

## 9. Warning Alert

### 9.1 Purpose

Warning Alert digunakan untuk memberi perhatian terhadap kondisi yang dapat memengaruhi hasil proses, tetapi tidak selalu berarti proses gagal.

### 9.2 Recommended Context

- Sebagian data tidak valid.
- Data akan dilewati saat proses.
- Informasi perlu diperiksa.
- Terdapat kondisi yang berpotensi memengaruhi hasil.
- Pengguna perlu memahami dampak sebelum melanjutkan.

### 9.3 Example

**Title:**

Sebagian Data Tidak Dapat Diproses

**Description:**

Beberapa data tidak memenuhi persyaratan. Periksa detail data sebelum melanjutkan proses.

### 9.4 AI Rules

- MUST menjelaskan risiko atau kondisi secara spesifik.
- MUST menjelaskan dampak jika diketahui.
- SHOULD memberikan instruksi yang dapat dilakukan pengguna.
- MUST NOT menggunakan Warning untuk kegagalan total jika Error lebih sesuai.
- MUST NOT menggunakan Warning hanya untuk menarik perhatian visual.

---

## 10. Error Alert

### 10.1 Purpose

Error Alert digunakan untuk menjelaskan kesalahan atau kegagalan yang memengaruhi kemampuan pengguna menyelesaikan suatu proses.

### 10.2 Recommended Context

- Data gagal dimuat.
- Validasi gagal diproses.
- Impor data gagal.
- Permintaan tidak dapat diproses.
- Terjadi masalah yang memerlukan perbaikan atau percobaan ulang.

### 10.3 Example

**Title:**

Data Gagal Dimuat

**Description:**

Data belum dapat ditampilkan. Silakan coba kembali.

### 10.4 Error Message Rules

- MUST menjelaskan proses yang gagal.
- SHOULD menjelaskan tindakan berikutnya.
- MUST NOT menyatakan proses berhasil jika sistem mengembalikan error.
- MUST NOT menampilkan detail teknis internal yang tidak relevan.
- MUST NOT mengasumsikan penyebab kegagalan jika sistem tidak menyediakannya.
- SHOULD mempertahankan pesan selama masalah masih memengaruhi halaman.
- MUST menggunakan Empty State atau pola error page jika seluruh konten tidak dapat ditampilkan dan desain memerlukannya.

---

## 11. Success & Informational Alert

### 11.1 Success Alert

**Purpose:**

Menampilkan hasil proses berhasil ketika informasi tersebut perlu tetap terlihat pada halaman.

**Recommended Context:**

- Validasi selesai dengan hasil berhasil.
- Proses berhasil dan hasilnya memerlukan penjelasan.
- Perubahan berhasil dengan informasi lanjutan.

**Example:**

**Title:** Validasi Data Berhasil

**Description:** Seluruh data telah berhasil divalidasi dan siap diproses.

**AI Rules:**

- MUST menggunakan kondisi keberhasilan yang telah dikonfirmasi.
- MUST NOT menampilkan Success sebelum proses selesai.
- SHOULD menggunakan Toast jika hanya diperlukan feedback singkat.
- SHOULD menggunakan Alert jika pengguna perlu membaca informasi lanjutan.

### 11.2 Informational Alert

**Purpose:**

Menampilkan informasi, ketentuan, atau instruksi yang relevan dengan halaman.

**Recommended Context:**

- Ketentuan proses.
- Informasi persyaratan.
- Penjelasan dampak perubahan.
- Informasi operasional.

**Example:**

**Title:** Informasi Pengajuan

**Description:** Pastikan seluruh informasi telah sesuai sebelum mengirim pengajuan.

**AI Rules:**

- MUST menggunakan informasi yang relevan.
- SHOULD menggunakan warna netral atau Brand sesuai konteks.
- MUST NOT menggunakan Error atau Warning jika tidak terdapat kondisi kesalahan atau risiko.
- MUST NOT mengubah informasi biasa menjadi peringatan tanpa alasan.

---

## 12. Alert Placement & Layout Patterns

### 12.1 Page-Level Alert

**When to Use:**

Informasi berlaku untuk seluruh halaman atau proses utama.

**Recommended Placement:**

- Setelah Page Header.
- Sebelum konten utama.
- Sebelum tabel atau form yang berkaitan.

**AI Rules:**

- MUST mempertahankan hubungan Alert dengan konteks halaman.
- SHOULD menggunakan Full-width jika sesuai desain.
- MUST NOT menempatkan Alert terlalu jauh dari informasi yang dijelaskan.

### 12.2 Section-Level Alert

**When to Use:**

Informasi hanya berlaku untuk satu section atau kelompok data.

**Recommended Placement:**

- Di dalam section terkait.
- Sebelum informasi yang terpengaruh.
- Dekat form atau tabel yang memerlukan perhatian.

### 12.3 Form-Level Alert

**When to Use:**

Terdapat kondisi yang memengaruhi pengisian atau pengiriman form.

**AI Rules:**

- SHOULD menempatkan Alert dekat form.
- MUST mempertahankan validasi individual pada field yang bermasalah.
- MUST NOT menggunakan Alert sebagai satu-satunya indikator field wajib yang belum diisi.

### 12.4 Table-Level Alert

**When to Use:**

Informasi berkaitan dengan data yang ditampilkan pada tabel.

**Recommended Context:**

- Hasil validasi impor.
- Sebagian data gagal diproses.
- Data tertentu tidak memenuhi persyaratan.
- Informasi yang memengaruhi seluruh atau sebagian baris tabel.

**AI Rules:**

- SHOULD menempatkan Alert sebelum tabel.
- MUST menjelaskan hubungan pesan dengan data.
- SHOULD menyediakan detail per baris apabila diperlukan.
- MUST NOT menggantikan informasi kesalahan pada tabel dengan Alert umum jika detail baris diperlukan.

### 12.5 Mobile Alert

**When to Use:**

Informasi penting pada aplikasi atau layout mobile.

**AI Rules:**

- MUST menggunakan variant Mobile.
- MUST mempertahankan hierarki Title dan Description.
- MUST memastikan pesan tetap terbaca.
- SHOULD menghindari pesan terlalu panjang.
- MUST NOT menutup konten penting secara tidak perlu.

---

## 13. Alert States & Interaction Behavior

### 13.1 Default Behavior

Alert menampilkan pesan berdasarkan kondisi sistem atau kebutuhan informasi.

**Expected Behavior:**

- Alert muncul ketika kondisi pemicu terpenuhi.
- Pesan sesuai dengan kondisi aktual.
- Alert dapat diperbarui ketika data berubah.
- Alert tidak mengubah data hanya karena ditampilkan.

### 13.2 Dismissible Alert

Jika variant dan requirement mendukung close:

- Pengguna dapat menutup Alert.
- Penutupan hanya menyembunyikan pesan sesuai aturan.
- Penutupan tidak otomatis menyelesaikan masalah.
- Kondisi error atau warning yang masih berlaku tetap harus ditangani oleh sistem.

**AI Rules:**

- MUST NOT menganggap semua Alert dapat ditutup.
- MUST NOT membuat close mengubah status bisnis.
- MUST NOT menghilangkan informasi kritis tanpa mekanisme yang sesuai.
- MUST mengikuti perilaku dismiss yang ditentukan.

### 13.3 Alert with Action

Jika Alert memiliki tindakan lanjutan:

- Gunakan action yang relevan.
- Pastikan label action menjelaskan tindakan.
- Gunakan komponen Button sesuai GEMS.
- Ikuti workflow dan hak akses.

**Example Actions:**

- Coba Lagi
- Periksa Data
- Lihat Detail

**AI Rules:**

- MUST NOT menambahkan action yang tidak tersedia pada requirement.
- MUST NOT menggunakan Alert untuk menjalankan aksi destruktif tanpa konfirmasi yang diperlukan.
- MUST NOT menambahkan Button custom di luar pola GEMS.

### 13.4 State Changes

| Condition | Expected Behavior |
|---|---|
| Kondisi baru terdeteksi | Alert ditampilkan |
| Informasi berubah | Pesan diperbarui |
| Masalah terselesaikan | Alert diperbarui atau dihilangkan sesuai requirement |
| Pengguna menutup Alert | Pesan disembunyikan jika dismiss diizinkan |
| Proses gagal | Alert menampilkan kondisi kegagalan |
| Proses berhasil | Pesan diperbarui sesuai hasil aktual |

---

## 14. Accessibility Rules

### 14.1 Visual Accessibility

- MUST memastikan teks mudah dibaca.
- MUST menjaga kontras teks dan latar.
- MUST NOT menyampaikan kondisi hanya melalui warna.
- SHOULD menggunakan ikon dan teks yang mendukung pemahaman.
- MUST menjaga hierarki Title dan Description.
- MUST memastikan layout tetap terbaca pada Desktop dan Mobile.

### 14.2 Screen Reader Accessibility

- MUST menggunakan semantik aksesibilitas yang sesuai dengan tingkat urgensi.
- SHOULD menggunakan `role="alert"` untuk pesan mendesak yang perlu segera diumumkan.
- SHOULD menggunakan `role="status"` untuk informasi nonmendesak yang perlu diumumkan.
- MUST NOT menggunakan live announcement mendesak untuk seluruh Alert tanpa mempertimbangkan konteks.
- MUST memastikan Title dan Description dapat dibaca secara logis.

### 14.3 Keyboard Accessibility

- MUST memastikan Close dan Action dapat diakses dengan keyboard jika tersedia.
- MUST memberikan accessible name pada tombol Close.
- MUST mempertahankan fokus yang logis.
- MUST NOT menjadikan seluruh container Alert fokus keyboard jika tidak memiliki interaksi.

### 14.4 Content Accessibility

- MUST menggunakan pesan yang mudah dipahami.
- SHOULD menghindari istilah teknis internal.
- SHOULD memberikan instruksi yang jelas.
- MUST NOT mengandalkan ikon saja untuk menjelaskan kondisi.

---

## 15. AI Alert Selection Workflow

1. **Read HSD/BRD:** Identifikasi kondisi yang perlu dikomunikasikan.
2. **Determine Message Purpose:** Tentukan apakah pesan merupakan informasi, peringatan, kesalahan, keberhasilan, atau hasil validasi.
3. **Validate Component Choice:** Pastikan Alert lebih tepat dibanding Toast, Modal, Badge, atau Empty State.
4. **Select Color:** Pilih `Default`, `Brand`, `Gray`, `Error`, `Warning`, atau `Success`.
5. **Select Size:** Pilih `Floating` atau `Full-width`.
6. **Select Breakpoint:** Gunakan `Desktop` atau `Mobile`.
7. **Define Content:** Susun Title dan Description.
8. **Explain Impact:** Jelaskan dampak terhadap data atau proses jika diperlukan.
9. **Define Next Action:** Berikan instruksi jika pengguna perlu bertindak.
10. **Define Interaction:** Tentukan apakah Close atau Action diperlukan dan didukung.
11. **Determine Placement:** Tempatkan Alert dekat konteks yang relevan.
12. **Verify Data Accuracy:** Pastikan jumlah, status, dan hasil proses sesuai data.
13. **Verify Accessibility:** Periksa keterbacaan, kontras, semantik, dan interaksi.
14. **Verify Figma:** Pastikan property dan kombinasi variant sesuai GEMS.
15. **Human Approval:** Minta persetujuan untuk pola baru yang belum ditentukan.

---

## 16. AI Restrictions

AI MUST NOT:

1. Membuat Color variant di luar GEMS tanpa persetujuan.
2. Membuat Size selain `Floating` atau `Full-width` tanpa persetujuan.
3. Membuat Breakpoint custom tanpa persetujuan.
4. Menggunakan kombinasi property yang tidak tersedia.
5. Menggunakan Alert untuk seluruh feedback sistem.
6. Menggantikan Toast dengan Alert tanpa alasan.
7. Menggantikan Modal konfirmasi dengan Alert.
8. Menggantikan field validation dengan Alert umum.
9. Menggantikan Badge status dengan Alert.
10. Menggunakan Error untuk informasi netral.
11. Menggunakan Success sebelum keberhasilan dikonfirmasi.
12. Menggunakan Warning hanya untuk menarik perhatian.
13. Membuat hasil validasi palsu.
14. Membuat jumlah data valid atau tidak valid tanpa sumber.
15. Mengasumsikan impor parsial selalu diperbolehkan.
16. Menghilangkan dampak proses dari pesan ketika informasi tersebut penting.
17. Menampilkan pesan ambigu tanpa konteks.
18. Menggunakan istilah teknis yang tidak dipahami pengguna.
19. Menganggap semua Alert dismissible.
20. Menganggap tombol Close menyelesaikan masalah.
21. Menambahkan action tanpa requirement.
22. Mengubah status bisnis melalui Alert tanpa workflow yang sesuai.
23. Menampilkan informasi kritis hanya melalui warna atau ikon.
24. Mengabaikan perbedaan layout Desktop dan Mobile.
25. Membuat pola interaksi baru tanpa Human Approval.

---

## 17. Implementation Requirements

### 17.1 Source of Truth

| Source | Responsibility |
|---|---|
| HSD / BRD | Kondisi bisnis, pesan, hasil proses, aturan validasi, dan hak akses |
| GEMS Design System | Color, Size, Breakpoint, struktur, dan visual Alert |
| System Data | Nilai aktual, jumlah data, hasil validasi, dan status proses |
| Human Approval | Persetujuan pola atau behavior baru yang belum ditentukan |

### 17.2 Final AI Instruction

When generating UI/UX designs, AI MUST:

1. Read the HSD/BRD to identify the condition requiring user attention.
2. Use the official GEMS Alert component.
3. Select supported Color, Size, and Breakpoint variants.
4. Write a clear Title and Description.
5. Explain the condition, its impact, and the next action when relevant.
6. Use actual system data for validation results and process outcomes.
7. Place the Alert near the related content or workflow.
8. Distinguish Alert from Toast, Modal, Badge, and Empty State.
9. Use appropriate accessibility semantics and keyboard interactions.
10. Avoid inventing messages, values, variants, or workflow behaviors.
11. Request Human Approval before introducing unsupported component behavior.

---

## 18. Official Figma Reference

| Component | Purpose | Figma Design |
|---|---|---|
| GEMS Alert | Official Alert component, colors, sizes, and responsive variants | [Open GEMS Alert Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=612-8756&t=oti8QS9H602K2cYU-1) |
