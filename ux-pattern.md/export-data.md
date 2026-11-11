# GEMS AI Design Guidelines — Export Data UX Pattern

## 1. Purpose & Scope

AI MUST menghasilkan desain UI/UX **Export Data** berdasarkan approved HSD/BRD, official GEMS UX Pattern, GEMS Design System, dan Role Access Matrix.

AI MUST:

1. Menganalisis HSD/BRD untuk mengidentifikasi business requirements, data scope, export permissions, file formats, filters, dan validation rules.
2. Memeriksa seluruh lima official Export Data UX Patterns melalui Figma MCP.
3. Memilih pattern berdasarkan entry point, kebutuhan pemilihan data, periode, dan jumlah record.
4. Mempertahankan approved Core Flow, termasuk decision branches, success, dan error paths.
5. Menggunakan official GEMS components, properties, variants, states, dan design tokens.
6. Menghasilkan **visual UX Flow Diagram di bagian atas** dan **UI Screens beserta applicable UI States di bagian bawah** dalam satu Figma section.
7. Menghasilkan screen untuk setiap langkah interaksi dan applicable state untuk setiap komponen.
8. Memastikan data yang diekspor sesuai selected scope, filters, permissions, dan approved requirements.
9. Memvalidasi input sebelum export diproses.
10. Menampilkan Loading, Success, dan Error Feedback sesuai kondisi sistem.
11. Mengidentifikasi requirement gaps dan component gaps.
12. Meminta explicit Human Approval sebelum mengubah approved Core Flow, business rules, navigation, atau Design System.
13. Memeriksa hasil aktual di Figma sebelum menyatakan desain selesai.

AI MUST NOT:

1. Mengarang file formats, data fields, export limits, permissions, atau validation rules.
2. Mengubah approved Core Flow tanpa Human Approval.
3. Menganggap semua data dapat diekspor oleh semua role.
4. Menganggap data yang difilter otomatis sama dengan data yang dipilih secara manual.
5. Menggunakan custom components sebagai pengganti official GEMS components tanpa approval.
6. Menghasilkan hanya happy path tanpa mengevaluasi applicable UI States.
7. Mengklaim file berhasil diunduh sebelum keberhasilannya dapat dikonfirmasi.

### 1.1 Export vs Print vs Download

AI MUST membedakan:

| Operation | Function | Expected Outcome |
|---|---|---|
| Export Data | Menghasilkan file dari data sesuai scope dan format | Exported dataset |
| Download | Mengambil file digital | Downloaded file |
| Print | Menjalankan proses pencetakan | Print workflow |
| Preview | Menampilkan konten sebelum tindakan | Preview interface |

AI MUST menggunakan Export Data UX Pattern untuk proses export, bukan Print Document UX Pattern.

AI MUST mengikuti approved HSD/BRD jika proses export juga mencakup download file.

---

## 2. Source of Truth & Design Governance

### 2.1 Source Hierarchy

AI MUST menggunakan sumber berikut sesuai kewenangannya.

| Source | Responsibility |
|---|---|
| Approved HSD/BRD | Business rules, data scope, filters, permissions, formats, validation |
| GEMS UX Pattern | Approved Core Flow, navigation, decision branches |
| GEMS Design System | Components, variants, states, visual tokens |
| Role Access Matrix | Export permissions dan data visibility |
| Human Approval | Authorization untuk perubahan approved design |

AI MUST menggunakan approved HSD/BRD sebagai sumber business logic.

AI MUST menggunakan official UX Pattern sebagai sumber interaction sequence.

AI MUST menggunakan GEMS Design System sebagai sumber komponen dan visual behavior.

### 2.2 Conflict Handling

Jika terdapat konflik antar-sumber, AI MUST:

1. Mengidentifikasi konflik.
2. Menjelaskan requirement yang bertentangan.
3. Menjelaskan dampak terhadap flow, screens, dan states.
4. Mengusulkan solusi jika diperlukan.
5. Meminta Human Review sebelum mengimplementasikan perubahan.

AI MUST NOT menyelesaikan konflik dengan membuat business rules baru.

### 2.3 Core Flow Governance

AI MUST:

1. Mengidentifikasi Start dan End.
2. Mengidentifikasi entry point.
3. Memeriksa seluruh flow nodes.
4. Memeriksa arah connectors.
5. Memeriksa decision branches.
6. Memeriksa validation conditions.
7. Memeriksa processing behavior.
8. Memeriksa success dan error paths.
9. Mempertahankan navigation sesuai reference.
10. Memetakan flow ke UI Screens.

AI MUST NOT menghilangkan decision branch hanya untuk menyederhanakan desain.

### 2.4 Design System Governance

**Official GEMS Design System:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System

AI MUST menggunakan official components, typography, colors, spacing, icons, layout, dan interaction variants.

AI MUST NOT mengubah official component anatomy atau membuat variants baru tanpa approval.

---

## 3. Official Export Data UX Pattern References

**Parent Reference — Export Data:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1214-42984

AI MUST memeriksa seluruh lima pattern berikut.

