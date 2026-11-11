# GEMS Design System — Add New Data UX Pattern Guidelines

## 1. Purpose & Core Principles

Add New Data merupakan UX Pattern yang digunakan untuk membuat atau menambahkan data baru ke dalam sistem.

GEMS menyediakan empat pattern penambahan data yang memiliki struktur dan alur interaksi berbeda. Pemilihan pattern MUST mempertimbangkan:

- Kompleksitas data dan formulir.
- Kebutuhan halaman atau modal.
- Pengelompokan informasi.
- Kebutuhan pengisian bertahap.
- Kebutuhan Save as Draft.
- Kebutuhan Preview sebelum penyimpanan.
- Alur bisnis dan hak akses berdasarkan HSD/BRD.
- Flow Diagram resmi pada GEMS Design System.

### Core Principles

**1. Requirement-Based Selection**

AI MUST memilih UX Pattern berdasarkan kebutuhan HSD/BRD, bukan preferensi visual.

**2. Official Pattern Reuse**

AI MUST menggunakan salah satu dari empat Add New Data UX Pattern resmi GEMS.

**3. Flow Integrity**

AI MUST mempertahankan struktur, urutan interaksi, decision point, dan navigasi sesuai pattern terpilih.

**4. Design System Compliance**

AI MUST menggunakan seluruh komponen GEMS yang diperlukan oleh pattern terpilih, termasuk variant dan state resmi yang relevan.

**5. Flow-Driven Design**

AI MUST menghasilkan UX Flow Diagram dan UI Design yang saling sesuai.

**6. Business Data Accuracy**

AI MUST menggunakan data, field, status, dan aturan bisnis dari HSD/BRD yang diberikan.

**7. Human Approval**

AI MUST meminta Human Approval sebelum melakukan perubahan terhadap pattern, flow, atau komponen resmi.

**Core Principle:**

> UX Pattern menentukan struktur dan alur interaksi. HSD/BRD menentukan kebutuhan bisnis. GEMS Design System menentukan komponen. AI MUST menggunakan ketiganya secara konsisten tanpa mengubah aturan yang telah disetujui.

---

## 2. Official UX Pattern Types

### 2.1 Available Patterns

| Pattern | Type | Karakteristik |
|---|---|---|
| Pattern 01 | Modal / Popup | Penambahan data melalui form dalam modal |
| Pattern 02 | New Page | Penambahan data melalui halaman khusus dengan Save as Draft |
| Pattern 03 | Multi-step New Page | Penambahan data melalui beberapa tahapan |
| Pattern 04 | Multi-step with Preview | Penambahan data bertahap dengan Preview dan Save as Draft |

### 2.2 UX Pattern Selection Matrix

| Kebutuhan | Recommended Pattern | Alasan |
|---|---|---|
| Form sederhana dengan input ringkas | Pattern 01 | Pengguna dapat mengisi data melalui modal |
| Form membutuhkan halaman khusus dan draft | Pattern 02 | Pengguna memiliki ruang pengisian lebih luas dan dapat menyimpan draft |
| Form memiliki beberapa kelompok informasi yang perlu diisi bertahap | Pattern 03 | Pengisian menggunakan navigasi antarstep |
| Form bertahap membutuhkan pemeriksaan data sebelum penyimpanan | Pattern 04 | Pengguna dapat meninjau data melalui Preview |

### AI Rules

- AI MUST memeriksa kebutuhan data sebelum menentukan pattern.
- AI MUST menggunakan pattern yang telah ditetapkan dalam approved design jika tersedia.
- AI SHOULD merekomendasikan pattern berdasarkan kompleksitas dan alur pengisian data.
- AI MUST mempertimbangkan seluruh behavior bawaan pattern, termasuk Draft dan Preview.
- AI MUST NOT memilih pattern hanya berdasarkan jumlah field.
- AI MUST NOT menggabungkan beberapa pattern menjadi satu.
- AI MUST NOT membuat pattern baru tanpa Human Approval.

---

## 3. Pattern 01 — Add Data via Modal

### 3.1 When to Use

Pattern 01 digunakan untuk penambahan data yang dapat diselesaikan melalui form dalam modal tanpa berpindah ke halaman khusus.

