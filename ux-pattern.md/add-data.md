# GEMS Design System — Add New Data UX Pattern Guidelines

## 1. Purpose & Core Principles

Add New Data merupakan UX Pattern yang digunakan untuk membuat atau menambahkan data baru ke dalam sistem.

GEMS menyediakan empat Add New Data UX Pattern resmi dengan struktur, alur interaksi, dan behavior yang berbeda.

AI MUST menganalisis kebutuhan HSD/BRD, memilih pattern yang paling sesuai, menggunakan komponen resmi GEMS Design System, serta menghasilkan UX Flow Diagram dan UI Screens yang mencakup seluruh kondisi interaksi pengguna.

### 1.1 Core Principles

**1. Requirement-Based Selection**

AI MUST memilih UX Pattern berdasarkan approved HSD/BRD, bukan preferensi visual.

**2. Official Pattern Reuse**

AI MUST menggunakan salah satu dari empat Add New Data UX Pattern resmi GEMS sebagai acuan utama.

**3. Flow Integrity**

AI MUST mempertahankan struktur, urutan interaksi, decision point, navigation, dan behavior pattern terpilih.

**4. GEMS Component Compliance**

AI MUST menggunakan komponen resmi GEMS Design System beserta properties, variants, states, dan visual specification yang tersedia.

**5. Flow-Driven Design**

AI MUST menghasilkan UX Flow Diagram secara fisik di atas UI Screens dalam section Figma yang sama, mengikuti struktur UX Pattern GEMS.

**6. Complete State Management**

AI MUST menangani dan mendesain seluruh UI States yang relevan, termasuk Default, Focus, Filled, Validation Error, Disabled, Loading, Success, Save Error, Network Error, Server Error, Draft, dan Unsaved Changes.

**7. Business Data Accuracy**

AI MUST menggunakan field, status, role, validation, dan business rules dari approved HSD/BRD.

**8. Human Approval**

AI MAY merekomendasikan perubahan UX Flow jika pattern resmi tidak memenuhi kebutuhan bisnis. AI MUST memperoleh explicit Human Approval sebelum menerapkan perubahan.

### 1.2 Core Enforcement

> UX Pattern menentukan struktur dan alur interaksi. HSD/BRD menentukan kebutuhan bisnis. GEMS Design System menentukan komponen. Human Approval menentukan apakah perubahan diperbolehkan.

AI MUST NOT mengubah approved flow atau komponen resmi berdasarkan asumsi.

---

## 2. Source of Truth & Pattern Selection

### 2.1 Source of Truth

| Source | Fungsi |
|---|---|
| Approved HSD/BRD | Kebutuhan bisnis, field, validation, status, dan proses |
| GEMS Add New Data UX Pattern | Flow, screens, navigation, dan interaction |
| GEMS Design System | Components, properties, variants, states, dan visual specification |
| Role Access Matrix | Hak akses dan tindakan pengguna |
| Human Approval | Persetujuan perubahan atau pengecualian |

AI MUST memeriksa sumber resmi sebelum menghasilkan desain.

AI MUST NOT mengarang field, role, validation, status, atau business rule.

### 2.2 Available Patterns

| Pattern | Type | Karakteristik |
|---|---|---|
| Pattern 01 | Modal / Popup | Penambahan data melalui Modal |
| Pattern 02 | New Page | Form halaman khusus dengan Save as Draft |
| Pattern 03 | Multi-step New Page | Pengisian melalui beberapa tahapan |
| Pattern 04 | Multi-step with Preview | Pengisian bertahap dengan Preview dan Save as Draft |

### 2.3 UX Pattern Selection Matrix

| Kebutuhan | Recommended Pattern | Alasan |
|---|---|---|
| Form sederhana dengan input ringkas | Pattern 01 | Pengisian dapat dilakukan melalui Modal |
| Form membutuhkan halaman khusus dan Draft | Pattern 02 | Form memiliki area lebih luas dan mendukung penyimpanan sementara |
| Form memiliki beberapa kelompok informasi | Pattern 03 | Pengisian menggunakan tahapan |
| Form bertahap membutuhkan pemeriksaan sebelum Save | Pattern 04 | Pengguna dapat meninjau informasi melalui Preview |

### 2.4 Pattern Selection Rules

AI MUST:

1. Membaca approved HSD/BRD.
2. Mengidentifikasi entry point penambahan data.
3. Memeriksa keempat pattern resmi.
4. Membandingkan kebutuhan dengan struktur dan behavior setiap pattern.
5. Mempertimbangkan Modal, New Page, Multi-step, Draft, dan Preview.
6. Memilih pattern yang paling sesuai.
7. Mempertahankan pattern yang sudah ditetapkan dalam approved design.
8. Menjelaskan alasan pemilihan.
9. Melaporkan konflik untuk Human Review.
10. Meminta Human Approval jika pattern perlu dimodifikasi.

AI MUST NOT:

- Memilih pattern hanya berdasarkan jumlah field.
- Memilih pattern berdasarkan preferensi visual.
- Menggabungkan pattern tanpa approval.
- Membuat pattern baru secara mandiri.
- Menambahkan Draft atau Preview ke pattern yang tidak mendukungnya.

---

## 3. Pattern 01 — Add Data via Modal

