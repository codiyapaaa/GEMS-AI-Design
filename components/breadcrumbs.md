# GEMS Design System — Breadcrumbs Guidelines

## 1. Purpose

Breadcrumbs merupakan komponen navigasi yang menunjukkan posisi halaman aktif dalam hierarki aplikasi dan membantu pengguna kembali ke halaman induk.

Breadcrumbs digunakan untuk memberikan konteks lokasi pengguna, khususnya pada aplikasi dengan navigasi bertingkat.

**Core Principle:**

> AI MUST menggunakan komponen Breadcrumbs resmi GEMS Design System. AI MUST memilih konfigurasi Divider, Type, dan Breakpoint yang tersedia tanpa membuat komponen atau visual variant baru.

### 1.1 Mandatory Design System Compliance

AI MUST:

1. Menggunakan instance Breadcrumbs resmi GEMS.
2. Memilih konfigurasi resmi berdasarkan kebutuhan halaman.
3. Menggunakan separator, typography, warna, dan spacing dari GEMS.
4. Menyesuaikan label berdasarkan struktur navigasi aplikasi.
5. Menggunakan komponen pendukung GEMS apabila diperlukan.
6. Mempertahankan struktur dan component properties resmi.
7. Mengikuti hierarki halaman berdasarkan HSD/BRD.

AI MUST NOT:

1. Membuat Breadcrumbs custom.
2. Menggunakan komponen dari library lain.
3. Membuat separator atau visual style baru.
4. Mengubah typography, warna, spacing, atau ukuran di luar GEMS.
5. Mengganti instance resmi dengan susunan Text dan Icon manual.
6. Mengubah struktur navigasi tanpa dasar kebutuhan bisnis.

---

## 2. Breadcrumbs Variants & Hierarchy

### 2.1 Official Component Properties

Berdasarkan metadata komponen GEMS, tersedia tiga kelompok properties.

| Property | Available Values |
|---|---|
| Divider | Chevron, Slash |
| Type | Text, Text with line, Button brand, Button gray |
| Breakpoint | Desktop, Mobile |

Kombinasi ketiga properties menghasilkan 16 konfigurasi yang tersedia dalam komponen resmi.

### 2.2 Divider Variants

**Chevron**

Menggunakan pemisah berbentuk Chevron.

Contoh konseptual:

`Manajemen › Transportasi › Detail Transportasi`

**Slash**

Menggunakan pemisah berbentuk garis miring.

Contoh konseptual:

`Manajemen / Transportasi / Detail Transportasi`

**Rules:**

- MUST menggunakan Divider resmi.
- MUST mempertahankan separator secara konsisten dalam satu Breadcrumbs.
- MUST mengikuti pattern navigasi aplikasi.
- MUST NOT mengganti Chevron atau Slash dengan separator custom.
- MUST NOT mencampur dua jenis separator dalam satu instance.

### 2.3 Type Variants

| Type | Description | Usage Guidance |
|---|---|---|
| Text | Breadcrumbs berbasis teks | Navigasi hierarki standar |
| Text with line | Breadcrumbs teks dengan elemen garis | Ketika layout menggunakan pattern garis GEMS |
| Button brand | Breadcrumbs dengan gaya Button brand | Ketika pattern navigasi membutuhkan penekanan brand |
| Button gray | Breadcrumbs dengan gaya Button gray | Ketika pattern navigasi menggunakan gaya netral |

**Important:** Panduan pemilihan Type di atas merupakan rekomendasi UX. Nama dan keberadaan keempat Type sudah terverifikasi dari metadata, tetapi aturan resmi pemilihannya masih perlu disesuaikan dengan contoh visual GEMS.

### 2.4 Breakpoint Variants

**Desktop**

Digunakan pada layout desktop sesuai breakpoint GEMS.

**Mobile**

Digunakan pada layout mobile sesuai breakpoint GEMS.

AI MUST memilih konfigurasi yang sesuai dengan target layar.

AI MUST NOT membuat responsive variant baru jika konfigurasi resmi sudah tersedia.

---

## 3. When to Use Breadcrumbs

### 3.1 Recommended Usage

Breadcrumbs SHOULD digunakan ketika:

1. Pengguna berada pada halaman dengan hierarki navigasi bertingkat.
2. Pengguna membuka halaman detail dari halaman daftar.
3. Pengguna berada pada subhalaman pengelolaan.
4. Pengguna perlu memahami hubungan halaman aktif dengan halaman induk.
5. Pengguna membutuhkan navigasi cepat ke tingkat sebelumnya.
6. Struktur halaman memiliki hubungan parent-child yang jelas.