| Kondisi | Penggunaan |
|---|---|
| Form sederhana | Recommended |
| Input ringkas | Recommended |
| Membutuhkan Modal | Recommended |
| Membutuhkan Multi-step | Not Recommended |
| Membutuhkan Save as Draft | Not Recommended |
| Membutuhkan Preview Page | Not Recommended |

### 3.2 Official Flow

AI MUST mengikuti urutan utama berikut:

1. Start.
2. List / Data Table.
3. Klik Add Data.
4. Add Form Modal (Popup).
5. Fill Form.
6. Klik Save.
7. Confirmation Modal.
8. Success Toast.
9. List Page dengan data terbaru.
10. End.

### 3.3 Cancel & Exit Flow

Pattern 01 memiliki alur keluar dari form yang mempertimbangkan kondisi data yang telah diisi.

**AI Rules:**

- AI MUST mengikuti decision point form kosong atau sudah terisi sesuai flow resmi.
- AI MUST menggunakan Confirmation Modal keluar jika ditentukan dalam pattern.
- AI MUST mempertahankan input ketika pengguna memilih kembali ke form.
- AI MUST mengikuti alur pembatalan dan penutupan sesuai referensi Figma.
- AI MUST NOT menutup form berisi perubahan dengan behavior yang berbeda dari pattern.

### 3.4 Pattern Restrictions

AI MUST NOT:

1. Mengubah Modal menjadi New Page.
2. Menambahkan Multi-step.
3. Menambahkan Preview.
4. Menambahkan Save as Draft.
5. Menghilangkan Confirmation Modal.
6. Mengubah urutan Save dan Confirmation.
7. Mengubah Cancel atau Exit Flow.

---

## 4. Pattern 02 — Add Data via New Page

### 4.1 When to Use

Pattern 02 digunakan ketika penambahan data membutuhkan halaman khusus dan mendukung penyimpanan sementara melalui Save as Draft.

| Kondisi | Penggunaan |
|---|---|
| Form membutuhkan halaman khusus | Recommended |
| Form lebih luas dibanding Modal | Recommended |
| Membutuhkan Save as Draft | Recommended |
| Membutuhkan Multi-step | Not Recommended |
| Membutuhkan Preview Page | Not Recommended |

### 4.2 Official Flow

AI MUST mengikuti urutan utama berikut:

1. Start.
2. List / Data Table.
3. Klik Add Data.
4. Add Form (New Page).
5. Fill Form.
6. Pengguna memilih Save atau Save as Draft.
7. Confirmation Modal pada alur final Save.
8. Success Toast atau Draft Success Toast.
9. List Page dengan data terbaru atau status Draft.
10. End.

### 4.3 Save as Draft

Save as Draft digunakan untuk menyimpan data yang belum diselesaikan sebagai draft.

**AI Rules:**

- AI MUST mengikuti mekanisme Save as Draft pada pattern resmi.
- AI MUST mempertahankan kontrol dan urutan interaksi draft.
- AI MUST menampilkan Draft Success Toast setelah penyimpanan draft berhasil.
- AI MUST menggunakan status Draft sesuai ketentuan bisnis.
- AI MUST NOT mengubah Save as Draft menjadi autosave.
- AI MUST NOT menganggap Draft sebagai final submission.

### 4.4 Cancel & Exit Flow

**AI Rules:**

- AI MUST mengikuti kondisi form kosong atau terisi sesuai flow.
- AI MUST menggunakan Confirmation Modal keluar sesuai referensi.
- AI MUST mempertahankan data ketika pengguna memilih kembali ke form.
- AI MUST NOT menghilangkan exit confirmation yang diwajibkan pattern.

### 4.5 Pattern Restrictions

AI MUST NOT:

1. Mengubah New Page menjadi Modal.
2. Menambahkan Stepper.
3. Menambahkan Preview Page.
4. Menghapus Save as Draft.
5. Mengubah urutan penyimpanan.
6. Mengubah Cancel atau Exit Flow.

---

## 5. Pattern 03 — Multi-step Add Data

### 5.1 When to Use

