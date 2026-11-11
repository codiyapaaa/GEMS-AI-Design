# GEMS AI Design Guidelines — Reject Data UX Pattern

## 1. Purpose & Scope

Dokumen ini merupakan instruksi wajib bagi AI untuk menghasilkan desain UI/UX proses **Reject / Tolak Data** berdasarkan approved HSD/BRD, GEMS UX Pattern, GEMS Design System, dan Role Access Matrix.

AI MUST memahami kebutuhan bisnis sebelum memilih UX Pattern, menggunakan Core Flow resmi GEMS, menghasilkan UI Screens beserta seluruh applicable UI States, dan memvalidasi hasil desain melalui Figma MCP.

AI MUST memastikan bahwa setiap desain Reject memiliki:

1. Core Flow yang sesuai pattern resmi.
2. Entry Point dan navigation yang jelas.
3. Role dan permission yang sesuai.
4. Reject Action yang mengikuti business rules.
5. Confirmation sebelum rejection diproses.
6. Success dan Error Feedback.
7. Disabled dan Restricted States jika berlaku.
8. UI Screens yang merepresentasikan setiap langkah flow.
9. Komponen resmi GEMS Design System.
10. Human Approval untuk perubahan yang belum disetujui.

### 1.1 Mandatory Design Principles

AI MUST:

- Membaca dan memahami HSD/BRD sebelum menghasilkan desain.
- Memeriksa referensi Reject UX Pattern resmi di Figma.
- Memilih pattern berdasarkan kebutuhan bisnis dan karakteristik interaksi.
- Menggunakan approved Core Flow tanpa perubahan sepihak.
- Menggunakan GEMS Design System untuk komponen, variants, states, dan visual styling.
- Menghasilkan UX Flow Diagram pada bagian atas dan UI Screens pada bagian bawah.
- Menghasilkan applicable UI States meskipun Core Flow referensi hanya memperlihatkan jalur utama.
- Memastikan state tambahan tidak mengubah approved business behavior.
- Meminta Human Approval untuk perubahan Core Flow, navigation, interaction behavior, atau Design System.
- Memeriksa hasil aktual di Figma sebelum menyatakan desain selesai.

AI MUST NOT mengarang business requirements, rejection rules, status transitions, permission, atau system behavior.

### 1.2 Reject vs CRUD

Reject merupakan workflow action, bukan pengganti operasi CRUD.

AI MUST menggunakan guideline yang sesuai untuk setiap operasi:

| Operation | Official Guideline |
|---|---|
| Create | Add Data UX Pattern |
| Read | View Detail UX Pattern |
| Update | Edit Data UX Pattern |
| Delete | Delete Data UX Pattern |
| Approve | Approve Data UX Pattern |
| Reject | Reject Data UX Pattern |

Jika satu fitur mencakup CRUD dan Reject, AI MUST menggunakan masing-masing pattern sesuai fungsi dan menghubungkannya berdasarkan approved HSD/BRD.

AI MUST NOT menganggap Reject sama dengan Edit, Delete, Approve, Submit, atau Revise.

---

## 2. Source of Truth & Design Governance

### 2.1 Source Hierarchy

| Source | Primary Responsibility |
|---|---|
| Approved HSD/BRD | Business requirements, role, rejection rules, status transitions |
| GEMS UX Pattern | Approved Core Flow, navigation, interaction sequence |
| GEMS Design System | Components, variants, states, visual tokens |
| Role Access Matrix | Action availability dan permission |
| Human Approval | Authorization untuk proposed changes |

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
- **Business-dependent States:** State yang membutuhkan aturan dari HSD/BRD, seperti rejection eligibility, status restrictions, atau rejection reason.
- **Proposed States:** State atau behavior yang belum didukung requirement maupun pattern resmi.

AI MUST menghasilkan Approved Flow States dan applicable Design System States.

Business-dependent States MUST mengikuti approved HSD/BRD.

Proposed States MUST memperoleh Human Approval sebelum diimplementasikan.

