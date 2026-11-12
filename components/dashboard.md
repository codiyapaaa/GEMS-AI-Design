# GEMS AI — Dashboard Design Generation

**Execution:** Claude AI + Figma MCP  
**Instruction Type:** Mandatory AI Execution Rules  
**Governance:** Human-in-the-Loop

## 1. Input & References

### 1.1 Target Figma — Design Destination

**Target Figma:** `[UPLOAD / MASUKKAN LINK FIGMA TUJUAN]`

Target Figma merupakan lokasi utama pembuatan dashboard. AI wajib menghasilkan desain langsung pada file tujuan yang diberikan.

### 1.2 Dashboard Requirements

**HSD / BRD / Dataset / Direct Task:**  
`[UPLOAD FILE / MASUKKAN LINK / TULIS INSTRUKSI]`

AI harus menerima satu atau beberapa sumber berikut:

- File upload: PDF, DOCX, XLSX, CSV, atau format yang didukung.
- Link: Google Docs, Google Sheets, atau dokumen lain yang dapat diakses.
- GitHub: Repository, folder, file Markdown, atau ZIP.
- Direct Task: Instruksi dashboard dalam bentuk teks.

Jika sumber tidak dapat diakses, AI wajib meminta akses, link yang valid, atau file upload sebelum melanjutkan. AI dilarang mengarang isi sumber yang tidak terbaca.

### 1.3 Official GEMS Design System

[GEMS Design System — Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System)

### 1.4 Additional Guidelines — GitHub

**Repository:** [GEMS AI Design — GitHub](https://github.com/codiyapaaa/GEMS-AI-Design)

| Guideline | GitHub Link |
|---|---|
| Dashboard Guidelines | [dashboard.md](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/guidelines/dashboard.md) |
| Design Guidelines | [design-guideline.md](https://github.com/codiyapaaa/GEMS-AI-Design/blob/main/guidelines/design-guideline.md) |
| Components | [components/](https://github.com/codiyapaaa/GEMS-AI-Design/tree/main/components) |
| UX Patterns | [ux-patterns/](https://github.com/codiyapaaa/GEMS-AI-Design/tree/main/guidelines/ux-patterns) |

AI MUST membaca isi guideline yang relevan, bukan hanya nama file. Jika path berbeda atau tidak tersedia, AI MUST memeriksa struktur repository dan meminta klarifikasi jika diperlukan.

## 2. Official GEMS Chart Components

AI MUST memeriksa komponen berikut melalui Figma MCP sebelum menentukan visualisasi.

| Component | Figma Reference | Recommended Use |
|---|---|---|
| Line and Bar Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-4196) | Trend & comparison |
| Pie Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=786-2005) | Data proportion |
| Chart Data | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3302) | Chart elements |
| Activity Gauge | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3540) | Target achievement |
| Radar Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3666) | Multidimensional comparison |
| Vertical Bar Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19393) | Category comparison |
| Horizontal Bar Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19715) | Ranking |
| Line Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19714) | Time-series trend |
| Bar & Line Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-18667) | Related metrics |
| Doughnut Chart | [View Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19848) | Data distribution |

AI MUST memilih komponen berdasarkan karakteristik data, analytical purpose, dan usability. AI MUST NOT menggunakan seluruh chart jika tidak diperlukan.

## 3. Dashboard Design References

AI MUST mempelajari referensi berikut untuk memahami penerapan information hierarchy, KPI Cards, Charts, Filters, Tables, dan dashboard layout.

