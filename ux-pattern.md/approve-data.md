# GEMS AI Design Guidelines — Approve Data UX Pattern

## 1. Purpose & Scope

Dokumen ini merupakan instruksi wajib bagi AI untuk menghasilkan desain UI/UX proses persetujuan data (Approve) berdasarkan approved HSD/BRD, GEMS UX Pattern, dan GEMS Design System.

AI MUST memahami kebutuhan bisnis sebelum memilih UX Pattern, menggunakan Core Flow resmi GEMS, menghasilkan UI Screens beserta seluruh applicable UI States, dan memvalidasi hasil desain yang dibuat melalui Figma MCP.

AI MUST memastikan bahwa setiap desain approval memiliki:

1. Core Flow yang sesuai pattern resmi.
2. Entry Point dan navigation yang jelas.
3. Role dan permission yang sesuai.
4. Approval Action yang mengikuti business rules.
5. Confirmation sebelum approval diproses.
6. Success dan Error Feedback.
7. Disabled dan Restricted States jika berlaku.
8. UI Screens yang merepresentasikan setiap langkah flow.
9. Komponen resmi GEMS Design System.
10. Human Approval untuk perubahan yang belum disetujui.

### 1.1 Mandatory Design Principles

AI MUST:

- Membaca dan memahami HSD/BRD sebelum menghasilkan desain.
- Memeriksa referensi Approve UX Pattern resmi di Figma.
- Memilih pattern berdasarkan kebutuhan bisnis dan karakteristik interaksi.
- Menggunakan approved Core Flow tanpa perubahan sepihak.
- Menggunakan GEMS Design System untuk komponen, variants, states, dan visual styling.
- Menghasilkan UX Flow Diagram pada bagian atas dan UI Screens pada bagian bawah.
- Menghasilkan applicable UI States meskipun Core Flow referensi hanya memperlihatkan jalur utama.
- Memastikan state tambahan tidak mengubah approved business behavior.
- Meminta Human Approval untuk perubahan Core Flow, navigation, interaction behavior, atau Design System.
- Memeriksa hasil aktual di Figma sebelum menyatakan desain selesai.

AI MUST NOT mengarang business requirements, approval rules, status transitions, permission, atau system behavior.

### 1.2 Approval vs CRUD

Approve merupakan workflow action, bukan pengganti operasi CRUD.

AI MUST menggunakan guideline yang sesuai untuk setiap operasi:

| Operation | Official Guideline |
|---|---|
| Create | Add Data UX Pattern |
| Read | View Detail UX Pattern |
| Update | Edit Data UX Pattern |
| Delete | Delete Data UX Pattern |
| Approve | Approve Data UX Pattern |

Jika satu fitur mencakup CRUD dan approval, AI MUST menggunakan masing-masing pattern sesuai fungsi dan menghubungkannya berdasarkan approved HSD/BRD.

AI MUST NOT menganggap Approve sama dengan Edit, Submit, Process, Reject, atau Delete.

---

## 2. Source of Truth & Design Governance

### 2.1 Source Hierarchy

| Source | Primary Responsibility |
|---|---|
| Approved HSD/BRD | Business requirements, role, approval rules, status transitions |
| GEMS UX Pattern | Approved Core Flow, navigation, interaction sequence |
| GEMS Design System | Components, variants, states, visual tokens |
| Role Access Matrix | Action availability and permission |
| Human Approval | Authorization for proposed changes |

AI MUST menggunakan setiap sumber sesuai kewenangannya.

Jika terjadi konflik, AI MUST mengidentifikasi dan melaporkan konflik tersebut, bukan mengubah salah satu sumber secara otomatis.

### 2.2 Core Flow Governance

AI MUST menggunakan GEMS UX Pattern sebagai mandatory reference untuk Core Flow.

Core Flow meliputi:

1. Start.
2. Entry Point.
3. User Action.
4. Confirmation.
5. Decision.
6. System Processing.
7. Feedback.
8. Navigation Destination.
9. End.

AI MUST mempertahankan langkah resmi dan urutannya.

AI MUST NOT menambahkan, menghilangkan, menggabungkan, atau mengubah langkah yang memengaruhi business flow tanpa explicit Human Approval.

### 2.3 Design System Governance

AI MUST menggunakan GEMS Design System sebagai sumber utama komponen UI.

**Official Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System

AI MUST memeriksa komponen dan variants sebelum membuat screens.

AI MUST NOT menggunakan komponen custom atau external UI library sebagai pengganti komponen GEMS tanpa approval.

### 2.4 Applicable State Governance

AI MUST mengevaluasi semua UI States yang relevan.

AI MUST membedakan:

- **Approved Flow States:** State yang secara eksplisit ditampilkan dalam UX Pattern.
- **Design System States:** State yang sudah didukung komponen resmi, seperti Hover, Focus, Disabled, Loading, dan Error.
- **Business-dependent States:** State yang membutuhkan aturan dari HSD/BRD, seperti approval eligibility, status restrictions, atau partial approval.
- **Proposed States:** State atau behavior yang belum didukung requirement maupun pattern resmi.

