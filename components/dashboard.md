# GEMS AI Design Guidelines — Dashboard Design

## 1. Mandatory AI Instructions

AI MUST menghasilkan desain dashboard berdasarkan approved HSD/BRD, data yang diberikan, direct user requirements, official GEMS Design System, dan Human Approval.

AI MUST:

1. Membaca seluruh dokumen atau instruksi task sebelum merencanakan dashboard.
2. Mengidentifikasi tujuan bisnis, target pengguna, keputusan yang perlu didukung, dan informasi yang diperlukan.
3. Menganalisis data untuk menentukan KPI, metrics, trends, distributions, comparisons, dan detailed records yang relevan.
4. Menyusun **Dashboard Data Summary** yang ringkas, jelas, dan berorientasi pada kebutuhan pengguna.
5. Meminta **Human Approval untuk Data & KPI** sebelum memilih komponen visualisasi dan menyusun desain.
6. Memeriksa official GEMS Design System melalui Figma MCP setelah data disetujui.
7. Merekomendasikan visualisasi paling efektif berdasarkan karakteristik data, menggunakan KPI Card, Chart, Table, atau komponen resmi lain yang sesuai.
8. Menentukan informasi yang perlu diprioritaskan, dibandingkan, atau ditampilkan secara detail.
9. Menyusun dashboard layout berdasarkan information hierarchy, usability, readability, dan task efficiency.
10. Mempertimbangkan daily, weekly, monthly, yearly, dan custom-period data sesuai requirements.
11. Menghasilkan seluruh applicable UI States, termasuk Loading, Empty Data, No Results, Error, dan Filter Applied.
12. Mengevaluasi interaction behavior, drill-down, navigation, dan applicable CRUD operations.
13. Menyusun **Dashboard Design Plan** untuk Human Review.
14. Meminta **Human Approval kedua** sebelum menghasilkan final UI Screens di Figma.
15. Menggunakan hanya approved GEMS components, variants, states, dan design tokens.
16. Memvalidasi hasil desain aktual terhadap approved Data Summary dan Design Plan.
17. Menghasilkan final Compliance Report.

AI MUST NOT:

1. Langsung menghasilkan dashboard sebelum Data & KPI Approval dan Dashboard Design Plan Approval.
2. Mengarang data, KPI values, target, percentage, atau business metrics.
3. Memilih chart hanya berdasarkan visual appearance.
4. Menggunakan semua jenis chart tanpa alasan analitis.
5. Menampilkan informasi yang tidak relevan dengan kebutuhan pengguna.
6. Mengubah approved data definitions tanpa Human Approval.
7. Membuat komponen baru di luar GEMS Design System tanpa Human Approval.
8. Menganggap seluruh dashboard membutuhkan struktur layout yang sama.
9. Menghasilkan hanya Default State.
10. Mengklaim dashboard compliant tanpa memverifikasi hasil aktual di Figma.

---

## 2. Source of Truth & Design Governance

AI MUST menggunakan sumber berikut sesuai kewenangannya.

| Source | Responsibility |
|---|---|
| Approved HSD/BRD | Business requirements, metrics, calculations, roles, permissions |
| User Task / Direct Instructions | Dashboard objectives, requested information, constraints |
| Provided Dataset | Available fields, records, values, time coverage |
| GEMS Design System | Components, variants, states, design tokens |
| Approved Dashboard References | Layout, visualization composition, information hierarchy |
| Role Access Matrix | Dashboard visibility, data permissions, actions |
| Human Approval | Authorization for data selection, design plans, and changes |

AI MUST memisahkan:

- Source-confirmed data.
- Calculated data.
- Proposed metrics.
- Missing data.
- Assumptions requiring validation.

AI MUST NOT menganggap contoh dummy data sebagai actual business data.

Jika terdapat konflik antar-sumber, AI MUST mengidentifikasi konflik, menjelaskan dampaknya, dan meminta Human Review.

---

## 3. Mandatory Dashboard Design Workflow

AI MUST mengikuti workflow berikut secara berurutan.

### Phase 01 — Requirement & Data Analysis

1. Read HSD/BRD or user task.
2. Identify dashboard objectives.
3. Identify user roles.
4. Identify business questions.
5. Identify available datasets.
6. Identify required metrics.
7. Identify calculation rules.
8. Identify available time dimensions.
9. Identify data gaps.
10. Generate Dashboard Data Summary.

**STOP — Request Human Approval #1.**

AI MUST NOT melanjutkan ke final visualization planning sebelum Data Summary disetujui.

### Phase 02 — Visualization & Design Planning

Setelah Data Summary disetujui, AI MUST:

1. Inspect official GEMS Design System.
2. Inspect available chart components.
3. Analyze each approved metric.
4. Recommend the most effective visualization.
5. Identify required KPI Cards.
6. Identify required Charts.
7. Identify required Tables.
8. Define information hierarchy.
9. Define dashboard sections.
10. Define filters and time-based behavior.
11. Define applicable UI States.
12. Define applicable interactions and CRUD flows.
13. Review dashboard reference examples.
14. Generate Dashboard Design Plan.

**STOP — Request Human Approval #2.**

AI MUST NOT menghasilkan final dashboard design sebelum Design Plan disetujui.

### Phase 03 — Figma Design Generation

Setelah kedua approval diberikan, AI MUST:

1. Generate dashboard UI directly in Figma.
2. Use approved GEMS components.
3. Follow approved Dashboard Design Plan.
4. Generate all required visualization sections.
5. Generate applicable UI States.
6. Generate approved interactions and related screens.
7. Verify actual Figma components.
8. Verify layout and data representation.
9. Generate Compliance Report.
10. Provide final Figma design link.

AI MUST NOT mengubah approved metrics atau visualization plan secara sepihak selama generation.

---

## 4. Dashboard Data Analysis

### 4.1 Identify Business Objectives

AI MUST mengidentifikasi:

1. Dashboard purpose.
2. Target user roles.
3. Main business questions.
4. Operational monitoring needs.
5. Decision-making requirements.
6. Reporting requirements.
7. Data refresh requirements jika tersedia.
8. Required user actions.

AI MUST mengutamakan informasi yang membantu pengguna memahami kondisi, menemukan masalah, dan mengambil keputusan.

### 4.2 Identify Data Structure

AI MUST memeriksa:

1. Dataset name.
2. Data source.
3. Available fields.
4. Field types.
5. Unique identifiers.
6. Date and time fields.
7. Categories.
8. Numeric measures.
9. Status values.
10. Relationships between datasets.
11. Missing values.
12. Data completeness.
13. Data granularity.
14. Historical coverage.

AI MUST NOT menganggap semua dataset memiliki data historis.

### 4.3 Identify Dashboard Metrics

AI MUST mengevaluasi kebutuhan:

- Total values.
- Counts.
- Averages.
- Percentages.
- Ratios.
- Status distributions.
- Trends.
- Comparisons.
- Rankings.
- Target achievements.
- Exceptions.
- Operational records.

AI MUST hanya merekomendasikan metrics yang relevan dan dapat didukung oleh data.

### 4.4 Metric Definition Rules

Untuk setiap metric, AI MUST mengidentifikasi:

1. Metric Name.
2. Business Definition.
3. Source Field.
4. Calculation Method.
5. Unit.
6. Aggregation Method.
7. Time Dimension.
8. Filter Dependencies.
9. Data Availability.
10. Business Relevance.

AI MUST NOT membuat formula atau KPI target tanpa approved requirement.

---

## 5. Dashboard Data Summary & Human Approval #1

### 5.1 Mandatory Data Summary

AI MUST menghasilkan ringkasan yang singkat, jelas, dan mudah diperiksa manusia.

AI MUST menghindari daftar metrik berlebihan yang tidak mendukung dashboard objectives.

### 5.2 Required Summary Format

AI MUST menggunakan format berikut:

| Priority | Metric / Information | Purpose | Data Source | Calculation | Availability |
|---|---|---|---|---|---|
| Primary | [Metric] | [Business purpose] | [Source] | [Rule] | [Status] |
| Secondary | [Metric] | [Business purpose] | [Source] | [Rule] | [Status] |
| Supporting | [Information] | [Business purpose] | [Source] | [Rule] | [Status] |

AI MUST mengklasifikasikan:

**Primary:** Informasi terpenting untuk memahami kondisi atau mengambil keputusan.

**Secondary:** Informasi untuk analisis, perbandingan, dan monitoring.

**Supporting:** Detail pendukung yang membantu investigasi atau tindak lanjut.

### 5.3 Data Availability Classification

AI MUST menandai data sebagai:

- Available.
- Calculable.
- Requires Clarification.
- Missing.
- Proposed.

AI MUST NOT menandai proposed metric sebagai approved.

### 5.4 Mandatory Approval Questions

AI MUST meminta manusia memvalidasi:

1. Apakah informasi yang dipilih sudah sesuai kebutuhan?
2. Apakah ada KPI yang perlu ditambah atau dihapus?
3. Apakah definisi dan perhitungan metric sudah benar?
4. Apakah prioritas informasi sudah tepat?
5. Apakah periode dan filter yang diperlukan sudah sesuai?

AI MUST menunggu explicit approval.

Jika terdapat revisi, AI MUST memperbarui Data Summary dan meminta persetujuan ulang.

---

## 6. Official GEMS Chart Component References

