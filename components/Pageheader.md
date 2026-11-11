# Page Header — GEMS AI Design Guidelines

## 1. Overview

Page Header merupakan komponen tingkat halaman yang digunakan untuk menampilkan judul, deskripsi, identitas, dan tindakan utama yang relevan dengan suatu halaman.

Page Header membantu pengguna memahami konteks halaman dan menemukan tindakan yang tersedia sebelum berinteraksi dengan konten utama.

Komponen ini dapat digunakan pada halaman yang berisi Data Table, Card, Dashboard, Form, atau Detail. Namun, Page Header tidak menggantikan Header internal komponen-komponen tersebut.

### General Rules

- AI MUST menggunakan instance Page Header resmi GEMS Design System.
- AI MUST menentukan kebutuhan Header berdasarkan HSD/BRD.
- AI MUST menggunakan variant dan properti yang tersedia.
- AI MUST memilih elemen yang ditampilkan berdasarkan kebutuhan halaman.
- AI MUST NOT membuat ulang komponen menggunakan susunan custom jika komponen resmi dapat digunakan.
- AI MUST NOT menggunakan Page Header sebagai Card Header, Table Header, atau Section Heading.

---

## 2. Component Variants

### 2.1 Official Styles

| Style | Desktop | Mobile |
|---|---|---|
| Simple | Tersedia | Tersedia |
| Simple-with-badge | Tersedia | Belum teridentifikasi |
| Avatar | Tersedia | Tersedia |
| Banner simple | Tersedia | Tersedia |
| Banner avatar | Tersedia | Tersedia |
| Banner simple centered | Tersedia | Tersedia |
| Banner avatar centered | Tersedia | Tersedia |

### 2.2 Variant Selection

**Simple**

Digunakan untuk halaman standar yang membutuhkan judul dan informasi pendukung tanpa identitas Avatar atau Banner.

**Simple-with-badge**

Digunakan ketika judul halaman perlu disertai atribut atau status menggunakan Badge.

**Avatar**

Digunakan untuk halaman yang berfokus pada identitas individu.

**Banner simple**

Digunakan ketika halaman membutuhkan area Banner tanpa Avatar.

**Banner avatar**

Digunakan ketika halaman membutuhkan Banner dan identitas individu.

**Centered variants**

Digunakan ketika kebutuhan komposisi halaman sesuai dengan struktur Banner terpusat yang tersedia di GEMS.

### AI Rules

- AI SHOULD menggunakan `Simple` sebagai pilihan awal untuk halaman standar.
- AI MUST memilih variant lain hanya ketika kebutuhan halaman mendukungnya.
- AI MUST NOT menggunakan Banner atau Avatar hanya untuk mempercantik tampilan.
- AI MUST NOT membuat variant Mobile yang tidak tersedia tanpa persetujuan.

---

## 3. Component Properties

### 3.1 Official Properties

Properti berikut teridentifikasi pada variasi Page Header GEMS yang diperiksa.

| Property | Values | Description |
|---|---|---|
| Style | Sesuai variant resmi | Menentukan tampilan Page Header |
| Breakpoint | Desktop / Mobile | Menentukan layout berdasarkan perangkat |
| Actions | True / False | Menampilkan atau menyembunyikan area tindakan |
| Breadcrumbs | True / False | Menampilkan atau menyembunyikan navigasi kontekstual |
| Supporting text | True / False | Menampilkan atau menyembunyikan deskripsi |
| Search | True / False | Menampilkan atau menyembunyikan pencarian |
| Divider | True / False | Menampilkan atau menyembunyikan garis pemisah |

Ketersediaan dan susunan elemen harus mengikuti instance yang digunakan.

### 3.2 Property Rules

- AI MUST menggunakan properti resmi pada instance terkait.
- AI MUST NOT menganggap semua properti wajib bernilai `True`.
- AI MUST menentukan nilai properti berdasarkan kebutuhan.
- AI MUST NOT mengubah struktur internal komponen secara manual.
- AI MUST memverifikasi ketersediaan kombinasi properti pada variant yang dipilih.

---

## 4. When to Use

### 4.1 List & Management Page

Digunakan untuk memperkenalkan halaman pengelolaan atau daftar data.

**Recommended Style:** Simple