### 3.2 Usage Examples

| Page Context | Example Hierarchy | Recommendation |
|---|---|---|
| Main Dashboard | Dashboard | Optional |
| Management List | Manajemen Transportasi | Optional |
| Detail Page | Manajemen Transportasi / Detail Transportasi | Recommended |
| Nested Detail | Akomodasi / Manajemen Mess / Detail Kamar | Recommended |
| Edit Page | Manajemen Asset / Detail Asset / Edit Asset | Recommended |
| Report Detail | Laporan / Rekap Makanan / Detail Rekap | Recommended |
| Settings Subpage | Pengaturan / Hak Akses | Recommended |

Contoh hierarki merupakan ilustrasi penggunaan, bukan hasil verifikasi halaman referensi.

### 3.3 Mandatory Usage Conditions

AI MUST menggunakan Breadcrumbs ketika:

- HSD/BRD atau layout resmi mewajibkannya.
- Pattern halaman yang telah disetujui menggunakan Breadcrumbs.
- Navigasi bertingkat membutuhkan Breadcrumbs sesuai standar aplikasi.

AI SHOULD menggunakan Breadcrumbs pada halaman detail atau subhalaman bertingkat apabila pattern aplikasi mendukungnya.

AI MUST NOT menambahkan Breadcrumbs secara otomatis hanya karena halaman memiliki judul.

---

## 4. When NOT to Use Breadcrumbs

Breadcrumbs SHOULD NOT digunakan pada:

- Halaman utama tanpa hierarki yang relevan.
- Dashboard utama yang tidak membutuhkan navigasi parent-child.
- Modal konfirmasi.
- Toast atau Notification.
- Dropdown.
- Halaman yang menggunakan navigasi bertahap dan lebih tepat menggunakan Stepper.
- Halaman yang hanya membutuhkan tombol Kembali.
- Konten yang tidak memiliki hubungan hierarki.

### Rules

- MUST NOT menggunakan Breadcrumbs sebagai pengganti Tabs.
- MUST NOT menggunakan Breadcrumbs sebagai pengganti Stepper.
- MUST NOT menggunakan Breadcrumbs untuk menunjukkan riwayat kunjungan pengguna.
- MUST NOT menampilkan hierarki palsu.
- MUST NOT menambahkan Breadcrumbs hanya untuk dekorasi.

---

## 5. Breadcrumbs Content Structure

### 5.1 Component Anatomy

| Element | Purpose | Requirement |
|---|---|---|
| Breadcrumb Container | Membungkus seluruh navigasi | Required |
| Parent Item | Menampilkan halaman induk | Sesuai hierarki |
| Divider | Memisahkan setiap level | Required untuk beberapa level |
| Intermediate Item | Menampilkan tingkat navigasi perantara | Context-dependent |
| Current Page | Menunjukkan halaman aktif | Required |
| Line Element | Elemen garis pada Text with line | Sesuai Type |
| Button Styling | Gaya item pada Button brand/gray | Sesuai Type |

### 5.2 Hierarchy Rules

AI MUST:

1. Menyusun item dari tingkat tertinggi ke halaman aktif.
2. Menggunakan label sesuai nama halaman.
3. Memastikan setiap parent merepresentasikan hierarki nyata.
4. Menempatkan halaman aktif sebagai item terakhir.
5. Memperbarui Breadcrumbs ketika lokasi navigasi berubah.

AI MUST NOT:

1. Menampilkan halaman yang tidak berada dalam hierarki.
2. Menggunakan urutan berdasarkan riwayat klik.
3. Menambahkan level navigasi yang tidak ada.
4. Menampilkan item duplikat.
5. Menggunakan label yang tidak sesuai dengan halaman tujuan.

### 5.3 Content Examples

**Two Levels**

`Manajemen Mess / Detail Mess`

**Three Levels**

`Akomodasi / Manajemen Mess / Detail Kamar`

**Four Levels**

`Manajemen Asset / Daftar Asset / Detail Asset / Edit Asset`

Jumlah level mengikuti hierarki aplikasi dan kemampuan komponen resmi.

---

## 6. Breadcrumbs States

State berikut merupakan aturan perilaku yang direkomendasikan untuk Breadcrumbs. Ketersediaan visual state sebagai Figma variant harus diverifikasi pada komponen resmi.

### 6.1 State Matrix