| Pattern | Official Name | Primary Use |
|---|---|---|
| 01 | Centralized Export Page | Export melalui halaman khusus |
| 02 | Contextual Export | Export dari List/Data Table |
| 03 | Data Selection Modal | Export dengan pemilihan data |
| 04 | Export with Period Selection Modal | Export berdasarkan periode |
| 05 | Single Data Export | Export satu record |

### 3.1 Pattern Selection Rules

AI MUST memilih pattern berdasarkan:

1. Entry point.
2. Export scope.
3. Single atau multiple records.
4. Filter requirements.
5. Period selection requirements.
6. File format requirements.
7. Data selection requirements.
8. Role permissions.
9. Approved business workflow.

AI MUST NOT memilih pattern hanya berdasarkan kemiripan visual.

AI MUST NOT menggabungkan beberapa pattern tanpa approved requirement atau Human Approval jika penggabungan mengubah Core Flow.

---

## 4. Pattern 01 — Centralized Export Page

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3396-90469

### 4.1 When to Use

AI MUST menggunakan Pattern 01 ketika approved requirements menetapkan halaman khusus untuk melakukan Export Data.

AI MUST memeriksa apakah pengguna perlu memilih modul, fitur, kategori data, atau periode sebelum export.

### 4.2 Core Flow

AI MUST merepresentasikan flow berikut berdasarkan official Figma reference:

**Start → Buka Halaman Export Data → Pilih Periode Export → Pilih Modul/Fitur/Kategori Data → Klik Tombol Export → Data Valid dan Siap Diekspor?**

AI MUST memetakan decision branches:

**Valid:** Sistem Memproses Export → File Berhasil Diunduh → Success Toast → End.

**Tidak Valid / Gagal:** Tampilkan Pesan Error Sesuai Kondisi → pengguna mengikuti approved correction atau recovery behavior.

AI MUST memeriksa arah connectors aktual untuk memastikan urutan pemilihan periode dan kategori serta titik kembalinya error branch.

### 4.3 Required UI Screens

AI MUST menghasilkan:

1. Centralized Export Page — Default.
2. Period Selection State.
3. Module/Feature/Category Selection State.
4. Selected Filters State.
5. Export Ready State.
6. Export Processing State.
7. Success Toast State.
8. Validation Error State.
9. Export Failed State.
10. Disabled State jika berlaku.
11. Empty Data State jika berlaku.
12. Access Restricted State jika berlaku.

### 4.4 Interaction Rules

AI MUST:

1. Menggunakan official page layout.
2. Menampilkan period controls sesuai reference.
3. Menampilkan module/category selection sesuai HSD/BRD.
4. Mempertahankan selected values ketika berpindah antar-input sesuai approved behavior.
5. Memvalidasi seluruh required inputs.
6. Menggunakan official Export Button.
7. Menampilkan processing feedback.
8. Menampilkan Success Toast ketika success criteria terpenuhi.
9. Menampilkan contextual Error Feedback ketika validation atau export gagal.

AI MUST NOT mengarang pilihan modul, kategori, periode, atau export formats.

### 4.5 Mandatory State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Selected, Filled, Disabled, Loading, Validation Error, Empty Data, Success, Export Error, Network Error, dan Access Restricted.

---

## 5. Pattern 02 — Contextual Export

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3396-98180

### 5.1 When to Use

AI MUST menggunakan Pattern 02 ketika Export Action tersedia langsung pada List/Data Table dan approved requirements memungkinkan pengguna mengekspor data berdasarkan konteks halaman.

### 5.2 Core Flow

AI MUST merepresentasikan:

**Start → Halaman List/Data Table → Atur Filter Jika Ada → Klik Tombol Export → Pilih Format File → Klik Tombol Export → Data Valid dan Siap Diekspor?**

**Valid:** Sistem Memproses Export → File Berhasil Diunduh → Success Toast → End.

**Tidak Valid / Gagal:** Tampilkan Pesan Error Sesuai Kondisi.

AI MUST memverifikasi arah connectors dan titik kembali pada error branch.

### 5.3 Required UI Screens

AI MUST menghasilkan:

1. List/Data Table — Default.
2. Filter Applied State.
3. Export Action State.
4. File Format Selection State.
5. Export Ready State.
6. Processing State.
7. Success Toast State.
8. Validation Error State.
9. Export Error State.
10. Empty Table State jika berlaku.
11. Disabled State jika berlaku.
12. Access Restricted State jika berlaku.

### 5.4 Interaction Rules

AI MUST:

1. Menggunakan official GEMS Table.
2. Menggunakan approved filters.
3. Mempertahankan filter context.
4. Menampilkan file format options sesuai HSD/BRD.
5. Memvalidasi selected format.
6. Memproses export berdasarkan approved data scope.
7. Menggunakan official Loading dan Notification components.
8. Memastikan exported data sesuai filter behavior yang ditetapkan.

AI MUST NOT menganggap export selalu mencakup seluruh record atau hanya visible rows.

### 5.5 Mandatory State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Filter Applied, Format Selected, Disabled, Loading, Success, Error, Empty Results, dan Access Restricted.

---

## 6. Pattern 03 — Data Selection Modal

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3398-19356