**Contoh kebutuhan:**

- Daftar pengguna.
- Pengelolaan data.
- Riwayat transaksi.
- Monitoring aktivitas.

**AI Rules:**

- AI MUST menampilkan judul halaman yang relevan.
- AI SHOULD menampilkan Supporting text jika membantu menjelaskan halaman.
- AI SHOULD menampilkan Actions jika tersedia tindakan utama.
- AI MUST NOT menggunakan Page Header sebagai judul internal tabel.

### 4.2 Dashboard Page

Digunakan untuk memperkenalkan dashboard atau halaman monitoring.

**Recommended Style:** Simple

**AI Rules:**

- AI MUST menjaga hierarki antara Page Header dan konten dashboard.
- AI SHOULD menampilkan tindakan tingkat halaman jika diperlukan.
- AI MUST NOT menggunakan Banner tanpa kebutuhan yang jelas.

### 4.3 Form Page

Digunakan pada halaman formulir yang berdiri sendiri.

**Recommended Style:** Simple

**AI Rules:**

- AI MUST menggunakan judul sesuai tujuan formulir.
- AI SHOULD menampilkan deskripsi jika diperlukan.
- AI MUST membedakan Page Header dari Form Section Heading.
- AI MUST NOT memindahkan tindakan formulir ke Page Header jika alur resmi menempatkannya pada area lain.

### 4.4 Detail Page

Digunakan untuk menampilkan identitas atau konteks data yang sedang dibuka.

**Recommended Style:**

- Simple untuk detail umum.
- Simple-with-badge untuk detail dengan atribut Badge.
- Avatar untuk detail individu.

**AI Rules:**

- AI MUST menggunakan informasi aktual.
- AI MUST memilih Style sesuai jenis data.
- AI MUST NOT menambahkan status atau identitas fiktif.

### 4.5 Profile Page

Digunakan ketika identitas individu menjadi fokus utama halaman.

**Recommended Style:** Avatar atau Banner avatar.

**AI Rules:**

- AI MUST menggunakan identitas valid.
- AI MUST menggunakan komponen Avatar resmi.
- AI MUST mengikuti fallback pada `avatar.md`.
- AI MUST NOT menganggap seluruh halaman profil membutuhkan Banner.

### 4.6 Banner-Based Page

Digunakan ketika halaman memang membutuhkan area Banner.

**Recommended Style:** Banner simple, Banner avatar, atau variasi centered yang sesuai.

**AI Rules:**

- AI MUST menggunakan struktur Banner resmi.
- AI MUST menjaga keterbacaan konten.
- AI MUST NOT menambahkan Banner tanpa kebutuhan desain yang dapat dipertanggungjawabkan.

---

## 5. When NOT to Use

| Context | Appropriate Component |
|---|---|
| Judul internal Card | Card Header |
| Judul kolom Table | Table Header |
| Judul section konten | Section Heading |
| Judul Modal | Modal Header |
| Navigasi global | App Header / Navigation |
| Judul Accordion | Accordion Header |
| Label field | Input Label |

### AI Rules

- AI MUST menggunakan Page Header hanya pada hierarki halaman.
- AI MUST NOT mengulang Page Header pada setiap Card.
- AI MUST NOT mengganti Header internal Table dengan Page Header.
- AI MUST NOT membuat beberapa Page Header utama tanpa kebutuhan yang telah disetujui.

---

## 6. Content Structure

### 6.1 Component Anatomy

| Element | Function | Requirement |
|---|---|---|
| Page Title | Menampilkan judul utama halaman | Utama |
| Supporting Text | Memberikan deskripsi halaman | Opsional |
| Actions | Menampilkan tindakan halaman | Opsional |
| Breadcrumbs / Back | Menampilkan navigasi kontekstual | Opsional |
| Search | Menampilkan pencarian | Opsional |
| Divider | Memisahkan Header dan konten | Opsional |
| Badge | Menampilkan atribut/status | Sesuai Style |
| Avatar | Menampilkan identitas | Sesuai Style |
| Banner | Menampilkan area visual | Sesuai Style |

### 6.2 Title

- AI MUST menggunakan judul yang sesuai dengan fungsi halaman.
- AI MUST menjaga hierarki tipografi GEMS.
- AI MUST NOT menggunakan teks yang tidak relevan.

