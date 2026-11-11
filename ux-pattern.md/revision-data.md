# GEMS AI Design Guidelines — Revision Data UX Pattern

## 1. Purpose & Scope

Dokumen ini merupakan instruksi wajib bagi AI untuk menghasilkan desain UI/UX proses **Revision / Revisi Data** berdasarkan approved HSD/BRD, GEMS UX Pattern, GEMS Design System, dan Role Access Matrix.

Revision merupakan workflow action yang digunakan ketika pengguna berwenang meminta perbaikan atau penyesuaian terhadap suatu record melalui proses bisnis yang telah ditetapkan.

AI MUST memahami bahwa **Revision berbeda dengan Edit, Reject, Approve, dan Delete**. Revision dapat memicu proses perbaikan data, tetapi tidak secara otomatis berarti pengguna yang meminta revisi dapat langsung mengedit data tersebut.

AI MUST menghasilkan visual UX Flow Diagram pada bagian atas dan UI Screens beserta seluruh applicable UI States pada bagian bawah dalam section Figma yang sama.

### 1.1 Mandatory Design Principles

AI MUST:

1. Membaca dan menganalisis approved HSD/BRD sebelum menghasilkan desain.
2. Memeriksa seluruh official Revision UX Pattern references.
3. Memilih pattern berdasarkan kebutuhan bisnis dan karakteristik interaksi.
4. Mempertahankan approved Core Flow tanpa perubahan sepihak.
5. Menggunakan GEMS Design System sebagai sumber komponen, variants, states, dan design tokens.
6. Menghasilkan visual UX Flow Diagram pada bagian atas section Figma.
7. Menghasilkan UI Screens pada bagian bawah sesuai urutan Core Flow.
8. Menghasilkan seluruh applicable UI States, bukan hanya happy path.
9. Memastikan setiap UI State memiliki trigger, expected behavior, dan hubungan dengan screen terkait.
10. Memvalidasi revision eligibility, role permission, revision reason, dan status transition terhadap HSD/BRD.
11. Memastikan Confirmation, Cancel, Loading, Success, dan Error behavior sesuai approved requirements.
12. Mengidentifikasi requirement atau component gap sebelum implementasi.
13. Meminta explicit Human Approval untuk perubahan pada approved flow, navigation, business behavior, atau Design System.
14. Memverifikasi hasil aktual di Figma sebelum menyatakan desain selesai.

AI MUST NOT mengarang business requirements, revision reasons, mandatory fields, status transitions, role permissions, atau navigation behavior.

### 1.2 Revision vs Other Operations

AI MUST membedakan:

| Operation | Function | Guideline |
|---|---|---|
| Add Data | Membuat record baru | Add Data UX Pattern |
| View Detail | Melihat informasi record | View Detail UX Pattern |
| Edit Data | Mengubah data | Edit Data UX Pattern |
| Delete Data | Menghapus data | Delete Data UX Pattern |
| Approve Data | Menyetujui record | Approve Data UX Pattern |
| Reject Data | Menolak record | Reject Data UX Pattern |
| Revision Data | Meminta revisi record | Revision Data UX Pattern |

AI MUST NOT menganggap Revision sebagai Edit langsung atau Reject permanen.

Jika proses Revision dilanjutkan dengan Edit oleh role tertentu, AI MUST menggunakan Edit Data UX Pattern untuk proses perubahan data dan mengikuti approved HSD/BRD untuk hubungan antar-workflow.

---

## 2. Source of Truth & Design Governance

### 2.1 Source Hierarchy

| Source | Primary Responsibility |
|---|---|
| Approved HSD/BRD | Business requirements, revision rules, validation, status transition |
| GEMS UX Pattern | Approved Core Flow, navigation, interaction sequence |
| GEMS Design System | Official components, variants, states, design tokens |
| Role Access Matrix | Role permissions dan action availability |
| Human Approval | Authorization untuk perubahan desain dan flow |

AI MUST menggunakan setiap sumber sesuai kewenangannya.

Jika terdapat konflik antara HSD/BRD, UX Pattern, atau Design System, AI MUST:

1. Mengidentifikasi konflik.
2. Menjelaskan sumber yang berbeda.
3. Menjelaskan dampaknya terhadap UX Flow dan UI Screens.
4. Menyampaikan rekomendasi jika diperlukan.
5. Meminta Human Review sebelum mengimplementasikan perubahan.

AI MUST NOT menyelesaikan konflik dengan mengubah approved requirements secara sepihak.

### 2.2 Core Flow Governance

AI MUST menggunakan official Revision UX Pattern sebagai acuan utama Core Flow.

Core Flow meliputi:

1. Start.
2. Entry Point.
3. View Detail.
4. Revision Action.
5. Confirmation.
6. Decision.
7. System Feedback.
8. Navigation Destination.
9. End.

AI MUST mempertahankan urutan dan hubungan antar-node yang ditetapkan dalam pattern resmi.

AI MUST NOT menambahkan, menghilangkan, atau mengganti langkah yang mengubah approved business flow tanpa Human Approval.

### 2.3 Design System Governance

**Official GEMS Design System:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System

AI MUST menggunakan official GEMS components, properties, variants, typography, colors, spacing, dan design tokens.

AI MUST NOT mengganti official GEMS components dengan custom components atau external UI libraries tanpa approval.

### 2.4 Applicable State Governance

AI MUST membedakan:

- **Approved Flow States:** State yang ditampilkan dalam official Revision UX Pattern.
- **Design System States:** State yang didukung komponen GEMS, seperti Hover, Focus, Disabled, Loading, dan Error.
- **Business-dependent States:** State yang membutuhkan ketentuan HSD/BRD, seperti revision eligibility, revision reason, dan status transition.
- **Proposed States:** State atau behavior tambahan yang belum didukung sumber resmi.

AI MUST menghasilkan seluruh applicable states yang memiliki dasar dari approved requirements dan Design System.

AI MUST menandai unresolved states sebagai Pending Requirement atau Pending Human Approval.

AI MUST NOT menganggap seluruh kemungkinan UI States otomatis menjadi bagian dari approved Core Flow.

---

## 3. Official Revision UX Pattern References

**Parent Reference — Revision:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1205-26388

Official Revision UX Pattern memiliki dua pattern utama dan masing-masing memiliki alternate reference.

| Pattern | Type | Reference Status |
|---|---|---|
| Pattern 01 — Revision | Individual Revision from Detail | Verified |
| Pattern 02 — Revision | Individual Revision Variation | Verified |

AI MUST memeriksa seluruh referensi yang relevan sebelum memilih pattern.

AI MUST NOT menganggap kedua pattern memiliki struktur UI identik hanya karena menggunakan Core Flow yang serupa.

### 3.1 Verified Reference Coverage

Referensi Figma telah menunjukkan keberadaan:

- Start.
- List Page.
- View Detail.
- Click "Revisi".
- Confirmation Modal.
- Toast Message (Back to Detail).
- End.

Detail cabang keputusan dan wording tombol pada Confirmation Modal MUST mengikuti referensi aktual serta approved HSD/BRD.

AI MUST NOT mengarang label konfirmasi yang belum terverifikasi.

---

## 4. Pattern 01 — Revision from Detail Page

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3364-119855

**Alternate Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3447-87882

### 4.1 When to Use

AI MUST mempertimbangkan Pattern 01 ketika pengguna melakukan permintaan revisi terhadap satu record melalui Detail Page setelah membuka data dari List Page.

Pattern ini dapat digunakan ketika pengguna perlu memeriksa informasi record sebelum meminta revisi.

AI MUST memvalidasi bahwa role dan status record memenuhi revision eligibility sesuai HSD/BRD.

### 4.2 Official Core Flow

**Start → List Page → View Detail → Click "Revisi" → Confirmation Modal → Confirm Revision → Toast Message (Back to Detail) → End.**

Confirmation memiliki decision branch yang harus mengikuti referensi resmi.

**Catatan:** `Confirm Revision` merupakan deskripsi tindakan dalam guideline, bukan klaim bahwa wording tombol Figma menggunakan teks tersebut.

AI MUST memeriksa exact button labels pada Figma dan approved requirements sebelum membuat UI.

### 4.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page — Default State.
3. Detail Page — Revision Action.
4. Confirmation Modal.
5. Cancel State.
6. Revision Processing / Loading State.
7. Success Toast.
8. Updated Detail Page.
9. Error State jika berlaku.
10. Disabled atau Access Restricted State jika berlaku.
11. Validation Error jika terdapat input yang diwajibkan.
12. Updated Revision Status sesuai HSD/BRD.

AI MUST NOT membuat field atau screen tambahan tanpa dasar requirement.

### 4.4 Interaction Rules

AI MUST:

1. Menggunakan Detail Page sesuai referensi Pattern 01.
2. Menggunakan official GEMS Button untuk Revision Action.
3. Menempatkan Revision Action sesuai struktur referensi.
4. Menggunakan Confirmation Modal sebelum revision request diproses.
5. Menyediakan Cancel behavior sesuai approved flow.
6. Memastikan Cancel tidak memproses revision request.
7. Menampilkan Loading Feedback selama proses jika relevan.
8. Menampilkan Success Toast hanya setelah proses berhasil.
9. Mengikuti navigation Back to Detail.
10. Memperbarui record status berdasarkan approved HSD/BRD.