AI MUST menghasilkan Approved Flow States dan applicable Design System States.

Business-dependent States MUST mengikuti approved HSD/BRD.

Proposed States MUST memperoleh Human Approval sebelum diimplementasikan.

---

## 3. Official Approve UX Pattern References

**Parent Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1161-4014

GEMS Approve UX Pattern memiliki delapan nomor pattern. Tujuh referensi individual tersedia dan telah diperiksa; Pattern 03 masih membutuhkan referensi untuk verifikasi.

| Pattern | Type | Reference Status |
|---|---|---|
| Pattern 01 | Individual Approval | Verified |
| Pattern 02 | Individual Approval | Verified |
| Pattern 03 | Pending Identification | Pending Reference |
| Pattern 04 | Individual Approval | Verified |
| Pattern 05 | Individual Approval | Verified |
| Pattern 06 | Bulk Approval | Verified |
| Pattern 07 | Individual Approval | Verified |
| Pattern 08 | Individual Approval | Verified |

AI MUST memeriksa semua pattern yang relevan sebelum memilih desain.

AI MUST NOT menganggap pattern yang memiliki Core Flow serupa memiliki layout, component placement, atau interaction specification yang identik.

---

## 4. Pattern 01 — Approve from Detail Page

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3357-58895

### 4.1 When to Use

AI MUST mempertimbangkan Pattern 01 ketika proses approval dilakukan setelah pengguna membuka Detail Page dari List Page.

Pattern ini dapat digunakan jika HSD/BRD mengharuskan pengguna melihat informasi record sebelum memberikan persetujuan.

### 4.2 Official Core Flow

Start → List Page → View Detail → Click Approve → Confirmation Modal → YA, SETUJUI → Toast Message (Back to Detail) → End.

Cabang Cancel menggunakan tindakan **BATAL**.

### 4.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page.
3. Detail Page dengan Approve Action.
4. Confirmation Modal.
5. Approval Processing State jika relevan.
6. Success Toast pada Detail Page.
7. Cancel State.
8. Error State jika relevan.
9. Disabled atau Restricted State sesuai business rules.

### 4.4 Interaction Rules

AI MUST:

- Menggunakan Detail Page resmi GEMS.
- Menempatkan Approve Action sesuai referensi pattern.
- Menggunakan Confirmation Modal sebelum approval.
- Menggunakan label konfirmasi sesuai konteks persetujuan.
- Memastikan BATAL tidak memproses approval.
- Menampilkan Success Feedback hanya setelah operasi berhasil.
- Mengikuti destination Back to Detail.
- Memperbarui status record sesuai HSD/BRD.

AI MUST NOT mengubah approval menjadi direct action tanpa confirmation.

### 4.5 State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Disabled, Confirmation, Cancel, Loading, Success, Error, Access Restricted, dan Updated Approval Status.

---

## 5. Pattern 02 — Approve Variation 02

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3357-58896

### 5.1 When to Use

AI MUST mempertimbangkan Pattern 02 ketika HSD/BRD membutuhkan approval individual melalui Detail Page dan struktur UI pada Pattern 02 paling sesuai dengan informasi yang ditampilkan.

AI MUST membandingkan Pattern 02 dengan Pattern 01 sebelum memilih.

### 5.2 Official Core Flow

Start → List Page → View Detail → Click Approve → Confirmation Modal → YA, SETUJUI → Toast Message (Back to Detail) → End.

Cabang Cancel: BATAL.

### 5.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page menggunakan struktur Pattern 02.
3. Approve Action.
4. Confirmation Modal.
5. Loading State.
6. Success Feedback.
7. Error Feedback.
8. Cancel State.
9. Disabled dan Restricted States jika berlaku.

### 5.4 Specific Rules

AI MUST:

- Mempertahankan struktur UI Pattern 02.
- Menggunakan komponen GEMS yang sesuai.
- Mempertahankan lokasi Approve Action.
- Mengikuti Core Flow resmi.
- Memastikan state ditampilkan dalam konteks screen yang benar.

AI MUST NOT mengganti struktur Pattern 02 dengan Pattern 01 hanya karena keduanya memiliki Core Flow serupa.

### 5.5 State Coverage

Default, Hover, Focus, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, dan Updated Status.

---

## 6. Pattern 03 — Pending Official Reference

**Figma Reference:** Pending Verification.

### 6.1 Current Status

Pattern 03 belum dapat diidentifikasi secara lengkap dari referensi individual yang tersedia.

AI MUST NOT mengarang:

- Nama variasi.
- Entry Point.
- Core Flow.
- Confirmation Behavior.
- Navigation Destination.
- Screen Structure.
- Component Placement.

### 6.2 Required AI Behavior

AI MUST:

1. Mencari Pattern 03 pada parent canvas resmi.
2. Memeriksa apakah node tersedia.
3. Mengidentifikasi Core Flow aktual.
4. Mengidentifikasi UI Screens.
5. Memeriksa komponen GEMS.
6. Menentukan applicable states.
7. Menandai pattern sebagai Pending Verification jika referensi belum tersedia.