### 6.3 Supporting Text

- AI SHOULD menggunakan deskripsi jika memberikan konteks tambahan.
- AI MUST menggunakan informasi yang valid.
- AI MUST NOT menambahkan deskripsi hanya untuk mengisi ruang.

### 6.4 Supporting Components

- Button mengikuti `components/button.md`.
- Avatar mengikuti `components/avatar.md`.
- Badge mengikuti `components/badge.md`.
- Breadcrumbs mengikuti `components/breadcrumbs.md`.
- Search menggunakan komponen Input resmi GEMS.

---

## 7. Actions & Button Guidelines

### 7.1 Overview

Page Header mendukung area `Actions` untuk menampilkan tindakan yang relevan dengan halaman.

Area Actions dapat diaktifkan atau dinonaktifkan melalui properti resmi.

### 7.2 When to Show Actions

Gunakan `Actions=True` ketika halaman memiliki tindakan yang memang perlu tersedia pada area Page Header.

**Contoh penggunaan:**

| Page Context | Possible Action |
|---|---|
| Halaman daftar | Tambah Data |
| Halaman manajemen | Buat Pengajuan |
| Halaman detail | Edit Data |
| Halaman laporan | Ekspor Data |
| Halaman profil | Edit Profil |

Contoh tersebut merupakan pola penggunaan yang direkomendasikan, bukan label atau tindakan wajib GEMS.

### 7.3 When to Hide Actions

Gunakan `Actions=False` ketika:

- Halaman hanya menampilkan informasi.
- Tidak terdapat tindakan utama.
- Tindakan telah ditempatkan pada area lain sesuai alur resmi.
- Pengguna tidak memiliki permission untuk menjalankan tindakan.

### 7.4 Button Hierarchy

Pada contoh Page Header GEMS yang diperiksa, area Actions dapat memuat Button dengan hierarki Primary, Secondary, dan Tertiary.

**AI Rules:**

- AI MUST menggunakan Button resmi GEMS.
- AI MUST mengikuti aturan hierarki Button pada `button.md`.
- AI SHOULD memprioritaskan tindakan utama sesuai kebutuhan bisnis.
- AI MUST NOT menambahkan semua jenis Button hanya karena contoh GEMS menampilkannya.
- AI MUST NOT menganggap jumlah Button pada contoh Figma sebagai jumlah wajib.
- AI MUST mengikuti permission dan kondisi tindakan.

### 7.5 Desktop & Mobile Actions

**Desktop:**

Area Actions dapat ditampilkan sejajar dengan informasi utama sesuai layout resmi.

**Mobile:**

Area Actions mengikuti susunan Mobile resmi dan dapat berada pada baris tersendiri.

**AI Rules:**

- AI MUST menggunakan layout Actions sesuai breakpoint.
- AI MUST NOT memaksakan susunan Desktop pada Mobile.
- AI MUST menjaga keterbacaan label Button.
- AI MUST NOT menyembunyikan tindakan penting tanpa pola pengganti yang disetujui.

---

## 8. Breadcrumbs, Search & Divider

### 8.1 Breadcrumbs

Breadcrumbs digunakan ketika pengguna membutuhkan informasi posisi atau navigasi kembali.

Pada contoh GEMS yang diperiksa, Desktop menggunakan susunan Breadcrumbs, sedangkan Mobile dapat menggunakan kontrol Back.

**AI Rules:**

- AI MUST menggunakan navigasi sesuai struktur halaman.
- AI MUST menggunakan komponen resmi.
- AI MUST NOT membuat jalur navigasi fiktif.
- AI MUST NOT menganggap Desktop dan Mobile harus menampilkan susunan Breadcrumbs yang identik.

### 8.2 Search

Search digunakan ketika kebutuhan halaman memerlukan pencarian yang sesuai dengan cakupan data.

**AI Rules:**

- AI MUST mengaktifkan Search hanya jika pencarian memang dibutuhkan.
- AI MUST menggunakan komponen Input resmi.
- AI MUST menentukan cakupan pencarian berdasarkan HSD/BRD.
- AI MUST NOT menambahkan Search tanpa fungsi yang jelas.
- AI MUST NOT menduplikasi Search di Page Header dan area konten tanpa alasan yang disetujui.

