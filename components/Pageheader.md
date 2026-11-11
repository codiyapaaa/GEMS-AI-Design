# Page Header — GEMS AI Design Guidelines

## 1. Purpose & Core Principles

Page Header adalah komponen GEMS Design System yang berfungsi menampilkan identitas dan konteks utama suatu halaman, termasuk judul, informasi pendukung, navigasi, pencarian, serta tindakan yang relevan.

### Core Principles

**1. Page-Level Hierarchy**

AI MUST menggunakan Page Header untuk konteks utama halaman, bukan sebagai Header internal Card, Table, atau Modal.

**2. Requirement-Driven Design**

AI MUST menentukan penggunaan dan konfigurasi Page Header berdasarkan HSD/BRD, kebutuhan pengguna, dan hak akses.

**3. Official Component Reuse**

AI MUST menggunakan instance Page Header resmi GEMS Design System, bukan membuat komponen pengganti.

**4. Purposeful Content**

AI MUST menampilkan elemen hanya jika memiliki fungsi yang relevan. Actions, Search, Breadcrumbs, dan Supporting Text tidak wajib selalu ditampilkan.

**5. Responsive Consistency**

AI MUST menggunakan variasi Desktop dan Mobile resmi, dengan mempertahankan informasi serta tindakan penting.

**6. Human Validation**

AI MUST meminta persetujuan manusia yang berwenang untuk penambahan atau perubahan variant, struktur, dan interaksi yang tidak didukung GEMS.

---

## 2. Component Types & Variants

### 2.1 Official Variants

| Style | Desktop | Mobile |
|---|---|---|
| Simple | Available | Available |
| Simple-with-badge | Available | Not identified |
| Avatar | Available | Available |
| Banner simple | Available | Available |
| Banner avatar | Available | Available |
| Banner simple centered | Available | Available |
| Banner avatar centered | Available | Available |

### 2.2 Variant Usage

| Variant | Recommended Usage |
|---|---|
| Simple | Halaman standar, daftar, dashboard, formulir, dan detail umum |
| Simple-with-badge | Halaman yang membutuhkan Badge atau status pada judul |
| Avatar | Halaman identitas atau profil individu |
| Banner simple | Halaman dengan kebutuhan visual Banner |
| Banner avatar | Halaman dengan Banner dan identitas individu |
| Banner simple centered | Halaman Banner dengan komposisi terpusat |
| Banner avatar centered | Halaman Banner dan Avatar dengan komposisi terpusat |

### AI Rules

- AI SHOULD menggunakan Simple sebagai pilihan awal halaman standar.
- AI MUST memilih variant berdasarkan konteks HSD/BRD.
- AI MUST memverifikasi kombinasi Style dan Breakpoint.
- AI MUST NOT menambahkan Banner, Badge, atau Avatar hanya untuk dekorasi.
- AI MUST NOT membuat variant yang tidak tersedia tanpa persetujuan.

---

## 3. Component Properties

### 3.1 Official Properties

| Property | Value | Function |
|---|---|---|
| Style | Official styles | Menentukan tampilan Page Header |
| Breakpoint | Desktop / Mobile | Menentukan layout perangkat |
| Actions | True / False | Menampilkan area tindakan |
| Breadcrumbs | True / False | Menampilkan navigasi kontekstual |
| Supporting text | True / False | Menampilkan deskripsi |
| Search | True / False | Menampilkan pencarian |
| Divider | True / False | Menampilkan garis pemisah |

### 3.2 Property Configuration

| Condition | Configuration |
|---|---|
| Halaman memiliki tindakan utama | Actions = True |
| Halaman tanpa tindakan utama | Actions = False |
| Membutuhkan navigasi kontekstual | Breadcrumbs = True |
| Membutuhkan deskripsi tambahan | Supporting text = True |
| Membutuhkan pencarian tingkat halaman | Search = True |
| Membutuhkan pemisah visual | Divider = True |

### AI Rules

- AI MUST menggunakan properti resmi yang tersedia.
- AI MUST menentukan konfigurasi berdasarkan kebutuhan halaman.
- AI MUST NOT menganggap seluruh properti wajib aktif.
- AI MUST NOT membuat properti baru.
- AI MUST memeriksa dukungan properti pada instance yang dipilih.

---

## 4. When to Use

### 4.1 List & Management Page

Digunakan pada halaman yang menampilkan daftar atau pengelolaan data.

**Recommended Variant:** Simple.