### 6.1 When to Use

AI MUST menggunakan Pattern 03 ketika approved requirements menetapkan pemilihan data yang akan disertakan dalam file export melalui modal.

### 6.2 Core Flow

AI MUST merepresentasikan:

**Start → Halaman List/Data Table → Atur Filter Jika Ada → Klik Tombol Export → Modal Pilih Data yang Disertakan dalam Export → Klik Tombol Export → Data Valid dan Siap Diekspor?**

**Valid:** Sistem Memproses Export → File Berhasil Diunduh → Success Toast → End.

**Tidak Valid / Gagal:** Tampilkan Pesan Error Sesuai Kondisi.

### 6.3 Required UI Screens

AI MUST menghasilkan:

1. List/Data Table — Default.
2. Filter Applied State.
3. Export Action State.
4. Data Selection Modal — Default.
5. Data Selection Modal — Selected.
6. Data Selection Modal — Unselected.
7. Data Selection Modal — Validation Error jika berlaku.
8. Modal Close/Cancel State.
9. Export Processing State.
10. Success Toast State.
11. Export Error State.
12. Disabled State jika berlaku.
13. Empty Selection State jika berlaku.

### 6.4 Data Selection Rules

AI MUST memeriksa HSD/BRD untuk menentukan:

1. Apakah pengguna memilih rows, fields, columns, atau data categories.
2. Apakah single selection atau multiple selection diperbolehkan.
3. Apakah terdapat default selection.
4. Apakah selection wajib.
5. Apakah Select All tersedia.
6. Apakah terdapat selection limit.
7. Apakah selected items tetap tersimpan setelah modal ditutup.
8. Apakah selection mengikuti active filters.

AI MUST NOT menganggap modal ini otomatis menggunakan checkbox atau multiple selection tanpa memeriksa official reference.

### 6.5 Modal Interaction Rules

AI MUST:

1. Menggunakan official GEMS Modal.
2. Menggunakan official selection components.
3. Menampilkan approved data options.
4. Menampilkan selected state dengan jelas.
5. Memvalidasi selection sebelum export.
6. Mengikuti approved Cancel behavior.
7. Tidak memproses export ketika pengguna membatalkan.
8. Menampilkan Error Feedback jika selection tidak valid.

### 6.6 Mandatory State Coverage

AI MUST mengevaluasi:

Modal Closed, Modal Open, Default, Hover, Focus, Selected, Unselected, Disabled, Validation Error, Empty Selection, Loading, Success, dan Export Error.

---

## 7. Pattern 04 — Export with Period Selection Modal

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3405-43072

### 7.1 When to Use

AI MUST menggunakan Pattern 04 ketika approved requirements menetapkan pemilihan periode melalui modal sebelum Export Data.

AI MUST mendukung Quick Select dan Custom Period hanya sesuai options yang tersedia dalam official reference dan HSD/BRD.

### 7.2 Core Flow

AI MUST merepresentasikan:

**Start → Halaman List/Data Table → Atur Filter Jika Ada → Klik Tombol Export → Modal Select Periode (Quick Select / Custom) → Klik Tombol Export → Data Valid dan Siap Diekspor?**

**Valid:** Sistem Memproses Export → File Berhasil Diunduh → Success Toast → End.

**Tidak Valid / Gagal:** Tampilkan Pesan Error Sesuai Kondisi.

### 7.3 Required UI Screens

AI MUST menghasilkan:

1. List/Data Table — Default.
2. Filter Applied State.
3. Export Action State.
4. Period Selection Modal — Default.
5. Quick Select State.
6. Custom Period State.
7. Selected Period State.
8. Invalid Period State.
9. Modal Close/Cancel State.
10. Export Processing State.
11. Success Toast State.
12. Export Error State.
13. Disabled State jika berlaku.
14. Empty Period Results State jika berlaku.

### 7.4 Quick Select Rules

AI MUST:

1. Menggunakan official period selection components.
2. Menampilkan hanya preset periods yang didukung requirement.
3. Menampilkan selected preset dengan jelas.
4. Memperbarui effective date range sesuai approved behavior.
5. Mengikuti approved date calculation rules.

AI MUST NOT mengarang preset seperti Today, This Week, This Month, atau Last Month jika tidak didukung sumber resmi.

### 7.5 Custom Period Rules

AI MUST memeriksa:

1. Start Date.
2. End Date.
3. Required Fields.
4. Date Format.
5. Minimum Date.
6. Maximum Date.
7. Maximum Date Range.
8. Future Date Restrictions.
9. Cross-month atau cross-year behavior.
10. Timezone requirements.

AI MUST NOT mengarang date range limits.

### 7.6 Date Validation

Jika HSD/BRD menetapkan rentang tanggal, AI MUST mengevaluasi:

- Start Date belum dipilih.
- End Date belum dipilih.
- Start Date setelah End Date.
- Date di luar allowed range.
- Periode tanpa data.
- Periode valid.
- Periode sedang diproses.

AI MUST menampilkan validation feedback sesuai approved rules.

AI MUST NOT mengimplementasikan validation constraints yang belum ditentukan.

