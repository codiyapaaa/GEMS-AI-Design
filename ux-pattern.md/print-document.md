# GEMS AI Design Guidelines — Print Document UX Pattern

## 1. Purpose & Scope

AI MUST menghasilkan desain UI/UX **Print Document** berdasarkan approved HSD/BRD, official GEMS UX Pattern, GEMS Design System, dan Role Access Matrix.

AI MUST:

1. Menganalisis approved HSD/BRD untuk mengidentifikasi business requirements, document types, user roles, permissions, dan print behavior.
2. Memeriksa seluruh official Print Document UX Pattern references di Figma.
3. Memilih Pattern 01 atau Pattern 02 berdasarkan kebutuhan fitur.
4. Mengikuti approved Core Flow tanpa mengubah urutan, navigation, atau interaction behavior.
5. Menggunakan official GEMS Design System components, variants, states, dan design tokens.
6. Menghasilkan **visual UX Flow Diagram di bagian atas** dan **UI Screens di bagian bawah** dalam satu Figma section.
7. Menghasilkan seluruh applicable UI States untuk setiap screen.
8. Memastikan Print, Download, dan Preview menggunakan behavior sesuai approved requirements.
9. Memvalidasi document selection, print eligibility, role permissions, dan output requirements.
10. Meminta explicit Human Approval sebelum mengimplementasikan perubahan terhadap approved Core Flow, business rules, atau Design System.
11. Memverifikasi hasil desain langsung di Figma sebelum menyatakan pekerjaan selesai.

AI MUST NOT:

1. Mengarang business requirements, document types, permissions, atau print behavior.
2. Mengubah approved Core Flow tanpa Human Approval.
3. Menggunakan custom components sebagai pengganti official GEMS components tanpa approval.
4. Menghasilkan hanya happy path tanpa mengevaluasi applicable UI States.
5. Menganggap Print dan Download sebagai tindakan yang sama.
6. Mengklaim desain compliant tanpa memverifikasi hasil aktual di Figma.

### 1.1 Print vs Download vs Preview

AI MUST membedakan:

| Operation | Function | Expected Outcome |
|---|---|---|
| Print | Menjalankan proses pencetakan dokumen | Print workflow sesuai approved pattern |
| Download | Mengunduh dokumen | File digital sesuai approved requirements |
| Preview | Menampilkan dokumen sebelum tindakan | Document Preview |
| Export | Menghasilkan data atau file dalam format tertentu | Export workflow sesuai HSD/BRD |

AI MUST menggunakan action, label, navigation, dan feedback sesuai masing-masing operation.

AI MUST NOT menambahkan Download atau Export Flow jika tidak didukung approved requirements.

---

## 2. Source of Truth & Design Governance

### 2.1 Source Hierarchy

AI MUST menggunakan sumber berikut sesuai kewenangannya.

| Source | Primary Responsibility |
|---|---|
| Approved HSD/BRD | Business requirements, document rules, print eligibility, output requirements |
| GEMS UX Pattern | Approved Core Flow, entry point, navigation, interaction sequence |
| GEMS Design System | Official components, variants, states, visual tokens |
| Role Access Matrix | Print permission dan document access |
| Human Approval | Authorization untuk perubahan flow, behavior, dan Design System |

AI MUST memprioritaskan approved HSD/BRD untuk business rules dan official UX Pattern untuk struktur interaksi.

AI MUST menggunakan GEMS Design System untuk seluruh komponen dan visual states.

### 2.2 Conflict Handling

Jika terdapat konflik antara HSD/BRD, UX Pattern, dan Design System, AI MUST:

1. Mengidentifikasi sumber yang bertentangan.
2. Menjelaskan requirement atau behavior yang berbeda.
3. Menjelaskan dampaknya terhadap UX Flow, UI Screens, dan UI States.
4. Menyampaikan rekomendasi jika diperlukan.
5. Meminta Human Review sebelum mengimplementasikan perubahan.

AI MUST NOT menyelesaikan konflik dengan mengubah approved requirements secara sepihak.

### 2.3 Core Flow Governance

AI MUST:

1. Menggunakan official Print Document UX Pattern sebagai acuan Core Flow.
2. Memeriksa seluruh flow nodes dan connectors.
3. Mempertahankan approved entry point.
4. Mempertahankan interaction sequence.
5. Mempertahankan navigation destination.
6. Mengikuti approved decision branches.
7. Menghubungkan setiap flow node dengan UI Screen atau annotation yang sesuai.

AI MUST NOT menambahkan, menghilangkan, atau mengganti langkah yang mengubah approved Core Flow tanpa Human Approval.

### 2.4 Design System Governance

**Official GEMS Design System:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System

AI MUST:

1. Menggunakan official GEMS components.
2. Menggunakan available component properties.
3. Menggunakan approved variants dan states.
4. Menggunakan official typography.
5. Menggunakan official colors dan design tokens.
6. Mengikuti spacing dan layout rules.
7. Mempertahankan component anatomy.

AI MUST NOT membuat atau mengganti official components tanpa approval.

---

## 3. Official Print Document UX Pattern References

**Parent Reference — Print Document:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1214-32412

AI MUST memeriksa dua official Print Document UX Patterns sebelum memilih desain.

| Pattern | Type | Figma Reference |
|---|---|---|
| Pattern 01 | Print from Document Preview | [Open Pattern 01](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1214-40255) |
| Pattern 02 | Print from Detail Data | [Open Pattern 02](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3375-194826) |

AI MUST:

1. Memeriksa kedua pattern melalui Figma MCP.
2. Mengidentifikasi perbedaan entry point.
3. Mengidentifikasi perbedaan document selection.
4. Mengidentifikasi perbedaan preview behavior.
5. Mengidentifikasi required UI Screens.
6. Mengidentifikasi applicable UI States.
7. Memilih pattern berdasarkan approved business requirements.

AI MUST NOT menganggap kedua pattern memiliki struktur UI atau interaction behavior yang identik.

---

## 4. Pattern 01 — Print from Document Preview

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1214-40255

### 4.1 When to Use

AI MUST menggunakan Pattern 01 ketika approved requirements menetapkan proses pencetakan melalui Document Preview atau halaman dokumen yang sudah tersedia.

AI MUST memvalidasi:

1. Document availability.
2. User role.
3. Print permission.
4. Document Preview requirements.
5. Print Action behavior.
6. Navigation destination.

### 4.2 Official Core Flow

AI MUST memeriksa dan merepresentasikan flow berikut berdasarkan official Figma reference:

**Start → Detail Page → Document Preview → Print Page → Klik Tombol Print → Toast Message → End.**

AI MUST memverifikasi arah connectors pada Figma sebelum menetapkan final flow.

AI MUST mempertahankan approved Print Action dan feedback behavior.

### 4.3 Required UI Screens

AI MUST menghasilkan:

1. Detail Page.
2. Document Preview.
3. Print Page atau print-related interface sesuai reference.
4. Print Action State.
5. Loading / Processing State jika berlaku.
6. Success Feedback sesuai approved behavior.
7. Error State jika berlaku.
8. Disabled State jika berlaku.
9. Access Restricted State jika berlaku.
10. Document Unavailable State jika diperlukan.
11. Preview Loading dan Preview Error jika relevan.

AI MUST NOT menambahkan Document Selection Modal jika tidak didukung Pattern 01 atau approved HSD/BRD.

### 4.4 Interaction Rules

AI MUST:

1. Menggunakan Detail Page sesuai official reference.
2. Menampilkan Document Preview menggunakan approved layout.
3. Menggunakan official GEMS Button untuk Print Action.
4. Mengikuti navigation dari Preview menuju Print Page sesuai reference.
5. Menampilkan processing feedback jika dokumen sedang disiapkan.
6. Menampilkan Success Feedback hanya ketika success criteria terpenuhi.
7. Menampilkan Error Feedback jika proses gagal.
8. Mengikuti approved navigation setelah Print Action.
9. Mempertahankan document content sesuai approved data dan template.

AI MUST NOT mengklaim physical printing completed hanya karena print dialog dibuka atau print request dikirim.