Contoh: Daftar Pengguna, Manajemen Dokumen, Riwayat Aktivitas.

Actions dapat digunakan untuk tindakan tingkat halaman seperti Tambah Data atau Buat Pengajuan, jika tercantum dalam kebutuhan.

### 4.2 Dashboard Page

Digunakan untuk menampilkan judul dan konteks halaman dashboard.

**Recommended Variant:** Simple.

Supporting Text dapat menjelaskan cakupan dashboard. Actions hanya digunakan jika terdapat tindakan tingkat halaman.

### 4.3 Form Page

Digunakan pada halaman formulir yang berdiri sendiri.

**Recommended Variant:** Simple.

Judul menjelaskan tujuan formulir. Tindakan penyimpanan atau pembatalan tetap mengikuti penempatan yang ditentukan dalam alur formulir.

### 4.4 Detail Page

Digunakan pada halaman detail suatu data atau entitas.

**Recommended Variant:** Simple atau Simple-with-badge.

Gunakan Badge ketika informasi status atau atribut memang perlu ditampilkan pada Page Header.

### 4.5 Profile Page

Digunakan pada halaman yang berfokus pada identitas individu.

**Recommended Variant:** Avatar atau Banner avatar.

AI MUST menggunakan data identitas yang valid dan mengikuti `avatar.md`.

### 4.6 Banner-Based Page

Digunakan ketika kebutuhan halaman mencakup area Banner.

**Recommended Variant:** Banner simple, Banner avatar, atau variasi centered.

AI MUST NOT menambahkan Banner tanpa kebutuhan yang jelas.

---

## 5. When NOT to Use

| Context | Use Instead |
|---|---|
| Judul Card | Card Header |
| Judul atau kolom Table | Table Header |
| Judul bagian konten | Section Heading |
| Judul Modal | Modal Header |
| Navigasi global aplikasi | App Header / Navigation |
| Label field | Input Label |

### AI Rules

- AI MUST NOT menggunakan Page Header sebagai judul setiap Card atau Section.
- AI MUST NOT menggantikan Table Header dengan Page Header.
- AI MUST NOT membuat lebih dari satu Page Header utama tanpa kebutuhan yang disetujui.

---

## 6. Content Structure

### 6.1 Component Anatomy

| Element | Requirement | Description |
|---|---|---|
| Page Title | Required | Judul utama halaman |
| Supporting Text | Optional | Deskripsi atau konteks tambahan |
| Actions | Optional | Tindakan tingkat halaman |
| Breadcrumbs / Back | Optional | Navigasi kontekstual |
| Search | Optional | Pencarian |
| Divider | Optional | Pemisah visual |
| Badge | Conditional | Atribut atau status |
| Avatar | Conditional | Identitas individu |
| Banner | Conditional | Area visual |

### 6.2 Content Guidelines

**Page Title**

- MUST menggambarkan fungsi halaman.
- MUST menggunakan istilah yang konsisten dengan sistem.
- MUST mengikuti hierarki tipografi GEMS.

**Supporting Text**

- SHOULD ringkas dan informatif.
- MUST relevan dengan konteks halaman.
- MUST NOT mengulang judul tanpa informasi tambahan.

**Actions**

- MUST memiliki fungsi yang jelas.
- MUST sesuai permission.
- MUST menggunakan komponen Button GEMS.

**Badge, Avatar & Banner**

- MUST mengikuti struktur variant resmi.
- MUST menggunakan data atau aset yang valid.
- MUST NOT digunakan hanya untuk mengisi ruang kosong.

---

## 7. States

### 7.1 Default

Page Header menampilkan elemen sesuai variant dan konfigurasi yang dipilih.

### 7.2 Optional Elements Hidden

Actions, Breadcrumbs, Supporting Text, Search, dan Divider dapat disembunyikan melalui properti resmi.

### 7.3 Loading

Jika data Header belum tersedia, AI MUST mengikuti pola loading resmi sistem. AI MUST NOT membuat skeleton atau state baru tanpa acuan.

### 7.4 Error & Missing Data

Jika informasi Header tidak tersedia, AI MUST mengikuti aturan penanganan data sistem dan komponen terkait.

### AI Rules

- AI MUST mempertahankan struktur komponen resmi.
- AI MUST NOT menciptakan state Page Header baru tanpa persetujuan.
- AI MUST membedakan state komponen pendukung dari state Page Header.

---

## 8. Interactions

### 8.1 Actions & Buttons

Area Actions digunakan untuk tindakan yang relevan dengan halaman.