AI MUST NOT memilih Pattern 03 untuk implementasi final sebelum struktur resminya terverifikasi.

---

## 7. Pattern 04 — Approve Variation 04

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3443-19451

### 7.1 When to Use

AI MUST mempertimbangkan Pattern 04 untuk approval individual melalui Detail Page ketika struktur dan komponen pada referensi ini sesuai dengan kebutuhan HSD/BRD.

### 7.2 Official Core Flow

Start → List Page → View Detail → Click Approve → Confirmation Modal → YA, SETUJUI → Toast Message (Back to Detail) → End.

Cabang Cancel: BATAL.

### 7.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page sesuai Pattern 04.
3. Approve Action.
4. Confirmation Modal.
5. Loading State.
6. Success State.
7. Error State.
8. Cancel State.
9. Disabled atau Restricted State jika berlaku.

### 7.4 Specific Rules

AI MUST mempertahankan layout, hierarchy, dan component placement yang digunakan pada Pattern 04.

AI MUST memeriksa penggunaan Detail Information dan Section Footer pada referensi sebelum menentukan penempatan action.

AI MUST NOT menganggap Section Footer sebagai komponen wajib untuk semua approval pattern.

### 7.5 State Coverage

Default, Hover, Focus, Confirmation, Cancel, Loading, Success, Error, Disabled, dan Updated Approval Status.

---

## 8. Pattern 05 — Approve Variation 05

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3443-19541

### 8.1 When to Use

AI MUST mempertimbangkan Pattern 05 ketika proses approval individual membutuhkan struktur Detail Page yang sesuai dengan referensi Pattern 05.

### 8.2 Official Core Flow

Start → List Page → View Detail → Click Approve → Confirmation Modal → YA, SETUJUI → Toast Message (Back to Detail) → End.

Cabang Cancel: BATAL.

### 8.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page.
3. Approve Action.
4. Confirmation Modal.
5. Processing State.
6. Success Toast.
7. Error Feedback.
8. Cancel State.
9. Disabled dan Restricted States jika berlaku.

### 8.4 Specific Rules

AI MUST menggunakan layout dan komponen yang sesuai Pattern 05.

AI MUST memeriksa penggunaan Section Footer dan action placement pada Figma.

AI MUST mempertahankan navigation destination resmi.

AI MUST NOT menambahkan approval steps baru tanpa approved requirements.

### 8.5 State Coverage

Default, Hover, Focus, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, dan Updated Status.

---

## 9. Pattern 06 — Bulk Approval

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3363-95220

### 9.1 When to Use

AI MUST menggunakan Pattern 06 ketika HSD/BRD mengizinkan pengguna menyetujui beberapa record dalam satu tindakan.

Pattern ini khusus untuk Bulk Approval.

### 9.2 Official Core Flow

Start → List/Data Table → Pilih Data (Checkbox satu atau semua) → Click Setujui Massal → Confirmation Modal → YA, SETUJUI → Toast Message → End.

Cabang Cancel: BATAL.

Referensi resmi juga menyatakan:

**Hanya data yang memenuhi ketentuan yang dapat diproses.**

AI MUST menerapkan aturan tersebut sesuai eligibility criteria dari HSD/BRD.

### 9.3 Required UI Screens

AI MUST menghasilkan:

1. List/Data Table.
2. Default Table State.
3. Single Row Selected State.
4. Multiple Rows Selected State.
5. Select All State.
6. Bulk Action State.
7. Disabled Bulk Action State.
8. Ineligible Record State jika berlaku.
9. Confirmation Modal.
10. Bulk Approval Loading State.
11. Bulk Approval Success State.
12. Bulk Approval Error State.
13. Cancel State.
14. Updated Table State.
15. Partial Success State hanya jika didukung business rules.

### 9.4 Selection Behavior

AI MUST:

- Menggunakan Checkbox resmi GEMS.
- Mengikuti selection behavior pada referensi.
- Menampilkan selected records secara jelas.
- Menjaga konsistensi antara jumlah terpilih dan tindakan.
- Memeriksa eligibility sebelum approval.
- Mengikuti aturan Select All resmi.
- Menggunakan Disabled State jika Bulk Action belum dapat dilakukan.

AI MUST NOT menganggap seluruh record eligible.

### 9.5 Eligibility Rules

AI MUST memeriksa:

- Role pengguna.
- Current approval status.
- Record eligibility.
- Business restrictions.
- Data dependencies.
- Approval prerequisites.

AI MUST NOT mengarang eligibility criteria.

Jika HSD/BRD tidak menjelaskan apakah ineligible records dapat dipilih, AI MUST meminta klarifikasi.

### 9.6 Confirmation Behavior

AI MUST menggunakan Confirmation Modal resmi.

Confirmation MUST merepresentasikan tindakan Bulk Approval.

Jika jumlah record ditampilkan, AI MUST memastikan jumlah tersebut sesuai selection yang valid.

AI MUST NOT menggunakan confirmation wording untuk Delete.

