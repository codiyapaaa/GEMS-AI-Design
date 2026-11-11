# GEMS Design System — Notification Guidelines

## 1. Purpose & Core Principles

Notification merupakan komponen komunikasi visual yang digunakan untuk menyampaikan pemberitahuan, feedback hasil tindakan, perubahan kondisi, atau informasi proses kepada pengguna.

Notification membantu pengguna mengetahui apakah tindakan berhasil, gagal, memerlukan perhatian, atau masih berlangsung tanpa harus memeriksa ulang seluruh halaman.

### 1.1 Primary Purposes

- Memberikan feedback setelah pengguna melakukan tindakan.
- Menyampaikan keberhasilan proses.
- Menyampaikan kegagalan atau kesalahan proses.
- Memberikan peringatan yang relevan.
- Menampilkan informasi atau pembaruan sistem.
- Menampilkan progress suatu proses.
- Menyampaikan pemberitahuan terkait aktivitas atau entitas.

### 1.2 Core Principles

1. Notification harus relevan dengan aktivitas pengguna.
2. Pesan harus menjelaskan kondisi atau hasil proses secara akurat.
3. Tingkat urgensi harus sesuai dengan makna informasi.
4. Notification tidak boleh mengganggu alur kerja secara berlebihan.
5. Notification harus menggunakan variant resmi GEMS.
6. Notification tidak boleh digunakan untuk menggantikan konfirmasi tindakan.
7. Informasi penting tidak boleh hilang sebelum pengguna memiliki kesempatan yang memadai untuk memahaminya.
8. Notification tidak boleh mengubah status bisnis hanya karena ditampilkan atau ditutup.

### 1.3 AI Rules

- MUST menggunakan komponen Notification resmi GEMS.
- MUST menentukan isi pesan berdasarkan kondisi aktual dan HSD/BRD.
- MUST memilih Type sesuai tujuan pesan.
- MUST menggunakan Breakpoint dan Position yang didukung GEMS.
- MUST NOT menampilkan feedback keberhasilan sebelum proses berhasil.
- MUST NOT membuat informasi atau hasil proses yang tidak tersedia.
- MUST NOT menggunakan Notification sebagai pengganti Modal konfirmasi.

---

## 2. When to Use Notification

### 2.1 Recommended Usage

| Context | When to Use | Example |
|---|---|---|
| Action Success | Tindakan berhasil diselesaikan | Data berhasil disimpan |
| Action Error | Tindakan gagal diproses | Data gagal disimpan |
| Submission Feedback | Hasil pengajuan atau pengiriman | Pesanan tamu berhasil diajukan |
| Delete Feedback | Hasil penghapusan data | Data berhasil dihapus |
| Update Feedback | Hasil perubahan data | Perubahan berhasil disimpan |
| Warning Feedback | Kondisi membutuhkan perhatian | Sebagian perubahan tidak dapat disimpan |
| System Information | Pembaruan sistem yang relevan | Informasi telah diperbarui |
| Process Progress | Proses masih berlangsung | Mengunggah dokumen |
| Activity Notification | Pemberitahuan terkait aktivitas | Pengajuan telah diperbarui |

### 2.2 When NOT to Use Notification

| Requirement | Reason | Recommended Component |
|---|---|---|
| Menampilkan hasil validasi yang harus diperiksa sebelum melanjutkan | Informasi perlu terlihat bersama data | Alert |
| Menjelaskan kesalahan pada satu field | Membutuhkan feedback dekat input | Input Validation |
| Meminta konfirmasi hapus | Membutuhkan keputusan eksplisit | Modal |
| Meminta konfirmasi pengiriman | Membutuhkan keputusan pengguna | Modal |
| Menampilkan status pada tabel | Informasi status bersifat ringkas | Badge |
| Menampilkan halaman tanpa data | Membutuhkan tampilan khusus | Empty State |
| Menampilkan informasi panjang yang harus terus tersedia | Membutuhkan konteks halaman | Alert atau konten halaman |
| Menjalankan aksi utama | Notification bukan kontrol aksi utama | Button |

### 2.3 Selection Rules