AI MUST NOT mengubah Revision Action menjadi direct submission tanpa confirmation.

### 4.5 State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Active, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, Validation Error, Updated Status, Empty, Not Found, dan Network/Server Error jika berlaku.

---

## 5. Pattern 02 — Revision Variation 02

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3364-119945

**Alternate Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3447-87972

### 5.1 When to Use

AI MUST mempertimbangkan Pattern 02 ketika proses Revision dilakukan melalui Detail Page dan struktur UI Pattern 02 paling sesuai dengan approved requirements.

AI MUST membandingkan Pattern 01 dan Pattern 02 berdasarkan:

1. Struktur Detail Page.
2. Content hierarchy.
3. Action placement.
4. Component composition.
5. Section Footer usage.
6. Business requirements.

AI MUST NOT memilih Pattern 02 hanya berdasarkan kesamaan Core Flow.

### 5.2 Official Core Flow

**Start → List Page → View Detail → Click "Revisi" → Confirmation Modal → Confirm Revision → Toast Message (Back to Detail) → End.**

AI MUST mempertahankan confirmation decision dan cancel behavior sesuai referensi aktual.

AI MUST memverifikasi exact confirmation labels sebelum implementasi.

### 5.3 Required UI Screens

AI MUST menghasilkan:

1. List Page.
2. Detail Page menggunakan struktur Pattern 02.
3. Revision Action State.
4. Confirmation Modal.
5. Cancel State.
6. Loading / Processing State.
7. Success Toast.
8. Updated Detail Page.
9. Error Feedback.
10. Disabled atau Restricted State jika berlaku.
11. Validation Error jika berlaku.
12. Updated Revision Status.

### 5.4 Specific Rules

AI MUST:

1. Mempertahankan content hierarchy Pattern 02.
2. Menggunakan official GEMS components.
3. Memeriksa action placement pada Section Footer.
4. Mempertahankan Confirmation Modal.
5. Mengikuti approved navigation.
6. Memastikan Success Feedback muncul setelah proses berhasil.
7. Mengikuti approved status transition.
8. Menempatkan applicable states pada screen terkait.

AI MUST NOT mengganti layout Pattern 02 dengan Pattern 01 tanpa alasan yang didukung requirement dan approval jika mengubah desain resmi.

### 5.5 State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, Validation Error jika berlaku, Updated Status, dan applicable failure states.

---

## 6. Mandatory UI State Generation

### 6.1 State Generation Principles

AI MUST mengevaluasi seluruh applicable UI States untuk setiap Revision Pattern.

AI MUST menghasilkan UI States menggunakan official GEMS components dan approved business behavior.

AI MUST memastikan bahwa setiap state memiliki:

1. Source Screen.
2. Trigger.
3. Expected UI Behavior.
4. Component Variant.
5. Business Rule Reference jika diperlukan.
6. Resulting State.
7. Flow-to-Screen Mapping.

AI MUST NOT menghasilkan hanya Default dan Success State.

### 6.2 Mandatory UI State Matrix

| State | Trigger | Expected UI Output | Applicability |
|---|---|---|---|
| Default | Screen dibuka | Normal UI | All |
| Hover | Pointer pada action | Hover Variant | Applicable controls |
| Focus | Keyboard focus | Focus Indicator | Applicable controls |
| Active | Action aktif | Active Variant | If supported |
| Confirmation | Click Revisi | Confirmation Modal | All |
| Cancel | Cancel dipilih | Return to Detail tanpa perubahan | All |
| Loading | Revision diproses | Processing Feedback | All |
| Success | Revision berhasil | Success Toast | All |
| Error | Revision gagal | Error Feedback | All |
| Disabled | Action tidak tersedia | Disabled Action | Based on rules |
| Validation Error | Input tidak valid | Field Error | If input exists |
| Empty | Tidak ada data | Empty State | If applicable |
| Not Found | Record tidak ditemukan | Not Found State | If applicable |
| Access Restricted | Role tidak berwenang | Permission State | Role-dependent |
| Updated Status | Revision berhasil | Updated Record Status | If status changes |
| Network Error | Gangguan koneksi | Error Feedback | If applicable |
| Server Error | Gangguan sistem | Error Feedback | If applicable |

### 6.3 Default State

AI MUST menggunakan screen normal sesuai selected Revision Pattern.

AI MUST memastikan informasi record, status, action, dan navigation sesuai approved requirements.

### 6.4 Hover, Focus & Active States

AI MUST menggunakan official GEMS component variants.

AI MUST NOT membuat interaction variants baru jika tidak tersedia dalam Design System.

AI MUST mempertahankan focus visibility dan accessibility behavior yang didukung komponen resmi.

