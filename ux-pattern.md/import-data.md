# GEMS AI Design Guidelines — Import Data UX Pattern

## 1. Purpose & Scope

AI MUST menghasilkan desain UI/UX **Import Data** berdasarkan approved HSD/BRD, official GEMS UX Pattern, GEMS Design System, dan Role Access Matrix.

AI MUST:

1. Menganalisis HSD/BRD untuk mengidentifikasi import requirements, supported file formats, data structure, validation rules, duplicate handling, dan user permissions.
2. Memeriksa official Import Data UX Pattern melalui Figma MCP.
3. Mengikuti approved Core Flow, termasuk upload, preview, validation, confirmation, processing, success, error, dan cancel branches.
4. Menggunakan official GEMS components, variants, states, dan design tokens.
5. Menghasilkan **visual UX Flow Diagram di bagian atas** dan **UI Screens beserta applicable UI States di bagian bawah** dalam satu Figma section.
6. Menghasilkan seluruh screens yang dibutuhkan untuk merepresentasikan proses Import Data.
7. Menghasilkan applicable states untuk setiap screen dan komponen.
8. Memastikan uploaded data divalidasi sebelum import diproses.
9. Memastikan duplicate handling mengikuti approved HSD/BRD.
10. Memastikan Cancel dan Close behavior mengikuti official UX Pattern.
11. Menampilkan processing feedback, success feedback, dan contextual error messages.
12. Memvalidasi updated data pada List/Table setelah import berhasil.
13. Meminta explicit Human Approval sebelum mengubah approved Core Flow, business rules, navigation, atau Design System.
14. Memeriksa hasil aktual di Figma sebelum menyatakan desain selesai.

AI MUST NOT:

1. Mengarang supported file formats, file size limits, templates, validation rules, atau duplicate handling.
2. Mengubah approved Core Flow tanpa Human Approval.
3. Menganggap semua uploaded files otomatis valid.
4. Menganggap semua duplicate records harus ditimpa atau dilewati.
5. Menghilangkan Preview Data atau Confirmation Import dari approved flow.
6. Memproses import sebelum validasi dan confirmation terpenuhi.
7. Menghasilkan hanya happy path tanpa error dan cancel branches.
8. Mengklaim import berhasil sebelum sistem mengonfirmasi keberhasilan.

---

## 2. Source of Truth & Design Governance

### 2.1 Source Hierarchy

AI MUST menggunakan sumber berikut sesuai kewenangannya.

| Source | Responsibility |
|---|---|
| Approved HSD/BRD | Import rules, file requirements, validation, duplicate handling, permissions |
| GEMS UX Pattern | Approved Core Flow, navigation, decisions, cancel behavior |
| GEMS Design System | Official components, variants, states, visual tokens |
| Role Access Matrix | Import permissions dan data access |
| Human Approval | Authorization untuk perubahan approved design |

### 2.2 Core Flow Governance

AI MUST:

1. Memeriksa seluruh flow nodes pada official Import Data Pattern.
2. Memeriksa arah connectors.
3. Memeriksa decision branches.
4. Memeriksa error paths.
5. Memeriksa cancel dan close paths.
6. Mempertahankan approved interaction sequence.
7. Memetakan seluruh flow nodes ke UI Screens atau annotations.
8. Menandai behavior yang belum dapat dipastikan sebagai Pending Verification.

AI MUST NOT mengubah approved flow berdasarkan asumsi.

### 2.3 Conflict Handling

Jika terdapat konflik antara HSD/BRD, UX Pattern, dan Design System, AI MUST:

1. Mengidentifikasi konflik.
2. Menjelaskan sumber yang berbeda.
3. Menjelaskan dampak terhadap flow, screens, dan states.
4. Memberikan rekomendasi jika diperlukan.
5. Meminta Human Review sebelum mengimplementasikan perubahan.

### 2.4 Design System Governance

**Official GEMS Design System:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System

AI MUST menggunakan official components, typography, colors, spacing, icons, layout, dan interaction variants.

AI MUST NOT mengganti official components dengan custom components tanpa approval.

---

## 3. Official Import Data UX Pattern References

**Parent Reference — Import Data:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1284-6558

**Pattern 01 — Import Data:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3414-107595

AI MUST menggunakan Pattern 01 sebagai official reference untuk Import Data.

### 3.1 Verified Flow Coverage

AI MUST memeriksa nodes berikut:

1. Start.
2. Table/List.
3. Klik Impor Data.
4. Upload File.
5. File Valid?
6. Preview Data.
7. Sudah Ada Data?
8. Validasi Data.
9. Data Valid?
10. Klik Impor.
11. Konfirmasi Impor.
12. Sistem Memproses Impor Data.
13. Berhasil?
14. List/Data Updated.
15. Success Toast.
16. Error Message.
17. Error — Coba Lagi.
18. Klik Icon Close / Tombol Batal.
19. Popup Konfirmasi Batal.
20. Tetap di Form.
21. End.

AI MUST memverifikasi urutan dan hubungan antar-node berdasarkan connectors aktual di Figma.

AI MUST NOT menganggap urutan daftar node di atas sebagai pengganti verifikasi visual Core Flow.

---