| Condition | Behavior |
|---|---|
| Ada tindakan tingkat halaman | Actions = True |
| Tidak ada tindakan tingkat halaman | Actions = False |
| Pengguna tidak memiliki permission | Tindakan mengikuti aturan akses sistem |
| Tindakan memiliki konfirmasi | Mengikuti flow konfirmasi resmi |

**AI Rules:**

- AI MUST menggunakan Button resmi GEMS.
- AI MUST mengikuti `components/button.md`.
- AI MUST menentukan hierarki Primary, Secondary, atau Tertiary berdasarkan prioritas tindakan.
- AI MUST NOT menyalin seluruh Button dari contoh Figma sebagai tindakan wajib.
- AI MUST NOT menambahkan tindakan yang tidak tercantum dalam kebutuhan.

### 8.2 Breadcrumbs & Back Navigation

- Desktop dapat menggunakan Breadcrumbs sesuai variant resmi.
- Mobile dapat menggunakan Back Navigation sesuai variant resmi.
- Navigasi MUST mengikuti struktur halaman yang valid.
- AI MUST NOT membuat rute atau tujuan navigasi fiktif.

### 8.3 Search

- Search MUST memiliki cakupan pencarian yang jelas.
- Search MUST menggunakan komponen resmi GEMS.
- Search MUST mengikuti kebutuhan HSD/BRD.
- AI MUST NOT menambahkan Search tanpa fungsi.

### 8.4 Supporting Components

Interaksi Button, Input, Breadcrumbs, dan komponen pendukung lainnya MUST mengikuti guideline masing-masing.

---

## 9. Responsive Behavior

### 9.1 Desktop

- MUST menggunakan variant Desktop resmi.
- MUST mengikuti spacing, alignment, dan hierarki GEMS.
- Actions mengikuti susunan Desktop pada instance yang dipilih.
- Breadcrumbs mengikuti struktur navigasi Desktop.

### 9.2 Mobile

- MUST menggunakan variant Mobile resmi.
- MUST mempertahankan keterbacaan judul dan informasi penting.
- Actions mengikuti susunan Mobile resmi, termasuk penempatan pada baris tersendiri jika ditentukan komponen.
- Back Navigation mengikuti pola Mobile resmi.
- MUST NOT sekadar memperkecil susunan Desktop.

### 9.3 Cross-Platform Rules

- Informasi inti MUST konsisten.
- Tindakan penting MUST tetap dapat diakses sesuai permission.
- Perbedaan visual MUST mengikuti variant resmi.
- AI MUST NOT membuat layout responsif custom tanpa persetujuan jika tidak didukung GEMS.

---

## 10. Accessibility

### 10.1 Heading Hierarchy

- Judul utama halaman MUST memiliki hierarki semantik yang sesuai.
- AI MUST NOT menggunakan heading hanya berdasarkan ukuran visual.

### 10.2 Keyboard & Focus

- Button dan Search MUST dapat dioperasikan menggunakan keyboard.
- Focus indicator MUST terlihat.
- Urutan fokus MUST mengikuti urutan interaksi yang logis.

### 10.3 Navigation

- Breadcrumbs MUST memiliki urutan yang dapat dipahami.
- Back Navigation MUST memiliki nama aksesibel.
- Tujuan navigasi MUST jelas.

### 10.4 Supporting Content

- Badge MUST NOT menyampaikan status hanya melalui warna.
- Avatar MUST mengikuti aksesibilitas `avatar.md`.
- Banner MUST menjaga kontras dan keterbacaan konten.
- Search MUST memiliki label aksesibel.

---

## 11. AI Decision Logic

AI MUST mengikuti proses berikut sebelum menggunakan Page Header.

### Step 1 — Identify Page Context

Identifikasi jenis halaman berdasarkan HSD/BRD: List, Management, Dashboard, Form, Detail, Profile, atau Banner-Based Page.

### Step 2 — Select Official Variant

| Requirement | Recommended Variant |
|---|---|
| Halaman standar | Simple |
| Halaman dengan status atau atribut | Simple-with-badge |
| Halaman identitas individu | Avatar |
| Halaman dengan Banner | Banner simple |
| Halaman dengan Banner dan identitas | Banner avatar |
| Halaman dengan komposisi Banner terpusat | Centered variant |

### Step 3 — Determine Breakpoint

Pilih Desktop atau Mobile dan verifikasi ketersediaan variant.

### Step 4 — Configure Content

