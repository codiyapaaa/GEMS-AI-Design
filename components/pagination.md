# Pagination — GEMS AI Design Guidelines

## 1. Purpose & Core Principles

Pagination merupakan komponen navigasi yang digunakan untuk membagi kumpulan data atau konten menjadi beberapa halaman, sehingga pengguna dapat berpindah antarhalaman tanpa harus menampilkan seluruh data sekaligus.

Pagination dapat digunakan pada tingkat halaman (*Page Pagination*) maupun di dalam Card atau Table (*Card Pagination*), sesuai konteks dan variant resmi GEMS Design System.

### Core Principles

1. **Data-Driven Navigation**  
   AI MUST menggunakan Pagination ketika data memang dibagi menjadi beberapa halaman.

2. **Context-Based Selection**  
   AI MUST memilih jenis Pagination berdasarkan konteks Page, Card, atau Table.

3. **Official Component Reuse**  
   AI MUST menggunakan instance Pagination resmi GEMS Design System.

4. **Accurate Page Information**  
   AI MUST menggunakan nomor halaman, total halaman, dan jumlah data berdasarkan kondisi aktual.

5. **Predictable Navigation**  
   AI MUST menjaga perilaku Previous, Next, dan pemilihan halaman tetap konsisten.

6. **Responsive Consistency**  
   AI MUST menggunakan variant Desktop dan Mobile resmi.

7. **Requirement Alignment**  
   AI MUST mengikuti HSD/BRD, aturan pengambilan data, dan user flow yang telah disetujui.

---

## 2. Component Types & Variants

### 2.1 Official Types

Jenis berikut ditemukan pada komponen Pagination GEMS.

| Type | Desktop | Mobile |
|---|---|---|
| Page default | Available | Available |
| Page minimal center aligned | Available | Available |
| Card default | Available | Available |
| Card minimal left aligned | Available | Available |
| Card minimal center aligned | Available | Available |
| Card minimal right aligned | Available | Available |
| Card button group left aligned | Available | Available |
| Card button group center aligned | Available | Available |
| Card button group right aligned | Available | Available |
| Card button group right aligned with dropdown | Available | Belum teridentifikasi |

### 2.2 Official Shapes

| Shape | Description |
|---|---|
| Square | Nomor halaman menggunakan bentuk persegi dengan sudut membulat |
| Circle | Nomor halaman menggunakan bentuk lingkaran |

Shape hanya boleh digunakan pada kombinasi Type dan Breakpoint yang tersedia di GEMS.

### 2.3 Variant Selection

| Context | Recommended Type |
|---|---|
| Navigasi halaman utama | Page default |
| Navigasi halaman sederhana | Page minimal center aligned |
| Tabel atau data dalam Card | Card default |
| Card dengan navigasi ringkas | Card minimal |
| Tabel dengan kontrol nomor halaman berkelompok | Card button group |
| Tabel dengan pengaturan jumlah data per halaman | Card button group right aligned with dropdown |

### AI Rules

- AI MUST memilih Type berdasarkan konteks komponen.
- AI MUST memeriksa kombinasi Type, Shape, dan Breakpoint yang tersedia.
- AI SHOULD menggunakan Card Pagination untuk tabel yang berada di dalam Card.
- AI MUST NOT menggunakan Page Pagination hanya karena halaman memuat tabel.
- AI MUST NOT menciptakan kombinasi variant yang tidak tersedia.

---

## 3. Component Properties

### 3.1 Official Properties

| Property | Values | Function |
|---|---|---|
| Type | Official Pagination Types | Menentukan struktur dan susunan Pagination |
| Shape | Square / Circle | Menentukan bentuk nomor halaman |
| Breakpoint | Desktop / Mobile | Menentukan layout perangkat |

### 3.2 Data & Behavior Configuration

Berikut adalah informasi fungsional yang perlu disediakan aplikasi, **bukan properti Figma resmi**.