| State | Applicable Item | Expected Behavior |
|---|---|---|
| Default | Parent / Intermediate | Ditampilkan menggunakan style normal |
| Hover | Item navigasi interaktif | Memberikan feedback ketika pointer diarahkan |
| Focused | Item navigasi interaktif | Menampilkan indikator fokus keyboard |
| Active / Current | Halaman aktif | Menunjukkan lokasi halaman saat ini |
| Disabled | Item yang tidak dapat digunakan, jika didukung | Tidak menjalankan navigasi |
| Pressed | Item interaktif, jika didukung | Memberikan feedback saat aktivasi |

### 6.2 Default State

Default State merupakan kondisi ketika item Breadcrumbs ditampilkan tanpa interaksi.

**Rules:**

- MUST menggunakan visual Default resmi GEMS.
- MUST menggunakan typography dan warna sesuai Type.
- MUST mempertahankan separator resmi.
- MUST NOT membuat styling Default custom.

### 6.3 Hover State

Hover State berlaku pada item yang dapat diklik ketika pengguna mengarahkan pointer.

**Rules:**

- MUST menggunakan Hover State resmi apabila tersedia.
- MUST mempertahankan konsistensi visual dengan Type yang dipilih.
- MUST NOT menerapkan Hover pada separator.
- MUST NOT membuat perubahan warna atau underline custom di luar GEMS.
- SHOULD memberikan indikasi bahwa item dapat dinavigasi.

### 6.4 Focused State

Focused State muncul ketika item navigasi menerima fokus melalui keyboard.

**Rules:**

- MUST menggunakan focus indicator resmi GEMS.
- MUST mendukung navigasi keyboard.
- MUST menjaga fokus tetap terlihat.
- MUST NOT menghilangkan focus indicator.
- MUST NOT membuat visual fokus custom jika state resmi tersedia.

### 6.5 Active / Current State

Active atau Current State menunjukkan halaman yang sedang dibuka.

**Rules:**

- MUST menampilkan halaman aktif sebagai item terakhir.
- MUST membedakan halaman aktif dari parent item.
- MUST menggunakan visual Current sesuai GEMS.
- SHOULD menjadikan halaman aktif sebagai teks non-interaktif.
- MUST NOT membuat halaman aktif terlihat seperti navigasi menuju halaman lain.
- MUST NOT menampilkan lebih dari satu Current Page dalam satu Breadcrumbs.

### 6.6 Disabled State

Disabled State hanya digunakan apabila didukung oleh komponen resmi dan memiliki kebutuhan fungsional.

**Rules:**

- MUST menggunakan visual Disabled resmi jika tersedia.
- MUST NOT menjalankan navigasi dari item Disabled.
- MUST NOT menggunakan Disabled hanya untuk menandai halaman aktif.
- MUST NOT membuat Disabled State baru tanpa Human Approval.

### 6.7 Pressed State

Pressed State digunakan ketika pengguna sedang mengaktifkan item navigasi, apabila didukung GEMS.

**Rules:**

- MUST mengikuti state resmi.
- MUST mempertahankan hierarchy navigasi.
- MUST NOT mengubah ukuran atau posisi item ketika ditekan.
- MUST NOT membuat visual Pressed custom.

---

## 7. Breadcrumbs Interaction Rules

### 7.1 Parent Navigation

Ketika pengguna memilih parent item:

- MUST menuju halaman induk yang sesuai.
- MUST menggunakan tujuan navigasi yang valid.
- MUST mempertahankan struktur aplikasi.
- MUST NOT mengarahkan ke halaman yang tidak berhubungan.

### 7.2 Intermediate Navigation

Ketika pengguna memilih item perantara:

- MUST menuju halaman sesuai level yang dipilih.
- MUST memperbarui halaman aktif.
- MUST memperbarui Breadcrumbs berdasarkan hierarki tujuan.
- MUST NOT menggunakan interaksi yang berbeda tanpa kebutuhan.

### 7.3 Current Page

- MUST menunjukkan lokasi halaman aktif.
- SHOULD tidak menjalankan navigasi ketika dipilih.
- MUST memiliki perbedaan visual sesuai GEMS.
- MUST NOT menggunakan Current Page sebagai tombol aksi.

### 7.4 Accessibility

AI MUST:

1. Menggunakan semantic navigation yang sesuai saat implementasi.
2. Menyediakan label navigasi Breadcrumbs.
3. Mendukung keyboard navigation pada item interaktif.
4. Menggunakan `aria-current="page"` untuk item aktif pada implementasi web.
5. Mempertahankan focus indicator.
6. Menggunakan label yang mudah dipahami.
7. Memastikan separator tidak menimbulkan informasi berulang bagi screen reader.

