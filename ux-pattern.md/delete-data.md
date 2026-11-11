# GEMS AI Design Guidelines — Delete Data UX Pattern

## 1. Purpose & Scope

Dokumen ini merupakan instruksi wajib bagi AI untuk menghasilkan desain UI/UX fitur Delete Data berdasarkan approved HSD/BRD, GEMS UX Pattern, dan GEMS Design System.

AI MUST menggunakan referensi resmi GEMS sebagai dasar untuk menentukan alur interaksi, komponen, layout, navigation, confirmation, dan UI States.

AI MUST menghasilkan desain yang tidak hanya konsisten secara visual, tetapi juga memenuhi kebutuhan bisnis, mudah dipahami pengguna, serta memiliki hubungan yang jelas antara UX Flow Diagram dan UI Screens.

Guideline ini berlaku untuk proses Delete dalam operasi CRUD (Create, Read, Update, Delete). Untuk Create, Read, dan Update, AI MUST merujuk pada guideline Add Data, View Detail, dan Edit Data yang relevan.

### 1.1 Mandatory AI Responsibilities

Sebelum dan selama menghasilkan desain, AI MUST:

1. **Understand Business Requirements** — Membaca HSD/BRD dan mengidentifikasi fitur, role, hak akses, data, status, aturan penghapusan, dan expected behavior.
2. **Inspect Official UX Patterns** — Memeriksa referensi Delete Data UX Pattern pada Figma untuk memahami flow, screens, actions, dan navigation.
3. **Select the Correct Pattern** — Memilih pattern resmi berdasarkan entry point dan kebutuhan bisnis.
4. **Follow Approved Core Flow** — Mengikuti alur utama yang ditetapkan dalam GEMS UX Pattern tanpa mengubah atau menambahkan langkah secara sepihak.
5. **Use GEMS Design System** — Menggunakan komponen resmi GEMS beserta properties, variants, states, typography, color, spacing, dan layout rules.
6. **Generate Visual UX Flow** — Membuat UX Flow Diagram di bagian atas section Figma.
7. **Generate UI Screens** — Membuat screens di bagian bawah sesuai urutan flow.
8. **Represent Applicable UI States** — Menampilkan seluruh kondisi yang relevan, termasuk Confirmation, Cancel, Loading, Success, Error, Disabled, dan Empty.
9. **Maintain Flow-to-Screen Consistency** — Memastikan setiap langkah flow memiliki screen atau state yang sesuai.
10. **Validate the Output** — Memeriksa hasil desain yang benar-benar dibuat di Figma terhadap HSD/BRD, UX Pattern, dan GEMS Design System.

AI MUST NOT melewati tahap verifikasi atau menganggap desain compliant tanpa pemeriksaan.

### 1.2 Scope of This Guideline

Guideline ini mencakup:

- Pemilihan Delete Data UX Pattern.
- Aturan penggunaan Core Flow.
- Penggunaan komponen GEMS Design System.
- Delete Confirmation dan Cancellation.
- Success, Error, Loading, Disabled, dan UI States lainnya.
- UX Flow Diagram dan UI Screen Arrangement.
- Business Rules dan Role Access.
- Pattern Recommendation.
- Human Approval.
- Final Design Validation.

---

## 2. Source of Truth & Design Governance

### 2.1 Source Hierarchy

AI MUST menggunakan sumber berikut sesuai fungsinya.

| Source | Authority | AI Responsibility |
|---|---|---|
| Approved HSD/BRD | Business requirements | Menentukan kebutuhan, data, role, dan business rules |
| GEMS UX Pattern | Core UX Flow | Menentukan urutan proses, navigation, dan interaction |
| GEMS Design System | UI Components & Visual Rules | Menentukan komponen, variants, states, dan styling |
| Role Access Matrix | Permissions | Menentukan tindakan yang dapat dilakukan setiap role |
| Human Approval | Change Authorization | Menyetujui perubahan terhadap approved flow atau design system |

### 2.2 Core Flow Governance

AI MUST menggunakan **Core Flow resmi GEMS UX Pattern** sebagai acuan utama.

Core Flow mencakup:

1. Entry Point.
2. User Action.
3. Confirmation atau Decision Point.
4. System Processing.
5. Feedback.
6. Navigation Destination.
7. End State.

AI MUST mempertahankan struktur dan urutan Core Flow yang telah disetujui.

AI MUST NOT:

- Mengubah entry point.
- Menghilangkan langkah confirmation.
- Mengubah navigation destination.
- Menggabungkan atau memisahkan langkah tanpa approval.
- Menambahkan screen baru yang mengubah proses.
- Mengganti interaction behavior resmi.
- Membuat Core Flow alternatif secara sepihak.