AI MUST memeriksa official chart components berikut melalui Figma MCP.

### 6.1 Line and Bar Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-4196

AI MAY merekomendasikan komponen ini untuk trends atau comparisons sesuai supported chart variants.

### 6.2 Pie Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=786-2005

AI MAY merekomendasikan Pie Chart untuk part-to-whole comparisons dengan jumlah kategori yang mudah dibaca.

### 6.3 Chart Data

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3302

AI MUST memeriksa supported chart elements, axes, labels, dan properties sebelum menggunakannya.

### 6.4 Activity Gauge

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3540

AI MAY merekomendasikan Activity Gauge untuk progress atau achievement terhadap target yang terdefinisi.

### 6.5 Radar Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3666

AI MAY merekomendasikan Radar Chart untuk perbandingan beberapa dimensi dengan skala yang kompatibel.

### 6.6 Vertical Bar Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19393

AI MAY merekomendasikan Vertical Bar Chart untuk perbandingan kategori atau periode.

### 6.7 Horizontal Bar Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19715

AI MAY merekomendasikan Horizontal Bar Chart untuk rankings dan kategori dengan label panjang.

### 6.8 Line Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19714

AI MAY merekomendasikan Line Chart untuk time-series trends.

### 6.9 Bar & Line Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-18667

AI MAY merekomendasikan kombinasi Bar & Line Chart untuk membandingkan metrik yang saling berkaitan.

### 6.10 Doughnut Chart

**Figma Reference:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2339-19848

AI MAY merekomendasikan Doughnut Chart untuk distribusi kategori dan komposisi.

### 6.11 Component Verification

AI MUST:

1. Inspect component structure.
2. Inspect component variants.
3. Inspect supported chart styles.
4. Inspect legends.
5. Inspect axis labels.
6. Inspect chart colors.
7. Inspect data labels.
8. Inspect responsive properties.
9. Inspect available states.
10. Use official GEMS instances.

AI MUST NOT membuat custom chart hanya karena official component memerlukan penyesuaian.

---

## 7. Intelligent Visualization Selection Rules

AI MUST memilih visualisasi berdasarkan **analytical purpose, data structure, readability, dan user needs**.

### 7.1 Visualization Decision Matrix

| Analytical Need | Preferred Visualization | Selection Reason |
|---|---|---|
| Single important value | KPI / Value Card | Membaca nilai secara cepat |
| Time-based trend | Line Chart | Melihat perubahan dari waktu ke waktu |
| Category comparison | Bar Chart | Membandingkan nilai |
| Ranking | Horizontal Bar Chart | Memudahkan perbandingan kategori |
| Part-to-whole | Pie / Doughnut Chart | Melihat proporsi |
| Target achievement | Activity Gauge / KPI Card | Melihat pencapaian |
| Two related measures | Bar & Line Chart | Membandingkan metrik terkait |
| Multiple comparable dimensions | Radar Chart | Melihat profil beberapa dimensi |
| Detailed records | Data Table | Membaca data secara presisi |
| Multiple summary metrics | KPI Card Group | Monitoring cepat |

AI MUST memeriksa ketersediaan official GEMS component sebelum menetapkan pilihan.

### 7.2 KPI Card Selection

AI MUST menggunakan KPI Card ketika informasi lebih efektif disampaikan sebagai nilai tunggal.

AI MUST mempertimbangkan:

1. Metric title.
2. Primary value.
3. Unit.
4. Comparison period.
5. Trend indicator jika tersedia.
6. Supporting context.
7. Data freshness jika relevan.

AI MUST NOT menambahkan trend indicator tanpa comparison data.

### 7.3 Line Chart Selection

AI MUST memprioritaskan Line Chart ketika tujuan utamanya adalah memahami perubahan nilai sepanjang waktu.

AI MUST memastikan:

1. Time dimension tersedia.
2. Time intervals konsisten.
3. Data aggregation sesuai.
4. Axis labels jelas.
5. Missing periods ditangani dengan benar.

AI MUST NOT menghubungkan missing values seolah-olah terdapat observasi nyata.

### 7.4 Bar Chart Selection

AI MUST menggunakan Bar Chart untuk perbandingan nilai antar kategori atau periode ketika representasi tersebut paling mudah dibaca.

AI MUST:

1. Memilih orientation berdasarkan jumlah dan panjang label.
2. Menggunakan baseline yang tidak menyesatkan.
3. Mengurutkan kategori sesuai analytical purpose.
4. Mempertahankan unit yang konsisten.
5. Menghindari kategori berlebihan.

### 7.5 Pie & Doughnut Selection

AI MUST menggunakan Pie atau Doughnut Chart hanya ketika:

1. Data merepresentasikan bagian dari keseluruhan.
2. Total memiliki definisi yang jelas.
3. Kategori tidak saling tumpang tindih.
4. Proporsi dapat dihitung.
5. Jumlah kategori tetap mudah dibandingkan.

AI MUST NOT menggunakan Pie Chart untuk time-series trends.

AI MUST NOT menampilkan percentage tanpa denominator yang valid.

### 7.6 Activity Gauge Selection

AI MUST menggunakan Gauge hanya jika:

1. Terdapat target atau batas yang terdefinisi.
2. Progress dapat dihitung.
3. Unit dan skala jelas.
4. Pengguna membutuhkan pembacaan pencapaian secara cepat.

AI MUST NOT mengarang target.

### 7.7 Radar Chart Selection

AI MUST menggunakan Radar Chart hanya jika dimensi memiliki skala yang dapat dibandingkan.

AI MUST NOT menggunakan Radar Chart untuk metrik dengan unit berbeda tanpa normalisasi yang disetujui.

### 7.8 Bar & Line Chart Selection

AI MUST:

1. Memastikan kedua metrik memiliki hubungan analitis yang relevan.
2. Menentukan apakah dual-axis diperlukan.
3. Menampilkan unit setiap series.
4. Menghindari skala yang menyesatkan.
5. Menggunakan official GEMS variants.

AI MUST NOT menggunakan dual-axis hanya untuk membuat visualisasi terlihat kompleks.

### 7.9 Data Table Selection

AI MUST memprioritaskan Table ketika pengguna perlu:

1. Membaca exact values.
2. Membandingkan detail records.
3. Melakukan sorting.
4. Melakukan filtering.
5. Mengakses record details.
6. Melakukan operational actions.

AI MUST NOT mengganti tabel dengan chart jika pengguna membutuhkan detail data yang presisi.

### 7.10 Visualization Efficiency

AI MUST memilih visualisasi paling sederhana yang mampu menjawab business question.

AI MUST NOT:

1. Menggunakan chart untuk satu nilai yang lebih jelas sebagai KPI Card.
2. Menggunakan Pie Chart untuk terlalu banyak kategori.
3. Menggunakan Radar Chart untuk data yang tidak sebanding.
4. Menggunakan Gauge tanpa target.
5. Menggunakan kombinasi chart yang tidak memiliki hubungan analitis.
6. Mengulang informasi identik dalam beberapa chart tanpa alasan.
7. Menambahkan decorative charts tanpa analytical value.

---

## 8. Dashboard Information Architecture & Layout

AI MUST menyusun dashboard berdasarkan prioritas informasi dan alur pembacaan pengguna.

### 8.1 Recommended Information Hierarchy

AI SHOULD mempertimbangkan urutan:

1. Dashboard Header.
2. Global Filters.
3. Primary KPI Cards.
4. Primary Charts.
5. Secondary Analysis.
6. Detailed Tables.
7. Supporting Information.

AI MAY menyesuaikan urutan jika approved business requirements membutuhkan struktur berbeda.

### 8.2 Dashboard Layout Rules

AI MUST:

1. Memprioritaskan informasi penting.
2. Menggunakan consistent grid.
3. Menggunakan official spacing.
4. Mengelompokkan informasi terkait.
5. Menghindari excessive scrolling tanpa alasan.
6. Menjaga chart readability.
7. Menjaga table readability.
8. Menggunakan official GEMS layout components.
9. Menjaga visual hierarchy.
10. Memastikan filter mudah ditemukan.

### 8.3 Chart Composition

AI MUST:

1. Menggunakan chart title yang jelas.
2. Menampilkan unit.
3. Menampilkan time context.
4. Menampilkan legend jika diperlukan.
5. Menggunakan approved colors.
6. Menghindari visual clutter.
7. Menampilkan data labels jika meningkatkan readability.
8. Menjaga axis consistency.
9. Mempertahankan spacing antar chart.
10. Memastikan chart tidak terpotong.

### 8.4 Dashboard Density

AI MUST menyeimbangkan information density dan readability.

AI MUST NOT memaksakan seluruh informasi ke satu screen jika mengurangi usability.

AI MAY merekomendasikan grouping, tabs, sections, atau drill-down jika didukung requirements dan mendapat approval ketika mengubah approved navigation.

---

## 9. Official Dashboard Implementation References

AI MUST memeriksa contoh dashboard berikut sebagai referensi layout dan penerapan chart.

### 9.1 Fuel Management

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=757-34567

### 9.2 Main Dashboard

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=4233-207299

### 9.3 Dashboard Visit

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3585-249006

### 9.4 Dashboard Accommodation

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3613-91801

### 9.5 Dashboard Meals Management

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3599-87213

### 9.6 Transport Dashboard

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3613-90610

### 9.7 Laundry Dashboard — Example 01

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3585-261583