| Data | Description |
|---|---|
| Current Page | Halaman yang sedang aktif |
| Total Items | Jumlah seluruh data |
| Page Size | Jumlah data per halaman |
| Total Pages | Jumlah keseluruhan halaman |
| Available Page Sizes | Pilihan jumlah data per halaman jika didukung |
| Loading Status | Kondisi saat data halaman dimuat |

### AI Rules

- AI MUST membedakan properti visual GEMS dan data aplikasi.
- AI MUST menghitung Total Pages berdasarkan Total Items dan Page Size.
- AI MUST NOT menggunakan angka contoh Figma sebagai data aktual.
- AI MUST NOT menambahkan dropdown Page Size pada variant yang tidak mendukungnya tanpa persetujuan.

---

## 4. When to Use

### 4.1 Data Table

Pagination digunakan ketika tabel memiliki data yang dibagi menjadi beberapa halaman.

**Recommended Type:** Card default atau Card button group.

Contoh penggunaan:

- Daftar transaksi.
- Manajemen aset.
- Daftar pengguna.
- Pengajuan dan riwayat data.
- Laporan operasional.

**AI Rules:**

- AI MUST menempatkan Pagination sesuai struktur Table/Card.
- AI MUST menggunakan jumlah data aktual.
- AI MUST menjaga Pagination tetap berkaitan dengan tabel yang dikontrol.
- AI MUST NOT membuat Pagination terpisah dari konteks datanya.

### 4.2 Management & List Page

Pagination digunakan ketika halaman pengelolaan memiliki banyak data dan menggunakan pembagian halaman.

**Recommended Type:** Card default atau Page default, tergantung struktur layout.

**AI Rules:**

- AI MUST menentukan apakah Pagination berada pada tingkat halaman atau di dalam Card.
- AI MUST menggunakan navigasi halaman yang konsisten.
- AI MUST mengikuti konfigurasi data dari sistem.

### 4.3 Search & Filter Results

Pagination digunakan ketika hasil pencarian atau filter memiliki lebih dari satu halaman.

**AI Rules:**

- AI MUST menerapkan Pagination pada hasil pencarian atau filter yang aktif.
- AI MUST menghitung ulang jumlah halaman setelah hasil berubah.
- AI SHOULD mengembalikan pengguna ke halaman pertama ketika filter baru menyebabkan konteks hasil berubah.
- AI MUST NOT menampilkan nomor halaman yang tidak tersedia.

### 4.4 Report & History Page

Pagination digunakan pada laporan atau riwayat dengan kumpulan data yang terbagi menjadi beberapa halaman.

**AI Rules:**

- AI MUST mempertahankan filter dan urutan data saat pengguna berpindah halaman.
- AI MUST menjaga konsistensi jumlah data dan total halaman.
- AI MUST mengikuti aturan data yang ditentukan sistem.

### 4.5 Card-Based Content

Pagination dapat digunakan untuk kumpulan Card yang dibagi menjadi beberapa halaman.

**Recommended Type:** Page default atau Card Pagination sesuai struktur konten.

**AI Rules:**

- AI MUST memastikan Pagination mengontrol kumpulan Card yang relevan.
- AI MUST NOT menggunakan Pagination untuk navigasi antar-Card tunggal yang sebenarnya membutuhkan Carousel.

### 4.6 Verified Usage — Meals Management ISS

Pada file **Meals Management ISS**, ditemukan instance Pagination di bagian bawah tabel pengajuan.

**Observed Pattern:**

- Pagination berada pada bagian bawah tabel.
- Menggunakan pola Card button group dengan dropdown.
- Terdapat kontrol jumlah data per halaman.
- Contoh kontrol menampilkan teks “Tampilkan”, nilai `10`, dan “data per halaman”.
- Terdapat navigasi halaman berbentuk Button Group.

**AI Rules:**

- AI MAY menggunakan pola ini sebagai acuan untuk tabel manajemen dengan kebutuhan pengaturan jumlah baris.
- AI MUST tetap menggunakan komponen GEMS resmi.
- AI MUST NOT menganggap nilai `10` sebagai Page Size wajib.
- AI MUST NOT menganggap seluruh tabel wajib memiliki dropdown Page Size.

---