- MUST menggunakan Notification ketika sistem perlu memberikan feedback atas suatu aktivitas.
- SHOULD menggunakan Notification untuk hasil simpan, ubah, hapus, dan kirim.
- SHOULD menggunakan Notification untuk proses yang sedang berlangsung jika diperlukan.
- MUST menggunakan Alert jika informasi perlu diperiksa dalam konteks halaman.
- MUST menggunakan Modal untuk tindakan yang membutuhkan konfirmasi.
- MUST NOT menggunakan Notification untuk setiap perubahan kecil yang tidak membutuhkan feedback.
- MUST NOT menampilkan Notification berulang untuk satu kejadian yang sama tanpa alasan.

---

## 3. Notification Component Structure

GEMS Design System menyediakan Notification dengan variasi Type, Breakpoint, dan Position.

### 3.1 Official Properties

| Property | Available Values |
|---|---|
| `Type` | `Avatar`, `Image`, `Primary icon`, `Success icon`, `Error icon`, `Warning icon`, `Gray icon`, `No icon`, `Progress indicator` |
| `Breakpoint` | `Desktop`, `Mobile` |
| `Position` | `Top`, `Bottom` |

Ketersediaan kombinasi property mengikuti variant yang tersedia pada GEMS.

### 3.2 Component Elements

| Element | Description | Usage |
|---|---|---|
| Container | Area visual Notification | Required |
| Title | Informasi utama | Menjelaskan hasil atau kondisi |
| Description | Informasi pendukung | Menjelaskan detail atau tindakan |
| Icon | Indikator visual | Sesuai Type |
| Avatar | Identitas pengguna atau entitas | Jika menggunakan Avatar |
| Image | Gambar pendukung | Jika menggunakan Image |
| Progress Indicator | Indikator proses | Jika menggunakan Progress indicator |
| Close Control | Menutup Notification | Jika didukung variant dan behavior |
| Action | Tindakan lanjutan | Jika didukung variant dan requirement |

Tidak seluruh elemen harus digunakan secara bersamaan.

### 3.3 Component Rules

- MUST menggunakan Type resmi GEMS.
- MUST menggunakan kombinasi property yang tersedia.
- MUST mengikuti struktur, typography, spacing, icon, dan visual GEMS.
- MUST NOT membuat Type baru tanpa persetujuan.
- MUST NOT menambahkan elemen interaktif yang tidak didukung tanpa validasi.
- SHOULD mempertahankan struktur Notification yang konsisten pada seluruh aplikasi.

---

## 4. Notification Types & Selection

### 4.1 Success Icon

**Purpose:**

Menampilkan feedback ketika tindakan atau proses berhasil.

**Recommended Context:**

- Data berhasil disimpan.
- Data berhasil diperbarui.
- Pengajuan berhasil dikirim.
- Data berhasil dihapus.
- Proses berhasil diselesaikan.

**AI Rules:**

- MUST menggunakan hasil keberhasilan yang telah dikonfirmasi.
- MUST NOT menampilkan Success sebelum proses selesai.
- SHOULD menggunakan judul yang menjelaskan tindakan yang berhasil.
- SHOULD menghindari deskripsi panjang jika hasil sudah jelas.

### 4.2 Error Icon

**Purpose:**

Menampilkan feedback ketika tindakan atau proses gagal.

**Recommended Context:**

- Data gagal disimpan.
- Pengajuan gagal dikirim.
- Penghapusan gagal.
- Proses tidak dapat diselesaikan.

**AI Rules:**

- MUST menjelaskan tindakan yang gagal.
- SHOULD memberikan instruksi berikutnya jika tersedia.
- MUST NOT menyatakan penyebab teknis tanpa informasi yang valid.
- MUST NOT menampilkan pesan keberhasilan ketika sistem mengembalikan kegagalan.

### 4.3 Warning Icon

**Purpose:**

Menampilkan pemberitahuan yang membutuhkan perhatian pengguna.

**Recommended Context:**

- Tindakan hanya berhasil sebagian.
- Terdapat kondisi yang perlu diperhatikan.
- Informasi memerlukan pemeriksaan.

**AI Rules:**

- MUST menjelaskan kondisi yang memerlukan perhatian.
- SHOULD menjelaskan dampak atau tindakan berikutnya.
- MUST NOT menggunakan Warning hanya untuk menarik perhatian visual.

### 4.4 Primary Icon

**Purpose:**

Menampilkan informasi atau pemberitahuan dengan ikon utama sesuai GEMS.

**Recommended Context:**

- Informasi aktivitas.
- Pembaruan sistem.
- Pemberitahuan umum.

**AI Rules:**

