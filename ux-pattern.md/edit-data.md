# GEMS Design System — Edit Data UX Pattern Guidelines

## 1. Purpose & Core Principles

Edit Data merupakan UX Pattern untuk mengubah informasi pada data yang sudah tersimpan di dalam sistem.

GEMS menyediakan tiga Edit Data UX Pattern resmi yang memiliki konteks penggunaan, struktur halaman, dan alur interaksi berbeda.

AI MUST menganalisis kebutuhan HSD/BRD, memilih pattern yang sesuai, menggunakan komponen resmi GEMS Design System, serta menghasilkan UX Flow Diagram dan UI Design yang mencakup seluruh kondisi interaksi pengguna.

### 1.1 Core Principles

**1. Requirement-Based Selection**

AI MUST memilih UX Pattern berdasarkan approved HSD/BRD, entry point, kompleksitas data, dan kebutuhan interaksi pengguna.

**2. Official Pattern Reuse**

AI MUST menggunakan salah satu dari tiga Edit Data UX Pattern resmi GEMS sebagai acuan utama.

**3. GEMS Component Compliance**

AI MUST menggunakan komponen resmi GEMS Design System beserta properties, variants, states, dan visual specification yang tersedia.

**4. Flow-Driven Design**

AI MUST menghasilkan UX Flow Diagram pada bagian atas dan UI Screens pada bagian bawah, mengikuti struktur dokumentasi UX Pattern GEMS.

**5. Complete State Management**

AI MUST menangani seluruh UI States yang relevan, termasuk Default, Modified, Validation Error, Disabled, Loading, Success, Save Error, Network Error, Server Error, dan Unsaved Changes.

**6. Existing Data Integrity**

AI MUST menampilkan existing values, mempertahankan identitas record, dan hanya mengubah informasi yang diizinkan.

**7. Human Approval**

AI MAY merekomendasikan penyesuaian UX Flow apabila pattern resmi tidak memenuhi kebutuhan bisnis. Namun, AI MUST memperoleh explicit Human Approval sebelum menerapkan perubahan.

### 1.2 Core Enforcement

> AI MUST menggunakan approved HSD/BRD sebagai sumber kebutuhan bisnis, official GEMS UX Pattern sebagai acuan flow, dan GEMS Design System sebagai sumber komponen UI. AI MUST NOT mengubah pattern, flow, screen, atau interaction behavior tanpa Human Approval.

---

## 2. Source of Truth

AI MUST menggunakan sumber berikut sesuai fungsinya.

| Source | Fungsi |
|---|---|
| Approved HSD/BRD | Kebutuhan bisnis, field, validasi, status, dan proses |
| GEMS Edit Data UX Pattern | Struktur flow, screens, navigation, dan interaction |
| GEMS Design System | Komponen, properties, variants, states, dan visual specification |
| Role Access Matrix | Hak akses dan tindakan pengguna |
| Human Approval | Persetujuan perubahan atau pengecualian |

### AI Rules

AI MUST:

1. Memeriksa sumber resmi sebelum membuat desain.
2. Menggunakan kebutuhan dari approved HSD/BRD.
3. Mengikuti struktur dan behavior pattern GEMS.
4. Menggunakan komponen resmi GEMS.
5. Mengidentifikasi kebutuhan yang belum tersedia.
6. Melaporkan konflik antarsumber untuk Human Review.

AI MUST NOT:

- Mengarang field, status, role, validation, atau business rule.
- Menggunakan UI library eksternal sebagai pengganti GEMS.
- Mengubah approved flow berdasarkan asumsi.
- Menganggap rekomendasi AI sebagai persetujuan.

---

## 3. Official Edit Data UX Patterns

### 3.1 Available Patterns

| Pattern | Type | Karakteristik |
|---|---|---|
| Pattern 01 | Edit via Modal | Edit langsung dari List / Data Table melalui Modal |
| Pattern 02 | Edit via New Page | Edit melalui halaman form khusus |
| Pattern 03 | Edit from Detail Page | Pengguna mengakses Detail Page sebelum melakukan Edit |

### 3.2 UX Pattern Selection Matrix

| Kebutuhan | Recommended Pattern | Alasan |
|---|---|---|
| Edit langsung dari tabel | Pattern 01 | Tidak membutuhkan navigasi halaman baru |
| Edit membutuhkan halaman form khusus | Pattern 02 | Area pengisian lebih luas |
| Edit membutuhkan konteks detail data | Pattern 03 | Pengguna melihat informasi sebelum mengedit |