**Figma Reference:** [Pattern 01 — Modal / Popup](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3305-14747&t=zv6vn5L7CsEWbtOz-1)

### 3.1 When to Use

Pattern 01 digunakan ketika penambahan data dapat diselesaikan melalui form dalam Modal tanpa berpindah ke halaman khusus.

| Kondisi | Penggunaan |
|---|---|
| Form sederhana | Recommended |
| Input ringkas | Recommended |
| Membutuhkan Modal | Recommended |
| Membutuhkan Multi-step | Not Recommended |
| Membutuhkan Save as Draft | Not Recommended |
| Membutuhkan Preview Page | Not Recommended |

### 3.2 Official Main Flow

AI MUST mengikuti:

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

AI MUST:

1. Mengikuti tindakan Cancel atau Tutup Form.
2. Memeriksa kondisi form kosong atau sudah terisi.
3. Mengikuti decision point resmi.
4. Menggunakan Exit Confirmation jika diwajibkan.
5. Mempertahankan input ketika pengguna kembali ke form.
6. Mengikuti navigasi resmi ketika pengguna mengonfirmasi keluar.

### 3.4 Required UI States

AI MUST menghasilkan representasi desain untuk:

- Default — Form kosong.
- Focus — Field sedang dipilih.
- Filled — Field telah diisi.
- Required — Field wajib diisi.
- Validation Error — Input tidak valid.
- Disabled — Tindakan belum tersedia.
- Read-only — Field tidak dapat diubah jika berlaku.
- Loading — Proses penyimpanan.
- Confirmation — Konfirmasi penyimpanan.
- Success — Data berhasil disimpan.
- Save Error — Penyimpanan gagal.
- Network Error — Gangguan koneksi.
- Server Error — Kesalahan sistem.
- Unsaved Changes — Keluar ketika form telah diisi.
- Cancelled — Pengguna membatalkan tindakan.
- Updated List — Daftar menampilkan data terbaru.

State yang tidak berlaku MUST disertai alasan.

### 3.5 Required Design Output

AI MUST menghasilkan:

1. UX Flow Diagram di bagian atas.
2. List / Data Table.
3. Add Form Modal.
4. Confirmation Modal.
5. Success Toast.
6. List Page dengan data terbaru.
7. Exit Confirmation.
8. Seluruh UI States yang relevan.

### 3.6 Pattern Restrictions

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

**Figma Reference:** [Pattern 02 — New Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3310-27399&t=zv6vn5L7CsEWbtOz-1)

### 4.1 When to Use

Pattern 02 digunakan ketika penambahan data membutuhkan halaman khusus dan mendukung penyimpanan sementara melalui Save as Draft.

| Kondisi | Penggunaan |
|---|---|
| Form membutuhkan halaman khusus | Recommended |
| Form lebih luas dibanding Modal | Recommended |
| Membutuhkan Save as Draft | Recommended |
| Membutuhkan Multi-step | Not Recommended |
| Membutuhkan Preview Page | Not Recommended |

### 4.2 Official Main Flow

AI MUST mengikuti:

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

AI MUST mempertahankan pemisahan antara Final Save dan Save as Draft.

### 4.3 Save as Draft Flow

AI MUST:

1. Menampilkan kontrol Save as Draft sesuai pattern.
2. Mengikuti urutan penyimpanan Draft resmi.
3. Menggunakan Draft Success Toast setelah proses berhasil.
4. Menggunakan status Draft sesuai HSD/BRD.
5. Mengikuti navigasi akhir Draft.
6. Mempertahankan perbedaan antara Draft dan final submission.

AI MUST NOT:

- Mengubah Save as Draft menjadi autosave.
- Menganggap Draft sebagai final submission.
- Menghapus Draft Flow tanpa approval.

### 4.4 Cancel & Exit Flow

AI MUST:

- Mengikuti kondisi form kosong atau terisi.
- Menggunakan Exit Confirmation sesuai pattern.
- Mempertahankan data ketika pengguna kembali ke form.
- Mengikuti navigasi pembatalan resmi.

### 4.5 Required UI States

AI MUST menghasilkan representasi desain untuk:

- Default.
- Focus.
- Filled.
- Required.
- Validation Error.
- Disabled.
- Read-only jika berlaku.
- Loading Final Save.
- Loading Draft Save.
- Confirmation.
- Success.
- Draft Success.
- Save Error.
- Draft Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.
- Cancelled.
- Updated List.

### 4.6 Required Design Output

AI MUST menghasilkan:

1. UX Flow Diagram di bagian atas.
2. List / Data Table.
3. Add Form New Page.
4. Final Save Flow.
5. Save as Draft Flow.
6. Confirmation Modal.
7. Success Toast.
8. Draft Success Toast.
9. List Page dengan data terbaru atau status Draft.
10. Exit Confirmation.
11. Seluruh UI States yang relevan.

### 4.7 Pattern Restrictions

AI MUST NOT:

1. Mengubah New Page menjadi Modal.
2. Menambahkan Stepper.
3. Menambahkan Preview Page.
4. Menghapus Save as Draft.
5. Mengubah urutan penyimpanan.
6. Mengubah Cancel atau Exit Flow.

---

## 5. Pattern 03 — Multi-step Add Data