## 4. Pattern 01 — Import Data from List/Table

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3414-107595

### 4.1 When to Use

AI MUST menggunakan Pattern 01 ketika approved requirements menetapkan proses import data melalui List/Table menggunakan uploaded file.

AI MUST memvalidasi:

1. Import entry point.
2. User role.
3. Import permission.
4. Supported file format.
5. File validation.
6. Data preview.
7. Duplicate detection.
8. Data validation.
9. Confirmation behavior.
10. Import processing.
11. Success dan error behavior.

### 4.2 Core Flow — Main Path

AI MUST merepresentasikan alur utama berikut berdasarkan official Figma reference:

**Start → Table/List → Klik Impor Data → Upload File → File Valid? → Preview Data → Validasi Data → Data Valid? → Klik Impor → Konfirmasi Impor → Sistem Memproses Impor Data → Berhasil? → List/Data Updated → Success Toast → End.**

AI MUST memeriksa posisi decision **Sudah Ada Data?** dan seluruh connectors sebelum finalisasi diagram.

AI MUST mempertahankan duplicate-handling branch sesuai reference dan HSD/BRD.

### 4.3 Core Flow — File Validation

AI MUST merepresentasikan decision **File Valid?**

**Valid:** Lanjutkan ke Preview Data sesuai approved flow.

**Invalid:** Tampilkan Error Message sesuai kondisi.

AI MUST menggunakan approved recovery behavior.

AI MUST NOT mengarang automatic file correction atau automatic conversion.

### 4.4 Core Flow — Existing Data Detection

AI MUST merepresentasikan decision **Sudah Ada Data?** sesuai official reference.

AI MUST memeriksa apakah existing data memengaruhi:

1. Duplicate detection.
2. Record matching.
3. Validation.
4. Import eligibility.
5. User confirmation.
6. Processing behavior.

AI MUST mengikuti approved HSD/BRD untuk menentukan tindakan terhadap existing records.

AI MUST NOT otomatis menerapkan Replace, Skip, Merge, atau Update.

### 4.5 Core Flow — Data Validation

AI MUST merepresentasikan decision **Data Valid?**

**Valid:** Pengguna dapat melanjutkan ke Import Action sesuai approved flow.

**Invalid:** Tampilkan validation feedback dan ikuti approved correction behavior.

AI MUST NOT mengizinkan invalid data diproses jika HSD/BRD melarangnya.

### 4.6 Core Flow — Import Confirmation

AI MUST:

1. Menampilkan Confirmation Import sesuai reference.
2. Menggunakan official GEMS Confirmation component.
3. Menggunakan approved wording.
4. Menyediakan confirmation dan cancel behavior sesuai pattern.
5. Tidak memproses import sebelum pengguna melakukan confirmation.

### 4.7 Core Flow — Processing & Result

AI MUST merepresentasikan decision **Berhasil?**

**Success:** List/Data Updated → Success Toast → End.

**Failure:** Tampilkan Error Feedback sesuai kondisi dan approved recovery behavior.

AI MUST NOT menampilkan Success Toast sebelum import berhasil.

### 4.8 Core Flow — Cancel & Close

AI MUST merepresentasikan:

**Klik Icon Close / Tombol Batal → Popup Konfirmasi Batal → Decision sesuai official reference.**

AI MUST mempertahankan branch **Tetap di Form (Step Terakhir Sebelum Klik Close/Batal)**.

AI MUST memastikan pengguna yang memilih tetap melanjutkan tidak kehilangan konteks form sesuai approved behavior.

AI MUST memverifikasi exit branch pada official diagram.

AI MUST NOT menganggap Close dan Cancel langsung menutup form tanpa confirmation.

---

## 5. Required UI Screens

AI MUST menghasilkan screens berikut sesuai approved pattern.

### 5.1 List/Table Screen

AI MUST:

1. Menggunakan official GEMS Table.
2. Menampilkan Import Data Action.
3. Mengikuti approved action placement.
4. Menampilkan data sesuai role permission.
5. Menampilkan updated records setelah import berhasil.

### 5.2 Upload File Screen

AI MUST:

1. Menggunakan official GEMS upload component jika tersedia.
2. Menampilkan file selection control.
3. Menampilkan selected file information.
4. Menggunakan approved helper text.
5. Menampilkan supported format information jika ditetapkan.
6. Menampilkan validation feedback.

### 5.3 Preview Data Screen

AI MUST:

1. Menampilkan uploaded data sebelum import.
2. Menggunakan approved preview layout.
3. Mempertahankan data hierarchy.
4. Menampilkan validation information sesuai requirements.
5. Menggunakan official GEMS Table atau preview component.
6. Menampilkan Import Action sesuai approved flow.

### 5.4 Data Validation Screen

AI MUST:

1. Menampilkan validation result.
2. Membedakan valid dan invalid data.
3. Menampilkan contextual error information.
4. Menggunakan approved status presentation.
5. Mengikuti approved correction behavior.

### 5.5 Confirmation Import Screen

AI MUST:

1. Menggunakan official Confirmation Modal.
2. Menampilkan approved confirmation title.
3. Menampilkan approved supporting text.
4. Menggunakan official action buttons.
5. Mengikuti approved button hierarchy.
6. Menyediakan cancel behavior.