| Dashboard | Figma Reference |
|---|---|
| Fuel Management | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=757-34567) |
| Main Dashboard | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=4233-207299) |
| Dashboard Visit | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3585-249006) |
| Dashboard Accommodation | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3613-91801) |
| Meals Management | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3599-87213) |
| Transport Dashboard | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3613-90610) |
| Laundry Dashboard 01 | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3585-261583) |
| Laundry Dashboard 02 | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3475-147760) |
| Charging Station | [View Figma](https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=619-23490) |
| HRGA Dashboard | [View Figma](https://www.figma.com/design/v3ggUUZOrTe6dh9wJ21Hcy/ISS-Registrasi-Asset?node-id=576-138623) |

AI MUST menggunakan referensi sebagai acuan UX dan visual composition, bukan menyalin desain tanpa mempertimbangkan kebutuhan bisnis.

## 4. Mandatory Execution Workflow

### Phase 01 — Data Analysis

AI MUST:

1. Membaca seluruh dokumen, dataset, atau direct task yang diberikan.
2. Mengidentifikasi tujuan dashboard, target users, dan business needs.
3. Menganalisis available data, KPI, metrics, trends, comparisons, distributions, dan detailed records.
4. Menentukan data source, unit, calculation, aggregation, dan time dimension.
5. Memilih informasi paling penting berdasarkan relevansi dan manfaat bagi pengguna.
6. Mengidentifikasi missing data, conflicting requirements, dan informasi yang membutuhkan klarifikasi.
7. Menyusun **Data Summary** yang singkat, jelas, dan terstruktur.
8. Memberikan rekomendasi informasi yang layak ditampilkan beserta alasannya.
9. Meminta Human Approval terhadap Data Summary.

**STOP — HUMAN APPROVAL #1 REQUIRED**

AI MUST NOT melanjutkan ke Design Planning sebelum Data Summary disetujui manusia.

### Phase 02 — Design Planning

Setelah Data Summary disetujui, AI MUST:

1. Membaca Dashboard Guidelines, Design Guidelines, dan Components Documentation.
2. Memeriksa official GEMS Design System melalui Figma MCP.
3. Mengidentifikasi KPI Cards, Charts, Tables, Filters, dan supporting components yang tersedia.
4. Memilih visualisasi paling efektif berdasarkan approved data.
5. Menentukan information hierarchy, layout structure, grouping, dan component placement.
6. Menentukan global filters, component-specific filters, dan time-based filters jika relevan.
7. Menentukan applicable UI States, interactions, dan responsive behavior.
8. Menggunakan Dashboard Design References untuk mempertimbangkan pola layout yang sesuai.
9. Menyusun **Dashboard Design Plan** berisi layout, component selection, visualization, filters, states, dan alasan rekomendasi.
10. Meminta Human Approval terhadap Dashboard Design Plan.

**STOP — HUMAN APPROVAL #2 REQUIRED**

AI MUST NOT menghasilkan desain Figma sebelum Dashboard Design Plan disetujui manusia.

### Phase 03 — Figma Design Generation

Setelah Design Plan disetujui, AI MUST:

1. Mengakses Target Figma menggunakan Figma MCP.
2. Membuat desain dashboard langsung pada Target Figma.
3. Menggunakan official GEMS component instances dan variants.
4. Mengimplementasikan approved KPI Cards, Charts, Tables, Filters, dan layout.
5. Menggunakan official design tokens, typography, colors, spacing, dan icons.
6. Membuat applicable UI States sesuai approved Design Plan.
7. Mengikuti approved UX Patterns untuk interactions jika diperlukan.
8. Menempatkan UX Flow di atas screens jika dashboard memiliki flow yang relevan.
9. Menjaga existing designs agar tidak berubah tanpa persetujuan.
10. Memberikan link langsung ke hasil desain pada Target Figma.

AI MUST NOT membuat desain pada file lain tanpa Human Approval.

Jika Figma MCP tidak mendukung operasi yang diperlukan, AI MUST menjelaskan keterbatasannya dan meminta persetujuan sebelum menggunakan alternatif.

## 5. Intelligent Visualization Rules

AI MUST memilih visualisasi berdasarkan tujuan analisis berikut:

| Analytical Need | Recommended Component |
|---|---|
| Single important value | KPI Card |
| Trend over time | Line Chart |
| Category comparison | Vertical Bar Chart |
| Ranking / Long Labels | Horizontal Bar Chart |
| Part-to-whole distribution | Pie / Doughnut Chart |
| Target achievement | Activity Gauge |
| Related metrics | Bar & Line Chart |
| Multidimensional comparison | Radar Chart |
| Detailed records | Data Table |

AI MUST:

1. Memilih visualisasi paling sederhana yang mampu menyampaikan informasi secara efektif.
2. Memastikan data, labels, units, legends, dan scales mudah dipahami.
3. Menggunakan chart hanya jika memberikan analytical value.
4. Memastikan perbandingan data menggunakan unit dan periode yang kompatibel.
5. Mempertimbangkan Data Table jika pengguna membutuhkan exact values.
6. Menggunakan komponen GEMS yang tersedia.

AI MUST NOT:

1. Menggunakan chart sebagai dekorasi.
2. Mengarang KPI, targets, formulas, atau historical data.
3. Menampilkan misleading visualizations.
4. Menggunakan Gauge tanpa target valid.
5. Menampilkan percentage tanpa calculation yang jelas.
6. Menganggap missing data sebagai zero.
7. Membuat custom chart tanpa Human Approval.

## 6. Dashboard Layout & Filters

AI MUST:

1. Menempatkan Primary KPI dan informasi terpenting pada hierarki utama.
2. Mengelompokkan related metrics secara logis.
3. Menyusun KPI Cards, Charts, Tables, dan Filters berdasarkan user needs.
4. Menggunakan official GEMS grid, spacing, alignment, dan typography.
5. Menentukan filter berdasarkan available data dan approved requirements.
6. Mempertimbangkan Daily, Weekly, Monthly, Yearly, dan Custom Range jika relevan.
7. Menentukan filter scope dan dependencies.
8. Memastikan perubahan filter konsisten terhadap related components.
9. Mempertimbangkan missing periods, partial data, dan no results.
10. Menghindari dashboard yang terlalu padat atau redundant.

AI MUST NOT membuat filter, metric, atau comparison yang tidak memiliki dasar kebutuhan.

## 7. UI States & UX Interactions

AI MUST membuat seluruh applicable UI States:

- Default / Available Data.
- Loading / Skeleton.
- Empty Data.
- No Filter Results.
- Zero Value / Missing Data.
- Partial Data.
- Error / Network Error.
- Filter Applied / Reset.
- Hover / Focus / Selected.
- Disabled / Access Restricted.
- Confirmation / Success / Cancel jika diperlukan.

AI MUST:

1. Mengikuti official GEMS component states dan variants.
2. Menggunakan approved UX Patterns jika dashboard memiliki interactions atau CRUD.
3. Menampilkan contextual feedback sesuai tindakan pengguna.
4. Mempertimbangkan role-based permissions.
5. Memastikan interactions konsisten dengan approved Design Plan.

AI MUST NOT membuat navigation, CRUD, atau business interactions di luar approved requirements.

## 8. Design System Enforcement

AI MUST:

1. Menggunakan GEMS Design System sebagai sumber utama UI components.
2. Membaca component documentation yang relevan dari GitHub.
3. Memeriksa component anatomy, variants, properties, dan states melalui Figma MCP.
4. Menggunakan official component instances, bukan membuat ulang komponen yang sudah tersedia.
5. Menggunakan official colors, typography, spacing, dan design tokens.
6. Meminta Human Approval jika komponen yang dibutuhkan belum tersedia.
7. Mengikuti approved GEMS UX Patterns.

AI MUST NOT:

1. Membuat custom components tanpa approval.
2. Mengubah official component anatomy.
3. Menggunakan unapproved design tokens.
4. Mengganti komponen GEMS dengan komponen lain tanpa persetujuan.
5. Mengabaikan guidelines yang telah diberikan.

## 9. Human Approval & Change Control

AI MUST:

1. Meminta **Human Approval #1** untuk Data Summary.
2. Meminta **Human Approval #2** untuk Dashboard Design Plan.
3. Berhenti dan menunggu explicit approval pada setiap approval gate.
4. Memisahkan Approved, Proposed, dan Pending Decisions.
5. Meminta approval tambahan jika terdapat perubahan business rules, metrics, calculations, permissions, UX Flow, atau GEMS components.
6. Mengajukan ulang bagian yang berubah secara material sebelum implementasi.

AI MAY memberikan UX recommendations dan alternative solutions.

AI MUST NOT mengimplementasikan perubahan yang belum disetujui.

## 10. Final Execution Rules

**Mandatory Sequence:**

`Read Input & References → Analyze Data → Data Summary → Human Approval #1 → Inspect GEMS Components → Select Visualizations & Layout → Dashboard Design Plan → Human Approval #2 → Generate Dashboard in Target Figma`

AI MUST:

1. Menjalankan workflow secara berurutan.
2. Mengutamakan data accuracy, usability, information hierarchy, dan effective visualization.
3. Menggunakan approved GEMS components dan guidelines.
4. Mengikuti seluruh Human Approval requirements.
5. Menghasilkan actual dashboard design langsung pada Target Figma.
6. Memberikan link hasil desain yang benar-benar dibuat.

AI MUST NOT:

1. Melewati Human Approval.
2. Langsung membuat desain sebelum Data Summary dan Design Plan disetujui.
3. Mengarang requirements, data, atau metrics.
4. Menggunakan unapproved components.
5. Mengubah approved decisions secara sepihak.
6. Mengklaim desain telah dibuat jika Figma MCP belum berhasil membuatnya.

**FINAL RULE: Data determines information. GEMS determines components. Human Approval authorizes decisions. Target Figma determines the design destination.**