## 5. When NOT to Use

| Condition | Recommended Behavior |
|---|---|
| Seluruh data ditampilkan dalam satu halaman | Pagination tidak diperlukan |
| Data kosong | Gunakan Empty State |
| Navigasi antar-slide | Gunakan Carousel |
| Navigasi antar-tab | Gunakan Tabs |
| Navigasi langkah formulir | Gunakan Stepper jika tersedia dan sesuai |
| Data menggunakan Infinite Scroll yang telah disetujui | Ikuti pola Infinite Scroll |
| Konten tidak memiliki pembagian halaman | Jangan menambahkan Pagination |

### AI Rules

- AI MUST NOT menambahkan Pagination hanya sebagai dekorasi.
- AI MUST NOT membuat beberapa Pagination untuk satu dataset tanpa kebutuhan.
- AI MUST NOT menggunakan Pagination sebagai pengganti navigasi utama.
- AI MUST NOT mencampurkan Pagination dan Infinite Scroll tanpa alur yang disetujui.

---

## 6. Content Structure

### 6.1 Component Anatomy

| Element | Function | Requirement |
|---|---|---|
| Previous | Menuju halaman sebelumnya | Conditional |
| Next | Menuju halaman berikutnya | Conditional |
| Page Numbers | Memilih nomor halaman | Variant-dependent |
| Active Page | Menunjukkan halaman aktif | Required |
| Page Indicator | Menampilkan posisi halaman | Variant-dependent |
| Ellipsis | Mewakili rentang nomor yang tidak ditampilkan | Conditional |
| Page Size Dropdown | Mengatur jumlah data per halaman | Variant-dependent |
| Button Group | Mengelompokkan kontrol navigasi | Variant-dependent |
| Divider | Memisahkan area Pagination dari konten | Sesuai variant |

### 6.2 Page Numbers

- AI MUST menampilkan nomor halaman yang valid.
- AI MUST memberikan penanda visual pada halaman aktif.
- AI MUST mengikuti bentuk Square atau Circle resmi.
- AI MUST NOT menampilkan seluruh nomor halaman jika pola resmi menggunakan pemendekan rentang.

### 6.3 Page Indicator

Pada contoh Mobile GEMS, informasi halaman ditampilkan dalam bentuk ringkas seperti `Page 1 of 10`.

**AI Rules:**

- AI MUST menggunakan nomor halaman aktual.
- AI MUST menjaga informasi posisi halaman mudah dipahami.
- AI MUST NOT menggunakan teks contoh sebagai nilai tetap.

### 6.4 Page Size

- AI MUST menggunakan nilai yang didukung aplikasi.
- AI MUST mengikuti dropdown resmi jika variant mendukungnya.
- AI MUST NOT membuat pilihan jumlah baris tanpa ketentuan sistem.

---

## 7. States

Bagian ini membedakan **state interaksi yang diperlukan aplikasi** dari **variant visual yang teridentifikasi pada GEMS**. Tidak semua state di bawah merupakan variant terpisah dalam komponen induk Pagination.

### 7.1 Default State

Pagination berada dalam kondisi normal dan siap digunakan.

- Nomor halaman ditampilkan sesuai dataset.
- Previous dan Next mengikuti posisi halaman.
- Halaman aktif memiliki penanda yang jelas.

### 7.2 Active / Current Page

Menunjukkan halaman yang sedang ditampilkan.

**AI Rules:**

- AI MUST menampilkan satu halaman aktif untuk satu Pagination.
- AI MUST menggunakan penanda aktif sesuai komponen GEMS.
- AI MUST menjaga kesesuaian antara nomor aktif dan data yang ditampilkan.

### 7.3 Hover State

Muncul ketika pengguna mengarahkan pointer pada kontrol interaktif.

**AI Rules:**

- AI MUST mengikuti Hover State dari komponen Button atau Pagination terkait.
- AI MUST NOT membuat warna Hover baru.

### 7.4 Focus State

Muncul ketika kontrol menerima fokus keyboard.

**AI Rules:**

