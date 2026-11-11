# GEMS Design System — View Detail UX Pattern Guidelines

## 1. Purpose & Core Principles

View Detail merupakan UX Pattern yang digunakan untuk menampilkan informasi lengkap dari suatu data yang dipilih pengguna melalui Dashboard atau List / Data Table.

GEMS menyediakan dua View Detail UX Pattern resmi dengan entry point dan alur navigasi yang berbeda.

AI MUST menganalisis approved HSD/BRD, memilih pattern yang sesuai, menggunakan komponen resmi GEMS Design System, serta menghasilkan UX Flow Diagram dan UI Screens yang konsisten.

### 1.1 Core Principles

**1. Requirement-Based Selection**

AI MUST memilih UX Pattern berdasarkan kebutuhan bisnis, entry point, dan approved HSD/BRD, bukan preferensi visual.

**2. Official Pattern Reuse**

AI MUST menggunakan View Detail UX Pattern resmi GEMS sebagai acuan struktur dan interaksi.

**3. Flow Integrity**

AI MUST mempertahankan urutan navigasi, user action, decision point, dan behavior sesuai pattern terpilih.

**4. GEMS Component Compliance**

AI MUST menggunakan komponen resmi GEMS Design System beserta properties, variants, states, dan visual specification yang tersedia.

**5. Flow-Driven Design**

AI MUST menghasilkan UX Flow Diagram secara fisik di atas UI Screens dalam section Figma yang sama.

**6. Business Data Accuracy**

AI MUST menggunakan field, label, status, informasi, role, dan business rules dari approved HSD/BRD.

**7. Read-only by Default**

AI MUST memperlakukan View Detail sebagai tampilan informasi. AI MUST NOT menambahkan kemampuan mengubah data tanpa approved requirement.

**8. Complete State Management**

AI MUST memeriksa dan merepresentasikan seluruh UI States yang relevan, termasuk Loading, Empty, Read-only, Network Error, Server Error, dan Access Restricted.

**9. Human Approval**

AI MAY memberikan rekomendasi perubahan jika pattern tidak memenuhi kebutuhan bisnis, tetapi AI MUST memperoleh explicit Human Approval sebelum mengimplementasikannya.

### 1.2 Core Enforcement

> UX Pattern menentukan struktur dan alur interaksi. HSD/BRD menentukan kebutuhan bisnis. GEMS Design System menentukan komponen. Human Approval menentukan apakah perubahan diperbolehkan.

AI MUST NOT mengubah approved pattern, navigation, atau komponen berdasarkan asumsi.

---

## 2. Source of Truth & Pattern Selection

### 2.1 Source of Truth

| Source | Fungsi |
|---|---|
| Approved HSD/BRD | Informasi, field, status, role, dan business rules |
| GEMS View Detail UX Pattern | Entry point, navigation, flow, dan UI Screens |
| GEMS Design System | Components, properties, variants, states, dan visual specification |
| Role Access Matrix | Hak akses melihat informasi dan tindakan |
| Human Approval | Persetujuan perubahan terhadap pattern atau komponen |

AI MUST memeriksa seluruh sumber yang relevan sebelum menghasilkan desain.

AI MUST NOT mengarang field, status, permission, atau business rule.

### 2.2 Available Patterns

| Pattern | Type | Karakteristik |
|---|---|---|
| Pattern 01 | View Detail from Dashboard | Mengakses Detail Page melalui View Action pada Dashboard |
| Pattern 02 | View Detail from List / Data Table | Mengakses Detail Data melalui View Action atau Row Interaction |

### 2.3 UX Pattern Selection Matrix

| Kebutuhan | Recommended Pattern | Alasan |
|---|---|---|
| Detail diakses melalui Dashboard | Pattern 01 | Entry point berasal dari Dashboard |
| Dashboard memiliki tabel dengan tindakan View | Pattern 01 | Pengguna membuka Detail Page dari tabel Dashboard |
| Detail diakses melalui List / Data Table | Pattern 02 | Entry point berasal dari halaman daftar |
| Detail dibuka melalui View atau klik row | Pattern 02 | Mengikuti interaksi resmi pada List Data |

### 2.4 Pattern Selection Rules

AI MUST:

1. Membaca approved HSD/BRD.
2. Mengidentifikasi entry point View Detail.
3. Memeriksa kedua pattern resmi GEMS.
4. Mengidentifikasi tindakan pengguna untuk membuka detail.
5. Membandingkan kebutuhan bisnis dengan pattern.
6. Memilih pattern yang paling sesuai.
7. Mempertahankan pattern yang telah disetujui jika tersedia.
8. Menjelaskan alasan pemilihan pattern.
9. Melaporkan konflik atau ketidaksesuaian.
10. Meminta Human Approval jika diperlukan perubahan.

AI MUST NOT:

- Memilih pattern berdasarkan preferensi visual.
- Mengubah entry point tanpa approval.
- Menggabungkan kedua pattern tanpa approval.
- Membuat pattern baru tanpa approval.

---

## 3. Pattern 01 — View Detail from Dashboard

**Figma Reference:** [Pattern 01 — View Detail from Dashboard](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1269-52700&t=zv6vn5L7CsEWbtOz-1)

### 3.1 When to Use

Pattern 01 digunakan ketika pengguna mengakses Detail Page dari Dashboard melalui View Action pada tabel.

| Kondisi | Penggunaan |
|---|---|
| Entry point dari Dashboard | Recommended |
| Dashboard memiliki tabel data | Recommended |
| Detail diakses melalui icon eye | Recommended |
| Entry point dari List Data khusus | Gunakan Pattern 02 |

### 3.2 Official Main Flow

AI MUST mengikuti urutan berikut:

1. Start.
2. Dashboard.
3. Click Icon Eye di Tabel.
4. Detail Page.
5. End.

AI MUST mempertahankan urutan interaksi dan navigasi tersebut.

### 3.3 Dashboard Behavior

AI MUST:

1. Menggunakan Dashboard sebagai entry point.
2. Menampilkan informasi Dashboard sesuai HSD/BRD.
3. Menggunakan komponen resmi GEMS.
4. Menyediakan View Action melalui icon eye sesuai referensi.
5. Membuka Detail Page berdasarkan record yang dipilih.
6. Memastikan data Detail Page sesuai record tersebut.
7. Mengikuti behavior tabel dan navigasi resmi.

AI MUST NOT:

- Mengubah icon eye menjadi tindakan lain tanpa approval.
- Mengganti Dashboard dengan List Page.
- Mengubah Detail Page menjadi Modal tanpa approval.
- Menambahkan Edit atau Delete Action tanpa approved requirement.

### 3.4 Detail Page Behavior

AI MUST:

- Menggunakan struktur Detail Page resmi.
- Menampilkan field sesuai HSD/BRD.
- Menggunakan label, status, dan informasi yang disetujui.
- Mengikuti pengelompokan informasi resmi.
- Menggunakan komponen GEMS.
- Mempertahankan identitas record yang dipilih.
- Mengikuti navigasi yang disetujui.
- Mengikuti Role Access Matrix.

### 3.5 Required UI States

AI MUST memeriksa dan merepresentasikan state yang relevan:

- Dashboard Default.
- Table with Data.
- View Action.
- Detail Loading.
- Detail with Data.
- Read-only.
- Empty Data jika berlaku.
- Data Not Found jika berlaku.
- Network Error.
- Server Error.
- Access Restricted jika berlaku.

AI MUST menggunakan representasi state resmi GEMS dan approved behavior.

### 3.6 Required Design Output

AI MUST menghasilkan:

1. UX Flow Diagram di bagian atas.
2. Dashboard Screen.
3. Dashboard Table dengan View Action.
4. Detail Page.
5. UI States yang relevan.
6. Flow-to-Screen Mapping.

### 3.7 Pattern Restrictions

AI MUST NOT:

1. Mengubah Dashboard menjadi List Page.
2. Mengubah View Action tanpa approval.
3. Mengubah Detail Page menjadi Modal tanpa approval.
4. Menambahkan Edit Flow tanpa approved requirement.
5. Menambahkan Delete Flow tanpa approved requirement.
6. Mengubah navigation flow.
7. Menambahkan screen baru tanpa approval.

---

## 4. Pattern 02 — View Detail from List / Data Table

**Figma Reference:** [Pattern 02 — View Detail from List / Data Table](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1259-37460&t=zv6vn5L7CsEWbtOz-1)

### 4.1 When to Use

Pattern 02 digunakan ketika pengguna melihat detail informasi dari List / Data Table melalui View Action atau Row Interaction.