**Figma Reference:** [Pattern 03 — Multi-step New Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3314-34982&t=zv6vn5L7CsEWbtOz-1)

### 5.1 When to Use

Pattern 03 digunakan ketika informasi perlu dibagi menjadi beberapa tahapan pengisian dengan urutan yang jelas.

| Kondisi | Penggunaan |
|---|---|
| Data memiliki beberapa kelompok informasi | Recommended |
| Pengisian membutuhkan tahapan | Recommended |
| Membutuhkan navigasi Next dan Back | Recommended |
| Membutuhkan Preview Page khusus | Not Recommended |

### 5.2 Official Main Flow

AI MUST mengikuti:

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

Jumlah, nama, dan urutan step MUST mengikuti approved requirements dan struktur pattern resmi.

### 5.3 Step Navigation

AI MUST:

1. Menggunakan struktur Multi-step resmi.
2. Menggunakan Progress Indicator resmi GEMS.
3. Mengikuti behavior Next dan Back.
4. Mempertahankan input ketika berpindah step.
5. Mengikuti validasi berdasarkan HSD/BRD.
6. Mengikuti urutan step yang disetujui.
7. Menampilkan state step yang sedang aktif.

AI MUST NOT menambah, menghapus, menggabungkan, atau mengubah urutan step tanpa approval.

### 5.4 Validation & Step Behavior

AI MUST:

- Menggunakan validation rules resmi.
- Menampilkan Validation Error pada field terkait.
- Mengikuti aturan kapan pengguna dapat melanjutkan step.
- Mempertahankan input ketika validasi gagal.
- Mengikuti behavior navigasi step resmi.

AI MUST NOT membuat aturan validasi atau step navigation baru.

### 5.5 Save & Exit Flow

AI MUST:

- Mengikuti Final Save pada step terakhir.
- Menggunakan Confirmation Modal.
- Menampilkan Success Toast setelah berhasil.
- Mengikuti Cancel dan Exit Flow resmi.
- Mempertahankan input jika pengguna kembali ke form.

### 5.6 Required UI States

AI MUST menghasilkan representasi desain untuk:

- Default Step.
- Active Step.
- Completed Step jika didukung.
- Focus.
- Filled.
- Required.
- Validation Error.
- Disabled Next.
- Disabled Save.
- Read-only jika berlaku.
- Loading.
- Confirmation.
- Success.
- Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.
- Cancelled.
- Updated List.

### 5.7 Required Design Output

AI MUST menghasilkan:

1. UX Flow Diagram di bagian atas.
2. List / Data Table.
3. Seluruh Multi-step Screens.
4. Progress Indicator.
5. Step Navigation.
6. Validation States per step.
7. Confirmation Modal.
8. Success Toast.
9. Updated List Page.
10. Exit Confirmation.
11. Seluruh UI States yang relevan.

### 5.8 Pattern Restrictions

AI MUST NOT:

1. Mengubah Multi-step menjadi Single Page.
2. Menambah atau menghapus step.
3. Mengubah urutan step.
4. Menambahkan Preview.
5. Menambahkan Draft yang tidak didukung.
6. Mengubah Next atau Back Behavior.
7. Mengubah Save dan Confirmation Flow.

---

## 6. Pattern 04 — Multi-step with Preview

**Figma Reference:** [Pattern 04 — Multi-step with Preview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3338-41046&t=zv6vn5L7CsEWbtOz-1)

### 6.1 When to Use

Pattern 04 digunakan ketika pengisian data dilakukan secara bertahap dan membutuhkan Preview untuk meninjau informasi sebelum final Save.

| Kondisi | Penggunaan |
|---|---|
| Data memiliki beberapa kelompok informasi | Recommended |
| Membutuhkan Multi-step | Recommended |
| Membutuhkan Preview Page | Recommended |
| Membutuhkan Save as Draft | Recommended |

### 6.2 Official Main Flow

AI MUST mengikuti:

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

AI MUST:

1. Menggunakan Preview Page resmi.
2. Menampilkan informasi dari step sebelumnya.
3. Mempertahankan pengelompokan data.
4. Mengikuti behavior Back dan Save.
5. Memastikan informasi Preview konsisten dengan input.
6. Menggunakan komponen GEMS.

AI MUST NOT:

- Mengubah Preview menjadi Modal.
- Menambahkan field baru pada Preview.
- Menghilangkan Preview tanpa approval.
- Membuat mekanisme edit langsung pada Preview tanpa dasar approved flow.

### 6.4 Save as Draft

AI MUST:

- Menggunakan mekanisme Draft resmi.
- Mengikuti posisi dan ketersediaan tindakan Draft.
- Menampilkan Draft Success Toast setelah berhasil.
- Menggunakan status Draft sesuai HSD/BRD.
- Mengikuti navigasi akhir Draft.

AI MUST NOT mengubah Draft menjadi autosave.

### 6.5 Cancel & Exit Flow

AI MUST:

- Mengikuti percabangan keluar resmi.
- Menggunakan Exit Confirmation sesuai pattern.
- Mempertahankan input jika pengguna kembali ke form.
- Mengikuti navigasi resmi setelah pembatalan.

### 6.6 Required UI States

AI MUST menghasilkan representasi desain untuk:

- Default Step.
- Active Step.
- Completed Step jika didukung.
- Focus.
- Filled.
- Required.
- Validation Error.
- Disabled.
- Read-only jika berlaku.
- Loading Final Save.
- Loading Draft Save.
- Preview Default.
- Preview with Data.
- Confirmation.
- Success.
- Draft Success.
- Save Error.
- Draft Save Error.
- Network Error.
- Server Error.
- Unsaved Changes.
- Cancelled.
- Updated List.

### 6.7 Required Design Output

AI MUST menghasilkan:

1. UX Flow Diagram di bagian atas.
2. List / Data Table.
3. Seluruh Multi-step Screens.
4. Progress Indicator.
5. Preview Page.
6. Final Save Flow.
7. Save as Draft Flow.
8. Confirmation Modal.
9. Success Toast.
10. Draft Success Toast.
11. Updated List Page.
12. Exit Confirmation.
13. Seluruh UI States yang relevan.

### 6.8 Pattern Restrictions

AI MUST NOT:

1. Mengubah Multi-step menjadi Single Page.
2. Menambah atau menghapus step.
3. Mengubah urutan step.
4. Menghapus Preview.
5. Menghapus Draft.
6. Mengubah Confirmation Modal.
7. Mengubah navigasi Preview.
8. Menggabungkan Pattern 04 dengan pattern lain.

---

## 7. Mandatory GEMS Component Usage

### 7.1 Official Component Source

Seluruh UI Add New Data MUST menggunakan komponen resmi GEMS Design System.

**Component Source:** [GEMS Design System — Official Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)

### 7.2 Component Retrieval Rules

Sebelum membuat desain, AI MUST:

1. Mengakses GEMS Design System melalui Figma.
2. Memeriksa komponen yang digunakan pada pattern terpilih.
3. Mengidentifikasi seluruh komponen yang diperlukan.
4. Mengambil komponen resmi GEMS.
5. Memeriksa properties dan variants.
6. Memeriksa states yang tersedia.
7. Menggunakan instance komponen resmi jika akses Figma mendukungnya.
8. Mengikuti typography, color, spacing, dan visual specification.
9. Memastikan penggunaan komponen sesuai konteks.
10. Memvalidasi hasil terhadap referensi GEMS.

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

- Menggunakan UI library eksternal sebagai pengganti GEMS.
- Mengubah komponen resmi.
- Membuat variant baru tanpa approval.
- Mengubah visual specification berdasarkan preferensi AI.
- Mengklaim menggunakan instance GEMS jika hanya membuat tiruan visual.

### 7.4 Missing Component Handling

Jika komponen tidak tersedia atau tidak dapat diverifikasi:

1. AI MUST mengidentifikasi komponen yang dibutuhkan.
2. AI MUST memeriksa alternatif resmi GEMS.
3. AI MAY memberikan rekomendasi.
4. AI MUST menjelaskan alasan dan dampaknya.
5. AI MUST meminta Human Approval untuk komponen baru atau perubahan.
6. AI MUST NOT mengimplementasikan perubahan sebelum approval.

### 7.5 Component Documentation

AI MUST menggunakan dokumentasi komponen GEMS yang relevan, termasuk:

- Button.
- Input.
- Textarea.
- Dropdown.
- Toggle.
- Badge.
- Alert.
- Notification.
- Header.
- Pagination.
- Modal.
- Breadcrumbs.
- Empty State.
- File Upload.
- Navigation dan komponen pendukung lainnya.

AI MUST memeriksa dokumentasi dan Figma resmi untuk memastikan komponen sesuai kebutuhan.

---

## 8. Mandatory UI States & Behavior

### 8.1 State Management Principles

Setiap desain Add New Data MUST menangani seluruh kondisi interaksi yang relevan.

AI MUST NOT hanya menghasilkan Default State dan Success State.

AI MUST memeriksa kondisi:

- Form pertama kali dibuka.
- Pengguna mulai mengisi data.
- Data belum lengkap.
- Input tidak valid.
- Tindakan belum tersedia.
- Penyimpanan berlangsung.
- Konfirmasi penyimpanan.
- Penyimpanan berhasil.
- Penyimpanan gagal.
- Gangguan koneksi.
- Kesalahan sistem.
- Penyimpanan Draft.
- Penyimpanan Draft gagal.
- Navigasi antarstep.
- Preview.
- Pembatalan.
- Keluar dengan data belum tersimpan.

### 8.2 Required State Matrix