### 5.6 Import Processing Screen

AI MUST:

1. Menggunakan official Loading Indicator.
2. Menampilkan processing feedback.
3. Mempertahankan relevant import context.
4. Mengikuti approved duplicate-submission behavior.
5. Tidak menampilkan false success.

### 5.7 Success Screen

AI MUST:

1. Menampilkan updated List/Data.
2. Menggunakan official Success Toast.
3. Menggunakan approved success wording.
4. Memastikan data yang ditampilkan sesuai hasil import.

### 5.8 Error Screen

AI MUST:

1. Menampilkan Error Feedback sesuai kondisi.
2. Menggunakan official GEMS error components.
3. Mengikuti approved retry atau correction behavior.
4. Tidak menghapus user input tanpa approved requirement.

### 5.9 Cancel Confirmation Screen

AI MUST:

1. Menggunakan official GEMS Confirmation Modal.
2. Menampilkan approved cancel wording.
3. Menyediakan decision untuk membatalkan atau tetap melanjutkan.
4. Mempertahankan form context ketika pengguna memilih tetap melanjutkan.

---

## 6. Mandatory UI State Generation

### 6.1 State Generation Principles

AI MUST:

1. Mengevaluasi seluruh applicable UI States.
2. Menggunakan official GEMS component variants.
3. Menentukan source screen setiap state.
4. Menentukan trigger.
5. Menentukan expected behavior.
6. Menentukan resulting state.
7. Memetakan states ke UX Flow.
8. Menghasilkan error dan cancel branches.
9. Melaporkan unresolved states.

AI MUST NOT menghasilkan hanya Default, Loading, dan Success.

### 6.2 Mandatory UI State Matrix

| State | Trigger | Expected UI Output | Applicability |
|---|---|---|---|
| Default | Screen dibuka | Normal UI | All |
| Hover | Pointer pada control | Hover Variant | Applicable controls |
| Focus | Keyboard focus | Focus Indicator | Applicable controls |
| Active | Action aktif | Active Variant | If supported |
| Empty Upload | Belum memilih file | Empty Upload State | Upload |
| File Selected | File dipilih | Selected File State | Upload |
| Uploading | File sedang diunggah | Upload Progress | If applicable |
| File Valid | File lolos validasi | Continue to Preview | Upload |
| File Invalid | File gagal validasi | Error Feedback | Upload |
| Preview Loading | Preview disiapkan | Loading Indicator | If applicable |
| Preview Ready | Preview tersedia | Preview Data | Preview |
| Existing Data | Data sudah tersedia | Duplicate-related State | Based on rules |
| No Existing Data | Data belum tersedia | Continue Flow | Based on rules |
| Data Valid | Data lolos validasi | Import Ready | Validation |
| Data Invalid | Data gagal validasi | Validation Error | Validation |
| Confirmation Open | Klik Impor | Confirmation Modal | Import |
| Confirmation Cancel | Pengguna batal konfirmasi | Return to approved state | Import |
| Processing | Import diproses | Loading Feedback | Import |
| Success | Import berhasil | Updated List + Toast | Import |
| Processing Error | Import gagal | Error Feedback | Import |
| Cancel Popup | Klik Close/Batal | Confirmation Modal | Cancel |
| Stay in Form | Pilih tetap melanjutkan | Previous Form Step | Cancel |
| Exit Form | Konfirmasi keluar | Exit Behavior | Based on reference |
| Disabled | Action tidak tersedia | Disabled Variant | Based on rules |
| Access Restricted | Role tidak berwenang | Permission State | Role-dependent |
| Network Error | Gangguan koneksi | Error Feedback | If applicable |
| Server Error | Gangguan sistem | Error Feedback | If applicable |

### 6.3 Default State

AI MUST menggunakan screen normal sesuai official reference.

AI MUST menampilkan available actions berdasarkan role permissions.

### 6.4 Hover, Focus & Active States

AI MUST menggunakan official GEMS variants.

AI MUST mempertahankan focus visibility dan accessibility behavior.

AI MUST NOT membuat variants baru tanpa approval.

### 6.5 Empty Upload State

AI MUST:

1. Menampilkan upload control.
2. Menggunakan approved placeholder atau helper text.
3. Menampilkan Import Action sesuai approved availability rules.
4. Tidak menampilkan selected file information sebelum file dipilih.

### 6.6 File Selected State

AI MUST:

1. Menampilkan selected filename jika didukung.
2. Menampilkan file information sesuai requirements.
3. Menggunakan official selected state.
4. Menampilkan available actions sesuai reference.

### 6.7 Uploading State

Jika upload progress tersedia, AI MUST:

1. Menggunakan official progress component.
2. Menampilkan upload status.
3. Mengikuti approved cancel behavior.
4. Tidak menampilkan Preview Ready sebelum data siap.

AI MUST NOT mengarang progress percentage atau upload duration.

### 6.8 File Valid State

AI MUST:

1. Memvalidasi file berdasarkan HSD/BRD.
2. Menampilkan approved success atau ready feedback.
3. Melanjutkan ke Preview sesuai Core Flow.
4. Mempertahankan uploaded file context.