| Kondisi | Penggunaan |
|---|---|
| Entry point dari List Data | Recommended |
| Data ditampilkan dalam tabel | Recommended |
| Pengguna memilih View | Recommended |
| Pengguna membuka detail melalui klik row | Recommended |
| Entry point dari Dashboard | Gunakan Pattern 01 |

### 4.2 Official Main Flow

AI MUST mengikuti urutan berikut:

1. Start.
2. List Data.
3. Klik View / Klik Row.
4. Detail Data.
5. End.

AI MUST mempertahankan urutan interaksi dan navigasi tersebut.

### 4.3 List / Data Table Behavior

AI MUST:

1. Menggunakan List Data sebagai entry point.
2. Menggunakan Table resmi GEMS.
3. Menampilkan data sesuai HSD/BRD.
4. Menggunakan View Action atau Row Interaction sesuai approved design.
5. Membuka Detail Data berdasarkan record yang dipilih.
6. Mempertahankan identitas record.
7. Mengikuti behavior navigasi resmi.

AI MUST NOT:

- Mengubah List Data menjadi Dashboard.
- Mengganti View Action dengan Edit.
- Menambahkan interaksi baru tanpa approval.
- Mengubah tujuan navigasi.
- Menambahkan tindakan yang tidak didukung requirement.

### 4.4 Detail Data Behavior

AI MUST:

- Menggunakan struktur Detail Data resmi.
- Menampilkan informasi sesuai record yang dipilih.
- Menggunakan komponen GEMS.
- Mengikuti pengelompokan informasi yang disetujui.
- Menggunakan status dan label dari HSD/BRD.
- Mengikuti role dan permission.
- Mempertahankan konsistensi informasi antara List Data dan Detail Data.

### 4.5 Required UI States

AI MUST memeriksa dan merepresentasikan state yang relevan:

- List Default.
- Table with Data.
- View Action.
- Row Interaction.
- Detail Loading.
- Detail with Data.
- Read-only.
- Empty Data jika berlaku.
- Data Not Found jika berlaku.
- Network Error.
- Server Error.
- Access Restricted jika berlaku.

### 4.6 Required Design Output

AI MUST menghasilkan:

1. UX Flow Diagram di bagian atas.
2. List / Data Table Screen.
3. View Action atau Row Interaction.
4. Detail Data Screen.
5. UI States yang relevan.
6. Flow-to-Screen Mapping.

### 4.7 Pattern Restrictions

AI MUST NOT:

1. Mengubah List Data menjadi Dashboard.
2. Mengubah View Action tanpa approval.
3. Mengubah Detail Page menjadi Modal tanpa approval.
4. Menambahkan Edit atau Delete Flow tanpa approved requirement.
5. Menambahkan screen baru tanpa approval.
6. Mengubah urutan flow.
7. Mengubah navigation behavior.

---

## 5. Mandatory GEMS Component Usage

### 5.1 Official Component Source

**Component Reference:** [GEMS Design System — Official Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)

AI MUST menggunakan komponen resmi GEMS Design System.

### 5.2 Component Retrieval Rules

Sebelum membuat desain, AI MUST:

1. Mengakses GEMS Design System melalui Figma.
2. Memeriksa pattern yang dipilih.
3. Mengidentifikasi komponen yang digunakan.
4. Memeriksa component anatomy.
5. Memeriksa properties dan variants.
6. Memeriksa states yang tersedia.
7. Menggunakan instance resmi jika akses Figma mendukungnya.
8. Mengikuti typography, color, spacing, dan visual specification.
9. Memastikan komponen sesuai konteks.
10. Memvalidasi hasil terhadap referensi resmi.

### 5.3 Component Integrity

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
- Mengganti komponen resmi dengan tiruan custom.
- Mengubah variant atau state tanpa approval.
- Mengubah visual specification berdasarkan preferensi AI.
- Mengklaim menggunakan instance GEMS jika hanya membuat tiruan visual.

### 5.4 Missing Component Handling

Jika komponen tidak tersedia atau tidak dapat diverifikasi, AI MUST:

1. Mengidentifikasi komponen yang dibutuhkan.
2. Memeriksa alternatif resmi GEMS.
3. Melaporkan keterbatasan.
4. Memberikan rekomendasi jika diperlukan.
5. Menjelaskan dampak terhadap desain.
6. Meminta Human Approval sebelum menggunakan komponen baru atau mengubah komponen resmi.

AI MUST NOT mengimplementasikan komponen baru tanpa approval.

---

## 6. Mandatory UI States & Behavior

### 6.1 State Management Principles