### 3.3 Pattern Selection Rules

AI MUST:

1. Membaca approved HSD/BRD.
2. Mengidentifikasi entry point tindakan Edit.
3. Memeriksa ketiga pattern resmi GEMS.
4. Membandingkan kebutuhan dengan struktur setiap pattern.
5. Memilih pattern yang paling sesuai.
6. Mempertahankan approved pattern jika telah ditentukan.
7. Menjelaskan alasan pemilihan.
8. Meminta Human Review jika terdapat konflik.
9. Meminta Human Approval jika pattern perlu dimodifikasi.

AI MUST NOT:

- Memilih pattern hanya berdasarkan jumlah field.
- Memilih pattern berdasarkan preferensi visual.
- Menggabungkan pattern tanpa approval.
- Membuat pattern baru secara mandiri.
- Mengubah approved pattern tanpa persetujuan.

---

## 4. Pattern 01 — Edit Data via Modal

**Figma Reference:** [Pattern 01 — Edit via Modal](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3339-72489&t=A8a8d9Xdh2dfZQ6G-1)

### 4.1 When to Use

Pattern 01 digunakan ketika pengguna dapat mengubah informasi langsung dari List / Data Table melalui Edit Form Modal.

**Gunakan Pattern 01 ketika:**

- Tindakan Edit tersedia pada List / Data Table.
- Form dapat ditampilkan melalui Modal.
- Pengguna tidak membutuhkan halaman Edit khusus.
- Setelah penyimpanan, pengguna kembali ke List Page.
- Struktur data sesuai dengan Modal resmi GEMS.

**Jangan gunakan Pattern 01 ketika:**

- Approved flow membutuhkan New Page.
- Pengguna wajib membuka Detail Page sebelum Edit.
- Form tidak dapat ditangani oleh struktur Modal resmi.

### 4.2 Official Main Flow

AI MUST mengikuti:

1. Start.
2. List / Data Table.
3. Klik Edit.
4. Edit Form Modal.
5. Pengguna mengubah data.
6. Klik Save.
7. Confirmation Modal Simpan.
8. Success Toast.
9. List Page (Data Diperbarui).
10. End.

### 4.3 Alternative Flow

AI MUST:

1. Mengikuti tindakan Tutup Form.
2. Memeriksa decision point "Sudah ada perubahan?".
3. Mengikuti jalur keluar resmi jika tidak ada perubahan.
4. Menggunakan Confirmation Modal keluar jika terdapat perubahan sesuai flow.
5. Mempertahankan perubahan jika pengguna kembali mengedit.
6. Mengikuti navigasi resmi jika pengguna mengonfirmasi keluar.

### 4.4 Required UI States

AI MUST menangani:

- Default dan Existing Data.
- Focus dan Filled.
- Modified dan Unchanged.
- Required dan Validation Error.
- Disabled dan Read-only.
- Loading.
- Confirmation.
- Success.
- Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.
- Updated Data.

Setiap state MUST menggunakan komponen dan behavior resmi GEMS.

### 4.5 Required Design Output

AI MUST menghasilkan:

- Flow Diagram di bagian atas.
- List / Data Table.
- Edit Form Modal.
- Confirmation Modal Simpan.
- Success Toast.
- List Page dengan data diperbarui.
- Exit Confirmation.
- Seluruh state yang relevan.

### 4.6 Pattern Restrictions

AI MUST NOT:

1. Mengubah Modal menjadi New Page.
2. Menambahkan Detail Page.
3. Menambahkan Multi-step.
4. Menambahkan Draft atau Preview.
5. Menghapus Confirmation Modal.
6. Mengubah Save Flow.
7. Mengubah Exit Flow.

---

## 5. Pattern 02 — Edit Data via New Page

**Figma Reference:** [Pattern 02 — Edit via New Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3339-72490&t=A8a8d9Xdh2dfZQ6G-1)

### 5.1 When to Use

Pattern 02 digunakan ketika proses Edit membutuhkan halaman khusus untuk menampilkan dan mengubah informasi.

**Gunakan Pattern 02 ketika:**

- Form membutuhkan ruang pengisian lebih luas.
- Approved design menggunakan New Page.
- Informasi tidak sesuai ditampilkan dalam Modal.
- Pengguna membutuhkan halaman khusus untuk mengelola perubahan.

**Jangan gunakan Pattern 02 ketika:**