---

## 8. Responsive Behavior

### 8.1 Desktop

AI MUST:

- Menggunakan konfigurasi `Breakpoint=Desktop`.
- Mempertahankan alignment sesuai komponen.
- Menggunakan ukuran dan spacing resmi.
- Menampilkan hierarchy sesuai kebutuhan dan kapasitas komponen.

### 8.2 Mobile

AI MUST:

- Menggunakan konfigurasi `Breakpoint=Mobile`.
- Mempertahankan komponen resmi.
- Mengikuti aturan layout mobile GEMS.
- Memastikan item navigasi tetap dapat digunakan.
- Menangani label panjang berdasarkan pattern resmi.

### 8.3 Long Breadcrumbs

Jika hierarki terlalu panjang:

- SHOULD memprioritaskan keterbacaan halaman aktif.
- MUST memeriksa apakah GEMS menyediakan truncation atau overflow behavior.
- MUST NOT membuat dropdown overflow, horizontal scroll, atau ellipsis custom tanpa acuan resmi.
- MUST NOT menghapus level penting secara sembarangan.
- MUST meminta Human Approval apabila tidak tersedia pattern yang sesuai.

---

## 9. Contextual Breadcrumbs Patterns

### 9.1 Management Detail Page

**Example:**

`Manajemen Transportasi / Detail Transportasi`

**Rules:**

- SHOULD digunakan ketika detail memiliki halaman tersendiri.
- MUST menjadikan Detail Transportasi sebagai Current Page.
- MUST menjadikan Manajemen Transportasi sebagai parent yang dapat dinavigasi apabila sesuai route.

### 9.2 Nested Management Page

**Example:**

`Akomodasi / Manajemen Mess / Detail Kamar`

**Rules:**

- MUST mengikuti hierarki halaman.
- MUST mempertahankan urutan parent-child.
- MUST menggunakan Divider resmi.
- MUST NOT menambahkan level yang tidak tersedia dalam struktur aplikasi.

### 9.3 Edit Page

**Example:**

`Manajemen Asset / Detail Asset / Edit Asset`

**Rules:**

- SHOULD digunakan jika Edit Asset merupakan halaman terpisah.
- MUST mengikuti struktur navigasi.
- MUST NOT menggunakan Breadcrumbs jika proses Edit ditampilkan dalam Modal dan tidak mengubah lokasi halaman.

### 9.4 Report Detail Page

**Example:**

`Laporan / Rekap Makanan / Detail Rekap`

**Rules:**

- SHOULD digunakan untuk laporan bertingkat.
- MUST menjadikan Detail Rekap sebagai Current Page.
- MUST menggunakan label sesuai terminologi aplikasi.

---

## 10. Breadcrumbs Labels & Content Rules

### 10.1 General Rules

- MUST menggunakan nama halaman yang jelas.
- MUST mengikuti terminologi HSD/BRD.
- MUST menjaga konsistensi dengan Page Title.
- SHOULD menggunakan label yang singkat.
- MUST mempertahankan urutan hierarki.
- MUST NOT menggunakan label generik yang ambigu.

### 10.2 Label Examples

| Page | Breadcrumb Label |
|---|---|
| Manajemen Transportasi | Manajemen Transportasi |
| Detail Transportasi | Detail Transportasi |
| Manajemen Mess | Manajemen Mess |
| Detail Kamar | Detail Kamar |
| Rekap Makanan | Rekap Makanan |
| Detail Asset | Detail Asset |

### 10.3 Current Page Rules

- MUST sesuai dengan halaman aktif.
- MUST menjadi item terakhir.
- MUST diperbarui saat route berubah.
- MUST NOT menggunakan nama halaman lain sebagai Current Page.

---

## 11. Breadcrumbs Selection Rules for AI

AI MUST mengikuti proses berikut.

### Step 1 — Identify Page Hierarchy

Analisis HSD/BRD dan struktur navigasi aplikasi.

Tentukan parent, intermediate, dan current page.

### Step 2 — Determine Necessity

Tentukan apakah Breadcrumbs diperlukan.

AI MUST NOT menambahkannya pada halaman tanpa hierarki yang relevan.

### Step 3 — Retrieve Official Component

AI MUST mengakses komponen Breadcrumbs resmi GEMS.

### Step 4 — Select Divider

Pilih salah satu:

- Chevron.
- Slash.

Pemilihan MUST mengikuti pattern aplikasi.

### Step 5 — Select Type

Pilih salah satu:

- Text.
- Text with line.
- Button brand.
- Button gray.

AI MUST memilih Type resmi yang sesuai konteks.

### Step 6 — Select Breakpoint

Pilih:

- Desktop.
- Mobile.

AI MUST menggunakan konfigurasi sesuai target layar.

### Step 7 — Configure Navigation Content

Atur:

- Parent Item.
- Intermediate Item.
- Current Page.
- Navigation Destination.

### Step 8 — Apply States

Pastikan:

- Default.
- Hover.
- Focused.
- Current.
- Disabled jika didukung dan diperlukan.
- Pressed jika didukung.

Visual MUST mengikuti GEMS.

### Step 9 — Validate Against Design System

AI MUST memastikan:

1. Menggunakan instance resmi.
2. Divider merupakan konfigurasi resmi.
3. Type merupakan konfigurasi resmi.
4. Breakpoint sesuai.
5. Typography sesuai.
6. Warna sesuai.
7. Spacing sesuai.
8. Separator sesuai.
9. Hierarki navigasi benar.
10. Current Page benar.
11. Interaksi berfungsi.
12. Tidak ada visual custom.

### Step 10 — Request Human Approval

Jika kebutuhan tidak didukung oleh konfigurasi resmi, AI MUST meminta Human Approval sebelum membuat alternatif.

---

## 12. AI Restrictions

AI MUST NOT:

1. Membuat Breadcrumbs custom ketika komponen resmi tersedia.
2. Menggunakan Breadcrumbs dari library lain.
3. Mengganti instance resmi dengan Frame custom.
4. Membuat Divider baru.
5. Mengubah bentuk Chevron atau Slash.
6. Mengubah typography di luar GEMS.
7. Mengubah warna di luar GEMS.
8. Mengubah spacing atau ukuran secara manual.
9. Membuat Type baru.
10. Membuat Breakpoint baru.
11. Membuat visual state baru tanpa persetujuan.
12. Menggunakan Breadcrumbs sebagai Tabs.
13. Menggunakan Breadcrumbs sebagai Stepper.
14. Menggunakan Breadcrumbs sebagai riwayat navigasi.
15. Menampilkan hierarchy palsu.
16. Menggunakan lebih dari satu Current Page.
17. Membuat separator interaktif.
18. Menggunakan label yang tidak sesuai route.
19. Membuat overflow pattern custom.
20. Mengubah struktur navigasi tanpa dasar HSD/BRD.
21. Mengabaikan aksesibilitas.
22. Mengklaim implementasi sesuai GEMS tanpa memverifikasi komponen.

---

## 13. Official GEMS Design System Component

### 13.1 Component Reference

**Component Name:** Breadcrumbs  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-40937

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `240:40937`

### 13.2 Verified Component Configurations

Berdasarkan metadata Figma, tersedia konfigurasi berikut:

**Divider:**
- Chevron
- Slash

**Type:**
- Text
- Text with line
- Button brand
- Button gray

**Breakpoint:**
- Desktop
- Mobile

**Total:** 16 konfigurasi komponen.

### 13.3 Mandatory Component Usage

AI MUST:

1. Mengakses komponen resmi GEMS.
2. Menggunakan instance Breadcrumbs resmi.
3. Memilih konfigurasi Divider, Type, dan Breakpoint yang tersedia.
4. Mempertahankan visual properties resmi.
5. Menggunakan label sesuai hierarki aplikasi.
6. Mengikuti aturan navigasi dan state.
7. Mempertahankan koneksi component library apabila didukung.
8. Memvalidasi implementasi terhadap sumber resmi.

### 13.4 Verification Requirements

Sebelum implementasi, AI MUST memeriksa:

- Component Name.
- Available Configurations.
- Component Properties.
- Typography.
- Colors.
- Spacing.
- Separator.
- Interaction States.
- Responsive Behavior.
- Navigation Hierarchy.

Jika state atau property tidak dapat diverifikasi, AI MUST NOT mengarang spesifikasinya.

### 13.5 Final AI Instruction

**AI MUST retrieve and reuse the official GEMS Breadcrumbs component from the specified Figma source whenever the integration supports it.**

AI MUST select a supported combination of Divider, Type, and Breakpoint, preserve the official component structure, and configure navigation labels according to the approved application hierarchy.

AI MUST use official GEMS components, tokens, and interaction states wherever available.

AI MUST NOT recreate Breadcrumbs manually, invent unsupported visual variants, or introduce custom navigation patterns without Human Approval.

**GEMS Design System is the single source of truth for Breadcrumbs component specifications.**