### 2.3 Design System Governance

AI MUST menggunakan GEMS Design System sebagai sumber utama untuk seluruh elemen UI.

AI MUST NOT menggunakan komponen, warna, typography, spacing, atau interaction pattern di luar GEMS tanpa explicit Human Approval.

Jika komponen atau variant yang dibutuhkan belum tersedia, AI MUST mengidentifikasi gap, memberikan rekomendasi, dan meminta approval sebelum membuat atau menggunakan solusi baru.

### 2.4 Conflict Resolution

Jika terdapat ketidaksesuaian antara HSD/BRD dan GEMS UX Pattern, AI MUST:

1. Mengidentifikasi requirement yang tidak sesuai.
2. Menunjukkan bagian Core Flow yang terdampak.
3. Menjelaskan dampak terhadap UI Screens dan States.
4. Memeriksa apakah pattern resmi lain dapat memenuhi kebutuhan.
5. Mengajukan rekomendasi jika diperlukan.
6. Meminta Human Approval sebelum mengimplementasikan perubahan.

AI MUST NOT menganggap salah satu sumber dapat diubah secara otomatis.

---

## 3. Official Delete Data UX Patterns

**Parent Figma Reference:** [GEMS Design System — Delete Data](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1161-2976)

GEMS menyediakan dua Delete Data UX Pattern resmi.

| Pattern | Entry Point | Delete Action | Success Destination |
|---|---|---|---|
| Pattern 01 — Delete from List | List Page | Trash Icon | Back to List |
| Pattern 02 — Delete from Detail | Detail Page setelah View/Row | Delete Action | Back to Detail Page sesuai referensi |

AI MUST memeriksa kedua pattern sebelum menentukan pilihan.

### 3.1 Pattern Selection Rules

AI MUST:

1. Mengidentifikasi entry point dari HSD/BRD.
2. Menentukan lokasi Delete Action.
3. Memeriksa kebutuhan melihat detail sebelum menghapus.
4. Memeriksa role dan permission.
5. Memilih pattern yang paling sesuai.
6. Mengikuti Core Flow pattern terpilih.
7. Menjelaskan alasan pemilihan.

AI MUST NOT memilih pattern hanya karena lebih sederhana atau lebih menarik secara visual.

---

## 4. Pattern 01 — Delete Data from List Page

**Figma Reference:** [Pattern 01 — Delete from List Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3346-105989&t=zv6vn5L7CsEWbtOz-1)

### 4.1 When to Use

AI MUST menggunakan Pattern 01 ketika pengguna melakukan penghapusan langsung dari List Page melalui Trash Icon pada record yang dipilih, sepanjang sesuai approved HSD/BRD.

### 4.2 Official Core Flow

AI MUST mempertahankan alur:

1. Start.
2. List Page.
3. Click Delete (Trash Icon).
4. Confirmation Modal.
5. Confirm Delete.
6. System Processing.
7. Toast Message.
8. Back to List.
9. End.

Langkah Confirm Delete dan System Processing menjelaskan behavior operasional yang harus ditangani, sedangkan struktur visual utama mengikuti node resmi pada Figma.

### 4.3 Required UI Screens

AI MUST menghasilkan:

1. **List Page** — Menampilkan daftar record dan Delete Action.
2. **Delete Confirmation Modal** — Menampilkan konfirmasi sebelum penghapusan.
3. **Delete Processing State** — Menampilkan feedback saat penghapusan berlangsung jika relevan.
4. **Delete Success State** — Menampilkan Success Toast setelah operasi berhasil.
5. **Updated List Page** — Menampilkan kondisi daftar setelah penghapusan.
6. **Delete Cancel State** — Merepresentasikan pembatalan tanpa menghapus data.
7. **Delete Error State** — Merepresentasikan kegagalan penghapusan sesuai approved behavior.

### 4.4 List Page Behavior

AI MUST:

- Menggunakan Table resmi GEMS.
- Menggunakan Trash Icon sesuai referensi.
- Menghubungkan Delete Action dengan record yang benar.
- Mengikuti permission.
- Membuka Confirmation Modal ketika Delete dipilih.
- Mempertahankan konteks daftar.

AI MUST NOT:

- Menghapus data langsung setelah Trash Icon diklik.
- Mengubah Trash Icon menjadi action lain tanpa approval.
- Menambahkan Bulk Delete tanpa approved requirement.
- Mengubah List Page menjadi Detail Page.