### 9.8 Laundry Dashboard — Example 02

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=3475-147760

### 9.9 Charging Station

https://www.figma.com/design/NR3xLOKvfTvElF1HGgnnmM/ISS-Website?node-id=619-23490

### 9.10 HRGA Dashboard

https://www.figma.com/design/v3ggUUZOrTe6dh9wJ21Hcy/ISS-Registrasi-Asset?node-id=576-138623

### 9.11 Reference Usage Rules

AI MUST:

1. Inspect layout structure.
2. Inspect information hierarchy.
3. Inspect KPI Card composition.
4. Inspect chart combinations.
5. Inspect filter placement.
6. Inspect table placement.
7. Inspect spacing and alignment.
8. Inspect dashboard sections.
9. Inspect official GEMS component usage.
10. Identify applicable design patterns.

AI MUST NOT:

1. Menyalin dashboard tanpa mempertimbangkan kebutuhan data baru.
2. Menggunakan contoh dashboard sebagai sumber business requirements.
3. Menganggap seluruh contoh sebagai approved universal template.
4. Menyalin dummy values sebagai actual data.
5. Mengabaikan approved HSD/BRD.

---

## 10. Time-Based Data Visualization & Filters

AI MUST mengevaluasi kebutuhan periode berdasarkan available data dan business requirements.

### 10.1 Supported Time Perspectives

AI MUST mempertimbangkan:

- Daily.
- Weekly.
- Monthly.
- Yearly.
- Custom Range.

AI MUST hanya mengimplementasikan filter yang relevan dan disetujui.

### 10.2 Weekly Filter

AI MUST memeriksa:

1. Week definition.
2. Start of week.
3. End of week.
4. Timezone.
5. Daily aggregation.
6. Previous week comparison.
7. Partial week behavior.
8. Missing daily data.

AI MUST NOT menganggap semua sistem menggunakan minggu Senin–Minggu tanpa approved requirement.

### 10.3 Monthly Filter

AI MUST memeriksa:

1. Selected month.
2. Selected year.
3. Monthly aggregation.
4. Daily breakdown.
5. Previous month comparison.
6. Partial month behavior.
7. Missing dates.

AI MUST NOT menganggap seluruh bulan memiliki jumlah hari yang sama.

### 10.4 Yearly Filter

AI MUST memeriksa:

1. Selected year.
2. Monthly aggregation.
3. Year-to-date behavior.
4. Previous year comparison.
5. Missing months.
6. Partial year behavior.
7. Annual totals.
8. Annual averages.

AI MUST NOT menghitung annual average sebagai annual total.

### 10.5 Custom Range Filter

AI MUST memeriksa:

1. Start Date.
2. End Date.
3. Required Fields.
4. Allowed Date Range.
5. Maximum Range.
6. Timezone.
7. Aggregation Granularity.
8. Comparison Period.

AI MUST NOT mengarang date range limits.

### 10.6 Filter Interaction Rules

AI MUST:

1. Menggunakan official GEMS filter components.
2. Menampilkan active filters.
3. Memperbarui relevant KPI Cards.
4. Memperbarui relevant Charts.
5. Memperbarui relevant Tables.
6. Menjaga filter consistency.
7. Menampilkan Loading State jika diperlukan.
8. Menampilkan No Results State ketika filter tidak menghasilkan data.
9. Mempertahankan approved filter persistence behavior.

### 10.7 Filter Dependency

AI MUST menentukan apakah filter berlaku untuk:

- Entire Dashboard.
- Specific Section.
- Specific Chart.
- Specific Table.

AI MUST menampilkan filter scope secara jelas.

AI MUST NOT menganggap semua filters bersifat global.

---

## 11. Data Aggregation, Calculation & Accuracy

AI MUST memastikan seluruh visualisasi merepresentasikan data dengan benar.

### 11.1 Aggregation Rules

AI MUST membedakan:

1. Sum.
2. Count.
3. Average.
4. Minimum.
5. Maximum.
6. Percentage.
7. Ratio.
8. Rate.
9. Distinct Count.
10. Weighted Average.

AI MUST menggunakan approved calculation rules.

### 11.2 Data Granularity

AI MUST mengidentifikasi apakah data tersedia pada tingkat:

- Transaction.
- Record.
- Daily.
- Weekly.
- Monthly.
- Yearly.
- Category.
- Location.
- Department.
- User.

AI MUST NOT mengarang detail granular yang tidak tersedia.

### 11.3 Data Integrity

AI MUST:

1. Memastikan unit konsisten.
2. Memastikan labels benar.
3. Memastikan calculation sesuai source.
4. Memastikan time aggregation benar.
5. Membedakan zero dari missing data.
6. Menghindari misleading axes.
7. Memastikan percentages memiliki denominator yang valid.
8. Memastikan total dan breakdown konsisten.
9. Menghindari double counting.
10. Menandai incomplete data jika relevan.