Pattern 03 digunakan ketika informasi perlu dibagi menjadi beberapa tahapan pengisian yang memiliki urutan jelas.

| Kondisi | Penggunaan |
|---|---|
| Data memiliki beberapa kelompok informasi | Recommended |
| Pengisian membutuhkan tahapan | Recommended |
| Membutuhkan navigasi Next dan Back | Recommended |
| Membutuhkan Preview Page khusus | Not Recommended |

### 5.2 Official Flow

AI MUST mengikuti urutan utama berikut:

1. Start.
2. List / Data Table.
3. Klik Add Data.
4. Add Form (New Page).
5. Pengguna mengisi data pada setiap step.
6. Pengguna menyelesaikan step terakhir.
7. Klik Save.
8. Confirmation Modal.
9. Success Toast.
10. List Page dengan data terbaru.
11. End.

Jumlah, nama, dan urutan step MUST mengikuti pattern dan desain fitur yang telah disetujui.

### 5.3 Step Navigation

**AI Rules:**

- AI MUST menggunakan struktur Multi-step resmi.
- AI MUST mengikuti urutan step yang telah disetujui.
- AI MUST menggunakan Progress Indicator resmi GEMS.
- AI MUST mengikuti behavior Next dan Back sesuai flow.
- AI MUST mempertahankan data ketika berpindah step sesuai ketentuan.
- AI MUST menerapkan validasi berdasarkan HSD/BRD.
- AI MUST NOT menambahkan, menghapus, menggabungkan, atau mengubah urutan step tanpa Human Approval.

### 5.4 Save & Exit Flow

**AI Rules:**

- AI MUST mengikuti alur Save pada tahap akhir.
- AI MUST menggunakan Confirmation Modal sesuai pattern.
- AI MUST menampilkan Success Toast setelah proses berhasil.
- AI MUST mengikuti alur pembatalan dan keluar yang tersedia.
- AI MUST NOT menambahkan Preview atau Draft yang tidak termasuk dalam pattern.

---

## 6. Pattern 04 — Multi-step with Preview

### 6.1 When to Use

Pattern 04 digunakan ketika pengisian data dilakukan secara bertahap dan membutuhkan Preview untuk meninjau informasi sebelum final Save.

| Kondisi | Penggunaan |
|---|---|
| Data memiliki beberapa kelompok informasi | Recommended |
| Membutuhkan Multi-step | Recommended |
| Membutuhkan Preview Page | Recommended |
| Membutuhkan Save as Draft | Recommended |

### 6.2 Official Flow

AI MUST mengikuti urutan utama berikut:

1. Start.
2. List / Data Table.
3. Klik Add Data.
4. Add Form (New Page).
5. Pengguna mengisi data pada setiap step.
6. Pengguna masuk ke Preview Page.
7. Pengguna meninjau informasi.
8. Klik Save.
9. Confirmation Modal.
10. Success Toast.
11. List Page dengan data terbaru.
12. End.

### 6.3 Preview Behavior

**AI Rules:**

- AI MUST menggunakan struktur Preview resmi.
- AI MUST menampilkan informasi yang telah diisi pada tahap sebelumnya.
- AI MUST mengikuti pengelompokan dan urutan informasi yang disetujui.
- AI MUST mengikuti behavior Back dan Save.
- AI MUST NOT mengubah Preview menjadi Modal.
- AI MUST NOT menambahkan field baru pada Preview.
- AI MUST NOT menghilangkan Preview tanpa Human Approval.

### 6.4 Save as Draft

**AI Rules:**

- AI MUST mengikuti mekanisme Save as Draft resmi.
- AI MUST menggunakan Draft Success Toast setelah proses berhasil.
- AI MUST mengikuti status dan navigasi Draft yang ditentukan.
- AI MUST NOT mengganti Save as Draft dengan autosave.

### 6.5 Cancel & Exit Flow

**AI Rules:**

- AI MUST mengikuti percabangan keluar dari form.
- AI MUST menggunakan Confirmation Modal sesuai pattern.
- AI MUST mempertahankan data jika pengguna kembali ke form.
- AI MUST NOT mengubah urutan atau behavior pembatalan.

### 6.6 Pattern Restrictions