### 8.3 Divider

Divider digunakan untuk memisahkan area Header dari konten sesuai struktur resmi.

**AI Rules:**

- AI MUST menggunakan properti Divider resmi.
- AI MUST mengikuti kebutuhan layout.
- AI MUST NOT membuat garis pemisah tambahan secara manual tanpa alasan.

---

## 9. States & Responsive Behavior

### 9.1 Default State

Page Header menampilkan konten dan elemen yang diaktifkan sesuai konfigurasi.

### 9.2 Optional Content Hidden

Ketika elemen opsional tidak diperlukan, gunakan properti resmi untuk menyembunyikannya.

### 9.3 Loading & Error

- AI MUST mengikuti mekanisme loading dan error sistem.
- AI MUST NOT membuat state Page Header baru tanpa acuan.
- AI MUST menjaga struktur Header tetap stabil.

### 9.4 Desktop

- AI MUST menggunakan variant Desktop resmi.
- AI MUST mengikuti alignment dan spacing GEMS.
- AI MUST mempertahankan hierarki judul dan Actions.

### 9.5 Mobile

- AI MUST menggunakan variant Mobile resmi.
- AI MUST menjaga keterbacaan judul dan deskripsi.
- AI MUST menggunakan susunan Actions sesuai komponen Mobile.
- AI MUST NOT hanya memperkecil layout Desktop.

---

## 10. Accessibility Guidelines

### 10.1 Heading

- AI MUST menjaga hierarki heading.
- AI MUST memastikan judul utama halaman dapat dikenali.
- AI MUST NOT membuat struktur heading yang membingungkan.

### 10.2 Actions

- Button harus memiliki label yang jelas.
- Button harus mendukung keyboard.
- Focus indicator harus terlihat.
- Disabled state harus sesuai aturan Button GEMS.

### 10.3 Breadcrumbs & Search

- Breadcrumbs harus memiliki urutan navigasi yang dapat dipahami.
- Kontrol Back harus memiliki nama aksesibel.
- Search harus memiliki label aksesibel.
- Elemen interaktif harus dapat dioperasikan dengan keyboard.

### 10.4 Supporting Content

- Avatar mengikuti aksesibilitas `avatar.md`.
- Badge mengikuti aksesibilitas `badge.md`.
- Banner tidak boleh mengurangi keterbacaan informasi utama.

---

## 11. AI Decision Logic

AI MUST mengikuti urutan keputusan berikut.

### Step 1 — Identify Page Context

Tentukan jenis halaman berdasarkan HSD/BRD.

### Step 2 — Select Style

| Requirement | Recommended Style |
|---|---|
| Halaman standar | Simple |
| Halaman dengan Badge | Simple-with-badge |
| Halaman identitas individu | Avatar |
| Halaman dengan Banner | Banner simple |
| Halaman dengan Banner dan identitas | Banner avatar |
| Kebutuhan komposisi terpusat | Centered variant |

### Step 3 — Select Breakpoint

Pilih variant Desktop atau Mobile yang tersedia.

### Step 4 — Configure Content

Tentukan:

- Page Title.
- Supporting Text.
- Avatar atau Badge jika relevan.
- Banner jika diperlukan.

### Step 5 — Configure Optional Properties

| Requirement | Property |
|---|---|
| Tindakan halaman diperlukan | `Actions=True` |
| Tidak ada tindakan halaman | `Actions=False` |
| Navigasi kontekstual diperlukan | `Breadcrumbs=True` |
| Tidak memerlukan navigasi kontekstual | `Breadcrumbs=False` |
| Deskripsi diperlukan | `Supporting text=True` |
| Deskripsi tidak diperlukan | `Supporting text=False` |
| Pencarian diperlukan | `Search=True` |
| Pencarian tidak diperlukan | `Search=False` |
| Pemisah diperlukan | `Divider=True` |
| Pemisah tidak diperlukan | `Divider=False` |

### Step 6 — Validate Supporting Components

Pastikan Button, Avatar, Badge, Breadcrumbs, dan Input menggunakan komponen resmi GEMS.

### Step 7 — Validate Output

AI MUST memastikan:

1. Page Header digunakan pada tingkat halaman.
2. Style dan Breakpoint tersedia.
3. Semua properti sesuai kebutuhan.
4. Actions hanya ditampilkan jika diperlukan.
5. Search memiliki fungsi yang jelas.
6. Breadcrumbs sesuai navigasi.
7. Informasi berasal dari data valid.
8. Layout Desktop dan Mobile mengikuti GEMS.
9. Aksesibilitas terpenuhi.
10. Tidak ada komponen atau perilaku baru tanpa persetujuan.

---

## 12. AI Implementation Rules

### 12.1 Mandatory Rules

AI MUST:

1. Menggunakan instance Page Header resmi GEMS.
2. Memilih Style sesuai konteks halaman.
3. Menggunakan Breakpoint resmi.
4. Mengonfigurasi Actions berdasarkan kebutuhan.
5. Menggunakan Button resmi ketika Actions diaktifkan.
6. Mengonfigurasi Breadcrumbs berdasarkan navigasi.
7. Mengonfigurasi Search berdasarkan fungsi pencarian.
8. Menggunakan Supporting text hanya jika diperlukan.
9. Menggunakan Divider sesuai layout.
10. Menggunakan Avatar dan Badge resmi.
11. Menjaga hierarki konten.
12. Mengikuti HSD/BRD dan permission.
13. Menjaga responsivitas.
14. Memenuhi aksesibilitas.
15. Meminta persetujuan untuk pola yang belum didukung.

### 12.2 Prohibited Rules

AI MUST NOT:

1. Membuat Page Header custom tanpa persetujuan.
2. Menggunakan Page Header sebagai Card Header.
3. Menggunakan Page Header sebagai Table Header.
4. Membuat Style atau Breakpoint baru.
5. Menambahkan Button tanpa kebutuhan tindakan.
6. Menganggap seluruh Page Header wajib memiliki Button.
7. Menambahkan Search tanpa fungsi.
8. Membuat Breadcrumbs fiktif.
9. Menambahkan Badge tanpa data.
10. Menambahkan Avatar tanpa kebutuhan identitas.
11. Menggunakan Banner sebagai dekorasi.
12. Mengubah susunan resmi secara sembarangan.
13. Menyalin jumlah Button contoh Figma sebagai ketentuan wajib.
14. Mengabaikan permission pengguna.
15. Menghilangkan tindakan penting pada Mobile tanpa pola yang disetujui.
16. Membuat state atau interaksi baru tanpa persetujuan.

### 12.3 Source of Truth

| Source | Responsibility |
|---|---|
| GEMS Design System | Komponen, Style, Breakpoint, properti, dan visual |
| HSD / BRD | Kebutuhan halaman, tindakan, navigasi, dan permission |
| System Data | Judul, identitas, status, dan informasi aktual |
| Human Approval | Persetujuan perubahan atau penambahan pola |

### 12.4 Final AI Instruction

AI MUST menggunakan Page Header resmi GEMS Design System sebagai komponen pengenal halaman.

AI MUST menentukan Style, Breakpoint, serta konfigurasi Actions, Breadcrumbs, Supporting text, Search, dan Divider berdasarkan kebutuhan halaman.

AI MUST menggunakan komponen resmi GEMS untuk seluruh elemen pendukung dan MUST NOT menganggap semua elemen opsional selalu wajib ditampilkan.

AI MUST NOT membuat komponen, variant, state, atau interaksi baru di luar GEMS tanpa persetujuan manusia yang berwenang.

---

## 13. Official GEMS Design System — Component Specifications

**Page Header:** [GEMS Design System — Page Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-7905)

**Variant dan properti yang telah diperiksa:**

- Style: Simple, Simple-with-badge, Avatar, Banner simple, Banner avatar, Banner simple centered, Banner avatar centered.
- Breakpoint: Desktop dan Mobile sesuai ketersediaan.
- Actions: True / False.
- Breadcrumbs: True / False.
- Supporting text: True / False.
- Search: True / False.
- Divider: True / False.

**Implementation Note:** AI MUST menggunakan instance dan properti resmi GEMS. Aturan penggunaan dalam dokumen ini tidak memberikan izin untuk membuat variasi atau komposisi baru di luar Design System.