### 6.9 File Invalid State

AI MUST:

1. Menampilkan contextual Error Feedback.
2. Menggunakan approved validation messages.
3. Mengikuti approved correction behavior.
4. Tidak melanjutkan ke import processing jika file tidak memenuhi requirement.

AI MUST NOT mengarang supported formats atau file size limits.

### 6.10 Preview Loading State

AI MUST menampilkan loading feedback jika preview sedang disiapkan.

AI MUST NOT menampilkan data preview yang belum tersedia sebagai hasil final.

### 6.11 Preview Ready State

AI MUST:

1. Menampilkan uploaded data.
2. Menggunakan approved table structure.
3. Menampilkan relevant validation information.
4. Mengikuti approved data formatting.
5. Mempertahankan Import Action sesuai reference.

### 6.12 Existing Data State

AI MUST:

1. Mengikuti decision **Sudah Ada Data?**
2. Menggunakan approved duplicate detection rules.
3. Menampilkan feedback sesuai HSD/BRD.
4. Mempertahankan data integrity.
5. Mengikuti approved next action.

AI MUST NOT mengarang Replace, Skip, Merge, atau Update behavior.

### 6.13 Data Valid State

AI MUST:

1. Menampilkan valid data status sesuai reference.
2. Mengizinkan Import Action sesuai approved rules.
3. Memastikan data memenuhi validation requirements.

### 6.14 Data Invalid State

AI MUST:

1. Menampilkan validation errors.
2. Mengidentifikasi invalid data sesuai approved presentation.
3. Menggunakan official error components.
4. Mengikuti approved correction behavior.
5. Tidak mengarang partial import rules.

### 6.15 Confirmation Open State

AI MUST:

1. Menggunakan official Confirmation Modal.
2. Menampilkan approved wording.
3. Menampilkan confirmation dan cancel actions.
4. Memastikan import belum diproses sebelum confirmation.

### 6.16 Confirmation Cancel State

AI MUST:

1. Mengikuti approved cancel behavior.
2. Tidak memproses import.
3. Mempertahankan form context sesuai reference.
4. Tidak menampilkan Success Toast.

### 6.17 Processing State

AI MUST:

1. Menggunakan official Loading Indicator.
2. Menampilkan processing feedback.
3. Mengikuti approved duplicate-submission behavior.
4. Menangani processing failure.
5. Tidak menampilkan Success sebelum proses berhasil.

### 6.18 Success State

AI MUST:

1. Menampilkan updated List/Data.
2. Menampilkan official Success Toast.
3. Menggunakan approved success wording.
4. Memastikan imported records sesuai hasil sistem.
5. Tidak mengklaim semua rows berhasil jika sistem hanya mengonfirmasi partial success.

### 6.19 Processing Error State

AI MUST:

1. Menggunakan official Error Feedback.
2. Menampilkan error sesuai kondisi.
3. Mengikuti approved retry behavior jika tersedia.
4. Mempertahankan relevant import context.
5. Tidak menampilkan false success.

### 6.20 Cancel Popup State

AI MUST:

1. Menampilkan Confirmation Popup ketika pengguna memilih Close/Batal sesuai reference.
2. Menggunakan official GEMS Modal.
3. Menampilkan approved cancel wording.
4. Menyediakan decision branches sesuai reference.

### 6.21 Stay in Form State

AI MUST:

1. Mengembalikan pengguna ke step terakhir sebelum Close/Batal.
2. Mempertahankan entered data sesuai approved behavior.
3. Tidak memproses import.
4. Tidak menghapus uploaded file tanpa approved requirement.

### 6.22 Exit Form State

AI MUST mengikuti approved exit behavior.

AI MUST memverifikasi apakah exit menghapus draft, mempertahankan draft, atau kembali ke List Page.

AI MUST NOT mengarang draft persistence.

### 6.23 Disabled State

AI MUST memeriksa kondisi ketika Import Action tidak tersedia.

AI MUST mengevaluasi:

1. File belum dipilih.
2. File tidak valid.
3. Data tidak valid.
4. Required input belum lengkap.
5. Import sedang diproses.
6. Role tidak memiliki permission.

AI MUST memvalidasi seluruh kondisi terhadap HSD/BRD.

### 6.24 Access Restricted State

AI MUST mengikuti Role Access Matrix.

AI MUST NOT menganggap View Permission otomatis memberikan Import Permission.

### 6.25 State Coverage Reporting

AI MUST mengklasifikasikan setiap state sebagai:

- Generated.
- Not Applicable.
- Pending Requirement.
- Pending Human Approval.
- Pending Verification.

AI MUST NOT menandai unresolved state sebagai Generated.

---

## 7. Mandatory File & Data Validation Rules

### 7.1 File Validation

AI MUST memeriksa HSD/BRD untuk:

1. Supported file formats.
2. File size limits.
3. File naming rules.
4. File structure.
5. Required columns.
6. Required sheets.
7. Header format.
8. Data types.
9. Encoding requirements.
10. Template requirements.

AI MUST NOT mengarang validation constraints.

### 7.2 Data Validation

AI MUST memeriksa:

1. Required fields.
2. Field data types.
3. Field formats.
4. Value ranges.
5. Duplicate rules.
6. Reference data matching.
7. Cross-field dependencies.
8. Date validation.
9. Unique identifiers.
10. Record eligibility.

AI MUST NOT mengarang validation logic.

### 7.3 Duplicate Data Handling

AI MUST:

1. Mengidentifikasi duplicate detection criteria.
2. Mengikuti approved duplicate handling.
3. Menampilkan feedback sesuai requirements.
4. Memastikan duplicate handling tidak mengubah data secara tidak sah.

AI MUST NOT otomatis melakukan Replace, Merge, Skip, atau Update.

### 7.4 Partial Import Rules

AI MUST memeriksa apakah HSD/BRD mengizinkan:

1. All-or-Nothing Import.
2. Partial Import.
3. Skip Invalid Rows.
4. Import Valid Rows Only.
5. Retry Failed Rows.

AI MUST NOT mengimplementasikan partial import tanpa approved requirement.

### 7.5 Validation Feedback

AI MUST menggunakan approved feedback untuk:

- Invalid file.
- Missing required column.
- Invalid data format.
- Duplicate data.
- Missing required field.
- Import processing failure.

AI MUST NOT mengarang exact error messages jika wording telah ditetapkan.

---

## 8. Mandatory GEMS Component Usage

### 8.1 Component Requirements

AI MUST memeriksa official GEMS components yang relevan:

1. Page Header.
2. Navbar.
3. GEMS Slide Bar.
4. Table.
5. Pagination.
6. Button.
7. Button Group.
8. File Upload.
9. File Input.
10. Modal.
11. Confirmation Modal.
12. Notification / Toast.
13. Alert.
14. Empty State.
15. Loading Indicator.
16. Progress Indicator jika tersedia.
17. Tooltip.
18. Status Badge.
19. Detail Information.
20. Button Close X.
21. Section Footer jika sesuai reference.

AI MUST menggunakan hanya komponen yang relevan dengan official pattern.

### 8.2 Component Retrieval

AI MUST:

1. Memeriksa official Figma component.
2. Mengidentifikasi component name.
3. Memeriksa properties.
4. Memeriksa variants.
5. Memeriksa supported states.
6. Memeriksa component anatomy.
7. Memeriksa typography.
8. Memeriksa colors.
9. Memeriksa spacing.
10. Memeriksa layout.
11. Menggunakan official instances jika tersedia.
12. Memverifikasi instances pada hasil desain.

### 8.3 Component Integrity

AI MUST NOT:

1. Mengganti official GEMS components tanpa approval.
2. Membuat custom Upload Component tanpa approval.
3. Membuat custom Modal tanpa approval.
4. Mengarang component variants.
5. Mengubah component anatomy.
6. Mengubah button hierarchy.
7. Mengubah validation presentation secara sepihak.
8. Mengklaim custom UI sebagai official GEMS component.

### 8.4 Missing Component Handling

Jika komponen tidak tersedia, AI MUST:

1. Mengidentifikasi missing component.
2. Memeriksa official alternatives.
3. Menjelaskan limitation.
4. Mengusulkan solusi.
5. Menjelaskan dampak terhadap flow dan screens.
6. Meminta Human Approval sebelum implementasi komponen baru.

---

## 9. Mandatory UX Flow Diagram & UI Screen Layout

### 9.1 Required Figma Structure

AI MUST menghasilkan dua area dalam satu Figma section.

**TOP — UX FLOW DIAGRAM**

AI MUST menampilkan approved Import Data Core Flow, decision branches, validation, processing, success, error, dan cancel paths.

**BOTTOM — UI SCREENS & STATES**

AI MUST menampilkan seluruh UI Screens dan applicable UI States.

### 9.2 UX Flow Diagram Requirements

AI MUST merepresentasikan:

1. Start.
2. Table/List.
3. Klik Impor Data.
4. Upload File.
5. File Valid?
6. Preview Data.
7. Sudah Ada Data?
8. Validasi Data.
9. Data Valid?
10. Klik Impor.
11. Konfirmasi Impor.
12. Sistem Memproses Impor Data.
13. Berhasil?
14. List/Data Updated.
15. Success Toast.
16. Error Message.
17. Retry/Error Recovery jika didukung.
18. Close/Cancel Action.
19. Cancel Confirmation.
20. Stay in Form.
21. Exit Behavior.
22. End.

AI MUST memverifikasi actual connectors dan decision branches melalui Figma MCP.

### 9.3 UI Screen Arrangement

AI MUST:

1. Mengurutkan screens sesuai Core Flow.
2. Menempatkan Upload State bersama Upload Screen.
3. Menempatkan Preview State setelah Upload.
4. Menempatkan Validation States bersama Preview/Data Validation.
5. Menempatkan Confirmation Modal bersama Import Action.
6. Menempatkan Processing State setelah confirmation.
7. Menempatkan Success Feedback pada updated List.
8. Menempatkan Error Feedback pada source context.
9. Menempatkan Cancel Popup bersama form terkait.
10. Mengelompokkan applicable component states.
11. Menggunakan consistent frame naming.
12. Menjaga alignment dan spacing.