---

## 3. Official Reject UX Pattern References

**Parent Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3359-89283

GEMS Reject UX Pattern memiliki dua pattern utama dengan empat referensi individual yang telah diverifikasi.

| Pattern | Type | Reference Status |
|---|---|---|
| Pattern 01 | Individual Rejection | Verified |
| Pattern 02 | Individual Rejection | Verified |

AI MUST memeriksa kedua pattern sebelum memilih desain.

AI MUST NOT menganggap pattern yang memiliki Core Flow serupa memiliki layout, component placement, atau interaction specification yang identik.

---

## 4. Pattern 01 — Reject from Detail Page

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3359-89284

**Alternate Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3447-83917

### 4.1 When to Use

AI MUST mempertimbangkan Pattern 01 ketika proses rejection dilakukan setelah pengguna membuka Detail Page dari List Page.

Pattern ini dapat digunakan jika HSD/BRD mengharuskan pengguna melihat informasi record sebelum melakukan penolakan.

### 4.2 Official Core Flow

Start → List Page → View Detail → Click Reject → Confirmation Modal → YA, TOLAK → Toast Message (Back to Detail) → End.

Cabang Cancel menggunakan tindakan **BATAL**.

### 4.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page.
3. Detail Page dengan Reject Action.
4. Confirmation Modal.
5. Rejection Processing State jika relevan.
6. Success Toast pada Detail Page.
7. Cancel State.
8. Error State jika relevan.
9. Disabled atau Restricted State sesuai business rules.
10. Updated Rejection Status.

### 4.4 Interaction Rules

AI MUST:

- Menggunakan Detail Page resmi GEMS.
- Menempatkan Reject Action sesuai referensi pattern.
- Menggunakan Confirmation Modal sebelum rejection.
- Menggunakan label konfirmasi sesuai konteks penolakan.
- Memastikan BATAL tidak memproses rejection.
- Menampilkan Success Feedback hanya setelah operasi berhasil.
- Mengikuti destination Back to Detail.
- Memperbarui status record sesuai HSD/BRD.

AI MUST NOT mengubah rejection menjadi direct action tanpa confirmation.

### 4.5 State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Disabled, Confirmation, Cancel, Loading, Success, Error, Access Restricted, Updated Rejection Status, dan Validation Error jika berlaku.

---

## 5. Pattern 02 — Reject Variation 02

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3359-89374

**Alternate Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3447-84007

### 5.1 When to Use

AI MUST mempertimbangkan Pattern 02 ketika HSD/BRD membutuhkan rejection individual melalui Detail Page dan struktur UI pada Pattern 02 paling sesuai dengan informasi yang ditampilkan.

AI MUST membandingkan Pattern 02 dengan Pattern 01 sebelum memilih.

### 5.2 Official Core Flow

Start → List Page → View Detail → Click Reject → Confirmation Modal → YA, TOLAK → Toast Message (Back to Detail) → End.

Cabang Cancel: BATAL.

### 5.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page menggunakan struktur Pattern 02.
3. Reject Action.
4. Confirmation Modal.
5. Loading State.
6. Success Feedback.
7. Error Feedback.
8. Cancel State.
9. Disabled dan Restricted States jika berlaku.
10. Updated Rejection Status.

### 5.4 Specific Rules

AI MUST:

- Mempertahankan struktur UI Pattern 02.
- Menggunakan komponen GEMS yang sesuai.
- Mempertahankan lokasi Reject Action.
- Mengikuti Core Flow resmi.
- Memastikan state ditampilkan dalam konteks screen yang benar.
- Memeriksa penggunaan Section Footer pada alternate reference.

AI MUST NOT mengganti struktur Pattern 02 dengan Pattern 01 hanya karena keduanya memiliki Core Flow serupa.

### 5.5 State Coverage

Default, Hover, Focus, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, Validation Error jika berlaku, dan Updated Status.

---

## 6. Mandatory Reject Confirmation & Safety Behavior