- MUST menggunakan ikon yang sesuai dengan informasi.
- MUST NOT menggunakan Primary Icon untuk menggantikan Error atau Warning jika makna semantik tersebut lebih tepat.

### 4.5 Gray Icon

**Purpose:**

Menampilkan pemberitahuan dengan penekanan visual netral.

**Recommended Context:**

- Informasi umum.
- Pembaruan nonkritis.
- Aktivitas yang tidak memiliki status keberhasilan atau kegagalan.

### 4.6 No Icon

**Purpose:**

Menampilkan Notification tanpa ikon.

**Recommended Context:**

- Pesan sederhana.
- Feedback ringkas yang tetap jelas tanpa indikator visual.

**AI Rules:**

- MUST memastikan teks menyampaikan makna secara mandiri.
- MUST NOT menghilangkan informasi penting hanya karena ikon tidak digunakan.

### 4.7 Avatar

**Purpose:**

Menampilkan pemberitahuan yang berkaitan dengan seseorang atau identitas tertentu.

**Recommended Context:**

- Aktivitas pengguna.
- Pemberitahuan dari seseorang.
- Pembaruan terkait entitas dengan avatar.

**AI Rules:**

- MUST menggunakan identitas yang relevan.
- MUST NOT menggunakan avatar acak untuk informasi sistem.
- MUST menjaga keterbacaan informasi utama.

### 4.8 Image

**Purpose:**

Menampilkan pemberitahuan yang membutuhkan gambar pendukung.

**Recommended Context:**

- Pemberitahuan terkait konten visual.
- Informasi aktivitas yang memiliki gambar relevan.

**AI Rules:**

- MUST menggunakan gambar yang relevan.
- MUST NOT menambahkan gambar dekoratif tanpa kebutuhan.
- MUST memastikan informasi tetap dapat dipahami jika gambar tidak tersedia.

### 4.9 Progress Indicator

**Purpose:**

Menampilkan pemberitahuan mengenai proses yang sedang berlangsung.

**Recommended Context:**

- Mengunggah file.
- Mengimpor data.
- Memproses permintaan.
- Menjalankan proses yang membutuhkan waktu.

**AI Rules:**

- MUST menampilkan status proses yang sesuai.
- MUST NOT menampilkan proses selesai sebelum dikonfirmasi.
- SHOULD memperbarui informasi ketika progress berubah.
- MUST NOT membuat persentase progress jika sistem tidak menyediakannya.
- MUST membedakan progress aktual dari indikator aktivitas tanpa persentase.

---

## 5. Notification Breakpoints

### 5.1 Desktop

**Recommended Usage:**

- Feedback pada aplikasi web.
- Pemberitahuan setelah tindakan.
- Informasi aktivitas.
- Progress proses.

**AI Rules:**

- MUST menggunakan `Breakpoint=Desktop`.
- MUST mengikuti dimensi dan struktur GEMS.
- MUST memastikan Notification tidak menutupi kontrol penting secara tidak perlu.

### 5.2 Mobile

**Recommended Usage:**

- Feedback pada aplikasi mobile.
- Hasil submit atau pengajuan.
- Kesalahan proses.
- Informasi aktivitas.

**AI Rules:**

- MUST menggunakan `Breakpoint=Mobile`.
- MUST mengikuti layout mobile GEMS.
- MUST menjaga keterbacaan Title dan Description.
- MUST NOT menggunakan dimensi Desktop secara langsung pada Mobile.
- SHOULD menghindari pesan terlalu panjang.

---

## 6. Notification Position

### 6.1 Top Position

**Purpose:**

Menampilkan Notification pada posisi atas sesuai layout GEMS.

**Recommended Context:**

- Feedback setelah tindakan.
- Pemberitahuan sistem.
- Informasi yang perlu segera diketahui.

### 6.2 Bottom Position

**Purpose:**

Menampilkan Notification pada posisi bawah sesuai variant GEMS.

**Recommended Context:**

- Feedback proses.
- Pemberitahuan yang tidak menghalangi konten utama.
- Informasi singkat setelah aksi.

### 6.3 Position Rules

- MUST menggunakan Position yang tersedia pada variant.
- MUST mempertahankan konsistensi posisi dalam aplikasi.
- MUST NOT menempatkan Notification secara acak.
- MUST NOT menutupi tombol, input, atau navigasi penting.
- MUST mempertimbangkan viewport dan breakpoint.
- MUST NOT mengasumsikan semua Position tersedia pada seluruh Breakpoint.