Setiap desain View Detail MUST menangani seluruh kondisi interaksi yang relevan.

AI MUST NOT hanya menghasilkan Detail Default State.

AI MUST memeriksa:

- Data tersedia.
- Data tidak tersedia.
- Pengguna memilih record.
- Detail sedang dimuat.
- Detail berhasil dimuat.
- Record tidak ditemukan.
- Gangguan koneksi.
- Kesalahan sistem.
- Pengguna tidak memiliki izin akses.

### 6.2 Required State Matrix

| State | When to Use | Required Behavior |
|---|---|---|
| Default | Halaman pertama ditampilkan | Menampilkan kondisi awal |
| Table with Data | Record tersedia | Menampilkan data |
| Empty State | Tidak ada record | Menggunakan Empty State resmi |
| Hover | Pointer berada pada tindakan atau row | Menggunakan state resmi jika tersedia |
| Selected Row | Record dipilih | Mengikuti behavior tabel resmi |
| Loading | Detail sedang dimuat | Menampilkan loading feedback |
| Detail with Data | Detail berhasil dimuat | Menampilkan informasi record |
| Read-only | Data hanya dapat dilihat | Tidak menyediakan perubahan langsung |
| Data Not Found | Record tidak ditemukan | Menampilkan feedback yang sesuai |
| Network Error | Gangguan koneksi | Menampilkan feedback koneksi |
| Server Error | Kesalahan sistem | Menampilkan error feedback |
| Access Restricted | Akses tidak diizinkan | Mengikuti permission dan feedback resmi |

State merupakan kondisi interaksi yang MUST diperiksa, bukan daftar variant visual yang otomatis tersedia pada setiap komponen GEMS.

### 6.3 Default & Table with Data

AI MUST:

- Menggunakan komponen Table resmi.
- Menggunakan data dari HSD/BRD.
- Menampilkan informasi sesuai permission.
- Mengikuti struktur kolom yang disetujui.
- Menggunakan View Action sesuai pattern.

### 6.4 Hover & Selected Row

AI MUST:

- Menggunakan state resmi jika tersedia.
- Mengikuti behavior Row Interaction yang disetujui.
- Memastikan record yang dibuka sesuai tindakan pengguna.

AI MUST NOT mengarang Row Interaction baru.

### 6.5 Loading State

AI MUST:

- Menggunakan loading component atau state resmi.
- Menampilkan feedback selama pengambilan data.
- Mempertahankan konteks navigasi.
- Tidak menampilkan informasi seolah telah berhasil dimuat sebelum hasil tersedia.

### 6.6 Empty State

AI MUST:

- Menggunakan Empty State resmi GEMS.
- Menggunakan wording sesuai konteks bisnis.
- Membedakan List Empty dari Detail Data Not Found.
- Mengikuti approved behavior.

### 6.7 Read-only State

AI MUST:

- Menampilkan data sesuai hak akses.
- Tidak menyediakan input yang dapat diedit tanpa approved requirement.
- Menggunakan komponen informasi resmi.
- Mempertahankan integritas data yang ditampilkan.

### 6.8 Data Not Found

AI MUST:

- Menggunakan feedback resmi GEMS.
- Menjelaskan bahwa record tidak ditemukan.
- Mempertahankan konteks navigasi jika didukung.
- Mengikuti approved recovery behavior.

AI MUST NOT mengarang mekanisme pemulihan.

### 6.9 Network Error

AI MUST:

- Menggunakan feedback gangguan koneksi resmi.
- Mempertahankan konteks halaman.
- Mengikuti retry behavior yang disetujui.
- Tidak menampilkan data yang belum terkonfirmasi sebagai hasil terbaru.

### 6.10 Server Error

AI MUST:

- Menggunakan error feedback resmi.
- Mengikuti approved error handling.
- Mempertahankan konteks pengguna.
- Tidak mengarang kode error atau backend behavior.

### 6.11 Access Restricted

AI MUST:

- Mengikuti Role Access Matrix.
- Menampilkan hanya informasi yang diizinkan.
- Menggunakan feedback resmi jika akses ditolak.
- Tidak mengarang permission baru.

### 6.12 State Completeness Rules

AI MUST:

1. Memeriksa seluruh state yang relevan.
2. Membuat representasi UI untuk state yang berlaku dan didukung.
3. Menggunakan komponen resmi GEMS.
4. Menghubungkan state dengan screen asalnya.
5. Menjelaskan state yang tidak berlaku.
6. Mengidentifikasi state yang membutuhkan flow baru.
7. Meminta Human Approval sebelum menambahkan flow atau screen yang belum disetujui.