| State | When to Use | Required Behavior |
|---|---|---|
| Default | Form pertama kali dibuka | Menampilkan kondisi awal |
| Focus | Field dipilih | Menggunakan Focus State resmi |
| Filled | Field memiliki nilai | Mempertahankan input |
| Required | Field wajib diisi | Mengikuti validation rules |
| Validation Error | Input tidak valid | Menampilkan feedback kesalahan |
| Disabled | Tindakan belum tersedia | Menggunakan Disabled State |
| Read-only | Field tidak dapat diubah | Menampilkan nilai tanpa izin perubahan |
| Active Step | Pengguna berada pada step tertentu | Menunjukkan step aktif |
| Completed Step | Step selesai jika didukung | Menggunakan state progress resmi |
| Loading | Sistem memproses Save | Menampilkan loading feedback |
| Confirmation | Pengguna memilih Final Save | Menampilkan Confirmation Modal |
| Success | Final Save berhasil | Menampilkan Success Toast |
| Save Error | Final Save gagal | Menampilkan Error Feedback |
| Network Error | Gangguan koneksi | Menampilkan feedback koneksi |
| Server Error | Kesalahan sistem | Menampilkan feedback sistem |
| Draft Saving | Draft sedang disimpan | Menampilkan loading feedback |
| Draft Success | Draft berhasil disimpan | Menampilkan Draft Success Toast |
| Draft Save Error | Penyimpanan Draft gagal | Menampilkan Error Feedback |
| Preview | Pengguna meninjau data | Menampilkan informasi yang telah diisi |
| Unsaved Changes | Keluar ketika form telah diisi | Mengikuti Exit Confirmation |
| Cancelled | Pengguna membatalkan tindakan | Mengikuti navigasi resmi |
| Updated List | Data berhasil disimpan | Menampilkan data terbaru |

**Important:** State pada tabel merupakan kondisi interaksi yang wajib diperiksa, bukan daftar variant visual yang otomatis tersedia pada seluruh komponen GEMS.

### 8.3 Default, Focus & Filled

AI MUST:

- Menggunakan form sesuai HSD/BRD.
- Menggunakan komponen resmi GEMS.
- Menampilkan kondisi awal.
- Menggunakan Focus State resmi.
- Mempertahankan input yang telah diisi.
- Mengikuti field behavior resmi.

### 8.4 Required & Validation Error

AI MUST:

- Menggunakan validation rules dari HSD/BRD.
- Menampilkan error pada field terkait.
- Menggunakan Error State resmi GEMS.
- Mempertahankan input pengguna.
- Mengikuti ketentuan validasi sebelum Save atau Next.

AI MUST NOT:

- Mengarang validation rules.
- Mengarang pesan teknis sistem.
- Membuat visual Error State baru tanpa approval.

### 8.5 Disabled & Read-only

AI MUST:

- Menggunakan state resmi GEMS.
- Mengikuti Role Access Matrix.
- Mengikuti business rules.
- Menentukan ketersediaan aksi berdasarkan requirement.

AI MUST NOT menonaktifkan field atau tindakan berdasarkan asumsi.

### 8.6 Loading

AI MUST:

- Menggunakan loading behavior resmi GEMS.
- Menunjukkan proses penyimpanan.
- Mencegah duplicate submission sesuai behavior sistem.
- Mempertahankan input selama proses.
- Menunggu hasil sistem sebelum menampilkan feedback akhir.

AI MUST NOT menampilkan Success sebelum penyimpanan berhasil.

### 8.7 Confirmation

AI MUST:

- Menggunakan Confirmation Modal resmi.
- Mengikuti urutan Save dan Confirmation.
- Menggunakan wording sesuai konteks bisnis.
- Mengikuti tindakan konfirmasi dan pembatalan.
- Mempertahankan input jika pengguna membatalkan konfirmasi.

### 8.8 Success

AI MUST:

- Menggunakan Success Toast resmi.
- Menampilkan feedback setelah penyimpanan berhasil.
- Mengikuti navigasi akhir pattern.
- Menampilkan data terbaru sesuai hasil sistem.

### 8.9 Save Error

AI MUST:

- Menggunakan Error Feedback resmi GEMS.
- Menjelaskan bahwa penyimpanan gagal.
- Mempertahankan input pengguna.
- Mengikuti retry behavior jika didukung.
- Menjaga konteks form sesuai approved flow.

AI MUST NOT menampilkan Success ketika Save gagal.

### 8.10 Network Error

AI MUST:

- Menggunakan feedback gangguan koneksi resmi GEMS.
- Mempertahankan input yang belum tersimpan.
- Mengikuti retry behavior yang disetujui.
- Tidak menganggap Save berhasil jika hasil belum terkonfirmasi.

AI MUST NOT membuat offline saving atau automatic retry tanpa approval.

### 8.11 Server Error

AI MUST:

- Menggunakan Error Feedback resmi.
- Menampilkan pesan sesuai konteks.
- Mempertahankan input pengguna.
- Mengikuti error handling berdasarkan requirement.

AI MUST NOT mengarang kode error atau mekanisme backend.

### 8.12 Draft Saving, Success & Error

Berlaku pada Pattern 02 dan Pattern 04.

AI MUST:

- Membedakan Final Save dan Draft Save.
- Menggunakan loading feedback saat Draft disimpan.
- Menggunakan Draft Success Toast setelah berhasil.
- Menampilkan Error Feedback jika Draft gagal.
- Mempertahankan input jika Draft gagal.
- Mengikuti status dan navigasi Draft resmi.

AI MUST NOT menganggap Draft sebagai final submission.

### 8.13 Multi-step States

Berlaku pada Pattern 03 dan Pattern 04.

AI MUST:

- Menampilkan Active Step.
- Menggunakan Progress Indicator resmi.
- Mengikuti Next dan Back Behavior.
- Mempertahankan input antarstep.
- Menampilkan Validation Error pada step terkait.
- Mengikuti ketentuan Disabled Next atau Save.

AI MUST NOT membuat step navigation baru tanpa approval.