### 4.5 Confirmation Behavior

AI MUST:

- Menggunakan Confirmation Modal resmi GEMS.
- Menampilkan judul dan deskripsi yang menjelaskan tindakan.
- Menggunakan label tombol sesuai konteks.
- Menyediakan Confirm dan Cancel.
- Menggunakan destructive styling resmi jika tersedia.
- Menjalankan penghapusan hanya setelah Confirm.

### 4.6 Cancel Behavior

Jika pengguna memilih Cancel, AI MUST memastikan:

1. Modal ditutup.
2. Data tidak dihapus.
3. List Page tetap tersedia.
4. Tidak muncul Delete Success Toast.
5. Tidak terjadi perubahan status data akibat pembatalan.

### 4.7 Success Behavior

Setelah sistem mengonfirmasi penghapusan berhasil, AI MUST:

1. Menampilkan Success Toast resmi.
2. Mengikuti destination Back to List.
3. Memperbarui representasi daftar sesuai hasil penghapusan.
4. Menampilkan Empty State jika daftar menjadi kosong.
5. Mempertahankan pagination behavior resmi.

### 4.8 Error Behavior

Jika penghapusan gagal, AI MUST:

1. Menampilkan Error Feedback resmi.
2. Tidak menampilkan Success Toast.
3. Tidak menghilangkan record seolah berhasil dihapus.
4. Mempertahankan konteks pengguna.
5. Mengikuti retry behavior yang telah disetujui.

AI MUST NOT mengarang error recovery flow.

---

## 5. Pattern 02 — Delete Data from Detail Page

**Figma Reference:** [Pattern 02 — Delete from Detail Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3346-108323&t=zv6vn5L7CsEWbtOz-1)

### 5.1 When to Use

AI MUST menggunakan Pattern 02 ketika pengguna membuka Detail Page terlebih dahulu melalui View Action atau Row Interaction sebelum melakukan penghapusan.

### 5.2 Official Core Flow

AI MUST mempertahankan alur:

1. Start.
2. List Page.
3. Klik View / Row.
4. Detail Page.
5. Click Delete.
6. Confirmation Modal.
7. Confirm Delete.
8. System Processing.
9. Toast Message.
10. Back to Detail Page.
11. End.

AI MUST mempertahankan destination yang tertulis pada referensi resmi sampai terdapat perubahan yang disetujui.

### 5.3 Required UI Screens

AI MUST menghasilkan:

1. **List Page** — Menampilkan record.
2. **Detail Page** — Menampilkan informasi record terpilih.
3. **Delete Action** — Menampilkan tindakan Delete sesuai permission.
4. **Confirmation Modal** — Menampilkan konfirmasi penghapusan.
5. **Delete Processing State** — Menampilkan feedback proses jika relevan.
6. **Success Toast** — Menampilkan feedback keberhasilan.
7. **Post-delete Detail State** — Mengikuti behavior yang telah disetujui.
8. **Cancel State** — Membatalkan penghapusan.
9. **Error State** — Menampilkan kegagalan penghapusan.

### 5.4 Detail Page Behavior

AI MUST:

- Menggunakan Detail Page resmi GEMS.
- Menampilkan informasi sesuai record.
- Menggunakan Delete Action sesuai role.
- Membuka Confirmation Modal sebelum Delete.
- Mempertahankan konteks record.
- Mengikuti navigation behavior resmi.

### 5.5 Confirmation & Cancel Behavior

AI MUST menggunakan Confirmation Modal resmi.

Jika pengguna memilih Cancel, AI MUST memastikan:

1. Modal ditutup.
2. Penghapusan tidak diproses.
3. Pengguna tetap berada pada Detail Page.
4. Record tetap tersedia.
5. Tidak muncul Success Toast.

### 5.6 Success & Post-delete Navigation

AI MUST mengikuti destination resmi **Back to Detail Page** sesuai referensi Figma.

Namun, AI MUST memeriksa apakah Detail Page masih dapat ditampilkan setelah record dihapus.

Jika HSD/BRD menyatakan bahwa record tidak lagi tersedia setelah penghapusan, AI MUST:

1. Mengidentifikasi konflik.
2. Menjelaskan konsekuensi terhadap navigation.
3. Mengusulkan alternatif seperti Back to List jika sesuai kebutuhan.
4. Meminta Human Approval.
5. Tidak menerapkan perubahan sebelum approval.

AI MUST NOT menampilkan record yang telah dihapus seolah masih aktif.

### 5.7 Error Behavior

AI MUST:

- Menampilkan Error Feedback resmi.
- Tidak menampilkan Success Toast.
- Mempertahankan konteks Detail Page.
- Tidak menganggap data telah dihapus.
- Mengikuti approved recovery behavior.

---

## 6. Mandatory CRUD & UX State Presentation Rules

### 6.1 CRUD Pattern Governance

AI MUST menggunakan guideline CRUD resmi sesuai jenis operasi.

| CRUD Operation | Required UX Pattern | Primary Behavior |
|---|---|---|
| Create | Add Data | Membuat record baru |
| Read | View Detail | Menampilkan informasi |
| Update | Edit Data | Mengubah record yang tersedia |
| Delete | Delete Data | Menghapus record melalui confirmation |

AI MUST NOT menggunakan flow dari operasi CRUD lain sebagai pengganti pattern terpilih tanpa Human Approval.

Jika satu fitur memiliki beberapa operasi CRUD, AI MUST memisahkan Core Flow masing-masing atau menghubungkannya hanya sesuai approved UX Flow.

### 6.2 UI State Presentation Principles

AI MUST memeriksa seluruh state yang relevan dengan operasi Delete.

AI MUST menampilkan state menggunakan komponen, variants, dan visual behavior resmi GEMS.

AI MUST NOT mengarang variant visual yang tidak tersedia dalam Design System.

### 6.3 Mandatory State Matrix

| UI State | Trigger | Required Presentation |
|---|---|---|
| Default | Halaman pertama dibuka | Tampilan normal |
| Hover | Pointer berada pada action | Hover variant resmi |
| Focus | Komponen menerima fokus | Focus state resmi |
| Disabled | Action tidak tersedia | Disabled state sesuai business rules |
| Confirmation | Delete dipilih | Confirmation Modal |
| Cancelled | Pengguna memilih Cancel | Modal ditutup, data tetap |
| Loading | Delete diproses | Loading feedback resmi |
| Success | Delete berhasil | Success Toast |
| Delete Error | Penghapusan gagal | Error feedback resmi |
| Network Error | Gangguan koneksi | Network error feedback |
| Server Error | Gangguan sistem | Server error feedback |
| Empty | Tidak ada data | Empty State resmi |
| Access Restricted | Tidak memiliki izin | Permission-based feedback |
| Updated List | Delete berhasil | List mencerminkan hasil |
| Post-delete Detail | Delete dari Detail Page | Mengikuti approved behavior |

### 6.4 Success State Rules

AI MUST:

1. Menggunakan Success Toast atau Notification resmi GEMS.
2. Menampilkan pesan sesuai tindakan.
3. Menampilkan feedback hanya setelah operasi berhasil.
4. Mengikuti destination resmi.
5. Menjaga konsistensi data pada UI.

AI MUST NOT menampilkan Success State sebelum hasil sistem terkonfirmasi.

### 6.5 Error State Rules

AI MUST:

1. Menggunakan Error Feedback resmi.
2. Menjelaskan tindakan yang gagal.
3. Mempertahankan konteks pengguna.
4. Tidak mengubah data seolah berhasil.
5. Mengikuti approved recovery behavior.

AI MUST NOT menambahkan Retry Button, halaman baru, atau navigation baru tanpa dukungan approved flow.

### 6.6 Disabled State Rules

AI MUST:

1. Memeriksa role dan permission.
2. Memeriksa status restrictions.
3. Menggunakan Disabled State resmi jika berlaku.
4. Menjaga konsistensi dengan business rules.
5. Menggunakan tooltip atau penjelasan hanya jika didukung GEMS dan approved requirements.

AI MUST NOT menonaktifkan tindakan berdasarkan asumsi.

### 6.7 Loading State Rules

AI MUST:

1. Menggunakan loading feedback resmi.
2. Menunjukkan bahwa operasi sedang diproses.
3. Mengikuti behavior komponen resmi.
4. Mencegah representasi keberhasilan sebelum respons sistem.
5. Mengikuti aturan pemrosesan berulang yang disetujui.

### 6.8 Empty State Rules

AI MUST:

1. Menggunakan Empty State resmi.
2. Menyesuaikan wording dengan konteks.
3. Membedakan daftar kosong dari record tidak ditemukan.
4. Mengikuti approved navigation behavior.

### 6.9 Confirmation State Rules

AI MUST:

1. Menggunakan Confirmation Modal resmi.
2. Menjelaskan tindakan penghapusan.
3. Menggunakan action label yang jelas.
4. Menyediakan Confirm dan Cancel.
5. Menggunakan destructive styling resmi.
6. Memastikan data tidak dihapus sebelum Confirm.