### 9.7 Bulk Approval Processing

AI MUST:

1. Menampilkan processing feedback.
2. Mengikuti komponen Loading resmi.
3. Memastikan hasil operasi belum dianggap berhasil sebelum dikonfirmasi sistem.
4. Menjaga konsistensi selected records.
5. Mengikuti approved business behavior.

### 9.8 Success Behavior

AI MUST:

- Menampilkan Success Feedback resmi.
- Memperbarui status record yang berhasil disetujui.
- Mengikuti destination resmi.
- Memperbarui representasi table sesuai hasil.

### 9.9 Error & Partial Success

AI MUST membedakan:

- Full Success.
- Full Failure.
- Partial Success jika didukung HSD/BRD.

AI MUST NOT menganggap Partial Success selalu didukung.

Jika sebagian record gagal diproses tetapi HSD/BRD tidak menentukan behavior-nya, AI MUST menandainya sebagai Pending Requirement dan meminta Human Approval sebelum menambahkan behavior baru.

### 9.10 State Coverage

Default, Hover, Focus, Selected, Multiple Selected, Select All, Disabled, Ineligible, Confirmation, Cancel, Loading, Success, Error, Updated Table, dan Partial Success jika berlaku.

---

## 10. Pattern 07 — Approve Variation 07

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3364-106181

### 10.1 When to Use

AI MUST mempertimbangkan Pattern 07 ketika proses approval individual melalui Detail Page membutuhkan struktur UI yang sesuai referensi Pattern 07.

### 10.2 Official Core Flow

Start → List Page → View Detail → Click Approve → Confirmation Modal → YA, SETUJUI → Toast Message (Back to Detail) → End.

Cabang Cancel: BATAL.

### 10.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page sesuai Pattern 07.
3. Approve Action.
4. Confirmation Modal.
5. Processing State.
6. Success Toast.
7. Error State.
8. Cancel State.
9. Disabled atau Restricted State jika berlaku.

### 10.4 Specific Rules

AI MUST:

- Mengikuti layout dan hierarchy Pattern 07.
- Menggunakan komponen resmi GEMS.
- Mempertahankan Core Flow.
- Menggunakan Confirmation Modal resmi.
- Mempertahankan Back to Detail behavior.
- Memastikan approval status sesuai HSD/BRD.

AI MUST NOT menggunakan komponen atau layout dari pattern lain tanpa alasan yang didukung referensi.

### 10.5 State Coverage

Default, Hover, Focus, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, dan Updated Status.

---

## 11. Pattern 08 — Approve Variation 08

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3443-40313

### 11.1 When to Use

AI MUST mempertimbangkan Pattern 08 ketika approval individual dilakukan melalui Detail Page dan struktur UI Pattern 08 paling sesuai dengan approved requirements.

### 11.2 Official Core Flow

Start → List Page → View Detail → Click Approve → Confirmation Modal → YA, SETUJUI → Toast Message (Back to Detail) → End.

Cabang Cancel: BATAL.

### 11.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page sesuai Pattern 08.
3. Approve Action.
4. Confirmation Modal.
5. Loading State.
6. Success State.
7. Error State.
8. Cancel State.
9. Disabled dan Restricted States jika berlaku.

### 11.4 Specific Rules

AI MUST:

- Mengikuti struktur UI Pattern 08.
- Memeriksa penggunaan Section Footer.
- Menggunakan GEMS components dan variants.
- Mempertahankan approval confirmation.
- Mengikuti Back to Detail.
- Memastikan hasil approval sesuai business rules.

AI MUST NOT mengubah interaction sequence atau navigation tanpa Human Approval.

### 11.5 State Coverage

Default, Hover, Focus, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, dan Updated Status.

---

## 12. Mandatory UI State Generation

### 12.1 State Generation Principles

AI MUST mengevaluasi seluruh UI States untuk setiap pattern.

AI MUST menghasilkan seluruh applicable states menggunakan komponen resmi GEMS.

AI MUST membedakan antara state yang wajib direpresentasikan, state yang hanya berlaku pada kondisi tertentu, dan state yang membutuhkan keputusan bisnis.

AI MUST NOT mengarang business behavior hanya untuk melengkapi jumlah screens.

### 12.2 UI State Matrix

| State | Trigger | Expected UI Output | Applicability |
|---|---|---|---|
| Default | Screen dibuka | Normal screen | All |
| Hover | Pointer pada action | Hover variant | Applicable controls |
| Focus | Keyboard focus | Focus indicator | Applicable controls |
| Active | Action aktif | Active variant | If supported |
| Selected | Record dipilih | Selected row | Bulk |
| Select All | Semua record dipilih | Checkbox state | Bulk |
| Disabled | Action tidak tersedia | Disabled action | Based on rules |
| Confirmation | Approve dipilih | Confirmation Modal | All |
| Cancel | BATAL dipilih | Return to source | All |
| Loading | Approval diproses | Loading feedback | All |
| Success | Approval berhasil | Success Toast | All |
| Error | Approval gagal | Error feedback | All |
| Validation Error | Input tidak valid | Field error | If form exists |
| Empty | Data tidak tersedia | Empty State | If applicable |
| Access Restricted | Role tidak berwenang | Permission state | Based on role |
| Ineligible | Record tidak memenuhi syarat | Restricted/disabled presentation | If applicable |
| Updated Status | Approval berhasil | Updated record status | All |
| Network Error | Gangguan koneksi | Error feedback | If applicable |
| Server Error | Gangguan sistem | Error feedback | If applicable |
| Partial Success | Sebagian record berhasil | Partial result feedback | Bulk, if supported |