AI MUST NOT menghilangkan Loading, Empty, Error, atau Access Restricted jika kondisi tersebut relevan.

---

## 7. Mandatory UX Flow Diagram & Figma Layout

### 7.1 Flow-First Design

Setiap output View Detail MUST memiliki:

**Bagian Atas — UX Flow Diagram**

**Bagian Bawah — UI Screens & States**

Keduanya MUST berada dalam section Figma yang sama.

### 7.2 Figma Layout Rules

AI MUST:

1. Membuat section untuk fitur View Detail.
2. Menempatkan UX Flow Diagram secara fisik di atas UI Screens.
3. Menampilkan Main Flow sebagai jalur utama.
4. Menampilkan Alternative Flow jika tersedia pada approved pattern.
5. Menempatkan UI Screens di bawah diagram.
6. Menyusun UI Screens sesuai urutan Main Flow.
7. Menempatkan variasi state bersama screen asalnya.
8. Menggunakan nama screen dan state yang jelas.
9. Memastikan flow node dapat ditelusuri ke screen atau state.
10. Menjaga konsistensi diagram dan UI.
11. Mengikuti layout referensi GEMS.

AI MUST NOT hanya memberikan deskripsi flow dalam teks tanpa membuat diagram visual pada canvas Figma.

### 7.3 Required Flow Elements

| Element | Function | Requirement |
|---|---|---|
| Start | Awal proses | Required |
| Entry Point | Dashboard atau List Data | Required |
| View Action | Tindakan membuka detail | Required |
| Detail Screen | Informasi record | Required |
| Navigation Path | Hubungan antarflow | Required |
| End | Akhir proses | Required |
| Decision Point | Percabangan kondisi | Jika tersedia dalam approved flow |
| Alternative Flow | Jalur alternatif | Jika tersedia dalam approved flow |
| Error Handling | Kondisi kegagalan | Sesuai approved behavior |

### 7.4 Main Flow

AI MUST:

- Menggunakan Main Flow resmi GEMS.
- Mempertahankan urutan node.
- Menggunakan nama halaman sesuai HSD/BRD.
- Menggunakan tindakan pengguna sesuai pattern.
- Memastikan UI Screens mengikuti flow.

AI MUST NOT membuat Main Flow baru tanpa approval.

### 7.5 Alternative Flow

AI MUST:

- Memeriksa Alternative Flow pada referensi resmi.
- Menggunakan percabangan yang tersedia.
- Mempertahankan decision point.
- Mengikuti navigation behavior resmi.
- Memastikan Alternative Flow sesuai UI.

AI MUST NOT menambahkan percabangan baru tanpa approved requirement dan Human Approval.

### 7.6 Flow-to-Screen Mapping

| Flow Node | UI Screen / State | User Action | Expected Result |
|---|---|---|---|
| Dashboard | Dashboard Screen | Klik icon eye | Detail Page terbuka |
| List Data | List / Data Table | Klik View / Row | Detail Data terbuka |
| Detail Page | Detail Screen | Melihat informasi | Data record ditampilkan |
| Loading | Detail Loading State | Menunggu data | Data atau feedback ditampilkan |
| Error | Detail Error State | Mengikuti tindakan yang tersedia | Feedback sesuai kondisi |

AI MUST menggunakan hanya mapping yang relevan dengan pattern terpilih.

### 7.7 State & Error Flow

AI MUST memastikan setiap state relevan memiliki hubungan yang jelas dengan flow.

Jika state dapat ditampilkan melalui variasi screen yang sudah tersedia, AI MUST menggunakan screen tersebut.

Jika diperlukan screen, decision point, atau navigation baru, AI MUST:

1. Mengidentifikasi kebutuhan.
2. Menjelaskan alasan.
3. Membuat rekomendasi terpisah.
4. Menjelaskan dampak.
5. Meminta Human Approval.
6. Menunggu approval sebelum implementasi.

---

## 8. Business Data Integration

### 8.1 Data Source Matrix

| Data | Source |
|---|---|
| Feature Name | HSD/BRD |
| User Role | HSD/BRD |
| Entry Point | Approved UX Flow |
| Table Columns | HSD/BRD |
| Detail Fields | HSD/BRD |
| Data Grouping | Approved requirements |
| Status | HSD/BRD |
| Permissions | Role Access Matrix |
| Navigation | Official GEMS Pattern |
| Feedback | GEMS dan approved behavior |