### 8.14 Preview States

Berlaku pada Pattern 04.

AI MUST:

- Menampilkan informasi yang telah diisi.
- Memastikan data Preview sesuai form.
- Mengikuti pengelompokan informasi resmi.
- Menggunakan komponen GEMS.
- Mengikuti Back dan Save Behavior.

AI MUST NOT menambahkan field atau aksi baru pada Preview tanpa approval.

### 8.15 Unsaved Changes

AI MUST:

- Memeriksa kondisi form kosong atau sudah terisi.
- Mengikuti decision point resmi.
- Menggunakan Exit Confirmation jika diwajibkan.
- Mempertahankan input jika pengguna kembali ke form.
- Mengikuti navigasi resmi setelah pengguna mengonfirmasi keluar.

### 8.16 State Completeness Rules

AI MUST:

1. Memeriksa seluruh state pada pattern terpilih.
2. Membuat representasi UI untuk setiap state yang relevan.
3. Menempatkan state bersama screen asalnya.
4. Menggunakan komponen GEMS.
5. Menghubungkan state dengan flow dan tindakan pengguna.
6. Menjelaskan state yang tidak berlaku.
7. Memisahkan kebutuhan error handling baru dari approved flow.
8. Meminta Human Approval jika diperlukan flow, screen, atau behavior baru.

AI MUST NOT menghilangkan Error, Loading, Validation, atau Unsaved Changes hanya karena tidak ditampilkan pada Main Flow.

---

## 9. Mandatory UX Flow Diagram & Figma Layout

### 9.1 Flow-First Design

Setiap output Add New Data MUST memiliki:

**Bagian Atas — UX Flow Diagram**

**Bagian Bawah — UI Screens & States**

Keduanya MUST berada dalam satu section atau kelompok desain yang sama di Figma.

AI MUST mengikuti struktur visual UX Pattern GEMS.

### 9.2 Figma Layout Rules

AI MUST:

1. Membuat satu section atau kelompok desain untuk setiap fitur Add New Data.
2. Menempatkan UX Flow Diagram secara fisik di atas UI Screens.
3. Menempatkan Main Flow sebagai jalur utama.
4. Menampilkan Alternative Flow sebagai percabangan terhubung.
5. Menempatkan UI Screens di bawah Flow Diagram.
6. Menyusun UI Screens sesuai urutan Main Flow.
7. Menempatkan variasi state bersama screen asalnya.
8. Menggunakan nama screen dan state yang jelas.
9. Memastikan seluruh flow node dapat ditelusuri ke screen atau state.
10. Menjaga konsistensi diagram dan UI.
11. Mengikuti layout referensi GEMS.

AI MUST NOT hanya memberikan deskripsi flow dalam teks tanpa membuat Flow Diagram pada canvas Figma.

### 9.3 Required Flow Elements

| Elemen | Fungsi | Ketentuan |
|---|---|---|
| Start | Awal proses | Required |
| Entry Point | Halaman awal | Required |
| User Action | Tindakan pengguna | Required |
| Screen / Page | Tampilan yang digunakan | Required |
| Decision Point | Percabangan kondisi | Sesuai pattern |
| Confirmation | Konfirmasi tindakan | Sesuai pattern |
| Draft Flow | Penyimpanan sementara | Pattern 02 & 04 |
| Step Navigation | Navigasi tahapan | Pattern 03 & 04 |
| Preview | Pemeriksaan data | Pattern 04 |
| System Feedback | Respons sistem | Required |
| Error Handling | Kondisi kegagalan yang relevan | Required untuk diperiksa |
| Navigation Path | Hubungan antarflow | Required |
| End | Akhir proses | Required |

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
- Menampilkan Cancel dan Exit.
- Mempertahankan decision point.
- Mengikuti Confirmation Modal.
- Menampilkan Draft Flow jika tersedia.
- Mempertahankan jalur kembali ke form.

AI MUST NOT menambahkan percabangan baru tanpa Human Approval.

### 9.6 State & Error Flow

AI MUST memastikan setiap state yang relevan memiliki hubungan yang jelas dengan flow.

Jika state dapat ditampilkan pada screen yang sudah tersedia, AI MUST menggunakan screen tersebut dengan variasi state yang sesuai.

Jika state membutuhkan screen, decision point, atau flow baru, AI MUST:

1. Mengidentifikasi kebutuhan.
2. Membuat rekomendasi terpisah.
3. Menjelaskan dampaknya.
4. Meminta Human Approval.
5. Menunggu approval sebelum implementasi.

### 9.7 Flow-to-Screen Mapping

| Flow Condition | UI Screen / State | Expected Result |
|---|---|---|
| Klik Add Data | Default Form | Form terbuka |
| Mulai mengisi | Focus / Filled | Input ditampilkan |
| Input tidak valid | Validation Error | Error feedback |
| Klik Next | Step Navigation | Step berikutnya sesuai aturan |
| Klik Preview | Preview | Data ditampilkan untuk ditinjau |
| Klik Save | Confirmation | Confirmation Modal |
| Konfirmasi Save | Loading | Proses penyimpanan |
| Save berhasil | Success | Success Toast |
| Save gagal | Save Error | Error feedback |
| Klik Save as Draft | Draft Saving | Proses penyimpanan Draft |
| Draft berhasil | Draft Success | Draft Success Toast |
| Draft gagal | Draft Save Error | Error feedback |
| Koneksi gagal | Network Error | Feedback koneksi |
| Server gagal | Server Error | Feedback sistem |
| Keluar dengan input | Unsaved Changes | Exit Confirmation |
| Save berhasil | Updated List | Data terbaru ditampilkan |