- AI MUST menggunakan indikator fokus yang jelas.
- AI MUST mengikuti komponen GEMS yang digunakan.

### 7.5 Disabled State

Digunakan ketika kontrol tidak dapat dijalankan.

| Condition | Behavior |
|---|---|
| Current Page = 1 | Previous tidak dapat digunakan |
| Current Page = Total Pages | Next tidak dapat digunakan |
| Navigasi sementara tidak tersedia | Mengikuti aturan loading sistem |

**AI Rules:**

- AI MUST mencegah navigasi di luar rentang halaman.
- AI MUST mengikuti Disabled State resmi komponen terkait.
- AI MUST NOT menggunakan tampilan Disabled sebagai satu-satunya penjelasan kondisi.

### 7.6 Loading State

Digunakan ketika data halaman berikutnya sedang dimuat.

**AI Rules:**

- AI MUST mengikuti mekanisme loading sistem.
- AI MUST mencegah permintaan navigasi berulang yang tidak diperlukan.
- AI MUST NOT membuat state visual baru tanpa acuan resmi.

### 7.7 Empty State

Ketika tidak terdapat data:

- AI MUST menggunakan komponen Empty State resmi.
- AI SHOULD menyembunyikan Pagination yang tidak memiliki halaman valid.
- AI MUST NOT menampilkan nomor halaman fiktif.

### 7.8 Single-Page State

Ketika seluruh hasil hanya membutuhkan satu halaman:

- AI SHOULD tidak menampilkan Pagination jika tidak ada kebutuhan navigasi.
- Jika sistem mewajibkan kontrol tetap tampil, AI MUST mengikuti pola yang telah disetujui.

---

## 8. Interactions

### 8.1 Previous

Memindahkan pengguna ke halaman sebelumnya.

- MUST mengurangi Current Page satu tingkat.
- MUST tidak dapat dijalankan pada halaman pertama.
- MUST memperbarui data yang ditampilkan.

### 8.2 Next

Memindahkan pengguna ke halaman berikutnya.

- MUST menambah Current Page satu tingkat.
- MUST tidak dapat dijalankan pada halaman terakhir.
- MUST memperbarui data yang ditampilkan.

### 8.3 Page Number Selection

- MUST menampilkan halaman yang dipilih.
- MUST memperbarui penanda Active Page.
- MUST mempertahankan filter dan sorting yang berlaku.

### 8.4 Page Size Selection

Jika variant dan kebutuhan aplikasi mendukung dropdown:

- MUST memperbarui jumlah data per halaman.
- MUST menghitung ulang Total Pages.
- MUST memastikan Current Page tetap valid.
- SHOULD kembali ke halaman pertama untuk menjaga konsistensi, kecuali alur sistem menentukan lain.

### 8.5 Search, Filter & Sorting

- MUST menghitung ulang hasil Pagination setelah dataset berubah.
- MUST menjaga filter dan sorting selama perpindahan halaman.
- MUST NOT menampilkan halaman yang sudah tidak tersedia.

### 8.6 Error Handling

Jika pengambilan data gagal:

- AI MUST mengikuti mekanisme error sistem.
- AI MUST NOT menampilkan perpindahan halaman sebagai berhasil jika data gagal dimuat.
- AI MUST menyediakan mekanisme pemulihan sesuai pola yang telah disetujui.

---

## 9. Responsive Behavior

### 9.1 Desktop

Pada GEMS, variant Desktop dapat menampilkan:

- Previous dan Next.
- Nomor halaman.
- Active Page.
- Button Group.
- Page Size Dropdown pada variant tertentu.

**AI Rules:**

- AI MUST menggunakan variant Desktop resmi.
- AI MUST mengikuti alignment yang tersedia.
- AI MUST NOT mengubah struktur Button Group secara manual.

### 9.2 Mobile

Pada contoh GEMS, Page Pagination Mobile menggunakan pola yang lebih ringkas dengan:

- Previous.
- Page Indicator.
- Next.

**AI Rules:**