---

## 7. Notification Content & Message Structure

### 7.1 Title

Title menjelaskan hasil tindakan atau kondisi utama.

**Guidelines:**

- MUST jelas dan spesifik.
- SHOULD menggunakan kalimat singkat.
- SHOULD menyebutkan objek atau tindakan.
- MUST NOT menggunakan judul ambigu jika kondisi dapat dijelaskan.
- MUST NOT menggunakan judul yang tidak sesuai dengan hasil proses.

**Examples:**

- Data Berhasil Disimpan
- Data Gagal Disimpan
- Pesanan Tamu Berhasil Diajukan
- Pesanan Tamu Gagal Diajukan
- Data Berhasil Dihapus
- Dokumen Sedang Diunggah

### 7.2 Description

Description memberikan informasi pendukung jika diperlukan.

**Guidelines:**

- MUST sesuai dengan kondisi aktual.
- SHOULD menjelaskan tindakan berikutnya jika proses gagal.
- SHOULD menghindari pengulangan judul.
- MUST NOT menggunakan informasi teknis internal yang tidak relevan.
- MUST NOT menjanjikan hasil yang belum dikonfirmasi.

### 7.3 Message Formula

Gunakan struktur:

**Action / Condition → Result → Next Step (if needed)**

| Element | Purpose | Example |
|---|---|---|
| Action | Tindakan yang dilakukan | Pengajuan pesanan tamu |
| Result | Hasil tindakan | Berhasil diajukan |
| Next Step | Tindakan berikutnya | Menunggu proses Catering |

### 7.4 Writing Rules

- MUST menggunakan bahasa sesuai produk.
- MUST mempertahankan istilah bisnis dari HSD/BRD.
- SHOULD menggunakan kalimat aktif dan langsung.
- SHOULD menggunakan pesan ringkas.
- MUST NOT menggunakan bahasa yang menyalahkan pengguna.
- MUST NOT menggunakan pesan teknis yang sulit dipahami.
- MUST NOT membuat informasi tambahan yang tidak tersedia.

---

## 8. Success Notification Patterns

### 8.1 Create Success

**Title:** Data Berhasil Ditambahkan

**Description:** Data baru berhasil disimpan.

### 8.2 Update Success

**Title:** Perubahan Berhasil Disimpan

**Description:** Informasi telah diperbarui.

### 8.3 Delete Success

**Title:** Data Berhasil Dihapus

**Description:** Data telah dihapus dari daftar.

### 8.4 Submit Success

**Title:** Pesanan Tamu Berhasil Diajukan

**Description:** Pesanan tamu telah dikirim untuk diproses.

### 8.5 Success Rules

- MUST menampilkan hasil sesuai tindakan.
- MUST menggunakan informasi keberhasilan aktual.
- SHOULD menghindari pesan yang terlalu panjang.
- MUST NOT menampilkan Success ketika proses masih berlangsung.
- MUST NOT menganggap pengajuan berhasil berarti seluruh workflow telah selesai.

---

## 9. Error Notification Patterns

### 9.1 Create Error

**Title:** Data Gagal Ditambahkan

**Description:** Data belum berhasil disimpan. Silakan coba kembali.

### 9.2 Update Error

**Title:** Perubahan Gagal Disimpan

**Description:** Perubahan belum berhasil disimpan. Silakan coba kembali.

### 9.3 Delete Error

**Title:** Data Gagal Dihapus

**Description:** Data belum dapat dihapus. Silakan coba kembali.

### 9.4 Submit Error

**Title:** Pesanan Tamu Gagal Diajukan

**Description:** Pengajuan belum berhasil dikirim. Silakan coba kembali.

### 9.5 Error Rules

- MUST menjelaskan tindakan yang gagal.
- MUST menggunakan hasil proses aktual.
- SHOULD memberikan instruksi yang dapat dilakukan.
- MUST NOT menghapus input pengguna secara otomatis tanpa kebutuhan.
- MUST NOT menampilkan pesan Success setelah kegagalan.
- SHOULD menyediakan mekanisme retry jika didukung sistem.
- MUST NOT mengasumsikan seluruh kegagalan dapat diselesaikan dengan retry.

---

## 10. Warning & Informational Notification Patterns

### 10.1 Warning Notification

**When to Use:**

Kondisi memerlukan perhatian pengguna tetapi tidak selalu merupakan kegagalan total.