### 6.1 Confirmation Rules

AI MUST:

1. Menggunakan Confirmation Modal resmi GEMS.
2. Menampilkan konteks tindakan Reject / Tolak.
3. Menggunakan label konfirmasi yang sesuai.
4. Menyediakan Confirm dan Cancel.
5. Mengikuti action hierarchy GEMS.
6. Tidak memproses rejection sebelum Confirm.

### 6.2 Cancel Rules

AI MUST memastikan:

1. Modal ditutup.
2. Rejection tidak diproses.
3. Data tidak berubah akibat pembatalan.
4. Pengguna tetap berada dalam konteks yang benar.
5. Tidak muncul Success Toast.

### 6.3 Rejection Reason Rules

AI MUST memeriksa apakah HSD/BRD mewajibkan alasan penolakan.

Jika alasan penolakan wajib, AI MUST:

1. Menggunakan official GEMS Input atau Textarea.
2. Menghasilkan Default State.
3. Menghasilkan Focus State.
4. Menghasilkan Filled State.
5. Menghasilkan Validation Error.
6. Mengikuti approved validation rules.
7. Memastikan rejection tidak diproses ketika input wajib belum valid.

Jika alasan penolakan optional, AI MUST NOT menjadikannya mandatory.

Jika HSD/BRD tidak menjelaskan kebutuhan alasan penolakan, AI MUST menandainya sebagai Pending Requirement.

AI MUST NOT mengarang minimum karakter, maximum karakter, predefined options, atau validation messages tanpa dasar requirement.

### 6.4 Safety Requirements

AI MUST NOT:

- Menggunakan Delete confirmation untuk Reject.
- Menggunakan Approve wording.
- Memproses rejection secara otomatis.
- Menampilkan Success sebelum hasil sistem diterima.
- Mengubah status setelah Cancel.
- Mengarang retry atau rollback behavior.

---

## 7. Mandatory UI State Generation

### 7.1 State Generation Principles

AI MUST mengevaluasi seluruh UI States untuk setiap Reject Pattern.

AI MUST menghasilkan seluruh applicable states menggunakan komponen resmi GEMS.

AI MUST membedakan antara state yang wajib direpresentasikan, state yang hanya berlaku pada kondisi tertentu, dan state yang membutuhkan keputusan bisnis.

AI MUST NOT mengarang business behavior hanya untuk melengkapi jumlah screens.

### 7.2 UI State Matrix

| State | Trigger | Expected UI Output | Applicability |
|---|---|---|---|
| Default | Screen dibuka | Normal screen | All |
| Hover | Pointer pada action | Hover variant | Applicable controls |
| Focus | Keyboard focus | Focus indicator | Applicable controls |
| Active | Action aktif | Active variant | If supported |
| Confirmation | Reject dipilih | Confirmation Modal | All |
| Cancel | BATAL dipilih | Return to Detail | All |
| Loading | Rejection diproses | Loading feedback | All |
| Success | Rejection berhasil | Success Toast | All |
| Error | Rejection gagal | Error feedback | All |
| Disabled | Action tidak tersedia | Disabled action | Based on rules |
| Validation Error | Input tidak valid | Field error | If form exists |
| Empty | Data tidak tersedia | Empty State | If applicable |
| Not Found | Record tidak ditemukan | Not Found State | If applicable |
| Access Restricted | Role tidak berwenang | Permission state | Based on role |
| Updated Status | Rejection berhasil | Updated record status | All |
| Network Error | Gangguan koneksi | Error feedback | If applicable |
| Server Error | Gangguan sistem | Error feedback | If applicable |

### 7.3 Default State

AI MUST menggunakan screen normal sesuai pattern terpilih.

AI MUST memastikan data, action, status, dan navigation sesuai HSD/BRD.

### 7.4 Hover, Focus & Active States

AI MUST menggunakan component variants resmi GEMS.

AI MUST NOT membuat visual interaction state baru jika tidak tersedia dalam Design System.