- AI MUST menggunakan variant Mobile resmi.
- AI MUST menjaga keterbacaan Page Indicator.
- AI MUST menjaga target interaksi tetap mudah digunakan.
- AI MUST NOT memaksakan seluruh nomor halaman Desktop pada Mobile.
- AI MUST NOT menghilangkan kontrol penting tanpa pola resmi.

### 9.3 Cross-Platform Consistency

- Current Page MUST konsisten dengan data.
- Total Pages MUST sesuai dataset.
- Navigasi MUST menghasilkan data yang benar.
- Perbedaan tampilan MUST mengikuti variant GEMS.

---

## 10. Accessibility

### 10.1 Keyboard Navigation

- Kontrol interaktif MUST dapat diakses menggunakan keyboard.
- Urutan fokus MUST logis.
- Focus Indicator MUST terlihat.

### 10.2 Accessible Labels

- Previous dan Next MUST memiliki nama aksesibel.
- Nomor halaman MUST dapat dikenali.
- Halaman aktif MUST ditandai secara semantik, misalnya melalui `aria-current="page"` pada implementasi web yang sesuai.

### 10.3 Disabled Controls

- Kontrol yang tidak tersedia MUST memiliki perilaku disabled yang benar.
- Pengguna MUST tidak dapat berpindah ke halaman di luar rentang valid.

### 10.4 Screen Reader

- Area Pagination SHOULD memiliki label navigasi yang jelas.
- Informasi halaman aktif MUST dapat dipahami tanpa bergantung pada warna.
- Perubahan hasil SHOULD dapat diketahui pengguna sesuai pola aksesibilitas aplikasi.

### 10.5 Touch Accessibility

- Kontrol Mobile MUST mudah disentuh.
- Jarak antarkontrol MUST mengikuti spesifikasi GEMS.
- AI MUST NOT memperkecil target interaksi secara sembarangan.

---

## 11. AI Decision Logic

### Step 1 — Identify Dataset

Tentukan apakah konten menggunakan pembagian halaman berdasarkan HSD/BRD.

Jika tidak, jangan gunakan Pagination.

### Step 2 — Identify Container

| Context | Pagination Family |
|---|---|
| Navigasi tingkat halaman | Page |
| Data Table dalam Card | Card |
| Daftar dalam Card | Card |
| Konten halaman tanpa Card | Page |

### Step 3 — Select Type

Pilih Default, Minimal, atau Button Group berdasarkan kebutuhan dan komponen resmi yang tersedia.

### Step 4 — Select Shape

Gunakan Square atau Circle sesuai variant GEMS dan konsistensi desain aplikasi.

### Step 5 — Select Breakpoint

Pilih Desktop atau Mobile.

### Step 6 — Configure Data

Tentukan:

- Current Page.
- Total Items.
- Page Size.
- Total Pages.
- Available Page Sizes jika diperlukan.

### Step 7 — Apply States

Pastikan:

- Active Page benar.
- Previous tidak aktif pada halaman pertama.
- Next tidak aktif pada halaman terakhir.
- Loading dan Error mengikuti aturan sistem.
- Empty State ditangani dengan benar.

### Step 8 — Validate Interactions

Pastikan navigasi mempertahankan filter dan sorting serta memperbarui dataset dengan benar.

### Step 9 — Validate Output

AI MUST memastikan:

1. Pagination diperlukan oleh dataset.
2. Type sesuai konteks.
3. Shape dan Breakpoint tersedia.
4. State navigasi benar.
5. Nomor halaman sesuai data.
6. Page Size sesuai kebutuhan.
7. Responsivitas mengikuti GEMS.
8. Aksesibilitas terpenuhi.
9. Tidak ada interaksi atau user flow baru tanpa persetujuan.

---

## 12. AI Implementation Rules

### 12.1 Mandatory Rules

AI MUST:

1. Menggunakan komponen Pagination resmi GEMS.
2. Memilih Type berdasarkan konteks Page atau Card.
3. Menggunakan Shape dan Breakpoint resmi.
4. Menggunakan data Pagination aktual.
5. Menampilkan halaman aktif secara jelas.
6. Menangani batas halaman pertama dan terakhir.
7. Mengikuti state komponen pendukung resmi.
8. Mempertahankan filter dan sorting saat berpindah halaman.
9. Menghitung ulang Pagination saat dataset berubah.
10. Mengikuti responsivitas dan aksesibilitas GEMS.
11. Memvalidasi perubahan yang tidak didukung komponen resmi.