AI MUST NOT:

1. Mengubah Multi-step menjadi Single Page.
2. Menambahkan atau menghapus step.
3. Mengubah urutan step.
4. Menghapus Preview.
5. Menghapus Draft.
6. Mengubah Confirmation Modal.
7. Mengubah navigasi Preview.
8. Menggabungkan Pattern 04 dengan pattern lain.

---

## 7. UX Flow Diagram

### 7.1 Purpose

UX Flow Diagram merupakan representasi visual dari perjalanan pengguna, mulai dari entry point, tindakan, percabangan keputusan, hingga proses selesai.

Setiap UX Pattern Add New Data pada GEMS memiliki Flow Diagram sebagai acuan alur interaksi.

AI MUST menghasilkan UX Flow Diagram pada setiap output desain Add New Data.

**Core Principle:**

> Setiap UI Design MUST memiliki UX Flow Diagram yang menggambarkan alur aktual berdasarkan pattern terpilih dan data HSD/BRD yang diberikan.

### 7.2 Flow Diagram Structure

| Elemen | Fungsi | Ketentuan |
|---|---|---|
| Start | Menandai awal proses | Required |
| Screen / Page | Menunjukkan halaman atau tampilan | Required |
| User Action | Menunjukkan tindakan pengguna | Required |
| Decision Point | Menunjukkan percabangan kondisi | Sesuai pattern |
| Confirmation | Menunjukkan proses konfirmasi | Sesuai pattern |
| System Feedback | Menunjukkan respons sistem | Sesuai pattern |
| Navigation Path | Menunjukkan perpindahan alur | Required |
| End | Menandai akhir proses | Required |

### 7.3 Main Flow

Main Flow merupakan alur utama yang digunakan pengguna untuk menyelesaikan proses penambahan data.

**AI Rules:**

- AI MUST mengambil Main Flow dari pattern resmi GEMS.
- AI MUST mempertahankan urutan interaksi.
- AI MUST mengganti contoh konten dengan data bisnis yang diberikan.
- AI MUST menggunakan nama halaman dan tindakan sesuai HSD/BRD.
- AI MUST memastikan setiap flow node sesuai dengan UI Design.
- AI MUST NOT membuat Main Flow baru di luar pattern resmi.

### 7.4 Alternative Flow

Alternative Flow merupakan alur yang muncul ketika pengguna memilih tindakan lain atau memenuhi kondisi tertentu.

Contoh percabangan yang terdapat dalam pattern:

- Pengguna membatalkan pengisian.
- Pengguna menutup form.
- Form kosong atau sudah terisi.
- Pengguna kembali mengedit.
- Pengguna memilih Save as Draft.
- Pengguna membatalkan Confirmation Modal.

**AI Rules:**

- AI MUST menampilkan seluruh Alternative Flow yang berlaku pada pattern terpilih.
- AI MUST mempertahankan decision point resmi.
- AI MUST mempertahankan hubungan antarflow.
- AI MUST NOT menghilangkan percabangan yang terdapat pada pattern.
- AI MUST NOT menambahkan percabangan baru tanpa dasar HSD/BRD dan Human Approval.

### 7.5 Business Data Integration

UX Flow Diagram MUST menggunakan data aktual dari kebutuhan fitur.

| Data | Sumber |
|---|---|
| Nama fitur | HSD/BRD |
| User Role | HSD/BRD / Role Access Matrix |
| Nama halaman | Approved design / HSD/BRD |
| Nama form | HSD/BRD |
| Tindakan pengguna | Approved business flow |
| Validasi | HSD/BRD |
| Status data | HSD/BRD |
| Confirmation | Pattern GEMS dan konteks bisnis |
| System Feedback | Pattern GEMS dan hasil proses |

**AI Rules:**

- AI MUST menggunakan informasi bisnis yang tersedia.
- AI MUST menjaga konsistensi istilah antara Flow Diagram dan UI Design.
- AI MUST menggunakan status yang telah ditentukan.
- AI MUST NOT mengarang field, role, status, atau business rule.
- AI MUST meminta klarifikasi jika informasi penting belum tersedia.

### 7.6 Flow-to-Screen Mapping