AI MUST menyesuaikan mapping dengan pattern terpilih.

---

## 10. Business Data Integration

### 10.1 Data Source Matrix

| Data | Sumber |
|---|---|
| Nama fitur | HSD/BRD |
| User Role | HSD/BRD / Role Access Matrix |
| Nama halaman | Approved design / HSD/BRD |
| Nama form | HSD/BRD |
| Field | HSD/BRD |
| Tindakan pengguna | Approved business flow |
| Validation | HSD/BRD |
| Status data | HSD/BRD |
| Confirmation | Pattern GEMS dan konteks bisnis |
| System Feedback | Pattern GEMS dan hasil proses |

### 10.2 Business Data Rules

AI MUST:

1. Menggunakan informasi bisnis yang tersedia.
2. Menjaga konsistensi istilah pada Flow Diagram dan UI.
3. Menggunakan field sesuai HSD/BRD.
4. Menggunakan status yang telah ditentukan.
5. Mengikuti role dan permission.
6. Menggunakan validation rules yang disetujui.
7. Mengikuti approved business flow.

AI MUST NOT:

- Mengarang field.
- Mengarang role.
- Mengarang status.
- Mengarang validation rules.
- Mengubah proses bisnis.
- Menggunakan data contoh sebagai business requirement.

Jika informasi penting belum tersedia, AI MUST meminta klarifikasi atau menandainya sebagai Pending Requirement.

---

## 11. Pattern Recommendation & Human Approval

### 11.1 When AI May Recommend Changes

AI MAY merekomendasikan penyesuaian UX Flow ketika:

- Tidak ada pattern resmi yang memenuhi kebutuhan.
- Entry point tidak sesuai.
- Struktur form tidak didukung.
- Business rule membutuhkan alur berbeda.
- Diperlukan state atau error handling baru.
- Terdapat konflik antara HSD/BRD dan pattern resmi.

AI MUST menggunakan pattern resmi sebagai dasar rekomendasi.

AI MUST NOT langsung mengimplementasikan proposed flow.

### 11.2 Recommendation Workflow

**Step 1 — Identify Gap**

AI MUST menjelaskan ketidaksesuaian antara requirement dan pattern.

**Step 2 — Evaluate Existing Patterns**

AI MUST memeriksa keempat pattern sebelum mengusulkan perubahan.

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

### 11.3 Recommendation Format

| Informasi | Keterangan |
|---|---|
| Feature | Nama fitur |
| User Role | Role pengguna |
| Current Pattern | Pattern resmi yang paling sesuai |
| Figma Reference | Referensi pattern |
| Business Requirement | Kebutuhan HSD/BRD |
| Identified Gap | Ketidaksesuaian |
| Recommended Flow | Usulan penyesuaian |
| Impact | Dampak screen, state, dan navigation |
| Approval Status | Pending Human Approval |

### 11.4 Approval Required

AI MUST meminta Human Approval sebelum:

1. Mengganti pattern yang sudah disetujui.
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
13. Mengubah error handling di luar approved behavior.

### 11.5 Approval Enforcement

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
- Mengubah bagian di luar cakupan persetujuan.

---

## 12. Required AI Design Output

Setiap permintaan Add New Data MUST menghasilkan:

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
- Draft Flow jika tersedia.
- Step Navigation jika tersedia.
- Preview Flow jika tersedia.
- Success Flow.
- Approved Error Handling.
- End State.

### Output 03 — UI Screens

- Seluruh screens sesuai pattern.
- Form dengan field dari HSD/BRD.
- Komponen resmi GEMS.
- Confirmation dan feedback.
- Seluruh UI States yang relevan.

### Output 04 — State Coverage

AI MUST memeriksa:

- Default.
- Focus.
- Filled.
- Required.
- Validation Error.
- Disabled.
- Read-only.
- Loading.
- Confirmation.
- Success.
- Save Error.
- Network Error.
- Server Error.
- Draft Saving jika tersedia.
- Draft Success jika tersedia.
- Draft Save Error jika tersedia.
- Active Step jika tersedia.
- Completed Step jika tersedia.
- Preview jika tersedia.
- Unsaved Changes.

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

## 13. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut.

**Step 1 — Read HSD/BRD**

Identifikasi kebutuhan bisnis, field, role, permission, validation, status, dan flow.

**Step 2 — Inspect GEMS Patterns**

Periksa keempat Add New Data UX Pattern beserta Flow Diagram dan UI Screens.

**Step 3 — Compare Patterns**

Bandingkan kebutuhan dengan struktur dan behavior setiap pattern.

**Step 4 — Select Pattern**

Pilih pattern paling sesuai dan jelaskan alasannya.

**Step 5 — Check Compatibility**

Identifikasi konflik dan kebutuhan yang belum didukung.

**Step 6 — Request Human Approval if Needed**