### 4.5 State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Active, Loading, Preview Loading, Preview Ready, Success, Error, Disabled, Access Restricted, Document Unavailable, dan Network/Server Error jika berlaku.

---

## 5. Pattern 02 — Print from Detail Data

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3375-194826

### 5.1 When to Use

AI MUST menggunakan Pattern 02 ketika approved requirements menetapkan proses pencetakan melalui Detail Data yang diakses dari List/Data Table dan melibatkan pemilihan data atau dokumen sebelum preview.

AI MUST memvalidasi:

1. Entry point.
2. Document selection requirements.
3. Available document types.
4. Print permission.
5. Preview requirements.
6. Print output behavior.

### 5.2 Official Core Flow

AI MUST memeriksa dan merepresentasikan flow berikut berdasarkan official Figma reference:

**Start → List/Data Table → Klik salah satu data → Detail Data → Klik Cetak atau Unduh → Klik Cetak → Modal Pilih Data yang Ingin Dicetak → Preview Dokumen → Print-related action dan feedback sesuai reference → End.**

AI MUST memverifikasi arah connectors dan decision branches sebelum menetapkan final flow.

AI MUST mempertahankan document selection sesuai approved pattern.

### 5.3 Required UI Screens

AI MUST menghasilkan:

1. List/Data Table.
2. Detail Data Page.
3. Cetak atau Unduh Action.
4. Print Action Selection.
5. Modal Pilih Data yang Ingin Dicetak.
6. Document Selection State.
7. Preview Dokumen.
8. Loading / Processing State jika berlaku.
9. Success Feedback sesuai approved behavior.
10. Error State jika berlaku.
11. Disabled State jika berlaku.
12. Access Restricted State jika berlaku.
13. Empty Selection State jika relevan.
14. Document Unavailable State jika relevan.

AI MUST NOT mengarang document options, selection rules, atau output formats.

### 5.4 Interaction Rules

AI MUST:

1. Menggunakan official GEMS List/Data Table.
2. Menggunakan Detail Data Page sesuai reference.
3. Menampilkan Cetak atau Unduh Action sesuai approved layout.
4. Memisahkan Print dan Download berdasarkan approved behavior.
5. Menggunakan official GEMS Modal untuk document selection.
6. Menampilkan pilihan dokumen berdasarkan selected data.
7. Menggunakan approved document labels.
8. Menampilkan Preview Dokumen sesuai selected data.
9. Menggunakan official Print Action.
10. Menampilkan feedback sesuai hasil proses.
11. Mempertahankan navigation dan screen context.

AI MUST NOT menampilkan document options yang tidak tersedia untuk selected record.

### 5.5 Document Selection Rules

AI MUST memeriksa HSD/BRD untuk menentukan:

1. Available document types.
2. Single atau Multiple Selection.
3. Default Selection.
4. Required Selection.
5. Selection Validation.
6. Disabled Options.
7. Document Preview behavior.
8. Document output format.
9. Permission per document type.

AI MUST NOT menganggap multiple selection tersedia hanya karena terdapat document selection modal.

### 5.6 State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Selected, Modal Open, Modal Close, Loading, Preview Ready, Success, Error, Disabled, Access Restricted, Empty Selection, Document Unavailable, dan Network/Server Error jika berlaku.

---

## 6. Mandatory UI State Generation

### 6.1 State Generation Principles

AI MUST:

1. Mengevaluasi seluruh applicable UI States untuk selected Print Document Pattern.
2. Menggunakan official GEMS component variants.
3. Menghasilkan state berdasarkan approved Core Flow dan business requirements.
4. Menghubungkan setiap state dengan source screen.
5. Menentukan trigger untuk setiap state.
6. Menentukan expected UI behavior.
7. Mengidentifikasi resulting state.
8. Membuat Flow-to-Screen Mapping.
9. Melaporkan states yang belum dapat diimplementasikan.

AI MUST NOT menghasilkan hanya Default dan Success State.

### 6.2 Mandatory UI State Matrix