### 7.7 Mandatory State Coverage

AI MUST mengevaluasi:

Default, Modal Open, Quick Select, Custom Period, Date Selected, Invalid Date, Required Error, Disabled, Loading, Success, Export Error, Empty Results, dan Access Restricted.

---

## 8. Pattern 05 — Single Data Export

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3406-47387

### 8.1 When to Use

AI MUST menggunakan Pattern 05 ketika pengguna mengekspor satu record melalui List Page atau Detail Page.

AI MUST memastikan selected record sesuai approved export scope.

### 8.2 Core Flow

AI MUST merepresentasikan:

**Start → Halaman List/Detail Data → Pilih 1 Data → Export Action sesuai reference → Sistem Memproses Export Data → Ada Masalah?**

**Tidak Ada Masalah:** Success Toast (Berhasil Diunduh) → End.

**Ada Masalah:** Tampilkan Pesan Error Sesuai Kondisi.

AI MUST memverifikasi exact Export Action node dan arah decision connectors pada official Figma reference.

### 8.3 Required UI Screens

AI MUST menghasilkan:

1. List atau Detail Page.
2. Single Record Selection State.
3. Export Action State.
4. Export Processing State.
5. Success Toast State.
6. Export Error State.
7. Disabled State jika berlaku.
8. Access Restricted State jika berlaku.
9. Record Not Found State jika berlaku.

### 8.4 Interaction Rules

AI MUST:

1. Menggunakan approved List atau Detail Page.
2. Memastikan hanya selected record yang masuk dalam export scope.
3. Menggunakan official Export Action.
4. Menampilkan Loading Feedback ketika export diproses.
5. Menampilkan Success Toast setelah success criteria terpenuhi.
6. Menampilkan Error Feedback jika proses gagal.
7. Mempertahankan navigation sesuai official pattern.

AI MUST NOT mengubah Single Data Export menjadi Bulk Export tanpa approval.

### 8.5 Mandatory State Coverage

AI MUST mengevaluasi:

Default, Hover, Focus, Record Selected, Disabled, Loading, Success, Error, Record Not Found, dan Access Restricted.

---

## 9. Mandatory UI State Generation

### 9.1 State Generation Principles

AI MUST:

1. Mengevaluasi seluruh applicable UI States berdasarkan selected pattern.
2. Menggunakan official GEMS component variants.
3. Menghasilkan UI States berdasarkan approved requirements.
4. Menentukan source screen setiap state.
5. Menentukan trigger.
6. Menentukan expected behavior.
7. Menentukan resulting state.
8. Memetakan state ke UX Flow.
9. Melaporkan states yang tidak dapat diverifikasi.

AI MUST NOT menghasilkan hanya Default dan Success State.

### 9.2 Mandatory UI State Matrix

| State | Trigger | Expected UI Output | Applicability |
|---|---|---|---|
| Default | Screen dibuka | Normal UI | All |
| Hover | Pointer pada action | Hover Variant | Applicable controls |
| Focus | Keyboard focus | Focus Indicator | Applicable controls |
| Active | Action aktif | Active Variant | If supported |
| Filter Applied | Filter diterapkan | Updated Data Context | Patterns 01–04 |
| Selected | Data atau option dipilih | Selected Variant | If applicable |
| Unselected | Selection dibatalkan | Unselected Variant | Pattern 03 |
| Modal Open | Modal dibuka | Modal Overlay | Patterns 03–04 |
| Modal Close | Modal ditutup | Return to Source | Patterns 03–04 |
| Quick Select | Preset period dipilih | Selected Preset | Pattern 04 |
| Custom Period | Custom date range dipilih | Date Range Controls | Pattern 04 |
| Validation Error | Input tidak valid | Error Feedback | If applicable |
| Disabled | Action tidak tersedia | Disabled Variant | Based on rules |
| Loading | Export diproses | Processing Feedback | All |
| Success | Export berhasil | Success Toast | All |
| Error | Export gagal | Error Feedback | All |
| Empty Data | Tidak ada data | Empty State | If applicable |
| Access Restricted | Role tidak berwenang | Permission State | Role-dependent |
| Network Error | Gangguan koneksi | Error Feedback | If applicable |
| Server Error | Gangguan sistem | Error Feedback | If applicable |

### 9.3 Default State

AI MUST menampilkan screen normal sesuai selected pattern.

AI MUST memastikan available actions, filters, data, dan permissions sesuai approved requirements.

### 9.4 Hover, Focus & Active States

AI MUST:

1. Menggunakan official GEMS variants.
2. Menjaga keyboard focus visibility.
3. Mengikuti official interaction behavior.
4. Menggunakan approved visual tokens.

AI MUST NOT membuat interaction variants baru tanpa approval.

### 9.5 Selected & Unselected States

AI MUST:

1. Menampilkan selected options secara jelas.
2. Menggunakan official selection components.
3. Mengikuti approved selection rules.
4. Mempertahankan selected values sesuai approved behavior.
5. Memastikan selected scope sesuai data yang akan diekspor.

AI MUST NOT mengarang multiple selection atau Select All.