### 12.2 Prohibited Rules

AI MUST NOT:

1. Membuat Pagination custom ketika instance resmi tersedia.
2. Menambahkan Pagination tanpa kebutuhan pembagian data.
3. Menggunakan Page Pagination sebagai pengganti Card Pagination tanpa mempertimbangkan konteks.
4. Membuat kombinasi Type, Shape, atau Breakpoint yang tidak tersedia.
5. Menggunakan nomor halaman fiktif.
6. Membiarkan Previous aktif pada halaman pertama.
7. Membiarkan Next aktif pada halaman terakhir.
8. Menghilangkan filter atau sorting saat navigasi.
9. Menambahkan Page Size Dropdown tanpa kebutuhan.
10. Membuat state atau pola interaksi baru tanpa persetujuan.
11. Mengubah struktur internal komponen resmi secara sembarangan.
12. Menganggap contoh data pada Figma sebagai ketentuan bisnis wajib.

### 12.3 Source of Truth

| Source | Responsibility |
|---|---|
| GEMS Design System | Type, Shape, Breakpoint, struktur, dan visual |
| HSD / BRD | Kebutuhan Pagination, jumlah data, dan alur |
| System Data | Current Page, Total Items, Page Size, dan Total Pages |
| Human Approval | Persetujuan perubahan komponen atau user flow |

### 12.4 Final AI Instruction

AI MUST use the official GEMS Pagination component and select the appropriate Type, Shape, and Breakpoint based on the page structure and HSD/BRD requirements.

AI MUST ensure accurate pagination data, valid navigation states, consistent responsive behavior, and accessible interactions.

AI MUST NOT invent unsupported variants, states, interactions, or user flows without authorized human validation.

---

## 13. Official GEMS Design System — Component Specifications

### 13.1 Official Component Reference

**Component Name:** Pagination  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=483-2504&t=oGvGAZSrsS9aDX5O-1

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `483:2504`

### 13.2 Official Component Retrieval

When Figma MCP is available, AI MUST:

1. Access the GEMS Design System using the specified Figma File Key.
2. Locate Pagination using Node ID `483:2504`.
3. Inspect the available Type, Shape, and Breakpoint combinations.
4. Select the correct official component variant.
5. Reuse the official instance when the integration supports it.
6. Configure the component without changing its unsupported internal properties.
7. Preserve the connection to the GEMS library where supported.
8. Validate the implementation against HSD/BRD.

If the specified node represents a component collection or documentation frame rather than an instantiable component, AI MUST locate the appropriate child component or component set before inserting an instance.

### 13.3 Verified Usage Reference

**Meals Management ISS — Pengajuan Pesanan Tamu**

**Figma File:**  
https://www.figma.com/design/FaD6En6EYVnjGzegaxhjzy/Meals-Management-ISS?node-id=159-43407

**Observed Pagination Instance Node:** `159:43564`

**Observed Pattern:** Card button group right aligned with dropdown.

This reference demonstrates Pagination usage within a management table, including Page Size selection and grouped page navigation.

The application file is a usage example. GEMS Design System remains the authoritative source for component specifications.

### 13.4 Component Reuse Rules

- AI MUST retrieve the official GEMS Pagination component when supported by Figma MCP.
- AI MUST inspect supported variants before use.
- AI MUST preserve the component's intended structure.
- AI MUST NOT substitute another design library.
- AI MUST NOT detach or modify the component's internal structure without authorization.
- AI MUST NOT treat example content as mandatory business data.

### 13.5 Final Component Instruction

**AI MUST retrieve and reuse the official GEMS Pagination component from the specified Figma source whenever the integration supports it. AI MUST select supported Type, Shape, and Breakpoint combinations and configure pagination behavior according to verified business requirements.**