AI MUST memeriksa keyboard focus dan interaction clarity untuk komponen yang mendukung interaksi.

### 7.5 Disabled State

AI MUST menampilkan Disabled State ketika rejection tidak tersedia berdasarkan approved business rules.

Contoh kondisi yang perlu diperiksa:

- User tidak memiliki permission.
- Record tidak memenuhi rejection requirements.
- Record telah diproses.
- Rejection action tidak tersedia pada status tertentu.
- Input wajib belum memenuhi validasi.

Contoh tersebut merupakan kondisi yang harus diperiksa terhadap HSD/BRD, bukan aturan bisnis yang boleh diasumsikan.

AI MUST NOT menonaktifkan action tanpa dasar requirement.

### 7.6 Confirmation State

AI MUST:

1. Menggunakan Confirmation Modal resmi.
2. Menampilkan konteks tindakan.
3. Menggunakan wording rejection.
4. Menyediakan Confirm dan Cancel.
5. Mengikuti action hierarchy GEMS.
6. Tidak memproses rejection sebelum Confirm.

### 7.7 Cancel State

AI MUST memastikan:

1. Modal ditutup.
2. Rejection tidak diproses.
3. Data tidak berubah.
4. Pengguna tetap berada dalam konteks yang benar.
5. Tidak muncul Success Toast.

### 7.8 Loading State

AI MUST:

1. Menggunakan loading indicator resmi.
2. Menunjukkan proses sedang berjalan.
3. Menggunakan processing state pada action jika tersedia.
4. Mencegah representasi keberhasilan sebelum respons sistem.
5. Mengikuti aturan multiple submission dari approved requirements.

### 7.9 Success State

AI MUST:

1. Menggunakan Success Toast atau Notification resmi.
2. Menampilkan feedback setelah rejection berhasil.
3. Memperbarui status record.
4. Mengikuti navigation destination.
5. Menjaga konsistensi data antara List dan Detail.

AI MUST NOT menampilkan Success State sebelum rejection berhasil.

### 7.10 Error State

AI MUST:

1. Menggunakan Error Feedback resmi.
2. Menjelaskan bahwa rejection gagal.
3. Mempertahankan konteks pengguna.
4. Tidak mengubah status seolah rejection berhasil.
5. Mengikuti approved recovery behavior.

AI MUST NOT menambahkan Retry Flow baru tanpa dukungan requirement.

### 7.11 Empty & Not Found States

AI MUST menggunakan Empty State resmi ketika daftar rejection tidak memiliki data.

AI MUST membedakan kondisi:

- Belum ada data.
- Tidak ada hasil filter.
- Data tidak ditemukan.

AI MUST mengikuti wording dan behavior yang sesuai konteks.

### 7.12 Access Restricted State

AI MUST mengikuti Role Access Matrix.

Jika pengguna tidak memiliki permission, AI MUST menggunakan behavior yang disetujui, misalnya action disembunyikan, disabled, atau akses ditolak.

AI MUST NOT menentukan sendiri apakah action harus hidden atau disabled jika HSD/BRD belum menetapkannya.

### 7.13 Updated Rejection Status

AI MUST menampilkan status terbaru setelah rejection berhasil.

AI MUST:

- Menggunakan Badge atau Status Component resmi jika sesuai referensi.
- Mengikuti status naming dari HSD/BRD.
- Memperbarui data yang relevan.
- Tidak mengarang status baru.

### 7.14 State Presentation Rules

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

## 8. Mandatory GEMS Component Usage

### 8.1 Component Requirements

AI MUST menggunakan komponen resmi sesuai kebutuhan pattern, termasuk:

- Page Header.
- Navbar.
- Sidebar.
- Table.
- Table Cell.
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
- Input / Textarea jika diperlukan.
- Section Footer jika sesuai pattern.

Daftar ini merupakan component coverage yang perlu diperiksa, bukan instruksi untuk menampilkan seluruh komponen pada setiap screen.

### 8.2 Component Retrieval

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