### 9.6 Modal Open & Close States

AI MUST:

1. Menggunakan official GEMS Modal.
2. Menampilkan modal sesuai selected pattern.
3. Menampilkan approved controls.
4. Mengikuti approved Close dan Cancel behavior.
5. Mempertahankan source context.
6. Tidak menjalankan export ketika pengguna membatalkan.

### 9.7 Filter Applied State

AI MUST:

1. Menampilkan applied filters.
2. Memperbarui data sesuai approved filter behavior.
3. Mempertahankan filter values sesuai requirements.
4. Memastikan export scope mengikuti approved rules.
5. Menampilkan Empty State jika tidak ada hasil dan state tersebut berlaku.

AI MUST NOT menganggap filtered rows, selected rows, dan all records sebagai scope yang sama.

### 9.8 Validation Error State

AI MUST:

1. Memvalidasi required inputs.
2. Menggunakan approved validation constraints.
3. Menampilkan field-level error jika relevan.
4. Menggunakan official Error Feedback.
5. Mencegah invalid submission sesuai approved behavior.

AI MUST NOT mengarang mandatory fields, limits, atau error rules.

### 9.9 Disabled State

AI MUST memeriksa kondisi ketika Export Action tidak tersedia.

Kondisi yang perlu dievaluasi:

1. Role tidak memiliki permission.
2. Required selection belum valid.
3. Required period belum valid.
4. Data tidak tersedia.
5. Export sedang diproses.
6. Record tidak memenuhi eligibility.

AI MUST memvalidasi seluruh kondisi terhadap approved HSD/BRD.

AI MUST NOT menganggap daftar tersebut sebagai business rules otomatis.

### 9.10 Loading State

AI MUST:

1. Menggunakan official GEMS Loading Indicator.
2. Menampilkan processing feedback.
3. Mempertahankan konteks export.
4. Mengikuti approved duplicate-submission behavior.
5. Tidak menampilkan Success sebelum success criteria terpenuhi.
6. Menangani processing failure sesuai approved requirements.

### 9.11 Success State

AI MUST:

1. Menggunakan official GEMS Success Toast.
2. Menampilkan approved success wording.
3. Menampilkan Success setelah export berhasil sesuai success criteria.
4. Memastikan selected export scope tidak berubah tanpa alasan.
5. Mengikuti approved navigation.
6. Tidak mengklaim file berhasil diunduh jika download completion tidak dapat diverifikasi.

### 9.12 Error State

AI MUST:

1. Menggunakan official GEMS Error Feedback.
2. Menampilkan error sesuai kondisi.
3. Membedakan validation error dari processing error.
4. Mempertahankan input atau selection sesuai approved behavior.
5. Mengikuti approved recovery behavior.
6. Tidak menampilkan false success.

AI MUST NOT mengarang automatic retry, rollback, atau background recovery.

### 9.13 Empty Data State

AI MUST membedakan:

1. Tidak ada data.
2. Tidak ada hasil filter.
3. Tidak ada selected data.
4. Tidak ada data dalam selected period.
5. Data tidak tersedia karena permission.

AI MUST menggunakan official GEMS Empty State atau approved feedback sesuai konteks.

### 9.14 Access Restricted State

AI MUST mengikuti Role Access Matrix.

AI MUST memeriksa:

1. View Permission.
2. Export Permission.
3. Data Scope Permission.
4. Module Permission.
5. Field Visibility.
6. File Format Restrictions jika berlaku.

AI MUST NOT menganggap View Permission otomatis memberikan Export Permission.

### 9.15 State Coverage Reporting

AI MUST mengklasifikasikan setiap state sebagai:

- Generated.
- Not Applicable.
- Pending Requirement.
- Pending Human Approval.
- Pending Verification.

AI MUST NOT menandai unresolved state sebagai Generated.

---

## 10. Mandatory GEMS Component Usage

### 10.1 Component Requirements

AI MUST memeriksa official GEMS components yang relevan:

1. Page Header.
2. Navbar.
3. GEMS Slide Bar.
4. Table.
5. Pagination.
6. Button.
7. Button Group.
8. Dropdown / Select.
9. Checkbox.
10. Radio Button jika sesuai reference.
11. Date Picker.
12. Date Range Picker jika tersedia.
13. Filter Controls.
14. Modal.
15. Tabs jika digunakan.
16. Notification / Toast.
17. Alert.
18. Empty State.
19. Loading Indicator.
20. Tooltip.
21. Detail Information.
22. Section Footer jika sesuai reference.

AI MUST menggunakan hanya komponen yang relevan dengan selected pattern.

AI MUST NOT menganggap semua komponen wajib muncul pada setiap screen.

### 10.2 Component Retrieval

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

### 10.3 Component Integrity

AI MUST NOT:

1. Mengganti official GEMS components dengan external components.
2. Membuat custom Export Button tanpa approval.
3. Membuat custom Modal tanpa approval.
4. Mengarang component variants.
5. Mengubah component anatomy.
6. Mengubah button hierarchy.
7. Mengubah selection behavior.
8. Mengubah validation presentation secara sepihak.
9. Mengklaim custom UI sebagai official GEMS component.