- Approved design menggunakan Modal.
- Pengguna wajib melalui Detail Page.
- New Page tidak sesuai dengan approved business flow.

### 5.2 Official Main Flow

AI MUST mengikuti:

1. Start.
2. List / Data Table.
3. Klik Edit.
4. Edit Form pada New Page.
5. Pengguna mengubah data.
6. Klik Save.
7. Confirmation Modal Simpan.
8. Success Toast.
9. List Page (Data Diperbarui).
10. End.

**Reference Consistency Rule:**

Jika terdapat perbedaan antara label Flow Diagram dan contoh UI pada Figma, AI MUST melaporkan perbedaan tersebut untuk Human Review.

AI MUST NOT mengubah referensi resmi berdasarkan asumsi.

### 5.3 Alternative Flow

AI MUST:

1. Mengikuti tindakan keluar dari Edit Form.
2. Memeriksa kondisi perubahan data.
3. Menggunakan Exit Confirmation sesuai pattern.
4. Mempertahankan perubahan jika pengguna kembali mengedit.
5. Mengikuti navigasi resmi setelah pembatalan.

### 5.4 Required UI States

AI MUST menangani:

- Default dan Existing Data.
- Focus dan Filled.
- Modified dan Unchanged.
- Required dan Validation Error.
- Disabled dan Read-only.
- Loading.
- Confirmation.
- Success.
- Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.
- Updated Data.

### 5.5 Required Design Output

AI MUST menghasilkan:

- Flow Diagram di bagian atas.
- List / Data Table.
- Edit Form New Page.
- Confirmation Modal Simpan.
- Success Toast.
- List Page dengan data diperbarui.
- Exit Confirmation.
- Seluruh state yang relevan.

### 5.6 Pattern Restrictions

AI MUST NOT:

1. Mengubah New Page menjadi Modal.
2. Menambahkan Multi-step.
3. Menambahkan Draft atau Preview.
4. Mengubah urutan Save Flow.
5. Menghapus Confirmation Modal.
6. Mengubah Cancel atau Exit Flow.

---

## 6. Pattern 03 — Edit Data from Detail Page

**Figma Reference:** [Pattern 03 — Edit from Detail Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3339-72491&t=A8a8d9Xdh2dfZQ6G-1)

### 6.1 When to Use

Pattern 03 digunakan ketika pengguna membuka Detail Page untuk melihat informasi sebelum melakukan perubahan data.

**Gunakan Pattern 03 ketika:**

- Data memiliki Detail Page.
- Tindakan Edit tersedia pada Detail Page.
- Pengguna membutuhkan konteks informasi sebelum mengedit.
- Setelah penyimpanan, pengguna kembali ke Detail Page dengan data terbaru.

**Jangan gunakan Pattern 03 ketika:**

- Edit langsung dilakukan dari List / Data Table.
- Fitur tidak memiliki Detail Page.
- Approved flow menggunakan Pattern 01 atau Pattern 02.

### 6.2 Official Main Flow

AI MUST mengikuti:

1. Start.
2. List / Data Table.
3. Detail Page.
4. Klik Edit.
5. Edit Form.
6. Pengguna mengubah data.
7. Klik Save.
8. Confirmation Modal Simpan.
9. Success Toast.
10. Detail Page (Data Diperbarui).
11. End.

### 6.3 Alternative Flow

AI MUST:

1. Mengikuti tindakan Tutup Form.
2. Memeriksa kondisi perubahan data.
3. Menggunakan Exit Confirmation sesuai pattern.
4. Mempertahankan perubahan jika pengguna kembali mengedit.
5. Mengikuti navigasi resmi setelah keluar.

### 6.4 Required UI States

AI MUST menangani:

- Detail Default.
- Edit Default dengan existing values.
- Focus dan Filled.
- Modified dan Unchanged.
- Required dan Validation Error.
- Disabled dan Read-only.
- Loading.
- Confirmation.
- Success.
- Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.
- Updated Detail Data.

### 6.5 Required Design Output

AI MUST menghasilkan:

- Flow Diagram di bagian atas.
- List / Data Table.
- Detail Page.
- Edit Form.
- Confirmation Modal Simpan.
- Success Toast.
- Detail Page dengan data diperbarui.
- Exit Confirmation.
- Seluruh state yang relevan.

### 6.6 Pattern Restrictions

AI MUST NOT:

1. Menghapus Detail Page.
2. Mengubah entry point Edit.
3. Menambahkan screen baru tanpa approval.
4. Menambahkan Multi-step.
5. Menambahkan Draft atau Preview.
6. Mengubah Confirmation Flow.
7. Mengubah navigasi akhir tanpa approval.

---

## 7. Mandatory GEMS Component Usage

### 7.1 Official Component Source

Seluruh UI Design Edit Data MUST menggunakan komponen resmi GEMS Design System.

**Component Source:** [GEMS Design System — Official Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)

### 7.2 Component Retrieval Rules

Sebelum menghasilkan desain, AI MUST:

1. Mengakses GEMS Design System melalui Figma.
2. Memeriksa komponen yang digunakan pada pattern terpilih.
3. Mengidentifikasi seluruh komponen yang diperlukan.
4. Mengambil komponen resmi GEMS.
5. Memeriksa properties dan variants.
6. Memeriksa seluruh states yang tersedia.
7. Menggunakan instance komponen resmi.
8. Mengikuti struktur dan visual specification.
9. Memastikan penggunaan komponen sesuai konteks.
10. Memvalidasi hasil desain terhadap referensi GEMS.

### 7.3 Component Integrity

AI MUST mempertahankan:

- Component structure.
- Component anatomy.
- Properties.
- Variants.
- States.
- Typography.
- Color.
- Spacing.
- Visual specification.
- Interaction behavior.

AI MUST NOT:

- Membuat komponen custom tanpa approval.
- Menggunakan UI library eksternal.
- Mengganti komponen resmi GEMS.
- Mengubah properties di luar konfigurasi yang tersedia.
- Membuat variant atau state baru tanpa approval.
- Mengubah visual specification berdasarkan preferensi AI.

### 7.4 Missing Component Handling

Jika komponen tidak tersedia atau tidak dapat diverifikasi:

1. AI MUST mengidentifikasi komponen yang dibutuhkan.
2. AI MUST memeriksa alternatif resmi GEMS.
3. AI MAY memberikan rekomendasi.
4. AI MUST menjelaskan alasan dan dampaknya.
5. AI MUST meminta Human Approval jika memerlukan perubahan.
6. AI MUST NOT mengimplementasikan komponen baru sebelum approval.

---

## 8. Mandatory UI States & Behavior

### 8.1 State Management Principles

Setiap desain Edit Data MUST menangani seluruh kondisi interaksi yang relevan.

AI MUST NOT hanya menghasilkan Default State dan Success State.

AI MUST mencakup kondisi:

- Form pertama kali dibuka.
- Data diubah.
- Data tidak berubah.
- Input tidak valid.
- Field atau aksi tidak tersedia.
- Penyimpanan berlangsung.
- Konfirmasi penyimpanan.
- Penyimpanan berhasil.
- Penyimpanan gagal.
- Gangguan koneksi.
- Kesalahan sistem.
- Pembatalan.
- Keluar dengan perubahan belum tersimpan.

### 8.2 Required State Matrix

| State | When to Use | Required Behavior |
|---|---|---|
| Default | Edit Form dibuka | Menampilkan existing values |
| Focus | Field dipilih | Menggunakan Focus State resmi |
| Filled | Field memiliki nilai | Menampilkan nilai input |
| Modified | Data diubah | Mempertahankan perubahan |
| Unchanged | Tidak ada perubahan | Mengikuti Save dan Exit Behavior |
| Required | Field wajib diisi | Mengikuti validation rules |
| Validation Error | Input tidak valid | Menampilkan feedback kesalahan |
| Disabled | Aksi tidak tersedia | Menggunakan Disabled State |
| Read-only | Field tidak dapat diedit | Menampilkan nilai tanpa izin perubahan |
| Loading | Save diproses | Menampilkan loading feedback |
| Confirmation | Pengguna memilih Save | Menampilkan Confirmation Modal |
| Success | Save berhasil | Menampilkan Success Toast |
| Save Error | Save gagal | Menampilkan Error Feedback |
| Network Error | Gangguan koneksi | Menampilkan feedback koneksi |
| Server Error | Kesalahan sistem | Menampilkan feedback sistem |
| Unsaved Changes | Keluar setelah mengubah data | Menampilkan Exit Confirmation |
| Cancelled | Pengguna membatalkan tindakan | Mengikuti navigasi resmi |
| Updated Data | Save berhasil | Menampilkan nilai terbaru |

### 8.3 Default & Existing Data

AI MUST:

- Menampilkan existing values.
- Menggunakan field sesuai HSD/BRD.
- Mengikuti role dan permission.
- Mempertahankan identitas record.
- Menggunakan komponen GEMS.

### 8.4 Modified & Unchanged

AI MUST:

- Membedakan nilai awal dan nilai terbaru.
- Mempertahankan perubahan selama Edit.
- Mengikuti Save Behavior resmi.
- Menggunakan kondisi perubahan untuk Exit Flow.

### 8.5 Validation Error

AI MUST:

- Menggunakan validation rules dari HSD/BRD.
- Menampilkan pesan error pada field terkait.
- Menggunakan Error State resmi GEMS.
- Mempertahankan input pengguna.
- Mengikuti ketentuan penyimpanan saat validasi gagal.

AI MUST NOT membuat validation rules baru.

### 8.6 Disabled & Read-only

AI MUST:

- Menggunakan state resmi GEMS.
- Mengikuti Role Access Matrix.
- Mengikuti status data.
- Menentukan ketersediaan aksi berdasarkan business rule.

AI MUST NOT mengubah permission berdasarkan asumsi.

### 8.7 Loading

AI MUST:

- Menggunakan loading behavior resmi GEMS.
- Menunjukkan proses penyimpanan.
- Mencegah duplicate submission sesuai behavior sistem.
- Mempertahankan data selama proses.
- Menunggu hasil sistem sebelum menampilkan feedback akhir.

### 8.8 Confirmation

AI MUST:

- Menggunakan Confirmation Modal resmi.
- Mengikuti urutan Save dan Confirmation.
- Menggunakan wording sesuai konteks Edit Data.
- Mengikuti tindakan konfirmasi dan pembatalan.

### 8.9 Success

AI MUST:

- Menggunakan Success Toast resmi.
- Menampilkan updated values.
- Mengikuti navigasi akhir pattern.
- Menampilkan feedback setelah proses berhasil.

### 8.10 Save Error

AI MUST:

- Menggunakan Error Feedback resmi GEMS.
- Menjelaskan bahwa penyimpanan gagal.
- Mempertahankan perubahan pengguna.
- Mengikuti retry behavior jika didukung.
- Menjaga konteks Edit sesuai approved flow.

AI MUST NOT menampilkan Success ketika Save gagal.

### 8.11 Network Error

AI MUST:

- Menggunakan feedback gangguan koneksi resmi GEMS.
- Mempertahankan perubahan yang belum tersimpan.
- Mengikuti retry behavior yang disetujui.
- Tidak menganggap Save berhasil jika status belum terkonfirmasi.

AI MUST NOT membuat offline saving atau automatic retry tanpa approval.

### 8.12 Server Error

AI MUST:

- Menggunakan Error Feedback resmi.
- Menampilkan pesan sesuai konteks.
- Mempertahankan perubahan pengguna.
- Mengikuti error handling berdasarkan requirement.

AI MUST NOT mengarang kode error atau mekanisme sistem.

### 8.13 Unsaved Changes

AI MUST:

- Memeriksa kondisi perubahan data.
- Mengikuti decision point resmi.
- Menggunakan Exit Confirmation jika diwajibkan.
- Mempertahankan perubahan jika pengguna kembali mengedit.
- Mengikuti navigasi resmi jika pengguna keluar.

### 8.14 State Completeness

AI MUST memeriksa seluruh state pada setiap pattern.

Setiap state yang relevan MUST dibuatkan representasi UI.

State yang tidak berlaku MUST disertai alasan.

Jika state membutuhkan behavior atau flow baru, AI MUST merekomendasikannya untuk Human Approval.

AI MUST NOT menghilangkan Error, Loading, atau Unsaved Changes hanya karena tidak ditampilkan pada contoh Main Flow.

---

## 9. Mandatory UX Flow Diagram & UI Screens

### 9.1 Flow-First Design

Setiap output Edit Data MUST memiliki UX Flow Diagram dan UI Screens.

Struktur output MUST mengikuti dokumentasi GEMS:

**Bagian Atas — UX Flow Diagram**

**Bagian Bawah — UI Screens & States**

AI MUST memastikan Flow Diagram menggambarkan desain aktual yang dihasilkan.

### 9.2 Figma Layout Rules

AI MUST:

1. Membuat satu kelompok desain untuk setiap fitur Edit Data.
2. Menempatkan UX Flow Diagram secara fisik di atas UI Screens dalam Figma.
3. Menempatkan Main Flow pada bagian utama diagram.
4. Menampilkan Alternative Flow sebagai percabangan yang terhubung.
5. Menempatkan UI Screens di bawah diagram sesuai urutan Main Flow.
6. Menempatkan variasi state yang relevan bersama screen asalnya.
7. Menggunakan nama screen dan state yang jelas.
8. Memastikan seluruh flow node dapat ditelusuri ke screen atau state.
9. Menjaga diagram dan UI berada dalam satu section atau kelompok desain.
10. Mengikuti struktur visual referensi GEMS.

AI MUST NOT hanya menuliskan flow sebagai deskripsi teks tanpa membuat Flow Diagram pada canvas Figma.

### 9.3 Required Flow Elements

AI MUST menampilkan:

1. Start.
2. Entry Point.
3. Edit Action.
4. Edit Form.
5. User Actions.
6. Decision Points.
7. Save Flow.
8. Confirmation Flow.
9. Success Flow.
10. Cancel & Exit Flow.
11. Approved Error Handling.
12. End State.

### 9.4 Main Flow

AI MUST:

- Mengambil Main Flow dari pattern resmi.
- Mempertahankan urutan node.
- Menggunakan data HSD/BRD.
- Menghasilkan screen sesuai flow.
- Mengikuti navigasi resmi.

AI MUST NOT membuat Main Flow baru tanpa approval.

### 9.5 Alternative Flow

AI MUST:

- Mengambil Alternative Flow dari pattern resmi.
- Menampilkan percabangan Cancel dan Exit.
- Mempertahankan decision point.
- Mengikuti Confirmation Modal.
- Mempertahankan jalur kembali ke form.

AI MUST NOT menambahkan percabangan baru tanpa Human Approval.

### 9.6 State & Error Flow

AI MUST memastikan setiap state yang relevan terhubung dengan interaksi pada flow.

Jika state dapat ditampilkan pada screen yang sudah tersedia, AI MUST menggunakan screen tersebut dengan variasi state yang sesuai.

Jika state membutuhkan screen atau flow baru, AI MUST:

1. Mengidentifikasi kebutuhan.
2. Membuat rekomendasi terpisah.
3. Menjelaskan dampaknya.
4. Meminta Human Approval.
5. Menunggu approval sebelum implementasi.

### 9.7 Flow-to-Screen Mapping

| Flow Condition | UI Screen / State | Expected Result |
|---|---|---|
| Buka Edit | Default Edit Form | Existing values ditampilkan |
| Ubah data | Modified | Nilai terbaru ditampilkan |
| Input tidak valid | Validation Error | Error feedback |
| Klik Save | Confirmation | Confirmation Modal |
| Konfirmasi Save | Loading | Proses penyimpanan |
| Save berhasil | Success | Success Toast |
| Save gagal | Save Error | Error feedback |
| Koneksi gagal | Network Error | Feedback koneksi |
| Server gagal | Server Error | Feedback sistem |
| Keluar dengan perubahan | Unsaved Changes | Exit Confirmation |
| Save berhasil | Updated Data | Data terbaru ditampilkan |

AI MUST menyesuaikan mapping dengan pattern terpilih.

---

## 10. Pattern Recommendation & Human Approval

### 10.1 When AI May Recommend Changes

AI MAY merekomendasikan penyesuaian UX Flow ketika:

- Tidak ada pattern resmi yang memenuhi kebutuhan.
- Entry point tidak sesuai.
- Struktur form tidak didukung.
- Business rule membutuhkan alur berbeda.
- Terdapat kebutuhan state atau error handling baru.
- Terdapat konflik antara HSD/BRD dan pattern resmi.

AI MUST menggunakan pattern resmi GEMS sebagai dasar rekomendasi.

AI MUST NOT langsung mengimplementasikan proposed flow.

### 10.2 Recommendation Workflow

**Step 1 — Identify Gap**

AI MUST menjelaskan ketidaksesuaian antara requirement dan pattern.

**Step 2 — Evaluate Existing Patterns**

AI MUST memeriksa ketiga pattern sebelum mengusulkan perubahan.

**Step 3 — Recommend Flow**

AI MAY memberikan usulan penyesuaian flow.

**Step 4 — Explain Impact**

AI MUST menjelaskan dampak terhadap screens, states, interactions, dan navigation.

**Step 5 — Request Human Approval**

AI MUST meminta persetujuan manusia yang berwenang.

**Step 6 — Wait for Approval**

AI MUST NOT menerapkan perubahan selama approval belum diberikan.