### 6.5 Confirmation State

AI MUST:

1. Menggunakan official GEMS Confirmation Modal.
2. Menampilkan konteks Revision Action.
3. Menggunakan approved confirmation wording.
4. Menyediakan Confirm dan Cancel.
5. Mengikuti official button hierarchy.
6. Tidak memproses revision request sebelum confirmation.

### 6.6 Cancel State

AI MUST memastikan:

1. Confirmation Modal ditutup.
2. Revision request tidak diproses.
3. Record tidak berubah akibat pembatalan.
4. Pengguna tetap berada dalam konteks Detail Page.
5. Success Toast tidak ditampilkan.

### 6.7 Loading State

AI MUST:

1. Menggunakan official loading indicator atau component variant.
2. Menampilkan processing feedback.
3. Tidak menampilkan Success sebelum respons sistem berhasil.
4. Mengikuti approved duplicate-submission behavior.
5. Mempertahankan konteks pengguna selama proses.

AI MUST NOT mengarang automatic retry atau background processing.

### 6.8 Success State

AI MUST:

1. Menggunakan official GEMS Success Toast.
2. Menampilkan feedback setelah revision request berhasil.
3. Mengikuti navigation Back to Detail.
4. Memperbarui status jika HSD/BRD menetapkan perubahan status.
5. Menjaga konsistensi informasi antara List dan Detail.
6. Menampilkan revision information jika diwajibkan requirement.

AI MUST NOT menganggap permintaan revisi berhasil berarti revisi data telah selesai dilakukan.

### 6.9 Error State

AI MUST:

1. Menggunakan official GEMS Error Feedback.
2. Menjelaskan bahwa proses revision request gagal.
3. Mempertahankan konteks pengguna.
4. Tidak mengubah status seolah proses berhasil.
5. Mengikuti approved recovery behavior.

AI MUST NOT mengarang retry, rollback, atau alternate flow tanpa approval.

### 6.10 Disabled State

AI MUST mengevaluasi kondisi ketika Revision Action tidak tersedia.

Contoh kondisi yang perlu diperiksa:

- Role tidak memiliki permission.
- Record tidak memenuhi revision eligibility.
- Status record tidak mengizinkan revisi.
- Revision request sedang diproses.
- Required input belum valid.

Contoh tersebut bukan business rules otomatis.

AI MUST memvalidasi seluruh kondisi terhadap HSD/BRD sebelum mengimplementasikan Disabled State.

### 6.11 Validation Error State

Jika Revision Reason atau input lain diwajibkan oleh HSD/BRD, AI MUST menghasilkan:

1. Default Input State.
2. Focus State.
3. Filled State.
4. Required Validation.
5. Invalid Input State.
6. Error Message.
7. Valid Submission State.

AI MUST menggunakan approved validation constraints.

AI MUST NOT mengarang minimum karakter, maximum karakter, atau required fields.

### 6.12 Empty & Not Found States

AI MUST membedakan:

- Belum ada data.
- Tidak ada hasil filter.
- Record tidak ditemukan.

AI MUST menggunakan official GEMS Empty State atau approved error presentation.

### 6.13 Access Restricted State

AI MUST mengikuti Role Access Matrix.

AI MUST menggunakan approved behavior untuk role yang tidak memiliki akses.

AI MUST NOT menentukan sendiri apakah Revision Action harus hidden, disabled, atau menampilkan Access Denied.

### 6.14 Updated Status State

AI MUST menggunakan status dari HSD/BRD.

AI MUST NOT mengarang status seperti:

- Need Revision.
- Revision Requested.
- Under Revision.
- Returned.
- Revised.
- Completed.

Status tersebut hanya dapat digunakan jika secara eksplisit didukung approved requirements.

### 6.15 State Coverage Reporting

AI MUST mengklasifikasikan setiap state sebagai:

- Generated.
- Not Applicable.
- Pending Requirement.
- Pending Human Approval.
- Pending Verification.

AI MUST NOT menandai unresolved state sebagai Generated.

---

## 7. Mandatory GEMS Component Usage

### 7.1 Component Requirements

AI MUST memeriksa dan menggunakan official GEMS components sesuai selected pattern.

Komponen yang ditemukan dalam referensi Revision mencakup:

- Page Header.
- Navbar.
- GEMS Slide Bar.
- Table.
- Pagination.
- Record Info.
- Detail Information.
- Buttons/Button.
- Button Group.
- Confirmation Modal.
- Notification.
- Button Close X.
- Featured Icon Outline.
- Title Section.
- Section Footer pada referensi yang menggunakannya.

AI MUST NOT menganggap seluruh komponen harus muncul pada setiap screen.