### 10.4 Missing Component Handling

Jika komponen tidak tersedia, AI MUST:

1. Mengidentifikasi missing component.
2. Memeriksa official alternatives.
3. Menjelaskan limitation.
4. Mengusulkan solusi.
5. Menjelaskan dampak terhadap UX Flow dan UI Screens.
6. Meminta Human Approval sebelum implementasi komponen baru.

---

## 11. Mandatory UX Flow Diagram & UI Screen Layout

### 11.1 Required Figma Structure

AI MUST menghasilkan dua area dalam satu Figma section.

**TOP — UX FLOW DIAGRAM**

AI MUST menampilkan approved Core Flow, validation decisions, processing, success, dan error branches.

**BOTTOM — UI SCREENS & STATES**

AI MUST menampilkan seluruh UI Screens dan applicable UI States sesuai selected pattern.

AI MUST NOT menghasilkan screens tanpa flow diagram.

### 11.2 UX Flow Diagram Requirements

AI MUST:

1. Menggunakan official pattern sebagai sumber flow.
2. Menampilkan Start dan End.
3. Menampilkan entry point.
4. Menampilkan user actions.
5. Menampilkan system actions.
6. Menampilkan decision nodes.
7. Menampilkan success branch.
8. Menampilkan error branch.
9. Menampilkan navigation destination.
10. Menghubungkan seluruh nodes dengan connectors yang benar.

AI MUST memverifikasi actual connectors melalui Figma MCP.

### 11.3 UI Screen Arrangement

AI MUST:

1. Mengurutkan screens sesuai Core Flow.
2. Menempatkan modal bersama source screen.
3. Menempatkan validation states bersama relevant input.
4. Menempatkan loading state setelah export submission.
5. Menempatkan success feedback pada resulting screen.
6. Menempatkan error feedback pada source context.
7. Mengelompokkan applicable component states.
8. Menjaga alignment.
9. Menggunakan consistent spacing.
10. Menggunakan consistent frame naming.

### 11.4 Flow-to-Screen Mapping

| Flow Node | UI Representation |
|---|---|
| Start | Entry Annotation |
| Export Page | Centralized Export Screen |
| List/Data Table | List Screen |
| Detail Data | Detail Screen |
| Filter | Filter Applied State |
| Select Format | File Format Selection |
| Select Data | Data Selection Modal |
| Select Period | Period Selection Modal |
| Click Export | Export Action |
| Validation Decision | Valid / Invalid States |
| Processing | Loading State |
| Success | Success Toast |
| Error | Error Feedback |
| End | Final Flow State |

AI MUST menggunakan hanya nodes yang relevan dengan selected pattern.

AI MUST memastikan setiap flow node memiliki UI representation atau annotation yang jelas.

---

## 12. Business Rules, Data Scope & Export Permissions

### 12.1 Required Business Analysis

AI MUST mengidentifikasi:

1. Feature Name.
2. Module Name.
3. User Role.
4. Export Permission.
5. Data Visibility.
6. Export Scope.
7. Available Filters.
8. Date Range Rules.
9. Data Selection Rules.
10. File Formats.
11. Exported Fields.
12. Export Eligibility.
13. Export Limits.
14. Success Criteria.
15. Error Criteria.
16. Navigation Behavior.

### 12.2 Export Scope Rules

AI MUST membedakan:

- All Records.
- Filtered Records.
- Selected Records.
- Single Record.
- Period-based Records.
- Module/Category-based Records.

AI MUST menggunakan scope sesuai approved HSD/BRD.

AI MUST NOT mengarang export scope.

### 12.3 Filter Rules

AI MUST memeriksa:

1. Available filters.
2. Default filters.
3. Filter dependencies.
4. Filter persistence.
5. Export behavior setelah filtering.
6. Empty results behavior.

AI MUST NOT menganggap filter hanya memengaruhi tampilan tabel tanpa memeriksa dampaknya terhadap export.

### 12.4 File Format Rules

AI MUST menggunakan file formats yang ditetapkan HSD/BRD.

AI MUST NOT mengarang PDF, Excel, CSV, atau format lain sebagai supported output.

### 12.5 Data Field Rules

AI MUST:

1. Menggunakan approved exported fields.
2. Mengikuti field visibility permissions.
3. Mengikuti approved column ordering.
4. Mengikuti approved data formatting.
5. Memastikan data yang tidak berwenang diakses tidak dimasukkan ke export.

AI MUST NOT menambahkan sensitive atau restricted fields tanpa permission.

### 12.6 Export Limits

AI MUST memeriksa apakah terdapat:

1. Maximum records.
2. Maximum date range.
3. File size limits.
4. Processing limits.
5. Rate limits.
6. Export frequency restrictions.

AI MUST NOT mengarang batasan tersebut.

### 12.7 Permission Handling

AI MUST mengikuti Role Access Matrix.

AI MUST memeriksa permission berdasarkan role, module, record, dan field jika relevan.

AI MUST NOT menganggap semua role memiliki akses export yang sama.

---

## 13. AI Recommendation & Human Approval