Setiap flow node yang merepresentasikan screen atau state MUST dapat ditelusuri ke desain yang dihasilkan.

**AI Rules:**

- AI MUST menghubungkan Flow Diagram dengan UI Screens.
- AI MUST memastikan tindakan dalam flow tersedia pada UI.
- AI MUST memastikan navigasi UI mengikuti flow.
- AI MUST menampilkan confirmation dan feedback yang diperlukan.
- AI MUST NOT membuat screen tambahan di luar approved flow.
- AI MUST NOT menghasilkan flow dan UI dengan behavior berbeda.

---

## 8. UX States & Feedback

UX States digunakan untuk menjelaskan kondisi interaksi pengguna dan respons sistem pada proses Add New Data.

### 8.1 State Usage Matrix

| State | Kapan Digunakan | Behavior |
|---|---|---|
| Default | Form pertama kali dibuka | Menampilkan kondisi awal |
| Filled | Pengguna telah mengisi field | Mempertahankan nilai input |
| Validation Error | Data tidak memenuhi aturan validasi | Menampilkan feedback validasi |
| Disabled | Tindakan belum tersedia | Mencegah aksi yang tidak diizinkan |
| Loading | Sistem sedang memproses | Menampilkan feedback proses |
| Success | Penyimpanan berhasil | Menampilkan Success Toast sesuai pattern |
| Error | Proses gagal | Menampilkan feedback error resmi |
| Draft Success | Draft berhasil disimpan | Mengikuti alur Draft Success |
| Unsaved Changes | Pengguna keluar dengan perubahan belum tersimpan | Mengikuti Exit Confirmation |

State pada tabel merupakan kondisi interaksi yang harus diperiksa, bukan daftar variant visual yang otomatis tersedia pada semua komponen GEMS.

### 8.2 Validation Error

**AI Rules:**

- AI MUST menggunakan validation rules dari HSD/BRD.
- AI MUST menggunakan state validasi resmi dari komponen GEMS terkait.
- AI MUST mempertahankan input saat validasi gagal.
- AI MUST NOT membuat aturan validasi baru.
- AI MUST NOT mengarang visual Error State.

### 8.3 Disabled State

**AI Rules:**

- AI MUST menggunakan Disabled State resmi jika tersedia.
- AI MUST menentukan kondisi disabled berdasarkan business rule.
- AI MUST NOT membuat visual disabled custom.
- AI MUST NOT menonaktifkan tindakan tanpa alasan yang didukung requirement.

### 8.4 Loading State

**AI Rules:**

- AI MUST mengikuti mekanisme loading yang tersedia dalam GEMS dan kebutuhan sistem.
- AI MUST menjaga agar proses penyimpanan tidak menghasilkan tindakan ganda yang tidak diinginkan.
- AI MUST NOT menampilkan Success sebelum proses berhasil.
- AI MUST NOT menciptakan visual Loading State baru tanpa referensi resmi.

### 8.5 Success State

**AI Rules:**

- AI MUST mengikuti Success Toast pada pattern.
- AI MUST menampilkan feedback setelah proses berhasil.
- AI MUST mengikuti navigasi akhir sesuai flow.
- AI MUST NOT mengganti Success Toast dengan Modal tambahan tanpa approval.

### 8.6 Error State

**AI Rules:**

- AI MUST menggunakan feedback Error resmi GEMS.
- AI MUST mempertahankan data yang relevan.
- AI MUST mengikuti behavior kegagalan yang telah ditentukan.
- AI MUST NOT menambahkan Error Page atau flow baru tanpa approval.

### 8.7 Draft Success

**AI Rules:**

- AI MUST menggunakan Draft Success hanya pada pattern yang mendukung Draft.
- AI MUST mengikuti status dan navigasi Draft.
- AI MUST NOT menganggap Draft sebagai final submission.

### 8.8 Unsaved Changes

**AI Rules:**

- AI MUST mengikuti Exit Confirmation sesuai pattern.
- AI MUST mempertahankan data jika pengguna kembali mengedit.
- AI MUST NOT membuang data pengguna di luar behavior yang disetujui.

---

## 9. GEMS Design System Compliance