### 12.3 Default State

AI MUST menggunakan screen normal sesuai pattern terpilih.

AI MUST memastikan data, action, status, dan navigation sesuai HSD/BRD.

### 12.4 Hover, Focus & Active States

AI MUST menggunakan component variants resmi GEMS.

AI MUST NOT membuat visual interaction state baru jika tidak tersedia dalam Design System.

AI MUST memeriksa keyboard focus dan interaction clarity untuk komponen yang mendukung interaksi.

### 12.5 Disabled State

AI MUST menampilkan Disabled State ketika approval tidak tersedia berdasarkan approved business rules.

Contoh kondisi yang perlu diperiksa:

- User tidak memiliki permission.
- Record tidak memenuhi approval requirements.
- Record telah diproses.
- Approval action tidak tersedia pada status tertentu.
- Tidak ada record yang dipilih untuk Bulk Approval.

Contoh tersebut merupakan kondisi yang harus diperiksa terhadap HSD/BRD, bukan aturan bisnis yang boleh diasumsikan.

AI MUST NOT menonaktifkan action tanpa dasar requirement.

### 12.6 Confirmation State

AI MUST:

1. Menggunakan Confirmation Modal resmi.
2. Menampilkan konteks tindakan.
3. Menggunakan wording approval.
4. Menyediakan Confirm dan Cancel.
5. Mengikuti action hierarchy GEMS.
6. Tidak memproses approval sebelum Confirm.

### 12.7 Cancel State

AI MUST memastikan:

1. Modal ditutup.
2. Approval tidak diproses.
3. Data tidak berubah akibat pembatalan.
4. Pengguna tetap berada dalam konteks yang benar.
5. Tidak muncul Success Toast.

### 12.8 Loading State

AI MUST:

1. Menggunakan loading indicator resmi.
2. Menunjukkan proses sedang berjalan.
3. Menggunakan processing state pada action jika tersedia.
4. Mencegah representasi keberhasilan sebelum respons sistem.
5. Mengikuti aturan multiple submission dari approved requirements.

### 12.9 Success State

AI MUST:

1. Menggunakan Success Toast atau Notification resmi.
2. Menampilkan feedback setelah approval berhasil.
3. Memperbarui status record.
4. Mengikuti navigation destination.
5. Menjaga konsistensi data antara List dan Detail.

AI MUST NOT menampilkan Success State sebelum approval berhasil.

### 12.10 Error State

AI MUST:

1. Menggunakan Error Feedback resmi.
2. Menjelaskan bahwa approval gagal.
3. Mempertahankan konteks pengguna.
4. Tidak mengubah status seolah approval berhasil.
5. Mengikuti approved recovery behavior.

AI MUST NOT menambahkan Retry Flow baru tanpa dukungan requirement.

### 12.11 Empty State

AI MUST menggunakan Empty State resmi ketika daftar approval tidak memiliki data.

AI MUST membedakan kondisi:

- Belum ada data.
- Tidak ada hasil filter.
- Data tidak ditemukan.

AI MUST mengikuti wording dan behavior yang sesuai konteks.

### 12.12 Access Restricted State

AI MUST mengikuti Role Access Matrix.

Jika pengguna tidak memiliki permission, AI MUST menggunakan behavior yang disetujui, misalnya action disembunyikan, disabled, atau akses ditolak.

AI MUST NOT menentukan sendiri apakah action harus hidden atau disabled jika HSD/BRD belum menetapkannya.

### 12.13 Updated Approval Status

AI MUST menampilkan status terbaru setelah approval berhasil.

AI MUST:

- Menggunakan Badge atau Status Component resmi jika sesuai referensi.
- Mengikuti status naming dari HSD/BRD.
- Memperbarui data yang relevan.
- Tidak mengarang status baru.

### 12.14 State Presentation Rules

AI MUST:

1. Mengelompokkan states bersama screen asalnya.
2. Menggunakan state label yang jelas.
3. Menampilkan trigger dan expected outcome.
4. Menggunakan komponen resmi.
5. Menjaga konsistensi layout.
6. Menyertakan state dalam Flow-to-Screen Mapping.
7. Menandai state yang belum dapat dipastikan.

AI MUST NOT menampilkan state sebagai kumpulan screens tanpa hubungan dengan flow.

---

## 13. Mandatory GEMS Component Usage

### 13.1 Component Requirements

AI MUST menggunakan komponen resmi sesuai kebutuhan pattern, termasuk:

- Page Header.
- Navbar.
- Sidebar.
- Table.
- Table Cell.
- Checkbox.
- Button.
- Badge.
- Detail Information.
- Record Information.
- Confirmation Modal.
- Toast / Notification.
- Alert.
- Pagination.
- Empty State.
- Loading Indicator.
- Section Footer jika sesuai pattern.

Daftar ini merupakan component coverage yang perlu diperiksa, bukan instruksi untuk menampilkan seluruh komponen pada setiap screen.

### 13.2 Component Retrieval

AI MUST:

1. Memeriksa official Figma component.
2. Mengidentifikasi component name.
3. Memeriksa properties.
4. Memeriksa variants.
5. Memeriksa available states.
6. Memeriksa component anatomy.
7. Memeriksa typography dan color tokens.
8. Memeriksa spacing dan layout rules.
9. Menggunakan instance resmi jika memungkinkan.
10. Memvalidasi instance pada hasil desain.

### 13.3 Component Integrity

AI MUST NOT:

- Mengganti GEMS components dengan external components.
- Membuat custom Button atau Modal tanpa approval.
- Mengarang variants.
- Mengubah component anatomy.
- Mengubah warna status secara sepihak.
- Mengubah button hierarchy.
- Mengubah interaction behavior resmi.
- Mengklaim sebuah tiruan sebagai instance resmi GEMS.

### 13.4 Missing Component Handling

Jika komponen tidak tersedia, AI MUST:

1. Mengidentifikasi gap.
2. Memeriksa alternatif resmi.
3. Menjelaskan keterbatasan.
4. Mengusulkan solusi.
5. Menjelaskan dampak.
6. Meminta Human Approval sebelum implementasi.

---

## 14. Mandatory UX Flow Diagram & UI Screen Layout

### 14.1 Required Figma Structure

AI MUST menghasilkan dua area dalam satu section Figma:

**TOP — UX FLOW DIAGRAM**

Berisi approved Core Flow dan applicable branches.

**BOTTOM — UI SCREENS & STATES**

Berisi seluruh UI Screens dan applicable states yang mengikuti flow.

### 14.2 UX Flow Diagram Requirements

AI MUST menampilkan:

- Start.
- Entry Point.
- View Detail jika berlaku.
- Approve Action.
- Confirmation Modal.
- Confirm.
- Cancel.
- Processing.
- Success Feedback.
- Approved Error Behavior.
- Navigation Destination.
- End.

Untuk Bulk Approval, AI MUST menambahkan Selection dan Bulk Action sesuai referensi.

AI MUST membedakan node resmi dari penjelasan state tambahan.

### 14.3 Screen Arrangement

AI MUST:

1. Mengurutkan screens sesuai Main Flow.
2. Menempatkan Confirmation bersama source screen.
3. Menempatkan Success State pada destination screen.
4. Menempatkan Error State pada konteks yang sesuai.
5. Menempatkan Disabled State bersama action terkait.
6. Menempatkan Bulk Selection States pada List/Data Table.
7. Menjaga alignment, spacing, dan naming.
8. Menggunakan layout resmi GEMS.

### 14.4 Flow-to-Screen Mapping

| Flow Node | UI Representation |
|---|---|
| List Page | List/Data Table |
| View Detail | Detail Page |
| Approve | Approve Action |
| Confirmation | Confirmation Modal |
| Cancel | Source Screen |
| Processing | Loading State |
| Success | Success Toast |
| Error | Error Feedback |
| Back to Detail | Updated Detail Page |
| Select Records | Selected Table State |
| Bulk Approve | Bulk Action |
| End | Final Approved State |

AI MUST menggunakan hanya node yang relevan dengan pattern terpilih.

---

## 15. Business Rules & Approval Permissions

### 15.1 Required Business Analysis

AI MUST mengidentifikasi:

1. Feature Name.
2. User Role.
3. Approval Permission.
4. Record Type.
5. Current Status.
6. Approval Eligibility.
7. Approval Prerequisites.
8. Confirmation Requirements.
9. Resulting Status.
10. Success Behavior.
11. Error Behavior.
12. Navigation Destination.
13. Bulk Approval Availability.
14. Partial Approval Rules jika berlaku.

### 15.2 Approval Eligibility

AI MUST menggunakan approved eligibility criteria.

AI MUST NOT menganggap semua record dapat disetujui.

Jika eligibility tidak dijelaskan, AI MUST menandai sebagai Pending Requirement.

### 15.3 Status Transition

AI MUST menggunakan status dari HSD/BRD.

AI MUST NOT membuat status seperti Approved, Processed, Completed, atau Rejected tanpa dasar requirement.

### 15.4 Permission Handling

AI MUST mengikuti Role Access Matrix.

AI MUST NOT memberikan Approve Action kepada role yang tidak memiliki izin.

### 15.5 Bulk Approval Rules

AI MUST memeriksa:

- Apakah Bulk Approval diizinkan.
- Apakah Select All berlaku untuk current page atau seluruh dataset.
- Apakah ineligible records dapat dipilih.
- Apakah seluruh record harus berhasil bersama.
- Apakah Partial Success diperbolehkan.
- Bagaimana hasil approval ditampilkan.

AI MUST meminta klarifikasi jika aturan tersebut tidak tersedia.

---

## 16. AI Recommendation & Human Approval

### 16.1 Recommendation Policy

AI MAY merekomendasikan:

- UX improvement.
- Alternative approval pattern.
- Additional UI State.
- Better feedback behavior.
- Improved error handling.
- Alternative navigation.
- New component variant.
- Additional approval validation.
- Improved Bulk Selection behavior.

Rekomendasi MUST didasarkan pada kebutuhan bisnis, usability, accessibility, atau keterbatasan pattern resmi.

### 16.2 Recommendation Format

AI MUST menyampaikan:

| Field | Description |
|---|---|
| Current Pattern | Pattern resmi |
| Business Requirement | Requirement terkait |
| Identified Issue | Masalah atau gap |
| Proposed Improvement | Rekomendasi |
| Reason | Alasan |
| UX Flow Impact | Dampak terhadap flow |
| UI Impact | Dampak terhadap screens |
| State Impact | Dampak terhadap states |
| Component Impact | Dampak terhadap GEMS |
| Approval Status | Pending Human Approval |

### 16.3 Mandatory Human Approval

AI MUST memperoleh explicit Human Approval sebelum:

1. Mengubah Core Flow.
2. Mengubah entry point.
3. Mengubah navigation.
4. Menambahkan approval step.
5. Menghilangkan confirmation.
6. Mengubah approval behavior.
7. Menambahkan status baru.
8. Mengubah eligibility rules.
9. Mengubah role permission.
10. Membuat komponen atau variant baru di luar GEMS.
11. Mengubah approved error recovery.
12. Mengimplementasikan Proposed Design.

### 16.4 Approved vs Proposed

AI MUST memisahkan:

**Approved Design:** Mengikuti sumber resmi dan dapat diimplementasikan sesuai requirement.

**Proposed Design:** Rekomendasi yang membutuhkan persetujuan.

AI MUST NOT mencampurkan Proposed Design ke dalam final approved implementation sebelum disetujui.

---

## 17. Required AI Design Output

AI MUST menghasilkan:

### 17.1 Pattern Selection Report

Berisi nama fitur, selected pattern, entry point, role, alasan pemilihan, dan link Figma.

### 17.2 UX Flow Diagram

Berisi approved Core Flow, confirmation, decision, dan navigation.

### 17.3 UI Screens

Berisi screens sesuai pattern dan seluruh applicable states.

### 17.4 UI State Coverage Report

Berisi:

- Applicable States.
- Generated States.
- Not Applicable States.
- Pending Requirement States.
- Pending Human Approval States.

### 17.5 Flow-to-Screen Mapping

Berisi hubungan antara flow nodes, UI Screens, dan UI States.

### 17.6 Component Usage Report

Berisi komponen resmi GEMS yang digunakan dan komponen yang belum dapat diverifikasi.

### 17.7 Compliance Report

Berisi:

- HSD/BRD Compliance.
- UX Pattern Compliance.
- Core Flow Compliance.
- GEMS Component Compliance.
- UI State Coverage.
- Role Access Compliance.
- Human Approval Status.
- Unresolved Issues.

---

## 18. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut:

**Step 1 — Analyze HSD/BRD**

Identifikasi kebutuhan approval, role, status, eligibility, dan expected behavior.

**Step 2 — Inspect Official Patterns**

Periksa seluruh referensi Approve yang relevan.

**Step 3 — Select Appropriate Pattern**

Pilih berdasarkan entry point, struktur UI, dan kebutuhan bisnis.

**Step 4 — Verify Core Flow**

Pastikan pattern mendukung kebutuhan tanpa perubahan yang belum disetujui.

**Step 5 — Inspect GEMS Design System**

Periksa components, variants, states, dan visual rules.

**Step 6 — Identify Applicable States**

Evaluasi Default, Hover, Focus, Loading, Success, Error, Disabled, Empty, Confirmation, Cancel, Restricted, dan Bulk States jika berlaku.

**Step 7 — Generate UX Flow Diagram**

Buat visual flow pada bagian atas section Figma.

**Step 8 — Generate UI Screens**

Buat screens sesuai pattern.

**Step 9 — Generate UI States**

Buat seluruh applicable states menggunakan komponen GEMS.

**Step 10 — Validate Business Behavior**

Pastikan approval eligibility, status transitions, dan role access sesuai HSD/BRD.

**Step 11 — Validate Flow-to-Screen Mapping**

Pastikan diagram, screens, dan states konsisten.

**Step 12 — Identify Gaps**

Temukan requirement, flow, state, atau component gaps.

**Step 13 — Request Human Approval**

Ajukan perubahan jika diperlukan.

**Step 14 — Inspect Actual Figma Output**

Periksa hasil desain yang benar-benar dibuat.

**Step 15 — Generate Compliance Report**