**Step 7 — Implement Approved Changes**

Setelah disetujui, AI MAY menerapkan perubahan sesuai cakupan approval.

**Step 8 — Validate**

AI MUST memvalidasi hasil terhadap HSD/BRD dan GEMS.

### 10.3 Recommendation Format

| Informasi | Keterangan |
|---|---|
| Feature | Nama fitur |
| User Role | Role pengguna |
| Current Pattern | Pattern resmi yang paling sesuai |
| Business Requirement | Kebutuhan HSD/BRD |
| Identified Gap | Ketidaksesuaian |
| Recommended Flow | Usulan penyesuaian |
| Impact | Dampak screen, state, dan navigation |
| Approval Status | Pending Human Approval |

### 10.4 Approval Enforcement

AI MUST:

- Memisahkan Approved Flow dan Proposed Flow.
- Menjelaskan alasan perubahan.
- Meminta explicit Human Approval.
- Menunggu keputusan sebelum implementasi.
- Mengikuti batasan persetujuan.

AI MUST NOT:

- Menganggap rekomendasi sebagai approval.
- Menganggap tidak adanya respons sebagai persetujuan.
- Menerapkan perubahan berstatus Pending.
- Mengubah komponen GEMS tanpa approval.
- Mengubah bagian di luar cakupan persetujuan.

---

## 11. Required AI Design Output

Setiap permintaan Edit Data MUST menghasilkan:

### Output 01 — Pattern Selection

- Feature Name.
- User Role.
- Selected Pattern.
- Selection Rationale.
- Requirement Compatibility.

### Output 02 — UX Flow Diagram

- Main Flow.
- Alternative Flow.
- Decision Points.
- Confirmation Flow.
- Cancel & Exit Flow.
- Success Flow.
- Approved Error Handling.
- End State.

### Output 03 — UI Screens

- Seluruh screens sesuai pattern.
- Existing data pada Edit Form.
- Field sesuai HSD/BRD.
- Komponen resmi GEMS.
- Confirmation dan feedback.
- Seluruh UI States yang relevan.

### Output 04 — State Coverage

AI MUST memeriksa:

- Default.
- Focus dan Filled.
- Modified dan Unchanged.
- Validation Error.
- Disabled dan Read-only.
- Loading.
- Confirmation.
- Success.
- Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.
- Updated Data.

State yang tidak berlaku MUST disertai alasan.

### Output 05 — Flow-to-Screen Mapping

AI MUST menunjukkan hubungan antara flow node, screen, action, state, dan expected result.

### Output 06 — Compliance & Approval

AI MUST melaporkan:

- Pattern Compliance.
- Flow Compliance.
- GEMS Component Compliance.
- HSD/BRD Compliance.
- State Completeness.
- Pending Recommendations.
- Human Approval Status.

---

## 12. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut.

**Step 1 — Read HSD/BRD**

Identifikasi kebutuhan bisnis, existing data, field, role, permission, validation, dan status.

**Step 2 — Inspect GEMS Patterns**

Periksa ketiga Edit Data UX Pattern beserta Flow Diagram dan UI Screens.

**Step 3 — Compare Patterns**

Bandingkan kebutuhan dengan struktur dan behavior setiap pattern.

**Step 4 — Select Pattern**

Pilih pattern yang paling sesuai dan jelaskan alasannya.

**Step 5 — Check Compatibility**

Identifikasi konflik dan kebutuhan yang belum didukung.

**Step 6 — Request Human Approval if Needed**

Jika pattern tidak sesuai, buat rekomendasi dan tunggu approval sebelum menerapkan perubahan.

**Step 7 — Retrieve GEMS Components**

Ambil seluruh komponen, properties, variants, dan states yang diperlukan.

**Step 8 — Generate UX Flow Diagram**

Gunakan flow resmi dan sesuaikan konteksnya dengan HSD/BRD.

**Step 9 — Generate UI Screens**

Buat seluruh screen sesuai pattern dan flow.

**Step 10 — Generate UI States**

Buat seluruh state relevan, termasuk validation, loading, error, dan unsaved changes.

**Step 11 — Map Flow to Screens**

Pastikan seluruh node, screens, actions, dan states saling sesuai.

**Step 12 — Validate Against GEMS**

Bandingkan hasil dengan pattern dan komponen resmi.

**Step 13 — Report Compliance**

Laporkan hasil validasi, keterbatasan, dan approval yang masih diperlukan.

---

## 13. AI Restrictions