AI MUST menggunakan komponen berdasarkan kebutuhan aktual dan struktur referensi.

### 7.2 Component Retrieval

AI MUST:

1. Memeriksa official Figma component.
2. Mengidentifikasi component name.
3. Memeriksa component properties.
4. Memeriksa available variants.
5. Memeriksa interaction states.
6. Memeriksa component anatomy.
7. Memeriksa typography.
8. Memeriksa colors dan design tokens.
9. Memeriksa spacing dan layout.
10. Menggunakan official instances jika tersedia.
11. Memvalidasi instance pada hasil desain.

### 7.3 Component Integrity

AI MUST NOT:

1. Mengganti GEMS components dengan external components.
2. Membuat custom Button tanpa approval.
3. Membuat custom Confirmation Modal tanpa approval.
4. Mengarang variants.
5. Mengubah component anatomy.
6. Mengubah status colors.
7. Mengubah button hierarchy.
8. Mengubah interaction behavior.
9. Mengklaim custom UI sebagai official GEMS component.

### 7.4 Missing Component Handling

Jika komponen tidak tersedia, AI MUST:

1. Mengidentifikasi missing component.
2. Memeriksa alternatif resmi.
3. Menjelaskan keterbatasan.
4. Mengusulkan solusi.
5. Menjelaskan dampak terhadap UI dan UX Flow.
6. Meminta Human Approval sebelum implementasi komponen baru.

---

## 8. Mandatory UX Flow Diagram & UI Screen Layout

### 8.1 Required Figma Structure

AI MUST menghasilkan dua area dalam satu section Figma.

**TOP — UX FLOW DIAGRAM**

Berisi approved Revision Core Flow dan decision branches.

**BOTTOM — UI SCREENS & STATES**

Berisi seluruh UI Screens dan applicable UI States.

AI MUST NOT memisahkan diagram dan screens ke section yang tidak memiliki hubungan dokumentasi yang jelas.

### 8.2 UX Flow Diagram Requirements

AI MUST merepresentasikan:

1. Start.
2. List Page.
3. View Detail.
4. Click Revisi.
5. Confirmation Modal.
6. Confirm Action.
7. Cancel Branch.
8. Success Feedback.
9. Back to Detail.
10. End.

Loading, Error, dan Validation States MUST dipetakan sebagai supplemental states jika relevan.

AI MUST NOT menambahkan supplemental states sebagai perubahan approved Core Flow tanpa Human Approval.

### 8.3 UI Screen Arrangement

AI MUST:

1. Mengurutkan screens sesuai Core Flow.
2. Menempatkan Confirmation Modal bersama source screen.
3. Menempatkan Cancel State pada konteks yang benar.
4. Menempatkan Loading State pada action terkait.
5. Menempatkan Success Feedback pada destination screen.
6. Menempatkan Error Feedback pada source screen yang sesuai.
7. Mengelompokkan Disabled dan Validation States.
8. Menjaga alignment dan spacing.
9. Menggunakan frame naming yang konsisten.
10. Menggunakan official GEMS layout.

### 8.4 Flow-to-Screen Mapping

| Flow Node | UI Representation |
|---|---|
| Start | Entry Annotation |
| List Page | List/Data Table |
| View Detail | Detail Page |
| Click Revisi | Revision Action |
| Confirmation Modal | Confirmation Screen/Overlay |
| Confirm | Processing State |
| Cancel | Return to Detail tanpa perubahan |
| Success Feedback | Success Toast |
| Back to Detail | Updated Detail Page |
| End | Final Flow State |

AI MUST memastikan setiap official flow node memiliki representasi UI atau annotation yang jelas.

AI MUST memastikan seluruh supplemental states memiliki source screen dan trigger.

---

## 9. Business Rules & Revision Permissions

### 9.1 Required Business Analysis

AI MUST mengidentifikasi:

1. Feature Name.
2. Record Type.
3. User Role.
4. Revision Permission.
5. Current Record Status.
6. Revision Eligibility.
7. Revision Prerequisites.
8. Revision Reason Requirements.
9. Confirmation Requirements.
10. Resulting Status.
11. Revision Recipient atau Responsible Role jika ditetapkan.
12. Success Behavior.
13. Error Behavior.
14. Navigation Destination.
15. Revision History Requirements jika berlaku.

### 9.2 Revision Eligibility

AI MUST menggunakan approved eligibility criteria.

AI MUST NOT menganggap semua record dapat diminta revisi.

Jika eligibility belum dijelaskan, AI MUST menandainya sebagai Pending Requirement.

### 9.3 Revision Reason Rules

AI MUST memeriksa apakah HSD/BRD menetapkan:

- Revision Reason wajib atau optional.
- Input atau Textarea.
- Predefined reason options.
- Character limits.
- Validation rules.
- Reason visibility.
- Reason persistence.
- Revision history.
- Role yang dapat melihat alasan revisi.

AI MUST NOT menambahkan mandatory revision reason tanpa dasar requirement.

### 9.4 Status Transition

AI MUST menggunakan status resmi HSD/BRD.

AI MUST memeriksa:

1. Status sebelum revision request.
2. Status setelah revision request.
3. Role yang bertanggung jawab menindaklanjuti.
4. Kondisi yang memungkinkan revision request berikutnya.
5. Kondisi penyelesaian revisi jika ditetapkan.

AI MUST NOT menganggap Revision Request otomatis menyelesaikan revisi data.

### 9.5 Permission Handling

AI MUST mengikuti Role Access Matrix.

AI MUST memeriksa role yang dapat:

- Meminta revisi.
- Melihat alasan revisi.
- Memperbaiki data.
- Mengirim ulang data.
- Melihat revision history.

AI MUST NOT memberikan akses hanya berdasarkan asumsi workflow.

---

## 10. Revision Reason & Validation Rules

### 10.1 Requirement Identification

AI MUST mengidentifikasi apakah Revision Reason:

1. Required.
2. Optional.
3. Not Applicable.
4. Pending Requirement.

### 10.2 Required Revision Reason

Jika HSD/BRD menetapkan Revision Reason wajib, AI MUST:

1. Menampilkan input menggunakan official GEMS component.
2. Menampilkan required indicator sesuai Design System.
3. Menggunakan approved field label.
4. Menggunakan approved helper text jika tersedia.
5. Menggunakan approved validation rules.
6. Menampilkan Validation Error ketika input tidak valid.
7. Mencegah submission yang tidak memenuhi validasi.
8. Menampilkan entered value sesuai approved interaction.

### 10.3 Optional Revision Reason

Jika optional, AI MUST:

1. Menampilkan field hanya jika requirement mendukungnya.
2. Tidak menggunakan mandatory indicator.
3. Mengikuti approved validation jika ada.
4. Tidak menghalangi submission hanya karena field kosong.

### 10.4 Reason Placement

AI MUST memeriksa apakah Revision Reason berada pada:

- Confirmation Modal.
- Separate Form.
- Detail Page.
- Other approved interaction.

AI MUST mengikuti HSD/BRD dan approved UX Pattern.

AI MUST NOT menambahkan separate form atau extra navigation tanpa Human Approval.

### 10.5 Revision History

AI MUST menambahkan revision history hanya jika requirement mendukungnya.

Jika tersedia, AI MUST mengikuti ketentuan mengenai:

- Revision requester.
- Revision date/time.
- Revision reason.
- Status changes.
- Revision responses.
- Visibility berdasarkan role.

AI MUST NOT mengarang audit trail atau revision history fields.

---

## 11. AI Recommendation & Human Approval

### 11.1 Recommendation Policy

AI MAY merekomendasikan:

1. UX improvement.
2. Alternative Revision Pattern.
3. Additional UI State.
4. Improved Confirmation wording.
5. Better Error Feedback.
6. Accessibility improvement.
7. Alternative component placement.
8. Additional validation.
9. Revision history presentation.
10. Better status visibility.

Rekomendasi MUST didasarkan pada kebutuhan bisnis, usability, accessibility, atau keterbatasan official pattern.

### 11.2 Recommendation Format

AI MUST menyampaikan:

| Field | Description |
|---|---|
| Current Pattern | Pattern resmi yang digunakan |
| Business Requirement | Requirement terkait |
| Identified Issue | Masalah atau gap |
| Proposed Improvement | Rekomendasi |
| Reason | Alasan |
| UX Flow Impact | Dampak terhadap flow |
| UI Impact | Dampak terhadap screens |
| State Impact | Dampak terhadap states |
| Component Impact | Dampak terhadap Design System |
| Approval Status | Status Human Approval |

### 11.3 Mandatory Human Approval

AI MUST memperoleh explicit Human Approval sebelum:

1. Mengubah Core Flow.
2. Mengubah entry point.
3. Mengubah navigation.
4. Menambahkan revision step.
5. Menghilangkan Confirmation Modal.
6. Mengubah Cancel behavior.
7. Mengubah revision reason requirements.
8. Mengubah revision eligibility.
9. Mengubah status transition.
10. Mengubah role permissions.
11. Menambahkan alternate workflow.
12. Membuat official component atau variant baru.
13. Mengubah approved error recovery.
14. Mengimplementasikan Proposed Design.

### 11.4 Approved vs Proposed Design

AI MUST memisahkan:

**Approved Design:** Mengikuti approved HSD/BRD, official UX Pattern, dan GEMS Design System.

**Proposed Design:** Rekomendasi yang membutuhkan Human Approval.

AI MUST NOT mencampurkan Proposed Design ke dalam approved implementation sebelum disetujui.

---

## 12. Required AI Design Output

AI MUST menghasilkan output berikut.

### 12.1 Pattern Selection Report

Berisi:

- Feature Name.
- Selected Pattern.
- Figma Reference.
- User Role.
- Entry Point.
- Selection Rationale.

### 12.2 UX Flow Diagram

Berisi approved Core Flow, Confirmation, Decision, Navigation, dan End State.

### 12.3 UI Screens

Berisi screens sesuai selected pattern dan approved requirements.

### 12.4 UI State Coverage Report

Berisi:

- Applicable States.
- Generated States.
- Not Applicable States.
- Pending Requirement States.
- Pending Human Approval States.
- Pending Verification States.

### 12.5 Flow-to-Screen Mapping

Berisi hubungan antara flow nodes, UI Screens, UI States, dan trigger.

### 12.6 Component Usage Report

Berisi:

- Official GEMS components.
- Component variants.
- Component states.
- Missing components.
- Pending component verification.

### 12.7 Business Compliance Report

Berisi:

- Revision Eligibility.
- Role Permission.
- Revision Reason Rules.
- Status Transition.
- Confirmation Behavior.
- Navigation Behavior.

### 12.8 Human Approval Register

Berisi proposed changes dan approval status.

### 12.9 Final Compliance Report

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

AI MUST mengikuti urutan berikut.

**Step 1 — Analyze HSD/BRD**

Identifikasi kebutuhan revision, role, eligibility, revision reason, status transition, dan expected behavior.

**Step 2 — Inspect Official Revision Patterns**

Periksa Pattern 01, Pattern 02, dan seluruh alternate references.

**Step 3 — Select Appropriate Pattern**

Pilih berdasarkan entry point, content hierarchy, component placement, dan business requirements.

**Step 4 — Verify Approved Core Flow**

Pastikan pattern mendukung kebutuhan tanpa perubahan yang belum disetujui.

**Step 5 — Inspect GEMS Design System**

Periksa official components, properties, variants, states, dan design tokens.

**Step 6 — Identify Applicable UI States**

Evaluasi Default, Hover, Focus, Active, Confirmation, Cancel, Loading, Success, Error, Disabled, Access Restricted, Validation Error, Empty, Not Found, dan Updated Status.

**Step 7 — Generate UX Flow Diagram**

Buat visual flow pada bagian atas section Figma.

**Step 8 — Generate UI Screens**

Buat screens sesuai selected Revision Pattern pada bagian bawah.

**Step 9 — Generate Applicable UI States**

Buat seluruh applicable states menggunakan official GEMS components.

**Step 10 — Validate Business Behavior**

Pastikan revision eligibility, reason requirements, status transition, dan role permission sesuai HSD/BRD.

**Step 11 — Validate Flow-to-Screen Mapping**

Pastikan diagram, screens, states, dan navigation saling terhubung.

**Step 12 — Identify Gaps**

Temukan requirement, component, flow, dan state gaps.

**Step 13 — Request Human Approval**

Ajukan proposed changes yang membutuhkan persetujuan.

**Step 14 — Inspect Actual Figma Output**

Periksa frames, components, variants, states, layout, dan flow yang benar-benar dibuat.

**Step 15 — Generate Compliance Report**

Laporkan hasil verifikasi, unresolved issues, dan approval status.

---

## 14. AI Restrictions

AI MUST NOT:

1. Mengubah approved Core Flow tanpa Human Approval.
2. Menggunakan pattern di luar GEMS tanpa approval.
3. Mengganti GEMS components dengan custom components tanpa approval.
4. Mengarang revision rules.
5. Mengarang revision eligibility.
6. Mengarang status transitions.
7. Mengarang role permissions.
8. Menghilangkan Confirmation Modal.
9. Memproses revision request sebelum confirmation.
10. Menampilkan Success sebelum proses berhasil.
11. Menggunakan Approve, Reject, atau Delete wording untuk Revision Action.
12. Mengubah Cancel behavior.
13. Mengubah navigation destination.
14. Mengarang mandatory revision reason.
15. Mengarang validation constraints.
16. Mengarang revision history fields.
17. Mengarang retry atau rollback behavior.
18. Menggunakan Disabled State tanpa dasar business rules.
19. Mengubah component variants secara sepihak.
20. Menghasilkan screens tanpa UX Flow Diagram.
21. Menghasilkan diagram yang bertentangan dengan screens.
22. Menghilangkan applicable UI States.
23. Mengimplementasikan Proposed Design tanpa approval.
24. Mengklaim custom component sebagai official GEMS instance.
25. Mengklaim desain compliant tanpa actual Figma verification.
26. Menganggap Pending Requirement sebagai approved behavior.
27. Menganggap Revision Request otomatis berarti data sudah diperbaiki.
28. Menganggap semua role dapat mengedit record setelah revision request.
29. Menambahkan Bulk Revision tanpa official pattern atau approval.
30. Menambahkan workflow lanjutan tanpa approved HSD/BRD.