### 8.2 Business Data Rules

AI MUST:

1. Menggunakan informasi sesuai HSD/BRD.
2. Menampilkan record yang dipilih.
3. Mengikuti permission.
4. Mempertahankan istilah bisnis.
5. Menggunakan status resmi.
6. Mengikuti pengelompokan informasi yang disetujui.
7. Menjaga konsistensi data antara Entry Point dan Detail Page.

AI MUST NOT:

- Mengarang field.
- Mengarang status.
- Mengarang business rules.
- Menampilkan informasi yang tidak diizinkan.
- Menambahkan tindakan tanpa requirement.
- Mengubah struktur informasi yang telah disetujui tanpa approval.

---

## 9. Pattern Recommendation & Human Approval

### 9.1 When AI May Recommend Changes

AI MAY memberikan rekomendasi ketika:

- Tidak ada pattern resmi yang memenuhi kebutuhan.
- Entry point berbeda dari pattern.
- Navigation behavior tidak sesuai kebutuhan bisnis.
- Struktur Detail Page tidak mendukung informasi yang diperlukan.
- Diperlukan tindakan atau state tambahan.
- Terdapat konflik antara HSD/BRD dan pattern resmi.

AI MUST NOT langsung mengimplementasikan rekomendasi.

### 9.2 Recommendation Workflow

**Step 1 — Identify Gap**

AI MUST mengidentifikasi ketidaksesuaian.

**Step 2 — Evaluate Official Patterns**

AI MUST memeriksa kedua pattern resmi.

**Step 3 — Recommend Adjustment**

AI MAY mengusulkan penyesuaian.

**Step 4 — Explain Impact**

AI MUST menjelaskan dampak terhadap flow, screen, state, dan navigation.

**Step 5 — Request Human Approval**

AI MUST meminta persetujuan manusia yang berwenang.

**Step 6 — Wait for Approval**

AI MUST menunggu persetujuan sebelum implementasi.

**Step 7 — Implement Approved Changes**

AI MAY menerapkan hanya perubahan yang telah disetujui.

**Step 8 — Validate**

AI MUST memvalidasi hasil terhadap HSD/BRD dan GEMS.

### 9.3 Recommendation Format

| Information | Description |
|---|---|
| Feature | Nama fitur |
| User Role | Role pengguna |
| Current Pattern | Pattern resmi |
| Figma Reference | Referensi resmi |
| Business Requirement | Kebutuhan HSD/BRD |
| Identified Gap | Ketidaksesuaian |
| Recommended Flow | Usulan penyesuaian |
| Impact | Dampak terhadap flow, screen, state, dan navigation |
| Approval Status | Pending Human Approval |

### 9.4 Approval Required

AI MUST meminta Human Approval sebelum:

1. Mengganti approved pattern.
2. Mengubah entry point.
3. Mengubah View Action.
4. Mengubah tujuan navigasi.
5. Mengganti Detail Page menjadi Modal.
6. Menambahkan Edit atau Delete Flow.
7. Menambahkan screen baru.
8. Mengubah komponen resmi.
9. Menambahkan behavior baru.
10. Mengubah approved error handling.

### 9.5 Approval Enforcement

AI MUST:

- Memisahkan Approved Flow dan Proposed Flow.
- Menjelaskan alasan perubahan.
- Menjelaskan dampaknya.
- Meminta explicit Human Approval.
- Menunggu keputusan sebelum implementasi.
- Mengikuti cakupan approval.

AI MUST NOT:

- Menganggap rekomendasi sebagai approval.
- Menganggap tidak adanya respons sebagai persetujuan.
- Menerapkan perubahan berstatus Pending.
- Mengubah bagian di luar cakupan persetujuan.

---

## 10. Required AI Design Output

Setiap permintaan View Detail MUST menghasilkan output berikut.

### Output 01 — Pattern Selection

AI MUST menjelaskan:

- Feature Name.
- User Role.
- Selected Pattern.
- Selection Rationale.
- Figma Reference.
- Requirement Compatibility.

### Output 02 — UX Flow Diagram

AI MUST menghasilkan:

- Start.
- Entry Point.
- View Action.
- Detail Page.
- Navigation Path.
- End.
- Alternative Flow jika tersedia.
- Decision Point jika berlaku.