### 13.1 Recommendation Policy

AI MAY merekomendasikan:

1. Alternative Export Pattern.
2. Better filter interaction.
3. Improved data selection.
4. Improved period selection.
5. Better validation feedback.
6. Better loading feedback.
7. Better error recovery.
8. Accessibility improvement.
9. Improved export scope visibility.
10. Improved empty state behavior.

AI MUST mendasarkan rekomendasi pada approved business requirements, usability, accessibility, atau limitation pada official pattern.

### 13.2 Recommendation Format

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

### 13.3 Mandatory Human Approval

AI MUST memperoleh explicit Human Approval sebelum:

1. Mengubah Core Flow.
2. Mengubah entry point.
3. Mengubah navigation.
4. Mengubah export scope.
5. Mengubah selection rules.
6. Mengubah period rules.
7. Mengubah validation rules.
8. Mengubah file formats.
9. Mengubah role permissions.
10. Mengubah exported fields.
11. Menambahkan export steps.
12. Menghilangkan official modal.
13. Mengubah success atau error behavior.
14. Membuat official component atau variant baru.
15. Mengimplementasikan Proposed Design.

### 13.4 Approved vs Proposed Design

AI MUST memisahkan:

**Approved Design:** Mengikuti approved HSD/BRD, official UX Pattern, dan GEMS Design System.

**Proposed Design:** Rekomendasi yang membutuhkan Human Approval.

AI MUST NOT mengimplementasikan Proposed Design sebelum disetujui.

---

## 14. Required AI Design Output

AI MUST menghasilkan output berikut.

### 14.1 Pattern Selection Report

AI MUST menyertakan:

- Feature Name.
- Selected Pattern.
- Figma Reference.
- User Role.
- Entry Point.
- Export Scope.
- Selection Rationale.

### 14.2 UX Flow Diagram

AI MUST menghasilkan approved Core Flow, decision branches, processing, success, error, dan End.

### 14.3 UI Screens

AI MUST menghasilkan screens sesuai selected pattern dan approved requirements.

### 14.4 UI State Coverage Report

AI MUST menyertakan:

- Applicable States.
- Generated States.
- Not Applicable States.
- Pending Requirement.
- Pending Human Approval.
- Pending Verification.

### 14.5 Flow-to-Screen Mapping

AI MUST memetakan flow nodes, UI Screens, UI States, dan triggers.

### 14.6 Component Usage Report

AI MUST menyertakan:

- Official GEMS components.
- Component variants.
- Component states.
- Missing components.
- Pending verification.

### 14.7 Business Compliance Report

AI MUST menyertakan:

- Export Scope.
- Filter Rules.
- Data Selection.
- Period Selection.
- File Formats.
- Export Permissions.
- Validation Rules.
- Success dan Error Behavior.

### 14.8 Human Approval Register

AI MUST mencatat proposed changes dan approval status.

### 14.9 Final Compliance Report

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

## 15. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut.

**Step 1 — Analyze HSD/BRD**

AI MUST mengidentifikasi export requirements, roles, permissions, data scope, filters, file formats, dan validation rules.

**Step 2 — Inspect All Export Data Patterns**

AI MUST memeriksa Pattern 01 sampai Pattern 05 melalui Figma MCP.

**Step 3 — Select Appropriate Pattern**

AI MUST memilih pattern berdasarkan approved requirements.

**Step 4 — Verify Approved Core Flow**

AI MUST memeriksa nodes, connectors, decisions, success, dan error branches.

**Step 5 — Inspect GEMS Design System**

AI MUST memeriksa components, properties, variants, states, dan design tokens.

**Step 6 — Identify Applicable UI States**

AI MUST mengevaluasi Default, Hover, Focus, Selected, Modal, Filter, Validation, Disabled, Loading, Success, Error, Empty, dan Access Restricted.

**Step 7 — Generate UX Flow Diagram**

AI MUST membuat visual flow pada bagian atas Figma section.

**Step 8 — Generate UI Screens**

AI MUST membuat screens sesuai selected pattern pada bagian bawah.

**Step 9 — Generate Applicable UI States**

AI MUST membuat states menggunakan official GEMS components.

**Step 10 — Validate Export Business Behavior**

AI MUST memastikan export scope, filters, selections, periods, formats, dan permissions sesuai HSD/BRD.

**Step 11 — Validate Flow-to-Screen Mapping**

AI MUST memastikan diagram, screens, states, dan navigation konsisten.

**Step 12 — Identify Gaps**

AI MUST mengidentifikasi requirement, component, flow, dan state gaps.

**Step 13 — Request Human Approval**

AI MUST meminta approval untuk proposed changes.

**Step 14 — Inspect Actual Figma Output**

AI MUST memeriksa frames, components, variants, states, layout, dan flow yang benar-benar dibuat.

**Step 15 — Generate Compliance Report**

AI MUST melaporkan hasil verifikasi dan unresolved issues.

---

## 16. AI Restrictions, Quality Assurance & Final Enforcement

### 16.1 AI Restrictions

AI MUST NOT:

1. Mengubah approved Core Flow tanpa Human Approval.
2. Menggunakan unapproved UX Pattern.
3. Mengganti official GEMS components tanpa approval.
4. Mengarang export formats.
5. Mengarang exported fields.
6. Mengarang export limits.
7. Mengarang role permissions.
8. Mengarang validation rules.
9. Mengarang period presets.
10. Mengarang multiple selection.
11. Mengarang Select All behavior.
12. Menganggap filtered data sama dengan selected data.
13. Menganggap semua record dapat diekspor.
14. Menghilangkan required selection modal.
15. Menghilangkan required period modal.
16. Menghilangkan validation decision.
17. Menghilangkan error branch.
18. Menampilkan false success.
19. Mengarang automatic retry atau rollback.
20. Menghasilkan hanya happy path.
21. Menghasilkan screens tanpa UX Flow Diagram.
22. Menghasilkan diagram yang bertentangan dengan screens.
23. Menghilangkan applicable UI States.
24. Mengimplementasikan Proposed Design tanpa approval.
25. Mengklaim custom components sebagai official GEMS components.
26. Menganggap Pending Requirement sebagai approved behavior.
27. Mengklaim desain compliant tanpa actual Figma verification.

### 16.2 Quality Assurance — Business Validation

AI MUST memverifikasi:

1. Export Scope.
2. Filter Rules.
3. Data Selection.
4. Period Selection.
5. File Formats.
6. Export Permissions.
7. Export Eligibility.
8. Validation Rules.
9. Success Criteria.
10. Error Behavior.

### 16.3 Quality Assurance — Pattern Validation

AI MUST memverifikasi:

1. Selected official pattern.
2. Correct Figma reference.
3. Entry point.
4. Flow nodes.
5. Connectors.
6. Decision branches.
7. Processing flow.
8. Success branch.
9. Error branch.
10. End state.

### 16.4 Quality Assurance — UI Validation

AI MUST memverifikasi:

1. Official GEMS components.
2. Correct variants.
3. Correct visual states.
4. Correct modal behavior.
5. Correct filter controls.
6. Correct selection controls.
7. Correct date controls.
8. Correct loading feedback.
9. Correct success feedback.
10. Correct error feedback.
11. Accessibility.
12. Flow-to-Screen Mapping.

### 16.5 Final Validation Instructions

Sebelum melaporkan completion, AI MUST:

1. Verify approved HSD/BRD.
2. Verify Role Access Matrix.
3. Verify selected Export Data Pattern.
4. Verify Core Flow integrity.
5. Verify all decision branches.
6. Verify entry point.
7. Verify export scope.
8. Verify filters.
9. Verify selection rules.
10. Verify period rules.
11. Verify file formats.
12. Verify validation states.
13. Verify disabled states.
14. Verify loading states.
15. Verify success feedback.
16. Verify error feedback.
17. Verify empty states.
18. Verify access restrictions.
19. Verify official GEMS components.
20. Verify component variants.
21. Verify UX Flow Diagram above UI Screens.
22. Verify Flow-to-Screen Mapping.
23. Verify applicable state coverage.
24. Verify Human Approval for changes.
25. Verify unresolved requirements are reported.
26. Inspect actual Figma output.
27. Generate final Compliance Report.

AI MUST NOT menandai item yang belum diverifikasi sebagai compliant.

### 16.6 Final AI Enforcement

AI MUST:

1. Analyze approved HSD/BRD.
2. Use official GEMS Export Data UX Patterns.
3. Preserve approved Core Flow.
4. Use GEMS Design System components.
5. Generate visual UX Flow Diagram.
6. Generate corresponding UI Screens.
7. Generate all applicable UI States.
8. Apply export scope rules.
9. Apply filter and selection rules.
10. Apply period validation jika berlaku.
11. Respect Role Access Matrix.
12. Handle Loading, Success, Error, Disabled, dan Empty States.
13. Maintain Flow-to-Screen consistency.
14. Identify requirement and component gaps.
15. Obtain explicit Human Approval for changes.
16. Validate actual Figma output.
17. Generate a Compliance Report.

### Final Enforcement Rule

AI MUST menggunakan approved HSD/BRD sebagai sumber business requirements, official GEMS Export Data UX Patterns sebagai sumber approved Core Flow, dan GEMS Design System sebagai sumber UI components, variants, dan states.

AI MUST menghasilkan **visual UX Flow Diagram di atas UI Screens** dalam satu Figma section dan merepresentasikan seluruh applicable UI States.

AI MUST mempertahankan validation decisions, processing states, success branches, dan error branches sesuai selected pattern.

AI MAY merekomendasikan UX improvements, additional states, alternative interactions, atau component enhancements jika didukung business requirements dan usability considerations.

AI MUST memperoleh explicit Human Approval sebelum mengimplementasikan perubahan pada approved Core Flow, navigation, export scope, validation, permissions, atau Design System.

AI MUST memverifikasi hasil aktual di Figma sebelum menyatakan desain selesai atau compliant.

**HSD/BRD defines business requirements. GEMS UX Pattern defines the approved Core Flow. GEMS Design System defines components and visual states. Human Approval authorizes changes.**