Tentukan Page Title, Supporting Text, Badge, Avatar, dan Banner sesuai kebutuhan.

### Step 5 — Configure Optional Properties

Tentukan nilai Actions, Breadcrumbs, Search, Supporting Text, dan Divider berdasarkan fungsi halaman.

### Step 6 — Validate Component Dependencies

Pastikan Button, Input, Badge, Avatar, dan Breadcrumbs menggunakan komponen resmi GEMS.

### Step 7 — Validate Output

AI MUST memastikan:

1. Page Header digunakan pada tingkat halaman.
2. Variant dan Breakpoint tersedia.
3. Properti sesuai kebutuhan.
4. Tindakan sesuai permission.
5. Search dan navigasi memiliki fungsi valid.
6. Konten berasal dari sumber yang benar.
7. Responsivitas mengikuti GEMS.
8. Aksesibilitas terpenuhi.
9. Tidak ada perubahan flow atau variant tanpa persetujuan.

---

## 12. AI Implementation Rules

### 12.1 Mandatory Rules

AI MUST:

1. Menggunakan Page Header resmi GEMS.
2. Menggunakan instance komponen yang tersedia.
3. Memilih variant berdasarkan HSD/BRD.
4. Menggunakan Breakpoint resmi.
5. Mengonfigurasi properti sesuai kebutuhan.
6. Menggunakan komponen pendukung resmi.
7. Menjaga hierarki dan struktur konten.
8. Mengikuti permission dan user flow yang disetujui.
9. Memastikan responsivitas dan aksesibilitas.
10. Memvalidasi perubahan yang belum didukung GEMS.

### 12.2 Prohibited Rules

AI MUST NOT:

1. Membuat Page Header pengganti jika instance resmi tersedia.
2. Menggunakan Page Header sebagai Card atau Table Header.
3. Membuat variant atau properti baru tanpa persetujuan.
4. Menambahkan Actions tanpa kebutuhan.
5. Menambahkan Search tanpa fungsi.
6. Membuat Breadcrumbs atau tujuan navigasi fiktif.
7. Menggunakan Badge, Avatar, atau Banner tanpa kebutuhan.
8. Mengubah struktur internal komponen di luar properti yang didukung.
9. Mengabaikan permission pengguna.
10. Membuat atau mengubah user flow tanpa validasi manusia yang berwenang.

### 12.3 Source of Truth

| Source | Responsibility |
|---|---|
| GEMS Design System | Komponen, variant, properties, dan visual |
| HSD / BRD | Kebutuhan bisnis, navigasi, tindakan, dan permission |
| System Data | Informasi aktual yang ditampilkan |
| Human Approval | Persetujuan perubahan komponen atau user flow |

### 12.4 Final AI Instruction

AI MUST use the official GEMS Page Header component, select its supported variant and properties according to HSD/BRD, and preserve the Design System's structure and behavior.

AI MUST NOT invent components, variants, interactions, or user flows without authorized human validation.

---

## 13. Official GEMS Design System — Component Specifications

### 13.1 Official Component Reference

**Component Name:** Page Header  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-7905&t=oGvGAZSrsS9aDX5O-1

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `240:7905`

### 13.2 Official Component Retrieval

When Figma MCP is available, AI MUST:

1. Access the GEMS Design System using the specified Figma File Key.
2. Locate the Page Header component using Node ID `240:7905`.
3. Inspect the available variants, properties, and component structure.
4. Select the appropriate Desktop or Mobile variant.
5. Reuse the official component instance when the integration supports instantiation.
6. Configure only supported properties and content.
7. Preserve the component's link to the GEMS library where supported.
8. Validate the resulting design against HSD/BRD and GEMS guidelines.

If Figma MCP cannot access or instantiate the component, AI MUST report the limitation and MUST NOT claim that an official instance has been inserted.

### 13.3 Component Reuse Rules

- AI MUST treat the Figma component as the authoritative visual source.
- AI MUST NOT recreate the component when official instance reuse is supported.
- AI MUST NOT replace the component with another design library.
- AI MUST NOT detach or modify the component's internal structure without authorization.
- AI MUST NOT assume example content in Figma represents mandatory business data.
- AI MUST request human validation for unsupported variants, properties, or interactions.

### 13.4 Final Component Instruction

**AI MUST retrieve and reuse the official GEMS Page Header component from the specified Figma source whenever the integration supports it. AI MUST preserve the component's supported variants, properties, visual structure, and intended behavior.**