AI MUST NOT:

1. Membuat pattern baru tanpa approval.
2. Menggabungkan pattern tanpa approval.
3. Mengubah approved pattern.
4. Menambah atau menghapus screen tanpa approval.
5. Mengubah entry point.
6. Mengubah urutan flow.
7. Mengubah decision point.
8. Mengubah Confirmation Flow.
9. Mengubah Cancel & Exit Flow.
10. Menghilangkan Error atau Loading State yang relevan.
11. Menghasilkan UI tanpa Flow Diagram.
12. Menghasilkan flow yang berbeda dari UI.
13. Mengarang existing data.
14. Mengarang field, validation, role, atau status.
15. Menggunakan komponen non-GEMS.
16. Membuat komponen custom tanpa approval.
17. Mengubah properties atau variants di luar ketentuan.
18. Mengimplementasikan Proposed Flow sebelum Human Approval.
19. Menyatakan desain compliant tanpa verifikasi.

---

## 14. Quality Assurance & Compliance

### 14.1 Requirement Compliance

AI MUST memastikan field, data, status, validation, dan permission sesuai approved HSD/BRD.

### 14.2 Pattern Compliance

AI MUST memastikan pattern terpilih sesuai kebutuhan dan mengikuti struktur resmi.

### 14.3 GEMS Component Compliance

AI MUST memastikan seluruh komponen menggunakan GEMS Design System, termasuk properties, variants, dan states yang tersedia.

### 14.4 Flow Compliance

AI MUST:

- Menempatkan Flow Diagram di atas UI Screens.
- Memastikan seluruh screen mengikuti flow.
- Menampilkan Main Flow dan Alternative Flow.
- Mempertahankan Decision Point.
- Memastikan Confirmation dan Exit Flow sesuai.

### 14.5 State Completeness

AI MUST memastikan seluruh state relevan ditangani, termasuk:

- Validation Error.
- Loading.
- Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.

AI MUST memastikan state dapat ditelusuri ke flow dan UI.

### 14.6 Human Approval Compliance

AI MUST:

- Mengidentifikasi ketidaksesuaian.
- Membuat rekomendasi terpisah.
- Meminta Human Approval sebelum perubahan.
- Tidak menerapkan perubahan berstatus Pending.

### 14.7 Final Validation Checklist

AI MUST memastikan output memiliki:

1. Pattern Selection.
2. UX Flow Diagram.
3. UI Screens.
4. Main Flow dan Alternative Flow.
5. Complete UI States.
6. Flow-to-Screen Mapping.
7. GEMS Component Compliance.
8. HSD/BRD Compliance.
9. Human Approval Status.

Jika terdapat ketidaksesuaian, AI MUST melaporkannya sebelum menyatakan desain siap diimplementasikan.

---

## 15. Final AI Enforcement

AI MUST:

1. Membaca approved HSD/BRD.
2. Memeriksa ketiga Edit Data UX Pattern resmi GEMS.
3. Memilih pattern berdasarkan kebutuhan bisnis.
4. Menggunakan pattern resmi sebagai acuan flow.
5. Menggunakan komponen resmi GEMS untuk seluruh UI.
6. Menghasilkan UX Flow Diagram di bagian atas desain.
7. Menghasilkan UI Screens di bagian bawah desain.
8. Menampilkan existing values secara akurat.
9. Menghasilkan seluruh UI States yang relevan.
10. Menangani Success, Error, Loading, dan Failure.
11. Menghubungkan seluruh screens dan states dengan flow.
12. Mempertahankan struktur pattern resmi.
13. Merekomendasikan perubahan jika pattern tidak sesuai.
14. Meminta Human Approval sebelum menerapkan perubahan.
15. Memvalidasi hasil terhadap HSD/BRD dan GEMS.

### Final Enforcement Rule

> AI MUST select the most appropriate official GEMS Edit Data UX Pattern based on approved HSD/BRD. Every design MUST include a complete UX Flow Diagram positioned above the corresponding UI Screens, with all applicable UI States, including success, error, loading, validation, and unsaved changes. All UI components MUST originate from the official GEMS Design System. If no existing pattern fully supports the business requirements, AI MAY recommend a modified UX Flow but MUST obtain explicit Human Approval before implementing any changes.

**GEMS UX Pattern menentukan alur. GEMS Design System menentukan komponen. HSD/BRD menentukan kebutuhan bisnis. Human Approval menentukan apakah perubahan diperbolehkan.**