### 8.3 Component Integrity

AI MUST NOT:

- Mengganti GEMS components dengan external components.
- Membuat custom Button atau Modal tanpa approval.
- Mengarang variants.
- Mengubah component anatomy.
- Mengubah warna status secara sepihak.
- Mengubah button hierarchy.
- Mengubah interaction behavior resmi.
- Mengklaim sebuah tiruan sebagai instance resmi GEMS.

### 8.4 Missing Component Handling

Jika komponen tidak tersedia, AI MUST:

1. Mengidentifikasi gap.
2. Memeriksa alternatif resmi.
3. Menjelaskan keterbatasan.
4. Mengusulkan solusi.
5. Menjelaskan dampak.
6. Meminta Human Approval sebelum implementasi.

---

## 9. Mandatory UX Flow Diagram & UI Screen Layout

### 9.1 Required Figma Structure

AI MUST menghasilkan dua area dalam satu section Figma:

**TOP — UX FLOW DIAGRAM**

Berisi approved Core Flow dan applicable branches.

**BOTTOM — UI SCREENS & STATES**

Berisi seluruh UI Screens dan applicable states yang mengikuti flow.

### 9.2 UX Flow Diagram Requirements

AI MUST menampilkan:

- Start.
- Entry Point.
- View Detail.
- Reject Action.
- Confirmation Modal.
- Confirm.
- Cancel.
- Processing.
- Success Feedback.
- Approved Error Behavior.
- Navigation Destination.
- End.

AI MUST membedakan node resmi dari penjelasan state tambahan.

### 9.3 Screen Arrangement

AI MUST:

1. Mengurutkan screens sesuai Main Flow.
2. Menempatkan Confirmation bersama source screen.
3. Menempatkan Success State pada destination screen.
4. Menempatkan Error State pada konteks yang sesuai.
5. Menempatkan Disabled State bersama action terkait.
6. Menjaga alignment, spacing, dan naming.
7. Menggunakan layout resmi GEMS.

### 9.4 Flow-to-Screen Mapping

| Flow Node | UI Representation |
|---|---|
| List Page | List/Data Table |
| View Detail | Detail Page |
| Reject | Reject Action |
| Confirmation | Confirmation Modal |
| Cancel | Source Screen |
| Processing | Loading State |
| Success | Success Toast |
| Error | Error Feedback |
| Back to Detail | Updated Detail Page |
| End | Final Rejected State |

AI MUST menggunakan hanya node yang relevan dengan pattern terpilih.

---

## 10. Business Rules & Rejection Permissions

### 10.1 Required Business Analysis

AI MUST mengidentifikasi:

1. Feature Name.
2. User Role.
3. Rejection Permission.
4. Record Type.
5. Current Status.
6. Rejection Eligibility.
7. Rejection Prerequisites.
8. Rejection Reason Requirements.
9. Confirmation Requirements.
10. Resulting Status.
11. Success Behavior.
12. Error Behavior.
13. Navigation Destination.

### 10.2 Rejection Eligibility

AI MUST menggunakan approved eligibility criteria.

AI MUST NOT menganggap semua record dapat ditolak.

Jika eligibility tidak dijelaskan, AI MUST menandai sebagai Pending Requirement.

### 10.3 Status Transition

AI MUST menggunakan status dari HSD/BRD.

AI MUST NOT membuat status seperti Rejected, Returned, Revision Required, atau Cancelled tanpa dasar requirement.

### 10.4 Permission Handling

AI MUST mengikuti Role Access Matrix.

AI MUST NOT memberikan Reject Action kepada role yang tidak memiliki izin.

### 10.5 Rejection Reason Rules

AI MUST memeriksa:

- Apakah rejection reason diwajibkan.
- Apakah field berupa Input, Textarea, atau pilihan.
- Apakah ada validation constraints.
- Apakah reason ditampilkan pada Detail Page.
- Apakah reason tercatat pada History.
- Apakah reason dapat diubah setelah rejection.