| State | Trigger | Expected UI Output | Applicability |
|---|---|---|---|
| Default | Screen dibuka | Normal UI | All |
| Hover | Pointer pada action | Hover Variant | Applicable controls |
| Focus | Keyboard focus | Focus Indicator | Applicable controls |
| Active | Action aktif | Active Variant | If supported |
| Selected | Dokumen dipilih | Selected State | Pattern 02 jika didukung |
| Modal Open | Document selection dibuka | Selection Modal | Pattern 02 |
| Modal Close | Modal ditutup | Return to source context | Pattern 02 |
| Loading | Dokumen diproses | Processing Feedback | If applicable |
| Preview Loading | Preview sedang dimuat | Loading Indicator | If applicable |
| Preview Ready | Preview tersedia | Document Preview | Both |
| Success | Success criteria terpenuhi | Success Feedback | Based on pattern |
| Error | Proses gagal | Error Feedback | If applicable |
| Disabled | Action tidak tersedia | Disabled Action | Based on rules |
| Validation Error | Selection tidak valid | Validation Feedback | If applicable |
| Empty | Tidak ada data | Empty State | If applicable |
| Document Unavailable | Dokumen tidak tersedia | Unavailable Feedback | If applicable |
| Access Restricted | Role tidak berwenang | Permission State | Role-dependent |
| Network Error | Gangguan koneksi | Error Feedback | If applicable |
| Server Error | Gangguan sistem | Error Feedback | If applicable |

### 6.3 Default State

AI MUST:

1. Menggunakan screen normal sesuai selected pattern.
2. Menampilkan document information sesuai approved requirements.
3. Menampilkan available actions sesuai role permissions.
4. Menggunakan official GEMS components.
5. Mempertahankan approved navigation.

### 6.4 Hover, Focus & Active States

AI MUST:

1. Menggunakan official GEMS variants.
2. Mempertahankan focus visibility.
3. Mengikuti component interaction behavior.
4. Menggunakan approved visual tokens.

AI MUST NOT membuat interaction variants baru tanpa approval.

### 6.5 Selected State

Untuk Pattern 02, AI MUST:

1. Menggunakan official selected variants.
2. Mengikuti approved selection rules.
3. Menampilkan selected documents secara jelas.
4. Mempertahankan selection state sesuai approved behavior.

AI MUST NOT mengarang Select All, Multiple Selection, atau selection limits.

### 6.6 Modal Open & Close States

AI MUST:

1. Menggunakan official GEMS Modal.
2. Menampilkan approved document options.
3. Menggunakan official selection components.
4. Mengikuti approved close dan cancel behavior.
5. Mempertahankan source context.
6. Tidak memproses Print ketika pengguna membatalkan.

### 6.7 Loading State

AI MUST:

1. Menggunakan official Loading Indicator.
2. Menampilkan processing feedback.
3. Membedakan document preparation dari completed print outcome.
4. Mengikuti approved duplicate-submission behavior.
5. Tidak menampilkan Success sebelum success criteria terpenuhi.

### 6.8 Preview Loading & Preview Ready

AI MUST:

1. Menampilkan loading feedback jika dokumen sedang disiapkan.
2. Menggunakan approved preview layout.
3. Menampilkan dokumen sesuai selected data.
4. Mempertahankan document readability.
5. Menampilkan Print Action sesuai selected pattern.
6. Menampilkan Error Feedback jika preview gagal.

### 6.9 Success State

AI MUST:

1. Menggunakan official GEMS Success Toast jika ditetapkan pattern.
2. Menggunakan approved success wording.
3. Menampilkan feedback sesuai kondisi yang benar-benar dapat diverifikasi.
4. Mengikuti approved navigation.
5. Tidak mengklaim physical printing completed jika tidak dapat diverifikasi.

### 6.10 Error State

AI MUST:

1. Menggunakan official GEMS Error Feedback.
2. Menjelaskan kegagalan sesuai konteks.
3. Mempertahankan selected data jika sesuai approved behavior.
4. Tidak menampilkan false success.
5. Mengikuti approved recovery behavior.

AI MUST NOT mengarang automatic retry, rollback, atau alternate printing mechanism.

### 6.11 Disabled State

AI MUST memeriksa kondisi yang membuat Print Action tidak tersedia, termasuk:

1. Role tidak memiliki permission.
2. Document belum tersedia.
3. Document selection belum valid.
4. Document sedang diproses.
5. Record tidak memenuhi print eligibility.

AI MUST memvalidasi seluruh kondisi terhadap approved HSD/BRD.

AI MUST NOT menganggap contoh kondisi tersebut sebagai business rules otomatis.

### 6.12 Validation Error State

Jika document selection diwajibkan, AI MUST:

1. Menggunakan approved validation rules.
2. Menampilkan validation feedback.
3. Menggunakan official GEMS error component.
4. Mencegah submission yang tidak valid sesuai requirement.

AI MUST NOT mengarang required selection atau validation constraints.

### 6.13 Empty & Document Unavailable States

AI MUST membedakan:

1. Tidak ada data.
2. Tidak ada hasil filter.
3. Dokumen tidak tersedia.
4. Dokumen gagal dimuat.
5. Tidak ada dokumen yang memenuhi kriteria.

AI MUST menggunakan official Empty State atau Error Feedback sesuai konteks.

### 6.14 Access Restricted State

AI MUST:

1. Mengikuti Role Access Matrix.
2. Memeriksa View Permission.
3. Memeriksa Preview Permission.
4. Memeriksa Print Permission.
5. Memeriksa Download Permission.
6. Menggunakan approved restricted behavior.

AI MUST NOT menganggap View Permission otomatis memberikan Print Permission.

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

AI MUST memeriksa official GEMS components yang relevan dengan selected pattern:

1. Page Header.
2. Navbar.
3. GEMS Slide Bar.
4. Table.
5. Pagination.
6. Detail Information.
7. Record Information.
8. Buttons/Button.
9. Button Group.
10. Modal.
11. Document Selection Controls.
12. Notification / Toast.
13. Button Close X.
14. Empty State.
15. Loading Indicator.
16. Document Preview Container jika tersedia.
17. Section Footer jika sesuai reference.

AI MUST menggunakan hanya komponen yang relevan dengan screen dan approved requirements.

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
2. Membuat custom Print Button tanpa approval.
3. Membuat custom Modal tanpa approval.
4. Mengarang component variants.
5. Mengubah component anatomy.
6. Mengubah button hierarchy.
7. Mengubah interaction behavior.
8. Mengklaim custom UI sebagai official GEMS component.

### 7.4 Missing Component Handling

Jika komponen tidak tersedia, AI MUST:

1. Mengidentifikasi missing component.
2. Memeriksa alternatif resmi.
3. Menjelaskan keterbatasan.
4. Mengusulkan solusi.
5. Menjelaskan dampak terhadap UX Flow dan UI Screens.
6. Meminta Human Approval sebelum implementasi komponen baru.

---

## 8. Mandatory UX Flow Diagram & UI Screen Layout

### 8.1 Required Figma Structure

AI MUST menghasilkan dua area dalam satu Figma section:

**TOP — UX FLOW DIAGRAM**

AI MUST menampilkan approved Print Document Core Flow beserta applicable decision branches.

**BOTTOM — UI SCREENS & STATES**

AI MUST menampilkan seluruh UI Screens dan applicable UI States sesuai selected pattern.

AI MUST NOT memisahkan diagram dan screens tanpa hubungan dokumentasi yang jelas.

### 8.2 UX Flow Diagram Requirements

Untuk Pattern 01, AI MUST merepresentasikan:

1. Start.
2. Detail Page.
3. Document Preview.
4. Print Page.
5. Klik Tombol Print.
6. Toast Message.
7. End.

Untuk Pattern 02, AI MUST merepresentasikan:

1. Start.
2. List/Data Table.
3. Klik salah satu data.
4. Detail Data.
5. Klik Cetak atau Unduh.
6. Klik Cetak.
7. Modal Pilih Data yang Ingin Dicetak.
8. Preview Dokumen.
9. Print-related steps sesuai reference.
10. Success Feedback.
11. End.

AI MUST memverifikasi actual connectors dan decision branches sebelum finalisasi diagram.

### 8.3 UI Screen Arrangement

AI MUST:

1. Mengurutkan screens sesuai selected Core Flow.
2. Menempatkan Document Selection Modal bersama source screen.
3. Menempatkan Preview Screen sesuai flow.
4. Menempatkan Loading State pada proses terkait.
5. Menempatkan Success Feedback pada konteks yang benar.
6. Menempatkan Error Feedback bersama source screen.
7. Mengelompokkan Disabled dan Validation States.
8. Menjaga alignment dan spacing.
9. Menggunakan frame naming yang konsisten.
10. Menggunakan official GEMS layout.

### 8.4 Flow-to-Screen Mapping

| Flow Node | UI Representation |
|---|---|
| Start | Entry Annotation |
| List/Data Table | List Screen |
| Detail Data | Detail Page |
| Document Preview | Preview Screen |
| Klik Cetak | Print Action |
| Document Selection | Selection Modal |
| Preview Dokumen | Selected Document Preview |
| Processing | Loading State |
| Success Feedback | Toast / Notification |
| Error | Error Feedback |
| End | Final Flow State |

AI MUST menggunakan hanya node yang relevan dengan selected pattern.

AI MUST memastikan setiap official flow node memiliki UI Screen atau annotation yang jelas.

---

## 9. Business Rules & Print Permissions

### 9.1 Required Business Analysis

AI MUST mengidentifikasi:

1. Feature Name.
2. Record Type.
3. User Role.
4. Print Permission.
5. Document Access Permission.
6. Document Type.
7. Document Availability.
8. Print Eligibility.
9. Document Selection Rules.
10. Document Template.
11. Preview Requirements.
12. Print Output Requirements.
13. Success Behavior.
14. Error Behavior.
15. Navigation Destination.
16. Download Permission jika tersedia.

### 9.2 Print Eligibility

AI MUST:

1. Menggunakan approved eligibility criteria.
2. Memeriksa record status jika memengaruhi Print.
3. Memeriksa document availability.
4. Memeriksa role permission.
5. Menggunakan approved disabled atau restricted behavior.

AI MUST NOT menganggap seluruh record dapat dicetak.

Jika print eligibility belum dijelaskan, AI MUST menandainya sebagai Pending Requirement.

### 9.3 Document Type Rules

AI MUST menggunakan document types yang ditetapkan HSD/BRD.

AI MUST NOT mengarang:

1. Nama dokumen.
2. Jumlah dokumen.
3. Format dokumen.
4. Document templates.
5. Data fields.
6. Document ordering.
7. Print restrictions.

### 9.4 Document Availability

AI MUST memeriksa apakah dokumen:

1. Selalu tersedia.
2. Tersedia setelah proses tertentu.
3. Bergantung pada record status.
4. Bergantung pada role permission.
5. Memerlukan document generation.

AI MUST NOT mengarang document availability rules.

### 9.5 Permission Handling

AI MUST mengikuti Role Access Matrix.

AI MUST membedakan:

- View Permission.
- Preview Permission.
- Print Permission.
- Download Permission.

AI MUST NOT memberikan Print atau Download Permission hanya karena pengguna dapat melihat Detail Page.

---

## 10. Document Selection, Preview & Print Rules

### 10.1 Document Selection Requirements

AI MUST:

1. Memeriksa apakah selected pattern membutuhkan document selection.
2. Menggunakan official selection flow untuk Pattern 02.
3. Menampilkan document options berdasarkan selected data.
4. Mengikuti approved document selection rules.
5. Menggunakan official GEMS selection components.

### 10.2 Selection Validation

AI MUST memeriksa:

1. Single atau Multiple Selection.
2. Required Selection.
3. Default Selection.
4. Disabled Options.
5. Selection Limits.
6. Available Document Types.
7. Selection Error Behavior.

AI MUST NOT mengarang selection rules.

### 10.3 Document Preview Requirements

AI MUST:

1. Menggunakan approved preview layout.
2. Menampilkan data sesuai selected record.
3. Menampilkan document type yang benar.
4. Memastikan konten mengikuti approved template.
5. Menempatkan Print Action sesuai reference.
6. Menggunakan Loading dan Error Feedback jika berlaku.

AI MUST NOT