### Output 03 — UI Screens

AI MUST menghasilkan:

- Entry Point Screen.
- View Action.
- Detail Screen.
- Seluruh UI States yang relevan.

### Output 04 — State Coverage

AI MUST memeriksa:

- Default.
- Table with Data.
- Empty.
- Hover.
- Selected Row.
- Loading.
- Detail with Data.
- Read-only.
- Data Not Found.
- Network Error.
- Server Error.
- Access Restricted.

AI MUST menjelaskan state yang tidak berlaku.

### Output 05 — Flow-to-Screen Mapping

AI MUST memastikan setiap flow node memiliki hubungan dengan UI Screen atau State.

### Output 06 — Compliance Report

AI MUST melaporkan:

- Pattern Compliance.
- Flow Compliance.
- Component Compliance.
- HSD/BRD Compliance.
- State Coverage.
- Human Approval Status.

---

## 11. Mandatory AI Execution Workflow

AI MUST mengikuti urutan berikut.

**Step 1 — Read HSD/BRD**

Identifikasi kebutuhan informasi, role, permission, dan business rules.

**Step 2 — Inspect Official Patterns**

Periksa kedua View Detail UX Pattern resmi beserta Flow Diagram dan UI Screens.

**Step 3 — Identify Entry Point**

Tentukan apakah View Detail diakses melalui Dashboard atau List / Data Table.

**Step 4 — Select Pattern**

Pilih pattern berdasarkan approved requirements.

**Step 5 — Validate Pattern Compatibility**

Pastikan entry point, View Action, Detail Screen, dan navigation sesuai kebutuhan.

**Step 6 — Retrieve GEMS Components**

Gunakan komponen, properties, variants, dan states resmi.

**Step 7 — Generate UX Flow Diagram**

Buat diagram berdasarkan pattern terpilih.

**Step 8 — Generate UI Screens**

Buat seluruh screens sesuai flow.

**Step 9 — Generate UI States**

Buat representasi state yang relevan.

**Step 10 — Validate Flow-to-Screen Mapping**

Pastikan seluruh flow node, user action, screen, dan state konsisten.

**Step 11 — Request Human Approval if Needed**

Ajukan rekomendasi jika diperlukan perubahan.

**Step 12 — Generate Compliance Report**

Laporkan hasil validasi, keterbatasan, dan approval status.

---

## 12. AI Restrictions

AI MUST NOT:

1. Membuat View Detail Pattern baru tanpa approval.
2. Menggabungkan pattern tanpa approval.
3. Mengubah approved entry point.
4. Mengubah View Action.
5. Mengubah navigation flow.
6. Mengubah Detail Page menjadi Modal tanpa approval.
7. Menambahkan Edit Flow tanpa approved requirement.
8. Menambahkan Delete Flow tanpa approved requirement.
9. Menambahkan screen baru tanpa approval.
10. Membuat UI tanpa UX Flow Diagram.
11. Membuat UX Flow Diagram yang tidak sesuai UI.
12. Mengarang field atau status.
13. Mengarang role atau permission.
14. Menggunakan komponen non-GEMS.
15. Mengubah komponen resmi tanpa approval.
16. Menghilangkan state yang relevan.
17. Mengimplementasikan Proposed Flow sebelum approval.
18. Menganggap screenshot contoh sebagai izin mengubah pattern.
19. Menyatakan desain compliant tanpa verifikasi.

---

## 13. Quality Assurance & Compliance

### 13.1 Requirement Compliance

AI MUST memastikan:

1. Seluruh informasi berasal dari approved HSD/BRD.
2. Role dan permission sesuai Role Access Matrix.
3. Status dan label sesuai kebutuhan bisnis.
4. Detail Data sesuai record yang dipilih.
5. Business flow tidak berubah.

### 13.2 Pattern Compliance

AI MUST memastikan:

1. Pattern yang dipilih merupakan salah satu dari dua pattern resmi.
2. Entry point sesuai kebutuhan.
3. View Action mengikuti referensi.
4. Navigation flow sesuai pattern.
5. Detail Screen mengikuti struktur yang disetujui.

### 13.3 Flow Compliance

AI MUST memastikan:

1. UX Flow Diagram telah dibuat.
2. Flow Diagram berada di atas UI Screens.
3. Main Flow lengkap.
4. Alternative Flow yang berlaku telah diperiksa.
5. UI Screens mengikuti urutan flow.
6. Seluruh flow node sesuai dengan screen atau state.