Seluruh UI yang dihasilkan dari Add New Data UX Pattern MUST menggunakan komponen resmi GEMS Design System.

### 9.1 Component Retrieval

AI MUST:

1. Mengakses GEMS Design System melalui Figma.
2. Memeriksa komponen yang digunakan pada pattern terpilih.
3. Mengidentifikasi seluruh komponen yang diperlukan.
4. Mengambil komponen resmi beserta variant dan state yang relevan.
5. Menggunakan komponen tersebut pada UI Design.
6. Memastikan penggunaan komponen sesuai referensi GEMS.

### 9.2 Component Integrity

AI MUST mempertahankan:

- Struktur komponen.
- Properties.
- Variant.
- State.
- Visual specification.
- Interaction behavior.

AI MUST NOT:

- Membuat komponen custom.
- Menggunakan komponen dari UI library eksternal.
- Mengubah variant atau state.
- Mengubah visual specification.
- Mengganti komponen resmi berdasarkan preferensi visual.

Jika komponen yang diperlukan tidak tersedia atau tidak dapat diverifikasi, AI MUST melaporkan keterbatasan tersebut dan meminta Human Review.

---

## 10. Required AI Design Output

Setiap permintaan desain Add New Data MUST menghasilkan output berikut.

### 10.1 UX Pattern Selection

AI MUST menjelaskan:

- Nama fitur.
- User Role.
- Pattern terpilih.
- Referensi Figma.
- Alasan pemilihan.
- Kesesuaian dengan HSD/BRD.

### 10.2 UX Flow Diagram

AI MUST menghasilkan:

- Main Flow.
- Alternative Flow.
- Decision Point.
- Confirmation Flow.
- Cancel dan Exit Flow.
- Draft Flow jika tersedia.
- Preview Flow jika tersedia.
- System Feedback.
- End State.

UX Flow Diagram MUST menggunakan data bisnis yang telah diberikan.

### 10.3 UI Design

AI MUST menghasilkan:

- Seluruh screen sesuai pattern terpilih.
- Form dengan data HSD/BRD.
- Komponen resmi GEMS.
- Confirmation dan feedback sesuai flow.
- State interaksi yang relevan.

### 10.4 Flow-to-Screen Mapping

AI MUST menyediakan hubungan antara flow dan UI.

| Flow Node | UI Screen / State | User Action | Expected Result |
|---|---|---|---|
| List Data | List Page | Klik Tambah Data | Form terbuka |
| Add Form | Modal / New Page | Isi data | Form terisi |
| Save | Form | Klik Simpan | Confirmation ditampilkan |
| Confirmation | Confirmation Modal | Konfirmasi | Proses penyimpanan |
| Success | Success Toast | Sistem memberikan feedback | Daftar data diperbarui |

Tabel merupakan contoh mapping alur utama. AI MUST menyesuaikannya dengan pattern terpilih dan menyertakan percabangan yang berlaku.

### 10.5 Compliance Report

AI MUST menjelaskan:

- Kesesuaian pattern.
- Kesesuaian Flow Diagram.
- Kesesuaian UI Screens.
- Penggunaan komponen GEMS.
- Kesesuaian dengan HSD/BRD.
- Kebutuhan Human Approval jika terdapat pengecualian.

---

## 11. UX Pattern Selection Rules for AI

AI MUST mengikuti urutan pengambilan keputusan berikut:

**Step 1 — Read Requirements**

Identifikasi fitur, tujuan, data, field, validation, status, role, dan business flow dari HSD/BRD.

**Step 2 — Inspect Official Patterns**

Periksa keempat Add New Data UX Pattern pada Figma GEMS, termasuk Flow Diagram dan UI Screens.

**Step 3 — Identify Interaction Needs**

Tentukan apakah proses membutuhkan Modal, New Page, Multi-step, Preview, atau Draft.

**Step 4 — Select Pattern**

Pilih pattern berdasarkan UX Pattern Selection Matrix dan approved requirements.

**Step 5 — Validate Pattern Compatibility**

Pastikan seluruh behavior bawaan pattern sesuai kebutuhan bisnis. Jika tidak sesuai, laporkan konflik dan minta Human Review.