**Example:**

**Title:** Sebagian Data Belum Diproses

**Description:** Beberapa data memerlukan pemeriksaan sebelum proses dilanjutkan.

**AI Rules:**

- MUST menjelaskan kondisi yang memerlukan perhatian.
- MUST NOT menyamakan Warning dengan Error.
- SHOULD menjelaskan dampak jika relevan.

### 10.2 Informational Notification

**When to Use:**

Memberikan informasi atau pembaruan yang relevan.

**Example:**

**Title:** Informasi Telah Diperbarui

**Description:** Terdapat pembaruan informasi pada data terkait.

**AI Rules:**

- MUST menggunakan informasi yang benar.
- SHOULD menghindari pesan yang tidak memberikan nilai bagi pengguna.
- MUST NOT menggunakan Error atau Warning untuk informasi biasa.

---

## 11. Progress Notification Patterns

### 11.1 Purpose

Progress Notification digunakan ketika sistem sedang menjalankan proses yang membutuhkan waktu.

### 11.2 Recommended Context

- Upload dokumen.
- Import data.
- Sinkronisasi data.
- Pemrosesan file.
- Pengiriman data dalam jumlah besar.

### 11.3 Example

**Title:** Mengimpor Data

**Description:** Sistem sedang memproses data. Mohon tunggu hingga proses selesai.

### 11.4 Progress States

| State | Expected Behavior |
|---|---|
| Started | Notification menunjukkan proses dimulai |
| In Progress | Informasi progress diperbarui |
| Completed | Notification menunjukkan hasil berhasil |
| Failed | Notification menunjukkan kegagalan |
| Cancelled | Notification mengikuti status pembatalan jika tersedia |

### 11.5 AI Rules

- MUST menggunakan status proses aktual.
- MUST NOT membuat persentase progress tanpa data.
- MUST NOT menampilkan Completed sebelum proses selesai.
- MUST menjelaskan kegagalan jika proses gagal.
- SHOULD menjaga Notification tetap relevan selama proses berlangsung.
- MUST mengikuti aturan pembatalan jika proses dapat dibatalkan.

---

## 12. Notification States & Interaction Behavior

### 12.1 Default Behavior

Notification muncul ketika sistem menghasilkan event atau kondisi yang membutuhkan pemberitahuan.

**Expected Behavior:**

- Menampilkan pesan sesuai event.
- Menggunakan Type yang sesuai.
- Muncul pada Position yang ditentukan.
- Tidak mengubah data ketika ditampilkan.

### 12.2 Dismiss Behavior

Jika Notification mendukung Close:

- Pengguna dapat menutup Notification.
- Close hanya menutup tampilan Notification.
- Close tidak membatalkan hasil tindakan.
- Close tidak mengubah status bisnis.

**AI Rules:**

- MUST NOT menganggap seluruh Notification memiliki Close.
- MUST NOT membuat Close membatalkan proses tanpa requirement.
- MUST mempertahankan aksesibilitas tombol Close.

### 12.3 Auto Dismiss

Notification dapat memiliki durasi tampil sesuai kebutuhan produk.

**AI Rules:**

- MUST mengikuti aturan durasi yang ditetapkan.
- MUST NOT mengasumsikan seluruh Notification otomatis hilang.
- SHOULD mempertimbangkan panjang pesan dan kebutuhan membaca.
- MUST NOT menghilangkan informasi kritis sebelum pengguna dapat memahaminya.
- SHOULD mempertahankan pesan error penting atau menyediakan cara mengaksesnya kembali jika diperlukan.

### 12.4 Action Notification

Jika Notification memiliki action:

- Action harus relevan.
- Label harus jelas.
- Action harus mengikuti hak akses dan workflow.
- Gunakan komponen GEMS yang sesuai.

**Example Actions:**

- Lihat Detail
- Coba Lagi
- Buka Pengajuan

**AI Rules:**

- MUST NOT menambahkan action tanpa requirement.
- MUST NOT menjalankan tindakan destruktif tanpa konfirmasi yang diperlukan.
- MUST NOT mengubah workflow melalui Notification tanpa aturan yang sesuai.

---

## 13. Notification Trigger & Display Logic

### 13.1 Trigger Rules

Notification ditampilkan berdasarkan event atau hasil sistem.