### 13.4 Component Compliance

AI MUST memastikan:

1. Seluruh komponen menggunakan GEMS Design System.
2. Properties dan variants sesuai referensi.
3. States menggunakan spesifikasi resmi.
4. Visual specification tidak berubah.
5. Komponen telah diverifikasi terhadap Figma.

### 13.5 State Completeness

AI MUST memastikan:

1. Seluruh state yang relevan telah diidentifikasi.
2. Loading State tersedia jika berlaku.
3. Empty State tersedia jika berlaku.
4. Read-only Behavior sesuai requirement.
5. Error State mengikuti GEMS.
6. Access Restricted mengikuti Role Access Matrix.
7. State memiliki hubungan dengan UI Screen yang sesuai.

### 13.6 Human Approval Compliance

AI MUST memastikan:

1. Seluruh perubahan terhadap approved pattern telah diidentifikasi.
2. Rekomendasi dipisahkan dari implementasi.
3. Human Approval diperoleh sebelum perubahan.
4. Perubahan berstatus Pending tidak diimplementasikan.
5. Hasil akhir mengikuti cakupan approval.

### 13.7 Final Validation Instructions

Before completing the design, AI MUST:

1. **Verify HSD/BRD Compliance** — Memastikan seluruh kebutuhan bisnis telah diperiksa dan diterapkan sesuai approved HSD/BRD.
2. **Verify UX Pattern Selection** — Memastikan pattern yang dipilih sesuai kebutuhan dan referensi resmi GEMS.
3. **Verify UX Flow Diagram** — Memastikan UX Flow Diagram telah dibuat secara lengkap dan ditempatkan di atas UI Screens.
4. **Verify UI Screens** — Memastikan seluruh UI Screens sesuai dengan Main Flow dan Alternative Flow yang berlaku.
5. **Verify GEMS Components** — Memastikan seluruh komponen menggunakan instance resmi GEMS beserta properties, variants, dan states yang sesuai.
6. **Verify UI State Coverage** — Memastikan seluruh state yang relevan telah diperiksa dan direpresentasikan.
7. **Verify Flow-to-Screen Mapping** — Memastikan setiap flow node, user action, screen, dan expected result saling sesuai.
8. **Verify Role & Permissions** — Memastikan seluruh informasi dan tindakan sesuai Role Access Matrix.
9. **Verify Human Approval** — Memastikan setiap perubahan terhadap approved pattern, flow, atau komponen telah memperoleh explicit Human Approval.
10. **Generate Compliance Report** — Menghasilkan laporan akhir yang mencakup hasil validasi, ketidaksesuaian, keterbatasan, dan approval status.

**Final Validation Rule:**

AI MUST NOT mark the design as completed, approved, or GEMS-compliant until all applicable validation requirements have been verified.

Any unresolved issue MUST be documented and reported for Human Review.

---

## 14. Final AI Enforcement

AI MUST:

1. Membaca approved HSD/BRD.
2. Memeriksa kedua View Detail UX Pattern resmi GEMS.
3. Memilih pattern berdasarkan entry point dan kebutuhan bisnis.
4. Menggunakan Flow Diagram resmi sebagai acuan.
5. Menempatkan UX Flow Diagram di atas UI Screens.
6. Menghasilkan seluruh UI Screens yang diperlukan.
7. Menggunakan komponen resmi GEMS.
8. Menghasilkan seluruh UI States yang relevan.
9. Mempertahankan navigation dan interaction behavior.
10. Menggunakan data bisnis yang disetujui.
11. Memastikan Flow-to-Screen Mapping sesuai.
12. Meminta Human Approval sebelum perubahan.
13. Memvalidasi hasil terhadap HSD/BRD dan GEMS.
14. Menghasilkan Compliance Report.

### Final Enforcement Rule

> AI MUST select the appropriate official GEMS View Detail UX Pattern based on approved HSD/BRD and the user's entry point. Every design MUST include a complete UX Flow Diagram positioned above its corresponding UI Screens, with all applicable UI States. All UI components MUST originate from the official GEMS Design System. AI MUST NOT modify the approved pattern, navigation, components, or interaction behavior without explicit Human Approval.

**GEMS UX Pattern menentukan alur. GEMS Design System menentukan komponen. HSD/BRD menentukan kebutuhan bisnis. Human Approval menentukan apakah perubahan diperbolehkan.**