**Step 6 — Retrieve GEMS Components**

Identifikasi dan gunakan seluruh komponen resmi GEMS yang diperlukan oleh pattern terpilih.

**Step 7 — Confirm Pattern**

Gunakan pattern yang telah disetujui. Jika belum ada keputusan dan pemilihan tidak dapat dipastikan, minta Human Approval.

**Step 8 — Generate UX Flow Diagram**

Gunakan Flow Diagram resmi dan sesuaikan konten dengan data HSD/BRD tanpa mengubah struktur.

**Step 9 — Generate UI Design**

Buat seluruh UI Screens sesuai flow dengan komponen resmi GEMS.

**Step 10 — Apply UX States**

Terapkan state dan feedback yang relevan berdasarkan requirement dan referensi resmi.

**Step 11 — Validate Flow & UI**

Pastikan setiap screen, interaction, confirmation, dan navigation sesuai dengan Flow Diagram.

**Step 12 — Request Human Approval When Needed**

Jika dibutuhkan perubahan terhadap pattern, flow, komponen, atau behavior, AI MUST meminta persetujuan manusia sebelum implementasi.

---

## 12. Human Approval Rules

AI MAY memberikan rekomendasi UX ketika pattern yang tersedia tidak sepenuhnya memenuhi kebutuhan bisnis.

Namun, rekomendasi MUST dipisahkan dari desain yang telah disetujui.

### 12.1 Approval Required

AI MUST meminta Human Approval sebelum:

1. Mengganti pattern.
2. Menggabungkan pattern.
3. Menambah atau menghapus screen.
4. Menambah atau menghapus step.
5. Mengubah urutan flow.
6. Mengubah decision point.
7. Menambah atau menghapus Draft.
8. Menambah atau menghapus Preview.
9. Mengubah Confirmation Flow.
10. Mengubah Cancel atau Exit Flow.
11. Menambahkan interaksi baru.
12. Mengubah komponen GEMS.

### 12.2 Recommendation Format

AI MUST menggunakan format berikut:

| Informasi | Keterangan |
|---|---|
| Feature | Nama fitur |
| Current Pattern | Pattern yang digunakan |
| Figma Reference | Referensi resmi |
| Business Requirement | Kebutuhan dari HSD/BRD |
| Identified Issue | Ketidaksesuaian atau keterbatasan |
| Recommendation | Usulan perubahan |
| Impact | Dampak terhadap flow dan screen |
| Approval Status | Pending Human Approval |

### 12.3 Approval Enforcement

- AI MUST memisahkan rekomendasi dari implementasi.
- AI MUST menunggu approval sebelum menerapkan perubahan.
- AI MUST NOT menganggap rekomendasi sebagai approval.
- AI MUST NOT menganggap tidak adanya respons sebagai persetujuan.
- AI MUST NOT mengubah approved pattern tanpa approval baru.

---

## 13. AI Restrictions

AI MUST NOT:

1. Membuat Add New Data UX Pattern baru.
2. Menggabungkan dua atau lebih pattern.
3. Mengganti pattern tanpa Human Approval.
4. Menambah atau menghapus screen.
5. Menambah atau menghapus step.
6. Mengubah urutan interaksi.
7. Mengubah decision point resmi.
8. Mengubah Save, Draft, Preview, atau Confirmation Flow.
9. Menghilangkan Cancel atau Exit Flow.
10. Membuat UI tanpa UX Flow Diagram.
11. Membuat UX Flow Diagram yang tidak sesuai UI.
12. Menggunakan data bisnis yang tidak terdapat dalam HSD/BRD.
13. Mengarang validation rules, role, atau status.
14. Membuat komponen custom.
15. Mengganti komponen resmi GEMS.
16. Mengubah variant, state, atau visual specification.
17. Menambahkan behavior yang belum disetujui.
18. Mengimplementasikan rekomendasi tanpa Human Approval.
19. Menganggap screenshot contoh sebagai izin untuk mengubah pattern.
20. Menyatakan desain compliant tanpa melakukan verifikasi.

---

## 14. Quality Assurance & Compliance