Jika pattern tidak sesuai, buat rekomendasi dan tunggu approval.

**Step 7 — Retrieve GEMS Components**

Ambil seluruh komponen, properties, variants, dan states yang diperlukan.

**Step 8 — Generate UX Flow Diagram**

Gunakan flow resmi dan sesuaikan dengan HSD/BRD.

**Step 9 — Generate UI Screens**

Buat seluruh screen sesuai pattern dan flow.

**Step 10 — Generate UI States**

Buat seluruh state relevan, termasuk validation, loading, error, Draft, dan unsaved changes.

**Step 11 — Map Flow to Screens**

Pastikan seluruh node, screens, actions, dan states saling sesuai.

**Step 12 — Validate Against GEMS**

Bandingkan hasil dengan pattern dan komponen resmi.

**Step 13 — Report Compliance**

Laporkan hasil validasi, keterbatasan, dan approval yang masih diperlukan.

---

## 14. AI Restrictions

AI MUST NOT:

1. Membuat pattern baru tanpa approval.
2. Menggabungkan pattern tanpa approval.
3. Mengubah approved pattern.
4. Menambah atau menghapus screen tanpa approval.
5. Menambah atau menghapus step tanpa approval.
6. Mengubah urutan flow.
7. Mengubah decision point.
8. Mengubah Save, Draft, Preview, atau Confirmation Flow.
9. Menghilangkan Cancel atau Exit Flow.
10. Menghilangkan Error atau Loading State yang relevan.
11. Menghasilkan UI tanpa Flow Diagram.
12. Menghasilkan flow yang berbeda dari UI.
13. Mengarang field, validation, role, atau status.
14. Menggunakan komponen non-GEMS.
15. Membuat komponen custom tanpa approval.
16. Mengubah properties atau variants di luar ketentuan.
17. Mengimplementasikan Proposed Flow sebelum Human Approval.
18. Menganggap screenshot contoh sebagai izin untuk mengubah pattern.
19. Menyatakan desain compliant tanpa verifikasi.

---

## 15. Quality Assurance & Compliance

### 15.1 Requirement Compliance

AI MUST memastikan field, status, validation, role, dan permission sesuai approved HSD/BRD.

### 15.2 Pattern Compliance

AI MUST memastikan pattern terpilih sesuai kebutuhan dan mengikuti struktur resmi.

### 15.3 GEMS Component Compliance

AI MUST memastikan seluruh komponen menggunakan GEMS Design System, termasuk properties, variants, dan states yang tersedia.

### 15.4 Flow Compliance

AI MUST:

- Menempatkan Flow Diagram di atas UI Screens.
- Memastikan seluruh screen mengikuti flow.
- Menampilkan Main Flow dan Alternative Flow.
- Mempertahankan Decision Point.
- Memastikan Save, Draft, Preview, Confirmation, dan Exit Flow sesuai pattern.

### 15.5 State Completeness

AI MUST memastikan seluruh state relevan ditangani, termasuk:

- Validation Error.
- Loading.
- Save Error.
- Network Error.
- Server Error.
- Draft Save Error.
- Unsaved Changes.

AI MUST memastikan setiap state memiliki representasi UI dan dapat ditelusuri ke flow.

### 15.6 Human Approval Compliance

AI MUST:

- Mengidentifikasi ketidaksesuaian.
- Membuat rekomendasi terpisah.
- Meminta Human Approval sebelum perubahan.
- Tidak menerapkan perubahan berstatus Pending.

### 15.7 Final Validation Checklist

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

## 16. Final AI Enforcement

AI MUST:

1. Membaca approved HSD/BRD.
2. Memeriksa keempat Add New Data UX Pattern resmi GEMS.
3. Memilih pattern berdasarkan kebutuhan bisnis.
4. Menggunakan pattern resmi sebagai acuan flow.
5. Menggunakan komponen resmi GEMS untuk seluruh UI.
6. Menghasilkan UX Flow Diagram di bagian atas desain.
7. Menghasilkan UI Screens di bagian bawah desain.
8. Menggunakan field dan business rules dari HSD/BRD.
9. Menghasilkan seluruh UI States yang relevan.
10. Menangani Success, Error, Loading, dan Failure.
11. Menangani Draft dan Preview sesuai pattern.
12. Menghubungkan seluruh screens dan states dengan flow.
13. Mempertahankan struktur pattern resmi.
14. Merekomendasikan perubahan jika pattern tidak sesuai.
15. Meminta Human Approval sebelum menerapkan perubahan.
16. Memvalidasi hasil terhadap HSD/BRD dan GEMS.

### Final Enforcement Rule

> AI MUST select the most appropriate official GEMS Add New Data UX Pattern based on approved HSD/BRD. Every design MUST include a complete UX Flow Diagram positioned above the corresponding UI Screens, with all applicable UI States, including success, error, loading, validation, draft, preview, and unsaved changes. All UI components MUST originate from the official GEMS Design System. If no existing pattern fully supports the business requirements, AI MAY recommend a modified UX Flow but MUST obtain explicit Human Approval before implementing any changes.

**GEMS UX Pattern menentukan alur. GEMS Design System menentukan komponen. HSD/BRD menentukan kebutuhan bisnis. Human Approval menentukan apakah perubahan diperbolehkan.**