---

## 15. Quality Assurance & Final Validation

### 15.1 Business Validation

AI MUST memastikan revision rules, role access, eligibility, reason requirements, dan status transitions sesuai approved HSD/BRD.

### 15.2 Pattern Validation

AI MUST memastikan selected pattern sesuai kebutuhan dan menggunakan official Figma reference.

### 15.3 Core Flow Validation

AI MUST memastikan Start, List Page, View Detail, Click Revisi, Confirmation Modal, Success Feedback, Back to Detail, dan End sesuai official pattern.

AI MUST memeriksa exact confirmation decision labels sebelum finalisasi.

### 15.4 Component Validation

AI MUST memastikan seluruh komponen menggunakan official GEMS Design System.

### 15.5 State Validation

AI MUST memastikan seluruh applicable states telah dihasilkan atau dilaporkan alasan belum dapat diimplementasikan.

### 15.6 Human Approval Validation

AI MUST memastikan tidak ada proposed change yang diimplementasikan tanpa explicit Human Approval.

### 15.7 Final Validation Instructions

Sebelum melaporkan completion, AI MUST:

1. Verify approved HSD/BRD.
2. Verify Role Access Matrix.
3. Verify selected official Revision Pattern.
4. Verify Core Flow integrity.
5. Verify entry point and navigation.
6. Verify Revision Action wording.
7. Verify Confirmation Modal.
8. Verify Confirm and Cancel behavior.
9. Verify applicable Loading States.
10. Verify Success Feedback.
11. Verify Error Feedback.
12. Verify Disabled and Access Restricted States.
13. Verify revision reason validation jika berlaku.
14. Verify status transitions.
15. Verify role permissions.
16. Verify official GEMS component usage.
17. Verify component variants dan states.
18. Verify Flow-to-Screen Mapping.
19. Verify UX Flow Diagram placement above UI Screens.
20. Verify applicable state coverage.
21. Verify Human Approval for changes.
22. Verify unresolved requirements are reported.
23. Inspect actual Figma output.
24. Generate final Compliance Report.

AI MUST NOT menandai item yang belum diverifikasi sebagai compliant.

Jika terdapat requirement yang belum dapat dipastikan, AI MUST melaporkan Pending Requirement atau Pending Validation.

---

## 16. Final AI Enforcement

AI MUST:

1. Analyze approved HSD/BRD.
2. Use official GEMS Revision UX Patterns.
3. Preserve approved Core Flow.
4. Use GEMS Design System components.
5. Generate visual UX Flow Diagram.
6. Generate corresponding UI Screens.
7. Generate all applicable UI States.
8. Apply revision eligibility rules.
9. Respect Role Access Matrix.
10. Use Confirmation before processing revision request.
11. Handle Cancel, Loading, Success, Error, dan Disabled behavior.
12. Apply revision reason requirements jika berlaku.
13. Maintain Flow-to-Screen consistency.
14. Identify requirement and component gaps.
15. Recommend improvements when appropriate.
16. Obtain explicit Human Approval for changes.
17. Validate actual Figma output.
18. Generate a Compliance Report.

### Final Enforcement Rule

AI MUST menggunakan approved HSD/BRD sebagai sumber business requirements, official GEMS Revision UX Patterns sebagai sumber approved Core Flow, dan GEMS Design System sebagai sumber UI components, variants, dan states.

AI MUST menghasilkan visual UX Flow Diagram di atas UI Screens yang sesuai serta merepresentasikan seluruh applicable UI States tanpa memperkenalkan unapproved business behavior.

AI MAY merekomendasikan UX improvements, additional states, alternative interactions, atau component enhancements jika didukung kebutuhan bisnis dan pertimbangan usability.

AI MUST memperoleh explicit Human Approval sebelum mengimplementasikan rekomendasi yang mengubah approved Core Flow, navigation, business behavior, permissions, atau GEMS Design System.

AI MUST memvalidasi hasil aktual di Figma sebelum menyatakan desain selesai atau compliant.

**HSD/BRD defines business requirements. GEMS UX Pattern defines the approved Core Flow. GEMS Design System defines components and visual states. Human Approval authorizes changes.**