### 11.4 Comparison Rules

AI MUST memeriksa:

1. Current period.
2. Comparison period.
3. Comparable time coverage.
4. Difference calculation.
5. Percentage change calculation.
6. Missing comparison data.
7. Partial period effects.

AI MUST NOT menampilkan growth percentage tanpa valid comparison baseline.

---

## 12. Mandatory Dashboard UI States

AI MUST menghasilkan seluruh applicable UI States untuk dashboard dan komponennya.

### 12.1 State Coverage Matrix

| State | Trigger | Expected UI |
|---|---|---|
| Default | Dashboard dibuka | Normal dashboard |
| Loading | Data sedang dimuat | Loading/Skeleton |
| Available Data | Data tersedia | KPI, Chart, Table |
| Empty Data | Dataset tidak memiliki records | Empty State |
| No Filter Results | Filter tidak menghasilkan data | Filtered Empty State |
| Partial Data | Sebagian data tersedia | Contextual data indication |
| Error | Data gagal dimuat | Error Feedback |
| Network Error | Koneksi gagal | Network Error State |
| Filter Applied | Filter dipilih | Updated visualization |
| Filter Reset | Filter dikembalikan | Default filter context |
| Hover | Pointer pada chart/control | Hover Variant |
| Focus | Keyboard focus | Focus Indicator |
| Selected | Data point atau filter dipilih | Selected State |
| Disabled | Action tidak tersedia | Disabled Variant |
| Access Restricted | Role tidak memiliki akses | Permission State |
| Drill-down | Pengguna membuka detail | Detail view jika didukung |
| No Historical Data | Data periode sebelumnya tidak ada | Comparison Unavailable |
| Zero Value | Nilai aktual nol | Valid zero representation |
| Data Unavailable | Data tidak tersedia | Unavailable State |

AI MUST mengevaluasi state applicability berdasarkan requirements.

### 12.2 Loading State

AI MUST:

1. Menggunakan official Loading/Skeleton components jika tersedia.
2. Mempertahankan dashboard layout.
3. Menampilkan loading pada area yang relevan.
4. Tidak menampilkan dummy values sebagai actual data.
5. Mengikuti approved refresh behavior.

### 12.3 Empty Data State

AI MUST:

1. Membedakan dashboard tanpa data dari filter tanpa hasil.
2. Menggunakan official GEMS Empty State.
3. Menampilkan contextual message.
4. Mempertahankan available navigation.
5. Menampilkan action hanya jika didukung requirements.

AI MUST NOT mengarang data untuk mengisi chart kosong.

### 12.4 No Filter Results State

AI MUST:

1. Mempertahankan active filter context.
2. Menampilkan No Results Feedback.
3. Menggunakan official GEMS components.
4. Menyediakan reset action jika approved.
5. Tidak mengubah data scope secara otomatis.

### 12.5 Zero Value State

AI MUST membedakan nilai nol dari data yang tidak tersedia.

AI MUST menampilkan `0` jika data memang bernilai nol.

AI MUST NOT mengganti missing values dengan `0` tanpa approved data rules.

### 12.6 Partial Data State

AI MUST:

1. Mengidentifikasi incomplete periods.
2. Mengidentifikasi missing records.
3. Menampilkan contextual indication jika relevan.
4. Menghindari misleading comparisons.
5. Menggunakan approved data availability rules.

### 12.7 Error State

AI MUST:

1. Menggunakan official GEMS Error Feedback.
2. Menjelaskan area yang gagal.
3. Mempertahankan available data jika sesuai requirements.
4. Mengikuti approved recovery behavior.
5. Tidak menampilkan false success.

### 12.8 Chart Interaction States

AI MUST mengevaluasi:

1. Default.
2. Hover.
3. Focus.
4. Selected Data Point.
5. Tooltip.
6. Legend Interaction.
7. Disabled Interaction.
8. Drill-down jika didukung.

AI MUST mengikuti official GEMS chart capabilities.

AI MUST NOT mengarang interactive behavior yang tidak didukung.

### 12.9 Filter States

AI MUST mengevaluasi:

1. Default.
2. Open.
3. Selected.
4. Applied.
5. Reset.
6. Disabled.
7. Invalid Range.
8. Loading.
9. No Results.

### 12.10 State Coverage Report

AI MUST mengklasifikasikan setiap state sebagai:

- Generated.
- Not Applicable.
- Pending Requirement.
- Pending Human Approval.
- Pending Verification.

---

## 13. Dashboard Interactions & Applicable CRUD Flows