AI MUST meminta klarifikasi jika aturan tersebut tidak tersedia dan memengaruhi desain.

---

## 11. AI Recommendation & Human Approval

### 11.1 Recommendation Policy

AI MAY merekomendasikan:

- UX improvement.
- Alternative rejection pattern.
- Additional UI State.
- Better feedback behavior.
- Improved error handling.
- Alternative navigation.
- New component variant.
- Additional rejection validation.

Rekomendasi MUST didasarkan pada kebutuhan bisnis, usability, accessibility, atau keterbatasan pattern resmi.

### 11.2 Recommendation Format

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

### 11.3 Mandatory Human Approval

AI MUST memperoleh explicit Human Approval sebelum:

1. Mengubah Core Flow.
2. Mengubah entry point.
3. Mengubah navigation.
4. Menambahkan rejection step.
5. Menghilangkan confirmation.
6. Mengubah rejection behavior.
7. Menambahkan status baru.
8. Mengubah eligibility rules.
9. Mengubah rejection reason requirements.
10. Mengubah role permission.
11. Membuat komponen atau variant baru di luar GEMS.
12. Mengubah approved error recovery.
13. Mengimplementasikan Proposed Design.

### 11.4 Approved vs Proposed

AI MUST memisahkan:

**Approved Design:** Mengikuti sumber resmi dan dapat diimplementasikan sesuai requirement.

**Proposed Design:** Rekomendasi yang membutuhkan persetujuan.

AI MUST NOT mencampurkan Proposed Design ke dalam final approved implementation sebelum disetujui.

---

## 12. Required AI Design Output

AI MUST menghasilkan:

### 12.1 Pattern Selection Report

Berisi nama fitur, selected pattern, entry point, role, alasan pemilihan, dan link Figma.

### 12.2 UX Flow Diagram

Berisi approved Core Flow, confirmation, decision, dan navigation.

### 12.3 UI Screens

Berisi screens sesuai pattern dan seluruh applicable states.

### 12.4 UI State Coverage Report

Berisi:

- Applicable States.
- Generated States.
- Not Applicable States.
- Pending Requirement States.
- Pending Human Approval States.

### 12.5 Flow-to-Screen Mapping

Berisi hubungan antara flow nodes, UI Screens, dan UI States.

### 12.6 Component Usage Report

Berisi komponen resmi GEMS yang digunakan dan komponen yang belum dapat diverifikasi.

### 12.7 Compliance Report

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

## 13. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut:

**Step 1 — Analyze HSD/BRD**

Identifikasi kebutuhan rejection, role, status, eligibility, rejection reason, dan expected behavior.

**Step 2 — Inspect Official Patterns**

Periksa seluruh referensi Reject yang relevan.

**Step 3 — Select Appropriate Pattern**

Pilih berdasarkan entry point, struktur UI, dan kebutuhan bisnis.

**Step 4 — Verify Core Flow**

Pastikan pattern mendukung kebutuhan tanpa perubahan yang belum disetujui.

**Step 5 — Inspect GEMS Design System**

Periksa components, variants, states, dan visual rules.

**Step 6 — Identify Applicable States**

Evaluasi Default, Hover, Focus, Loading, Success, Error, Disabled, Empty, Confirmation, Cancel, Restricted, dan Validation States jika berlaku.

**Step 7 — Generate UX Flow Diagram**

Buat visual flow pada bagian atas section Figma.

**Step 8 — Generate UI Screens**

Buat screens sesuai pattern.

**Step 9 — Generate UI States**

Buat seluruh applicable states menggunakan komponen GEMS.

**Step 10 — Validate Business Behavior**

Pastikan rejection eligibility, reason requirements, status transitions, dan role access sesuai HSD/BRD.

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

## 14. AI Restrictions

AI MUST NOT:

1. Mengubah approved Core Flow tanpa Human Approval.
2. Menggunakan pattern di luar GEMS tanpa approval.
3. Mengganti GEMS components dengan custom components tanpa approval.
4. Mengarang rejection rules.
5. Mengarang status transitions.
6. Mengarang role permission.
7. Menghilangkan Confirmation Modal.
8. Memproses rejection sebelum confirmation.
9. Menampilkan Success sebelum rejection berhasil.
10. Menggunakan Approve atau Delete wording untuk Reject.
11. Mengubah Cancel Behavior.
12. Mengubah navigation destination.
13. Mengarang mandatory rejection reason.
14. Mengarang validation constraints.
15. Mengarang retry atau rollback behavior.
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

## 15. Quality Assurance & Final Validation

### 15.1 Business Validation

AI MUST memastikan rejection rules, role access, eligibility, reason requirements, dan status transitions sesuai HSD/BRD.

### 15.2 Pattern Validation

AI MUST memastikan selected pattern sesuai kebutuhan dan menggunakan referensi resmi.

### 15.3 Core Flow Validation

AI MUST memastikan urutan flow, confirmation, cancel, dan navigation sesuai approved pattern.

### 15.4 Component Validation

AI MUST memastikan seluruh komponen menggunakan GEMS Design System.

### 15.5 State Validation

AI MUST memastikan seluruh applicable states telah dihasilkan atau dijelaskan alasan tidak dapat diimplementasikannya.

### 15.6 Human Approval Validation

AI MUST memastikan tidak ada proposed change yang diimplementasikan tanpa explicit approval.

### 15.7 Final Validation Instructions

Sebelum melaporkan completion, AI MUST:

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
11. Verify rejection reason validation jika berlaku.
12. Verify status transitions.
13. Verify role permissions.
14. Verify official GEMS component usage.
15. Verify Flow-to-Screen Mapping.
16. Verify UX Flow Diagram placement above UI Screens.
17. Verify applicable state coverage.
18. Verify Human Approval for changes.
19. Inspect actual Figma output.
20. Generate final Compliance Report.

AI MUST NOT menandai item yang belum diverifikasi sebagai compliant.

Jika ada requirement yang belum dapat diverifikasi, AI MUST melaporkan **Pending Validation**.

---

## 16. Final AI Enforcement

AI MUST:

1. Analyze approved HSD/BRD.
2. Use official GEMS Reject UX Patterns.
3. Preserve approved Core Flow.
4. Use GEMS Design System components.
5. Generate visual UX Flow Diagram.
6. Generate corresponding UI Screens.
7. Generate all applicable UI States.
8. Apply rejection eligibility rules.
9. Respect Role Access Matrix.
10. Use Confirmation before processing rejection.
11. Handle Cancel, Loading, Success, Error, dan Disabled behavior.
12. Apply rejection reason requirements jika berlaku.
13. Maintain Flow-to-Screen consistency.
14. Identify gaps and conflicts.
15. Recommend improvements when appropriate.
16. Obtain explicit Human Approval for changes.
17. Validate actual Figma output.
18. Generate a Compliance Report.

### Final Enforcement Rule

AI MUST menggunakan approved HSD/BRD sebagai sumber business requirements, official GEMS Reject UX Patterns sebagai sumber approved Core Flows, dan GEMS Design System sebagai sumber UI components, variants, dan states.

AI MUST menghasilkan visual UX Flow Diagram di atas UI Screens yang sesuai serta merepresentasikan setiap applicable UI State tanpa memperkenalkan unapproved business behavior.

AI MAY merekomendasikan UX improvements, additional states, alternative interactions, atau component enhancements jika didukung kebutuhan bisnis dan pertimbangan usability.

AI MUST memperoleh explicit Human Approval sebelum mengimplementasikan rekomendasi yang mengubah approved Core Flow, navigation, business behavior, permissions, atau GEMS Design System.

AI MUST memvalidasi hasil aktual di Figma sebelum menyatakan desain selesai atau compliant.

**HSD/BRD defines business requirements. GEMS UX Pattern defines the approved Core Flow. GEMS Design System defines components and visual states. Human Approval authorizes changes.**