### 9.4 Flow-to-Screen Mapping

| Flow Node | UI Representation |
|---|---|
| Start | Entry Annotation |
| Table/List | List Screen |
| Klik Impor Data | Import Action |
| Upload File | Upload Screen |
| File Valid? | Valid / Invalid File States |
| Preview Data | Preview Screen |
| Sudah Ada Data? | Duplicate-related State |
| Validasi Data | Validation Screen |
| Data Valid? | Valid / Invalid Data States |
| Klik Impor | Import Action |
| Konfirmasi Impor | Confirmation Modal |
| Processing | Loading State |
| Berhasil? | Success / Error Branch |
| List/Data Updated | Updated List Screen |
| Success Toast | Success Notification |
| Close/Batal | Cancel Action |
| Popup Konfirmasi Batal | Cancel Confirmation Modal |
| Tetap di Form | Previous Form Step |
| End | Final Flow State |

AI MUST memastikan seluruh official flow nodes memiliki UI representation atau annotation yang jelas.

---

## 10. Business Rules & Import Permissions

### 10.1 Required Business Analysis

AI MUST mengidentifikasi:

1. Feature Name.
2. Module Name.
3. User Role.
4. Import Permission.
5. Data Access Permission.
6. Supported File Formats.
7. File Template.
8. File Validation Rules.
9. Data Validation Rules.
10. Duplicate Detection Rules.
11. Duplicate Handling Rules.
12. Import Eligibility.
13. Import Limits.
14. Confirmation Requirements.
15. Success Criteria.
16. Error Criteria.
17. Cancel Behavior.
18. Navigation Destination.

### 10.2 Import Eligibility

AI MUST menggunakan approved eligibility criteria.

AI MUST NOT menganggap semua records atau file dapat diimpor.

### 10.3 Import Permissions

AI MUST mengikuti Role Access Matrix.

AI MUST memeriksa apakah pengguna memiliki:

1. View Permission.
2. Import Permission.
3. Create Permission jika relevan.
4. Update Permission jika import dapat mengubah existing records.
5. Module Access.
6. Data Scope Permission.

AI MUST NOT menganggap Import Permission otomatis mengizinkan overwrite existing records.

### 10.4 Import Limits

AI MUST memeriksa apakah terdapat:

1. Maximum file size.
2. Maximum rows.
3. Maximum columns.
4. Maximum import frequency.
5. Maximum processing time.
6. Batch limits.

AI MUST NOT mengarang batasan tersebut.

### 10.5 Data Integrity

AI MUST:

1. Mengikuti approved data validation.
2. Mengikuti approved duplicate handling.
3. Memastikan imported data sesuai permissions.
4. Tidak mengubah existing records tanpa approved behavior.
5. Tidak menampilkan success untuk proses yang gagal.

---

## 11. Cancel, Confirmation & Error Recovery Rules

### 11.1 Import Confirmation

AI MUST:

1. Menggunakan official GEMS Confirmation Modal.
2. Menggunakan approved title.
3. Menggunakan approved description.
4. Menggunakan approved button labels.
5. Memastikan Confirm dan Cancel mengikuti official flow.
6. Tidak memproses import sebelum confirmation.

### 11.2 Cancel Confirmation

AI MUST:

1. Menampilkan Popup Konfirmasi Batal sesuai reference.
2. Menggunakan official GEMS Modal.
3. Mempertahankan previous form step ketika pengguna memilih tetap melanjutkan.
4. Mengikuti approved exit behavior ketika pengguna mengonfirmasi pembatalan.

### 11.3 Error Recovery

AI MUST membedakan:

1. File Validation Error.
2. Data Validation Error.
3. Duplicate-related Error.
4. Import Processing Error.
5. Network Error.
6. Server Error.

AI MUST menggunakan approved recovery behavior.

AI MUST NOT mengarang automatic retry atau rollback.

### 11.4 Data Preservation

AI MUST memeriksa apakah approved requirements menetapkan:

1. Uploaded file persistence.
2. Preview data persistence.
3. Form state preservation.
4. Draft preservation.
5. Reset behavior setelah error.
6. Reset behavior setelah cancel.

AI MUST NOT mengarang persistence behavior.

---

## 12. AI Recommendation & Human Approval

### 12.1 Recommendation Policy

AI MAY merekomendasikan:

1. Improved Upload Experience.
2. Better Validation Feedback.
3. Better Duplicate Handling Visibility.
4. Improved Preview Layout.
5. Better Error Recovery.
6. Accessibility Improvement.
7. Improved Cancel Confirmation.
8. Additional UI States.
9. Better Import Progress Feedback.
10. Improved Success Summary.

AI MUST mendasarkan rekomendasi pada business requirements, usability, accessibility, atau limitation official pattern.

### 12.2 Recommendation Format

AI MUST menyampaikan:

| Field | Description |
|---|---|
| Current Pattern | Pattern resmi |
| Business Requirement | Requirement terkait |
| Identified Issue | Masalah atau gap |
| Proposed Improvement | Rekomendasi |
| Reason | Alasan |
| UX Flow Impact | Dampak flow |
| UI Impact | Dampak screens |
| State Impact | Dampak states |
| Component Impact | Dampak Design System |
| Approval Status | Human Approval status |