AI MUST mengevaluasi apakah dashboard memiliki interactions atau CRUD actions.

### 13.1 Dashboard Interactions

AI MUST memeriksa kebutuhan:

1. Filter.
2. Sorting.
3. Pagination.
4. Drill-down.
5. View Detail.
6. Navigation.
7. Export.
8. Print.
9. Refresh.
10. Date Selection.
11. Chart Interaction.
12. Record Selection.

AI MUST hanya mengimplementasikan actions yang didukung requirements.

### 13.2 CRUD Integration

Jika dashboard menyediakan CRUD actions, AI MUST menggunakan approved GEMS UX Patterns untuk:

- Add Data.
- View Detail.
- Edit Data.
- Delete Data.
- Approve Data.
- Reject Data.
- Revision Data.
- Export Data.
- Import Data.
- Print Document.

AI MUST NOT membuat CRUD flow baru yang bertentangan dengan official UX Patterns.

### 13.3 Drill-down Rules

AI MUST:

1. Mengidentifikasi clickable metric atau chart.
2. Menentukan destination sesuai requirements.
3. Mempertahankan selected data context.
4. Mempertahankan filter context sesuai approved behavior.
5. Menggunakan approved navigation.

AI MUST NOT mengarang detail page atau navigation destination.

### 13.4 Dashboard Action States

AI MUST mengevaluasi:

1. Default.
2. Hover.
3. Focus.
4. Disabled.
5. Loading.
6. Success.
7. Error.
8. Confirmation jika berlaku.
9. Cancel jika berlaku.
10. Empty jika berlaku.

---

## 14. Mandatory GEMS Component Usage

AI MUST menggunakan official GEMS components untuk seluruh dashboard.

### 14.1 Required Component Inspection

AI MUST memeriksa:

1. Navbar.
2. Sidebar.
3. Page Header.
4. Section Header.
5. KPI / Information Card.
6. Chart Components.
7. Table.
8. Pagination.
9. Filter.
10. Dropdown.
11. Date Picker.
12. Date Range Picker.
13. Button.
14. Tabs.
15. Badge.
16. Tooltip.
17. Modal.
18. Notification.
19. Empty State.
20. Loading Indicator.
21. Skeleton jika tersedia.
22. Error Feedback.

AI MUST hanya menggunakan komponen yang relevan.

### 14.2 Component Integrity

AI MUST:

1. Menggunakan official instances.
2. Menggunakan approved variants.
3. Menggunakan approved states.
4. Menggunakan official colors.
5. Menggunakan official typography.
6. Menggunakan official spacing.
7. Menggunakan official icons.
8. Mempertahankan component anatomy.
9. Memverifikasi actual Figma instances.

### 14.3 Missing Component Handling

Jika komponen yang diperlukan tidak tersedia, AI MUST:

1. Mengidentifikasi missing component.
2. Menjelaskan analytical requirement.
3. Memeriksa available GEMS alternatives.
4. Membandingkan alternatives.
5. Merekomendasikan solusi.
6. Menjelaskan dampak terhadap UX.
7. Meminta explicit Human Approval.

AI MUST NOT membuat custom component sebelum approval.

---

## 15. Dashboard Design Plan & Human Approval #2

AI MUST menghasilkan Dashboard Design Plan setelah Data Summary disetujui.

### 15.1 Required Visualization Plan

AI MUST menggunakan format:

| Section | Approved Metric | Recommended Component | Reason | GEMS Reference |
|---|---|---|---|---|
| Primary KPI | [Metric] | [Card] | [Reason] | [Reference] |
| Main Analysis | [Metric] | [Chart] | [Reason] | [Reference] |
| Supporting Analysis | [Metric] | [Chart/Table] | [Reason] | [Reference] |
| Detailed Data | [Dataset] | [Table] | [Reason] | [Reference] |

AI MUST memberikan alasan untuk setiap rekomendasi komponen.

### 15.2 Required Layout Plan

AI MUST menjelaskan:

1. Dashboard Header.
2. Global Filters.
3. Primary KPI placement.
4. Main Chart placement.
5. Secondary Chart placement.
6. Detailed Table placement.
7. Supporting information.
8. Responsive considerations.
9. Applicable UI States.
10. Applicable interactions.

### 15.3 Required Review

AI MUST meminta manusia memvalidasi:

1. Apakah pilihan chart sudah sesuai?
2. Apakah KPI Cards sudah efektif?
3. Apakah informasi penting sudah diprioritaskan?
4. Apakah layout mudah dipahami?
5. Apakah filter sesuai kebutuhan?
6. Apakah ada informasi berlebihan?
7. Apakah applicable UI States sudah lengkap?
8. Apakah ada komponen yang membutuhkan approval khusus?

AI MUST menunggu explicit Human Approval sebelum membuat final Figma design.