### 6.10 State-to-Screen Relationship

AI MUST menempatkan state di bawah atau berdekatan dengan screen asalnya.

AI MUST memastikan setiap state memiliki:

- State Name.
- Trigger.
- Related Screen.
- User Action jika berlaku.
- Expected System Feedback.
- Navigation Result jika berlaku.

AI MUST NOT menampilkan kumpulan states tanpa konteks flow.

---

## 7. Mandatory GEMS Design System Usage

### 7.1 Official Reference

**Figma Reference:** [GEMS Design System](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)

AI MUST menggunakan GEMS Design System sebagai sumber komponen dan visual specification.

### 7.2 Component Retrieval Workflow

AI MUST:

1. Membuka referensi GEMS.
2. Memeriksa komponen yang digunakan pada pattern.
3. Mengidentifikasi component name.
4. Memeriksa component anatomy.
5. Memeriksa properties.
6. Memeriksa variants.
7. Memeriksa available states.
8. Memeriksa typography.
9. Memeriksa color tokens.
10. Memeriksa spacing dan layout rules.
11. Menggunakan instance resmi jika didukung Figma MCP.
12. Memvalidasi komponen pada hasil desain.

### 7.3 Component Integrity Rules

AI MUST mempertahankan:

- Component hierarchy.
- Component anatomy.
- Properties.
- Variants.
- States.
- Typography.
- Colors.
- Spacing.
- Radius.
- Icons.
- Interaction behavior.

AI MUST NOT:

- Menggunakan UI library eksternal sebagai pengganti GEMS.
- Membuat komponen custom tanpa approval.
- Mengubah visual specification resmi.
- Mengarang variant.
- Mengubah destructive styling.
- Mengganti Confirmation Modal resmi.
- Mengklaim komponen sebagai instance GEMS jika hanya berupa tiruan.

### 7.4 Missing Component Handling

Jika komponen atau variant tidak tersedia, AI MUST:

1. Mengidentifikasi komponen yang dibutuhkan.
2. Memeriksa alternatif resmi GEMS.
3. Menjelaskan keterbatasan.
4. Mengusulkan solusi.
5. Menjelaskan dampak terhadap desain.
6. Meminta Human Approval sebelum implementasi.

AI MAY merekomendasikan komponen baru.

AI MUST NOT mengimplementasikannya tanpa approval.

---

## 8. Mandatory UX Flow Diagram & Figma Layout

### 8.1 Required Design Structure

AI MUST menempatkan:

**TOP SECTION — UX FLOW DIAGRAM**

**BOTTOM SECTION — UI SCREENS & UI STATES**

Kedua bagian MUST berada dalam satu section Figma yang sama.

### 8.2 UX Flow Diagram Rules

AI MUST:

1. Menggunakan Core Flow pattern terpilih.
2. Menampilkan Start dan End.
3. Menampilkan Entry Point.
4. Menampilkan Delete Action.
5. Menampilkan Confirmation Modal.
6. Menampilkan Confirm dan Cancel behavior.
7. Menampilkan Success Flow.
8. Menampilkan Error Flow yang telah disetujui.
9. Menggunakan connector yang jelas.
10. Menjaga arah alur yang konsisten.
11. Menghubungkan flow dengan UI Screens.

AI MUST NOT membuat diagram yang bertentangan dengan UI Screens.

### 8.3 UI Screens Arrangement

AI MUST:

1. Menempatkan screens di bawah Flow Diagram.
2. Mengurutkan screens sesuai Main Flow.
3. Menempatkan Confirmation Modal bersama konteks screen asal.
4. Menempatkan Success State sesuai destination.
5. Menempatkan Error dan Disabled States bersama screen terkait.
6. Menggunakan penamaan screen yang konsisten.
7. Menjaga alignment dan spacing.
8. Mengikuti struktur layout GEMS.

### 8.4 Flow-to-Screen Mapping

| Flow Node | UI Screen | UI State |
|---|---|---|
| List Page | List / Data Table | Default |
| Delete Action | List atau Detail | Hover / Disabled |
| Confirmation | Confirmation Modal | Default |
| Cancel | Source Screen | Cancelled |
| Confirm | Confirmation / Processing | Loading |
| Success | Destination Screen | Success Toast |
| Failure | Source Context | Error |
| Back to List | Updated List | Updated / Empty |
| Back to Detail | Detail Context | Approved Post-delete State |

AI MUST menggunakan hanya mapping yang relevan dengan pattern terpilih.

### 8.5 Flow Integrity Validation

AI MUST memeriksa:

1. Apakah seluruh node memiliki screen atau state yang sesuai.
2. Apakah urutan UI mengikuti flow.
3. Apakah Confirmation Modal berada sebelum Delete Processing.
4. Apakah Success Toast hanya muncul setelah operasi berhasil.
5. Apakah Cancel tidak menghapus data.
6. Apakah destination sesuai pattern.
7. Apakah error handling tidak mengubah approved flow.

---

## 9. Business Rules & Role Access

### 9.1 Business Requirement Mapping

AI MUST mengidentifikasi:

- Feature Name.
- User Role.
- Record Type.
- Record Identifier.
- Delete Permission.
- Status Restrictions.
- Dependency Rules.
- Deletion Consequences.
- Confirmation Requirements.
- Success Behavior.
- Error Behavior.
- Navigation Destination.

Seluruh informasi MUST berasal dari HSD/BRD atau approved supporting documents.

### 9.2 Role Access Rules

AI MUST:

1. Memeriksa Role Access Matrix.
2. Menentukan role yang dapat menghapus.
3. Menentukan kondisi Delete Action tersedia.
4. Mengikuti permission resmi.
5. Menggunakan UI State yang sesuai.

AI MUST NOT memberikan kemampuan Delete kepada role yang tidak memiliki izin.

### 9.3 Deletion Type

AI MUST memeriksa apakah HSD/BRD menentukan:

- Soft Delete.
- Hard Delete.
- Archive.
- Deactivate.
- Restore.

AI MUST NOT menganggap seluruh tindakan tersebut setara.

Jika deletion type tidak dijelaskan, AI MUST menandainya sebagai Pending Requirement.

AI MUST NOT mengarang konsekuensi penghapusan.

---

## 10. AI Recommendation & Human Approval

### 10.1 Recommendation Permission

AI MAY memberikan rekomendasi jika:

1. Pattern resmi tidak memenuhi kebutuhan bisnis.
2. Terdapat konflik HSD/BRD dan UX Pattern.
3. Diperlukan perubahan Core Flow.
4. Diperlukan screen tambahan.
5. Diperlukan UI State baru.
6. Komponen GEMS tidak tersedia.
7. Navigation destination tidak sesuai kebutuhan.
8. Confirmation behavior membutuhkan penyesuaian.

### 10.2 Mandatory Recommendation Format

AI MUST menyampaikan rekomendasi dengan struktur berikut.

| Field | Required Information |
|---|---|
| Feature | Nama fitur |
| Current Pattern | Pattern resmi yang digunakan |
| Figma Reference | Link pattern |
| Business Requirement | Kebutuhan dari HSD/BRD |
| Identified Gap | Ketidaksesuaian |
| Proposed Change | Perubahan yang direkomendasikan |
| Reason | Alasan rekomendasi |
| UX Impact | Dampak terhadap flow dan interaction |
| UI Impact | Dampak terhadap screens dan components |
| State Impact | Dampak terhadap UI States |
| Approval Status | Pending Human Approval |

### 10.3 Human Approval Workflow

AI MUST:

1. Mengidentifikasi gap.
2. Memeriksa seluruh pattern resmi yang relevan.
3. Menjelaskan rekomendasi.
4. Menjelaskan dampak.
5. Memisahkan Proposed Flow dari Approved Flow.
6. Meminta Human Approval.
7. Menunggu keputusan.
8. Mengimplementasikan hanya perubahan yang disetujui.
9. Memvalidasi hasil.

### 10.4 Approval Restrictions

AI MUST NOT:

- Menganggap rekomendasi sebagai persetujuan.
- Menganggap tidak adanya respons sebagai approval.
- Mengimplementasikan perubahan berstatus Pending.
- Mengubah komponen resmi tanpa approval.
- Mengubah Core Flow tanpa approval.
- Mengubah navigation destination tanpa approval.
- Menambahkan behavior baru tanpa approval.

### 10.5 Approved vs Proposed Design

AI MUST membedakan:

**Approved Design**

Desain yang mengikuti HSD/BRD, GEMS UX Pattern, dan komponen resmi.

**Proposed Design**

Usulan perubahan yang belum disetujui.

AI MAY menyiapkan dokumentasi atau representasi konsep terpisah untuk Proposed Design jika diminta.

AI MUST NOT memasukkan Proposed Design ke dalam implementasi final sebelum Human Approval.

---

## 11. Required AI Design Output

AI MUST menghasilkan output berikut.

### 11.1 Pattern Selection Report

AI MUST menjelaskan:

- Feature Name.
- Selected Pattern.
- Entry Point.
- User Role.
- Selection Rationale.
- Figma Reference.

### 11.2 UX Flow Diagram

AI MUST menghasilkan visual diagram yang mencakup:

- Start.
- Entry Point.
- Delete Action.
- Confirmation.
- Confirm.
- Cancel.
- Processing.
- Success.
- Approved Error Handling.
- Navigation.
- End.

### 11.3 UI Screens

AI MUST menghasilkan:

- Source Screen.
- Delete Action.
- Confirmation Modal.
- Processing State jika relevan.
- Success State.
- Destination Screen.
- Cancel State.
- Error State yang relevan.

### 11.4 UI State Coverage

AI MUST menjelaskan:

- State yang diterapkan.
- State yang tidak berlaku.
- State yang membutuhkan approval.
- Komponen GEMS yang digunakan.

### 11.5 Flow-to-Screen Mapping

AI MUST memastikan setiap flow node memiliki screen atau state yang sesuai.

### 11.6 Compliance Report

AI MUST melaporkan:

- HSD/BRD Compliance.
- UX Pattern Compliance.
- Core Flow Compliance.
- GEMS Component Compliance.
- UI State Coverage.
- Role Access Compliance.
- Human Approval Status.
- Unresolved Issues.

---

## 12. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut.

**Step 1 — Read Requirements**

Baca HSD/BRD dan supporting documents.

**Step 2 — Identify Business Rules**

Identifikasi data, role, permission, status restrictions, dan deletion behavior.

**Step 3 — Inspect Official UX Patterns**

Periksa Pattern 01 dan Pattern 02 pada Figma.

**Step 4 — Select Core Flow**

Pilih pattern berdasarkan entry point dan kebutuhan bisnis.

**Step 5 — Validate Flow Compatibility**

Pastikan pattern mendukung kebutuhan tanpa perubahan yang belum disetujui.

**Step 6 — Inspect GEMS Components**

Periksa komponen, properties, variants, dan states.

**Step 7 — Generate UX Flow Diagram**

Buat diagram visual pada bagian atas section Figma.

**Step 8 — Generate UI Screens**

Buat UI Screens sesuai urutan flow.

**Step 9 — Generate Applicable UI States**

Buat Confirmation, Cancel, Loading, Success, Error, Disabled, Empty, dan state relevan lainnya.

**Step 10 — Validate CRUD Behavior**

Pastikan operasi Delete mengikuti aturan penghapusan dan tidak tercampur dengan flow CRUD lain.

**Step 11 — Validate Flow-to-Screen Mapping**

Pastikan diagram, screens, states, dan navigation konsisten.

**Step 12 — Identify Design Gaps**

Identifikasi kebutuhan yang tidak didukung GEMS atau HSD/BRD.

**Step 13 — Request Human Approval**

Ajukan rekomendasi jika diperlukan perubahan.

**Step 14 — Validate Actual Figma Output**

Periksa hasil desain yang benar-benar dibuat pada Figma, bukan hanya rencana atau deskripsi.

**Step 15 — Generate Compliance Report**

Laporkan hasil verifikasi dan unresolved issues.

---

## 13. AI Restrictions

AI MUST NOT:

1. Mengubah Core Flow resmi tanpa approval.
2. Menggunakan UX Pattern di luar GEMS tanpa approval.
3. Mengganti komponen resmi dengan komponen custom.
4. Mengarang properties atau variants.
5. Menghapus Confirmation Modal.
6. Memproses Delete sebelum Confirm.
7. Menampilkan Success sebelum operasi berhasil.
8. Mengubah Cancel Behavior.
9. Mengubah navigation destination.
10. Menambahkan Bulk Delete tanpa requirement.
11. Menambahkan Undo atau Restore tanpa requirement.
12. Mengarang Soft Delete atau Hard Delete.
13. Mengarang role atau permission.
14. Mengarang business rules.
15. Menggabungkan CRUD Flow tanpa approval.
16. Membuat UI Screens tanpa UX Flow Diagram.
17. Membuat UX Flow Diagram yang tidak sesuai screens.
18. Menghilangkan state yang relevan.
19. Mengimplementasikan Proposed Flow sebelum approval.
20. Mengklaim desain compliant tanpa verifikasi aktual.

---

## 14. Quality Assurance & Final Validation

### 14.1 Business Requirement Validation

AI MUST memastikan seluruh field, role, permission, status restrictions, dan deletion rules sesuai approved HSD/BRD.

### 14.2 UX Pattern Validation

AI MUST memastikan pattern terpilih sesuai entry point, user action, confirmation, dan destination.