### 12.3 Mandatory Human Approval

AI MUST memperoleh explicit Human Approval sebelum:

1. Mengubah Core Flow.
2. Mengubah entry point.
3. Mengubah navigation.
4. Menghilangkan Preview Data.
5. Menghilangkan Validation Step.
6. Mengubah duplicate handling.
7. Mengubah import eligibility.
8. Mengubah file validation.
9. Mengubah data validation.
10. Mengubah confirmation behavior.
11. Mengubah cancel behavior.
12. Mengubah error recovery.
13. Mengubah role permissions.
14. Mengimplementasikan partial import.
15. Membuat official component atau variant baru.
16. Mengimplementasikan Proposed Design.

### 12.4 Approved vs Proposed Design

AI MUST memisahkan:

**Approved Design:** Mengikuti approved HSD/BRD, official UX Pattern, dan GEMS Design System.

**Proposed Design:** Rekomendasi yang membutuhkan Human Approval.

AI MUST NOT mengimplementasikan Proposed Design sebelum disetujui.

---

## 13. Required AI Design Output

AI MUST menghasilkan:

### 13.1 Pattern Selection Report

- Feature Name.
- Selected Pattern.
- Figma Reference.
- User Role.
- Entry Point.
- Selection Rationale.

### 13.2 UX Flow Diagram

- Main Flow.
- File Validation.
- Duplicate Detection.
- Data Validation.
- Import Confirmation.
- Processing.
- Success Branch.
- Error Branch.
- Cancel Branch.
- End.

### 13.3 UI Screens

- List/Table.
- Upload.
- Preview.
- Validation.
- Confirmation.
- Processing.
- Success.
- Error.
- Cancel Confirmation.

### 13.4 UI State Coverage Report

- Applicable States.
- Generated States.
- Not Applicable States.
- Pending Requirement.
- Pending Human Approval.
- Pending Verification.

### 13.5 Flow-to-Screen Mapping

AI MUST memetakan flow nodes, UI Screens, UI States, dan triggers.

### 13.6 Component Usage Report

AI MUST menyertakan official GEMS components, variants, states, dan missing components.

### 13.7 Business Compliance Report

AI MUST menyertakan file validation, data validation, duplicate handling, permissions, confirmation, dan cancel behavior.

### 13.8 Human Approval Register

AI MUST mencatat proposed changes dan approval status.

### 13.9 Final Compliance Report

AI MUST menyertakan:

- HSD/BRD Compliance.
- UX Pattern Compliance.
- Core Flow Compliance.
- GEMS Component Compliance.
- UI State Coverage.
- Role Access Compliance.
- Human Approval Status.
- Unresolved Issues.

---

## 14. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut.

**Step 1 — Analyze HSD/BRD**

AI MUST mengidentifikasi import requirements, permissions, file formats, validation, duplicate handling, dan expected results.

**Step 2 — Inspect Official Import Data Pattern**

AI MUST memeriksa Pattern 01 melalui Figma MCP.

**Step 3 — Verify Approved Core Flow**

AI MUST memeriksa nodes, connectors, decisions, success, error, dan cancel branches.

**Step 4 — Inspect GEMS Design System**

AI MUST memeriksa official components, properties, variants, states, dan design tokens.

**Step 5 — Identify Applicable UI States**

AI MUST mengevaluasi Upload, File Validation, Preview, Data Validation, Confirmation, Processing, Success, Error, Cancel, Disabled, dan Access Restricted.

**Step 6 — Generate UX Flow Diagram**

AI MUST membuat visual flow pada bagian atas Figma section.

**Step 7 — Generate UI Screens**

AI MUST membuat screens sesuai official Import Data Pattern pada bagian bawah.

**Step 8 — Generate Applicable UI States**

AI MUST membuat seluruh applicable states menggunakan official GEMS components.

**Step 9 — Validate Import Business Behavior**

AI MUST memastikan file validation, duplicate handling, data validation, permissions, dan import processing sesuai HSD/BRD.

**Step 10 — Validate Flow-to-Screen Mapping**

AI MUST memastikan diagram, screens, states, dan navigation konsisten.

**Step 11 — Identify Gaps**

AI MUST mengidentifikasi requirement, component, flow, dan state gaps.

**Step 12 — Request Human Approval**

AI MUST meminta approval untuk proposed changes.

**Step 13 — Inspect Actual Figma Output**

AI MUST memeriksa frames, components, variants, states, layout, dan flow yang benar-benar dibuat.

**Step 14 — Generate Compliance Report**

AI MUST melaporkan hasil verifikasi dan unresolved issues.

---

## 15. AI Restrictions

AI MUST NOT:

1. Mengubah approved Core Flow tanpa Human Approval.
2. Menggunakan unapproved UX Pattern.
3. Mengganti official GEMS components tanpa approval.
4. Mengarang supported file formats.
5. Mengarang file size limits.
6. Mengarang file templates.
7. Mengarang required columns.
8. Mengarang data validation rules.
9. Mengarang duplicate handling.
10. Mengarang partial import behavior.
11. Mengarang role permissions.
12. Menghilangkan File Validation.
13. Menghilangkan Preview Data.
14. Menghilangkan Data Validation.
15. Menghilangkan Import Confirmation.
16. Menghilangkan Cancel Confirmation.
17. Menghilangkan error branches.
18. Menganggap invalid data dapat diimpor tanpa requirement.
19. Menganggap duplicate data otomatis ditimpa.
20. Menganggap Import Permission otomatis memberikan Update Permission.
21. Mengarang retry atau rollback behavior.
22. Mengarang draft persistence.
23. Menampilkan false success.
24. Menghasilkan hanya happy path.
25. Menghasilkan screens tanpa UX Flow Diagram.
26. Menghasilkan diagram yang bertentangan dengan screens.
27. Menghilangkan applicable UI States.
28. Mengimplementasikan Proposed Design tanpa approval.
29. Mengklaim custom components sebagai official GEMS components.
30. Mengklaim desain compliant tanpa actual Figma verification.

---

## 16. Quality Assurance & Final Enforcement

### 16.1 Business Validation

AI MUST memverifikasi:

1. Import Permission.
2. Supported File Formats.
3. File Validation.
4. Data Validation.
5. Duplicate Detection.
6. Duplicate Handling.
7. Import Eligibility.
8. Confirmation Behavior.
9. Cancel Behavior.
10. Success Criteria.
11. Error Behavior.

### 16.2 Pattern Validation

AI MUST memverifikasi:

1. Official Figma reference.
2. Entry point.
3. Flow nodes.
4. Connectors.
5. File Valid decision.
6. Existing Data decision.
7. Data Valid decision.
8. Import Confirmation.
9. Processing.
10. Success decision.
11. Error branch.
12. Cancel branch.
13. End state.

### 16.3 UI Validation

AI MUST memverifikasi:

1. Official GEMS components.
2. Correct variants.
3. Correct visual states.
4. Upload component.
5. Preview layout.
6. Validation feedback.
7. Confirmation Modal.
8. Cancel Confirmation.
9. Loading Feedback.
10. Success Toast.
11. Error Feedback.
12. Accessibility.
13. Flow-to-Screen Mapping.

### 16.4 Final Validation Instructions

Sebelum melaporkan completion, AI MUST:

1. Verify approved HSD/BRD.
2. Verify Role Access Matrix.
3. Verify official Import Data Pattern.
4. Verify Core Flow integrity.
5. Verify all decision branches.
6. Verify Upload File.
7. Verify File Validation.
8. Verify Preview Data.
9. Verify Existing Data decision.
10. Verify Data Validation.
11. Verify Import Confirmation.
12. Verify Processing State.
13. Verify Success Feedback.
14. Verify Error Feedback.
15. Verify Cancel Confirmation.
16. Verify Stay in Form behavior.
17. Verify Exit behavior.
18. Verify Disabled States.
19. Verify Access Restricted States.
20. Verify official GEMS components.
21. Verify component variants.
22. Verify UX Flow Diagram above UI Screens.
23. Verify Flow-to-Screen Mapping.
24. Verify applicable state coverage.
25. Verify Human Approval for changes.
26. Verify unresolved requirements are reported.
27. Inspect actual Figma output.
28. Generate final Compliance Report.

AI MUST NOT menandai item yang belum diverifikasi sebagai compliant.

### 16.5 Final AI Enforcement

AI MUST:

1. Analyze approved HSD/BRD.
2. Use official GEMS Import Data UX Pattern.
3. Preserve approved Core Flow.
4. Use GEMS Design System components.
5. Generate visual UX Flow Diagram.
6. Generate corresponding UI Screens.
7. Generate all applicable UI States.
8. Apply File Validation.
9. Apply Data Validation.
10. Apply approved Duplicate Handling.
11. Respect Role Access Matrix.
12. Handle Confirmation, Cancel, Loading, Success, dan Error.
13. Maintain Flow-to-Screen consistency.
14. Identify requirement and component gaps.
15. Obtain explicit Human Approval for changes.
16. Validate actual Figma output.
17. Generate a Compliance Report.

### Final Enforcement Rule

AI MUST menggunakan approved HSD/BRD sebagai sumber business requirements, official GEMS Import Data UX Pattern sebagai sumber approved Core Flow, dan GEMS Design System sebagai sumber UI components, variants, dan states.

AI MUST menghasilkan **visual UX Flow Diagram di atas UI Screens** dalam satu Figma section dan merepresentasikan seluruh applicable UI States.

AI MUST mempertahankan File Validation, Existing Data Decision, Data Validation, Import Confirmation, Processing, Success, Error, dan Cancel branches sesuai official pattern.

AI MAY merekomendasikan UX improvements, additional states, alternative interactions, atau component enhancements jika didukung business requirements dan usability considerations.

AI MUST memperoleh explicit Human Approval sebelum mengimplementasikan perubahan pada approved Core Flow, navigation, validation, duplicate handling, permissions, atau Design System.

AI MUST memverifikasi hasil aktual di Figma sebelum menyatakan desain selesai atau compliant.

**HSD/BRD defines business requirements. GEMS UX Pattern defines the approved Core Flow. GEMS Design System defines components and visual states. Human Approval authorizes changes.**