| Trigger | Recommended Notification |
|---|---|
| Create succeeded | Success icon |
| Create failed | Error icon |
| Update succeeded | Success icon |
| Update failed | Error icon |
| Delete succeeded | Success icon |
| Delete failed | Error icon |
| Submit succeeded | Success icon |
| Submit failed | Error icon |
| Process running | Progress indicator |
| Condition requires attention | Warning icon |
| General activity update | Primary icon / Gray icon |

### 13.2 Duplicate Notification

- SHOULD menghindari Notification identik yang muncul berulang akibat satu event.
- SHOULD mengelola beberapa event agar pesan tetap mudah dipahami.
- MUST NOT menampilkan hasil yang saling bertentangan untuk satu proses.

### 13.3 Multiple Notifications

- MUST mengikuti pola penumpukan atau antrean yang ditentukan produk.
- SHOULD menghindari Notification berlebihan.
- MUST mempertahankan urutan informasi yang logis.
- MUST NOT membuat aturan stacking baru tanpa validasi.

### 13.4 Navigation Behavior

- Notification tidak otomatis mengubah halaman.
- Navigasi hanya terjadi jika pengguna memilih action atau workflow memang mengharuskannya.
- MUST NOT mengarahkan pengguna ke halaman lain tanpa requirement.

---

## 14. Notification vs Alert vs Modal

### 14.1 Component Comparison

| Component | Primary Purpose | Typical Usage |
|---|---|---|
| Notification | Feedback atau pemberitahuan sistem | Berhasil simpan, gagal submit, progress |
| Alert | Informasi penting dalam konteks halaman | Hasil validasi, peringatan pada form atau tabel |
| Modal | Konfirmasi atau keputusan pengguna | Konfirmasi hapus, kirim, atau batalkan |

### 14.2 Selection Examples

| Scenario | Recommended Component |
|---|---|
| Pengguna klik Simpan dan berhasil | Notification |
| Pengguna klik Simpan dan gagal | Notification |
| Pengguna ingin menghapus data | Modal untuk konfirmasi |
| Data berhasil dihapus | Notification |
| Hasil validasi menunjukkan sebagian data tidak valid | Alert |
| Field wajib belum diisi | Input Validation |
| Proses import sedang berlangsung | Notification dengan Progress indicator jika sesuai |
| Pengguna perlu membaca risiko sebelum melanjutkan | Alert |
| Pengguna harus menyetujui tindakan berisiko | Modal |

### 14.3 AI Rules

- MUST membedakan feedback sementara dari informasi kontekstual.
- MUST menggunakan Notification untuk hasil tindakan ketika pola feedback sesuai.
- MUST menggunakan Alert untuk informasi yang perlu tetap terlihat bersama konten.
- MUST menggunakan Modal untuk keputusan yang membutuhkan konfirmasi.
- MUST NOT menggunakan ketiga komponen secara bersamaan untuk satu pesan tanpa kebutuhan yang jelas.

---

## 15. Accessibility Rules

### 15.1 Visual Accessibility

- MUST memastikan teks mudah dibaca.
- MUST mempertahankan kontras yang memadai.
- MUST NOT menyampaikan hasil hanya melalui warna.
- SHOULD menggunakan ikon yang mendukung makna.
- MUST memastikan layout terbaca pada Desktop dan Mobile.

### 15.2 Screen Reader Accessibility

- SHOULD menggunakan `role="status"` untuk feedback nonmendesak.
- SHOULD menggunakan `role="alert"` untuk kegagalan atau kondisi mendesak yang perlu segera diumumkan.
- MUST NOT menggunakan pengumuman mendesak untuk seluruh Notification.
- MUST memastikan Title dan Description dapat dibaca.
- SHOULD menghindari pengumuman berulang untuk event yang sama.

### 15.3 Keyboard Accessibility

- MUST memastikan Close dan Action dapat diakses dengan keyboard.
- MUST memberikan accessible name untuk kontrol interaktif.
- MUST mempertahankan urutan fokus yang logis.
- MUST NOT memindahkan fokus secara tiba-tiba tanpa kebutuhan.

### 15.4 Timing Accessibility

- MUST mempertimbangkan waktu yang cukup untuk membaca pesan.
- SHOULD memberikan durasi lebih panjang untuk pesan kompleks jika auto-dismiss digunakan.
- MUST NOT membuat informasi penting hanya tersedia dalam waktu terlalu singkat.
- SHOULD menyediakan cara melihat kembali informasi penting jika diperlukan.

---

## 16. AI Notification Selection Workflow