### 14.3 Core Flow Validation

AI MUST memastikan seluruh langkah Core Flow dipertahankan dan tidak ada perubahan tanpa approval.

### 14.4 GEMS Component Validation

AI MUST memastikan seluruh komponen berasal dari GEMS Design System dan menggunakan properties, variants, serta states yang sesuai.

### 14.5 UI State Validation

AI MUST memastikan seluruh state yang relevan telah direpresentasikan menggunakan komponen resmi.

### 14.6 Flow-to-Screen Validation

AI MUST memastikan seluruh flow node, user action, UI Screen, state, dan expected result saling sesuai.

### 14.7 Human Approval Validation

AI MUST memastikan seluruh perubahan terhadap approved pattern, Core Flow, komponen, atau behavior telah memperoleh explicit Human Approval.

### 14.8 Final Validation Instructions

Before completing the design, AI MUST:

1. **Verify Business Requirements** — Memastikan seluruh kebutuhan dan aturan bisnis sesuai approved HSD/BRD.
2. **Verify Official Pattern Usage** — Memastikan pattern yang digunakan berasal dari GEMS.
3. **Verify Core Flow Integrity** — Memastikan Core Flow tidak berubah tanpa approval.
4. **Verify UX Flow Diagram** — Memastikan diagram lengkap dan berada di atas UI Screens.
5. **Verify UI Screens** — Memastikan screens mengikuti Main Flow dan approved Alternative Flow.
6. **Verify GEMS Components** — Memastikan komponen, properties, variants, dan states sesuai GEMS.
7. **Verify Confirmation Behavior** — Memastikan Delete tidak diproses sebelum konfirmasi.
8. **Verify Cancel Behavior** — Memastikan pembatalan tidak menghapus data.
9. **Verify Success & Error States** — Memastikan feedback sesuai kondisi operasi.
10. **Verify Disabled & Access States** — Memastikan ketersediaan Delete Action sesuai role dan business rules.
11. **Verify Flow-to-Screen Mapping** — Memastikan seluruh flow node memiliki representasi UI yang sesuai.
12. **Verify Navigation Destination** — Memastikan destination sesuai approved pattern.
13. **Verify Human Approval** — Memastikan perubahan yang diterapkan telah disetujui.
14. **Inspect Actual Figma Output** — Memastikan hasil yang benar-benar dibuat sesuai guideline.
15. **Generate Compliance Report** — Menyampaikan hasil validasi dan unresolved issues.

**Final Validation Rule**

AI MUST NOT mark the design as completed, approved, or GEMS-compliant until all applicable validation requirements have been verified.

If any requirement, component, flow, or state cannot be verified, AI MUST report it as **Pending Validation**.

---

## 15. Final AI Enforcement

AI MUST:

1. Menggunakan approved HSD/BRD sebagai sumber kebutuhan bisnis.
2. Menggunakan GEMS UX Pattern sebagai sumber Core Flow.
3. Menggunakan GEMS Design System sebagai sumber komponen.
4. Memilih pattern berdasarkan kebutuhan, bukan preferensi visual.
5. Mempertahankan Core Flow resmi.
6. Menggunakan Confirmation Modal sebelum Delete.
7. Menangani Cancel, Success, Error, Loading, Disabled, dan Empty States yang relevan.
8. Menempatkan UX Flow Diagram di atas UI Screens.
9. Menghubungkan seluruh flow node dengan screens dan states.
10. Mengikuti Role Access Matrix.
11. Tidak mengarang deletion rules atau system behavior.
12. Mengidentifikasi ketidaksesuaian.
13. Memberikan rekomendasi jika diperlukan.
14. Meminta Human Approval sebelum perubahan.
15. Memvalidasi hasil aktual di Figma.
16. Menghasilkan Compliance Report.

### Final Enforcement Rule

> AI MUST use the official GEMS UX Patterns as the mandatory source for all approved Core Flows and the GEMS Design System as the mandatory source for all UI components, visual properties, variants, and states. AI MUST generate a complete UX Flow Diagram above the corresponding UI Screens and represent all applicable interaction states. AI MAY recommend improvements when the official pattern does not fully support approved business requirements, but MUST obtain explicit Human Approval before implementing any changes to the Core Flow, navigation, interaction behavior, or Design System. AI MUST validate the actual Figma output before reporting completion or compliance.

**HSD/BRD menentukan kebutuhan bisnis. GEMS UX Pattern menentukan Core Flow. GEMS Design System menentukan komponen dan UI States. Human Approval menentukan perubahan yang diperbolehkan.**