Laporkan hasil verifikasi dan unresolved issues.

---

## 19. AI Restrictions

AI MUST NOT:

1. Mengubah approved Core Flow tanpa Human Approval.
2. Menggunakan pattern di luar GEMS tanpa approval.
3. Mengganti GEMS components dengan custom components tanpa approval.
4. Mengarang approval rules.
5. Mengarang status transitions.
6. Mengarang role permission.
7. Menghilangkan Confirmation Modal.
8. Memproses approval sebelum confirmation.
9. Menampilkan Success sebelum approval berhasil.
10. Menggunakan destructive Delete wording untuk Approve.
11. Mengubah Cancel Behavior.
12. Mengubah navigation destination.
13. Mengaktifkan Bulk Approval tanpa requirement.
14. Menganggap semua record eligible.
15. Mengarang Partial Success behavior.
16. Menggunakan Disabled State tanpa dasar business rules.
17. Mengubah component variants secara sepihak.
18. Menghasilkan screens tanpa UX Flow Diagram.
19. Menghasilkan diagram yang bertentangan dengan screens.
20. Menghilangkan applicable UI States.
21. Mengimplementasikan Proposed Design tanpa approval.
22. Mengklaim komponen custom sebagai official GEMS instance.
23. Mengklaim desain compliant tanpa verifikasi aktual.
24. Menganggap Pending Requirement sebagai approved behavior.

---

## 20. Quality Assurance & Final Validation

### 20.1 Business Validation

AI MUST memastikan approval rules, role access, eligibility, dan status transitions sesuai HSD/BRD.

### 20.2 Pattern Validation

AI MUST memastikan selected pattern sesuai kebutuhan dan menggunakan referensi resmi.

### 20.3 Core Flow Validation

AI MUST memastikan urutan flow, confirmation, dan navigation sesuai approved pattern.

### 20.4 Component Validation

AI MUST memastikan seluruh komponen menggunakan GEMS Design System.

### 20.5 State Validation

AI MUST memastikan seluruh applicable states telah dihasilkan atau dijelaskan alasan tidak dapat diimplementasikannya.

### 20.6 Bulk Approval Validation

Untuk Pattern 06, AI MUST memeriksa selection, eligibility, disabled behavior, confirmation, processing, dan result feedback.

### 20.7 Human Approval Validation

AI MUST memastikan tidak ada proposed change yang diimplementasikan tanpa explicit approval.

### 20.8 Final Validation Instructions

Before reporting completion, AI MUST:

1. Verify approved business requirements.
2. Verify selected official UX Pattern.
3. Verify Core Flow integrity.
4. Verify entry point and navigation.
5. Verify Confirmation Modal.
6. Verify Confirm and Cancel behavior.
7. Verify applicable Loading States.
8. Verify Success Feedback.
9. Verify Error Feedback.
10. Verify Disabled and Restricted States.
11. Verify Bulk Selection behavior if applicable.
12. Verify status transitions.
13. Verify role permissions.
14. Verify official GEMS component usage.
15. Verify Flow-to-Screen Mapping.
16. Verify UX Flow Diagram placement above UI Screens.
17. Verify applicable state coverage.
18. Verify Human Approval for changes.
19. Inspect actual Figma output.
20. Generate final Compliance Report.

AI MUST NOT mark unverified items as compliant.

If any requirement cannot be verified, AI MUST report **Pending Validation**.

---

## 21. Final AI Enforcement

AI MUST:

1. Analyze approved HSD/BRD.
2. Use official GEMS Approve UX Patterns.
3. Preserve approved Core Flow.
4. Use GEMS Design System components.
5. Generate visual UX Flow Diagram.
6. Generate corresponding UI Screens.
7. Generate all applicable UI States.
8. Apply approval eligibility rules.
9. Respect Role Access Matrix.
10. Use Confirmation before processing approval.
11. Handle Cancel, Loading, Success, Error, and Disabled behavior.
12. Support Bulk Approval only when required.
13. Maintain Flow-to-Screen consistency.
14. Identify gaps and conflicts.
15. Recommend improvements when appropriate.
16. Obtain explicit Human Approval for changes.
17. Validate actual Figma output.
18. Generate a Compliance Report.

### Final Enforcement Rule

AI MUST use approved HSD/BRD as the source of business requirements, official GEMS UX Patterns as the source of approved Core Flows, and GEMS Design System as the source of UI components, variants, and states.

AI MUST generate a complete visual UX Flow Diagram above the corresponding UI Screens and represent every applicable UI State without introducing unapproved business behavior.

AI MAY recommend UX improvements, additional states, alternative interactions, or component enhancements when justified by business requirements or usability considerations.

AI MUST obtain explicit Human Approval before implementing any recommendation that changes the approved Core Flow, navigation, business behavior, permissions, or GEMS Design System.

AI MUST validate the actual Figma output before reporting the design as completed or compliant.

**HSD/BRD defines business requirements. GEMS UX Pattern defines the approved Core Flow. GEMS Design System defines components and visual states. Human Approval authorizes changes.**