1. **Read HSD/BRD:** Identifikasi event atau kondisi yang memerlukan Notification.
2. **Determine Purpose:** Tentukan apakah pesan merupakan Success, Error, Warning, Information, Activity, atau Progress.
3. **Validate Component:** Pastikan Notification lebih tepat dibanding Alert atau Modal.
4. **Select Type:** Gunakan Type resmi GEMS.
5. **Select Breakpoint:** Gunakan `Desktop` atau `Mobile`.
6. **Select Position:** Gunakan Position yang tersedia.
7. **Define Title:** Jelaskan kondisi atau hasil tindakan.
8. **Define Description:** Tambahkan informasi pendukung jika diperlukan.
9. **Define Trigger:** Tentukan kapan Notification ditampilkan.
10. **Define Duration:** Gunakan aturan durasi yang tersedia.
11. **Define Dismiss:** Tentukan apakah Close diperbolehkan.
12. **Define Action:** Tambahkan action hanya jika didukung.
13. **Verify Data:** Pastikan pesan sesuai hasil proses aktual.
14. **Verify Accessibility:** Periksa keterbacaan, pengumuman, keyboard, dan timing.
15. **Verify Figma:** Pastikan variant dan kombinasi property tersedia pada GEMS.
16. **Human Approval:** Minta persetujuan untuk behavior baru yang belum ditentukan.

---

## 17. AI Restrictions

AI MUST NOT:

1. Membuat Notification Type baru tanpa persetujuan.
2. Membuat Breakpoint di luar GEMS tanpa persetujuan.
3. Menggunakan Position yang tidak tersedia pada variant.
4. Membuat struktur visual custom tanpa persetujuan.
5. Menggunakan Notification sebagai pengganti Modal konfirmasi.
6. Menggunakan Notification untuk hasil validasi kompleks yang harus dibaca bersama data.
7. Menampilkan Success sebelum proses berhasil.
8. Menampilkan Error tanpa kegagalan aktual.
9. Menggunakan Warning hanya untuk penekanan estetika.
10. Membuat pesan hasil proses yang tidak tersedia.
11. Mengubah status bisnis melalui Notification tanpa workflow.
12. Menganggap seluruh Notification otomatis hilang.
13. Menganggap seluruh Notification dapat ditutup.
14. Membuat durasi auto-dismiss tanpa aturan yang jelas.
15. Membuat persentase progress tanpa data sistem.
16. Menganggap progress selesai sebelum sistem mengonfirmasi.
17. Menambahkan action tanpa requirement.
18. Menampilkan Notification identik berulang tanpa alasan.
19. Membuat aturan stacking baru tanpa validasi.
20. Menutupi kontrol penting pada halaman.
21. Menggunakan pesan ambigu atau terlalu teknis.
22. Menampilkan informasi penting hanya melalui ikon atau warna.
23. Mengabaikan aksesibilitas keyboard dan screen reader.
24. Mengubah navigasi tanpa requirement.
25. Membuat pola interaksi baru tanpa Human Approval.

---

## 18. Implementation Requirements

### 18.1 Source of Truth

| Source | Responsibility |
|---|---|
| HSD / BRD | Event, workflow, pesan, hak akses, dan kondisi bisnis |
| GEMS Design System | Type, Breakpoint, Position, dan visual Notification |
| System Data | Hasil tindakan, status proses, dan progress aktual |
| Human Approval | Persetujuan behavior atau pola baru yang belum ditentukan |

### 18.2 Final AI Instruction

When generating UI/UX designs, AI MUST:

1. Read the HSD/BRD to identify events requiring user feedback.
2. Use the official GEMS Notification component.
3. Select supported Type, Breakpoint, and Position variants.
4. Write clear and accurate notification titles and descriptions.
5. Trigger notifications based on actual system events.
6. Distinguish Notification from Alert, Modal, and field validation.
7. Define display duration and dismiss behavior according to requirements.
8. Use actual progress information when displaying process status.
9. Preserve accessibility and responsive behavior.
10. Avoid inventing notification types, data, interactions, or workflow rules.
11. Request Human Approval for unsupported behaviors or new patterns.

---

## 19. Official Figma Reference

| Component | Purpose | Figma Design |
|---|---|---|
| GEMS Notification | Official Notification component, types, positions, and responsive variants | [Open GEMS Notification Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1813-98074&t=oti8QS9H602K2cYU-1) |