AI MUST melakukan validasi sebelum menyatakan desain siap digunakan.

### 14.1 Requirement Compliance

- AI MUST memastikan seluruh kebutuhan data berasal dari HSD/BRD.
- AI MUST memastikan role dan permission sesuai dokumen yang disetujui.
- AI MUST memastikan business flow tidak berubah.
- AI MUST NOT menambahkan kebutuhan berdasarkan asumsi.

### 14.2 Pattern Compliance

- AI MUST memastikan pattern terpilih merupakan salah satu dari empat pattern resmi.
- AI MUST memastikan seluruh Main Flow dan Alternative Flow yang berlaku telah digunakan.
- AI MUST mempertahankan urutan screen, step, dan decision point.
- AI MUST memastikan Save, Draft, Preview, Confirmation, dan Exit mengikuti pattern.
- AI MUST NOT mengubah pattern tanpa Human Approval.

### 14.3 Flow Compliance

- AI MUST menghasilkan UX Flow Diagram lengkap.
- AI MUST menggunakan data HSD/BRD pada flow.
- AI MUST memastikan flow sesuai UI Design.
- AI MUST memastikan seluruh percabangan resmi terwakili.
- AI MUST NOT menghasilkan flow yang berbeda dari desain.

### 14.4 Design System Compliance

- AI MUST menggunakan komponen GEMS resmi.
- AI MUST menggunakan variant dan state yang tersedia.
- AI MUST mempertahankan spesifikasi visual.
- AI MUST memverifikasi komponen terhadap Figma.
- AI MUST NOT mengarang komponen atau state baru.

### 14.5 Human Approval Compliance

- AI MUST mengidentifikasi setiap kebutuhan yang tidak dapat dipenuhi pattern.
- AI MUST menjelaskan rekomendasi perubahan.
- AI MUST meminta Human Approval.
- AI MUST mempertahankan pattern yang disetujui selama rekomendasi belum disetujui.
- AI MUST NOT menerapkan perubahan berstatus Pending.

### 14.6 Final Validation

Jika terdapat requirement yang belum dapat diverifikasi, AI MUST melaporkan keterbatasannya.

AI MUST NOT menyatakan desain selesai, sesuai GEMS, atau telah disetujui apabila masih terdapat penyimpangan yang belum memperoleh Human Approval.

---

## 15. Official Figma References

**Source:** GEMS Design System

**Main UX Pattern:**

[GEMS Add New Data UX Pattern](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1161-481)

**Individual Patterns:**

- [Pattern 01 — Modal / Popup](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3305-14747)
- [Pattern 02 — New Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3310-27399)
- [Pattern 03 — Multi-step New Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3314-34982)
- [Pattern 04 — Multi-step with Preview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3338-41046)

**Components:**

[GEMS Design System — Official Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)

AI MUST menggunakan referensi resmi tersebut untuk memeriksa flow, screens, komponen, variant, dan state.

---

## 16. Final AI Enforcement

AI MUST:

1. Membaca approved HSD/BRD.
2. Memeriksa keempat Add New Data UX Pattern resmi.
3. Memilih pattern berdasarkan kebutuhan bisnis.
4. Menggunakan Flow Diagram resmi sebagai acuan.
5. Menghasilkan UX Flow Diagram lengkap dengan data bisnis.
6. Menghasilkan UI Screens yang sesuai dengan flow.
7. Menggunakan seluruh komponen GEMS yang diperlukan.
8. Mempertahankan struktur dan interaksi pattern.
9. Menggunakan state dan feedback resmi yang relevan.
10. Memastikan kesesuaian flow dengan UI.
11. Meminta Human Approval sebelum perubahan.
12. Memvalidasi hasil terhadap Figma GEMS.

**Final Rule:**

> AI MUST menggunakan salah satu dari empat Add New Data UX Pattern resmi GEMS berdasarkan kebutuhan HSD/BRD. Setiap output desain MUST menyertakan UX Flow Diagram lengkap dan UI Screens yang konsisten. Seluruh komponen MUST berasal dari GEMS Design System. AI MUST NOT menambah, menghapus, menggabungkan, atau mengubah struktur dan interaksi pattern tanpa explicit Human Approval.