---

## 16. Mandatory Figma Design Output

Setelah kedua approval diberikan, AI MUST menghasilkan:

### 16.1 Dashboard UI

1. Dashboard Default State.
2. Approved KPI Cards.
3. Approved Charts.
4. Approved Tables.
5. Approved Filters.
6. Supporting Information.
7. Approved Actions.

### 16.2 Applicable UI States

AI MUST menghasilkan:

1. Loading.
2. Available Data.
3. Empty Data.
4. No Filter Results.
5. Error.
6. Filter Applied.
7. Disabled.
8. Access Restricted.
9. Chart Interaction States.
10. Applicable CRUD States.
11. Other approved states.

### 16.3 Figma Organization

AI MUST:

1. Menggunakan clear frame naming.
2. Mengelompokkan dashboard screens.
3. Mengelompokkan UI States.
4. Menggunakan consistent spacing.
5. Menggunakan official GEMS components.
6. Mempertahankan information hierarchy.
7. Menyediakan annotations jika diperlukan.
8. Memastikan dashboard mudah direview.

### 16.4 Final Deliverables

AI MUST menyertakan:

- Approved Data Summary.
- Approved Visualization Plan.
- Dashboard Figma Design.
- UI State Coverage.
- Component Usage Report.
- Human Approval Register.
- Compliance Report.
- Figma Design Link.

---

## 17. Quality Assurance & Final Enforcement

### 17.1 Data Validation

AI MUST memverifikasi:

1. Data source.
2. Metric definitions.
3. Calculation rules.
4. Aggregation.
5. Time periods.
6. Comparison logic.
7. Missing values.
8. Data completeness.
9. Data permissions.
10. Approved Data Summary.

### 17.2 Visualization Validation

AI MUST memverifikasi:

1. Chart suitability.
2. KPI relevance.
3. Table suitability.
4. Axis accuracy.
5. Unit consistency.
6. Percentage accuracy.
7. Legend clarity.
8. Label readability.
9. Color consistency.
10. Visual hierarchy.

### 17.3 Filter Validation

AI MUST memverifikasi:

1. Weekly filters.
2. Monthly filters.
3. Yearly filters.
4. Custom filters.
5. Filter dependencies.
6. Filter applied states.
7. Filter reset behavior.
8. Empty results.
9. Partial periods.
10. Data aggregation.

AI MUST hanya memvalidasi filters yang berlaku pada approved requirements.

### 17.4 UI State Validation

AI MUST memverifikasi:

1. Default.
2. Loading.
3. Available Data.
4. Empty Data.
5. No Results.
6. Error.
7. Disabled.
8. Filter Applied.
9. Access Restricted.
10. Chart Interaction.
11. Applicable CRUD States.

### 17.5 Human Approval Validation

AI MUST memastikan:

1. Data Summary telah disetujui.
2. KPI definitions telah disetujui.
3. Visualization Plan telah disetujui.
4. Layout Plan telah disetujui.
5. New components telah disetujui jika diperlukan.
6. Changes terhadap approved requirements telah disetujui.

### 17.6 Final AI Restrictions

AI MUST NOT:

1. Generate final dashboard sebelum kedua approval.
2. Invent business metrics.
3. Invent calculation formulas.
4. Invent target values.
5. Invent historical data.
6. Invent comparison periods.
7. Invent permissions.
8. Invent filter behavior.
9. Misrepresent missing data as zero.
10. Use misleading charts.
11. Use unapproved chart components.
12. Create custom GEMS components without approval.
13. Ignore Empty States.
14. Ignore Error States.
15. Ignore applicable CRUD flows.
16. Modify approved Data Summary without approval.
17. Modify approved Visualization Plan without approval.
18. Claim compliance without verification.

### 17.7 Final Enforcement Rule

AI MUST mengikuti urutan:

**Analyze Requirements → Analyze Data → Generate Data Summary → Human Approval #1 → Inspect GEMS Design System → Recommend Visualizations → Plan Dashboard Layout & States → Human Approval #2 → Generate Figma Dashboard → Validate → Deliver.**

AI MUST mengutamakan **data accuracy, analytical clarity, information hierarchy, usability, accessibility, dan GEMS Design System compliance**.

AI MAY merekomendasikan chart, KPI Card, Table, layout, dan interactions yang paling efektif berdasarkan approved data dan business objectives.

AI MUST memperoleh explicit Human Approval untuk seluruh perubahan terhadap approved metrics, business rules, interaction flows, atau GEMS Design System.

AI MUST memverifikasi hasil aktual di Figma sebelum menyatakan dashboard selesai.

**Data defines the information. Business requirements define the purpose. GEMS Design System defines the components. Human Approval authorizes the design.**
