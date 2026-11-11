# GEMS Design System — Empty State Guidelines

## 1. Purpose

Empty State adalah komponen yang digunakan ketika suatu halaman, tabel, daftar, atau area konten tidak memiliki data yang dapat ditampilkan.

Empty State membantu pengguna memahami kondisi konten yang kosong dan, jika diperlukan, memberikan arahan mengenai tindakan berikutnya.

**Core Principle:**

> AI MUST menggunakan komponen Empty State resmi GEMS Design System untuk menampilkan kondisi tanpa data. AI MUST menggunakan variant, ukuran, ikon, ilustrasi, typography, warna, dan layout yang tersedia dalam GEMS Design System.

### 1.1 Mandatory Design System Compliance

AI MUST:

1. Menggunakan instance Empty State resmi GEMS.
2. Memilih konfigurasi resmi berdasarkan konteks.
3. Menggunakan visual assets resmi GEMS.
4. Menggunakan typography, warna, dan spacing resmi.
5. Menggunakan Button resmi GEMS apabila diperlukan.
6. Menyesuaikan judul dan deskripsi dengan kondisi data.
7. Mengikuti HSD/BRD untuk menentukan tindakan yang tersedia.
8. Mempertahankan struktur dan visual properties komponen.
9. Memastikan Empty State muncul berdasarkan kondisi data yang benar.

AI MUST NOT:

1. Membuat Empty State custom jika komponen resmi tersedia.
2. Menggunakan ilustrasi atau ikon dari library lain.
3. Membuat visual variant baru.
4. Mengganti instance resmi dengan Frame custom.
5. Mengubah ukuran, warna, radius, spacing, atau typography di luar GEMS.
6. Menambahkan tindakan yang tidak didukung kebutuhan bisnis.
7. Menggunakan pesan yang tidak sesuai dengan kondisi data.

---

## 2. Empty State Variants & Properties

### 2.1 Official Component Properties

Berdasarkan metadata GEMS Design System, komponen Empty State memiliki dua kelompok properties.

| Property | Available Values |
|---|---|
| Icon | Featured icon, Illustration, File type icon |
| Size | sm, md, lg |

Tersedia sembilan konfigurasi resmi.

### 2.2 Featured Icon

**Property:** `Icon=Featured icon`

Menggunakan featured icon sebagai elemen visual utama.

**Recommended Usage:**

- Empty State pada area konten sederhana.
- Tabel atau daftar tanpa data.
- Hasil pencarian kosong.
- Kondisi kosong yang membutuhkan visual ringkas.

**Rules:**

- MUST menggunakan Featured Icon resmi.
- MUST menggunakan ukuran yang tersedia.
- MUST mempertahankan visual styling resmi.
- MUST NOT mengganti dengan ikon custom.

### 2.3 Illustration

**Property:** `Icon=Illustration`

Menggunakan ilustrasi sebagai elemen visual utama.

**Recommended Usage:**

- Empty State pada area konten yang luas.
- Halaman utama tanpa data.
- Kondisi awal penggunaan fitur.
- Halaman yang membutuhkan penjelasan lebih menonjol.

**Rules:**

- MUST menggunakan Illustration resmi GEMS.
- MUST mengikuti ukuran dan layout komponen.
- MUST NOT menggunakan ilustrasi eksternal.
- MUST NOT membuat ilustrasi baru tanpa Human Approval.

### 2.4 File Type Icon

**Property:** `Icon=File type icon`

Menggunakan ikon yang merepresentasikan file atau dokumen.

**Recommended Usage:**

- Daftar dokumen kosong.
- Halaman lampiran tanpa file.
- Area unggahan yang belum memiliki dokumen.
- Daftar laporan atau file yang belum tersedia.

**Rules:**

- MUST menggunakan File Type Icon resmi.
- MUST memilih ikon sesuai konfigurasi yang didukung.
- MUST NOT membuat file icon custom.
- MUST NOT menggunakan visual yang tidak relevan.

### 2.5 Size Variants

| Size | Recommended Usage |
|---|---|
| sm | Area konten terbatas |
| md | Tabel, daftar, atau container standar |
| lg | Area konten luas atau halaman utama |

Pemilihan ukuran di atas merupakan rekomendasi penggunaan. AI MUST tetap mengikuti ukuran dan layout resmi GEMS.

### 2.6 Variant Selection Rules

AI MUST:

1. Mengidentifikasi konteks Empty State.
2. Memilih jenis Icon resmi.
3. Memilih Size resmi.
4. Mempertahankan struktur komponen.
5. Menggunakan component properties yang tersedia.

AI MUST NOT:

1. Membuat Size baru.
2. Membuat Icon variant baru.
3. Mengubah ukuran secara manual di luar properties.
4. Menggabungkan beberapa visual utama tanpa acuan resmi.

---

## 3. When to Use Empty State

### 3.1 Recommended Usage

Empty State SHOULD digunakan ketika:

1. Halaman belum memiliki data.
2. Tabel tidak memiliki baris data.
3. Daftar belum memiliki item.
4. Pencarian tidak menghasilkan data.
5. Filter tidak menghasilkan data.
6. Pengguna belum membuat konten.
7. Belum ada dokumen atau lampiran.
8. Belum tersedia riwayat aktivitas.
9. Belum ada laporan atau rekap.
10. Area konten tertentu belum memiliki informasi.

### 3.2 Usage Matrix

| Context | Condition | Recommendation |
|---|---|---|
| Data Table | Tidak ada data | Use Empty State |
| List | Daftar kosong | Use Empty State |
| Search Results | Tidak ada hasil pencarian | Use Empty State |
| Filter Results | Tidak ada data sesuai filter | Use Empty State |
| Document List | Belum ada dokumen | Use Empty State |
| Report Page | Belum ada laporan | Use Empty State |
| Activity History | Belum ada aktivitas | Use Empty State |
| Detail Page | Bagian tertentu belum memiliki data | Use contextual Empty State |
| First-time Use | Pengguna belum membuat data | Use Empty State |

### 3.3 Mandatory Usage Conditions

AI MUST menggunakan Empty State ketika:

- Data berhasil dimuat tetapi hasilnya kosong.
- Tabel atau daftar tidak memiliki data yang perlu ditampilkan.
- HSD/BRD menentukan kondisi tanpa data.
- Pattern halaman resmi menggunakan Empty State untuk kondisi tersebut.

AI MUST NOT membiarkan area konten kosong tanpa penjelasan apabila pengguna membutuhkan informasi mengenai kondisi data.

---

## 4. When NOT to Use Empty State

Empty State MUST NOT digunakan untuk:

1. Data yang masih dimuat.
2. Kegagalan jaringan.
3. Kegagalan server.
4. Kesalahan validasi form.
5. Notifikasi keberhasilan.
6. Konfirmasi tindakan.
7. Kondisi akses ditolak tanpa pattern resmi yang sesuai.
8. Konten yang sebenarnya tersedia tetapi gagal ditampilkan.
9. Kondisi error yang membutuhkan Error State khusus.

### 4.1 State Differentiation

| Condition | Appropriate Pattern |
|---|---|
| Data sedang dimuat | Loading / Skeleton |
| Data berhasil dimuat, hasil kosong | Empty State |
| Pencarian berhasil, hasil kosong | Empty State |
| Filter berhasil, hasil kosong | Empty State |
| Permintaan gagal | Error State |
| Koneksi terputus | Network Error |
| Akses tidak diizinkan | Access / Permission State |
| Data tersedia | Normal Content |

AI MUST membedakan kondisi tanpa data dari kondisi kegagalan sistem.

---

## 5. Empty State Component Anatomy

### 5.1 Component Structure

Empty State dapat memiliki elemen berikut sesuai konfigurasi resmi.

| Element | Purpose | Usage |
|---|---|---|
| Container | Membungkus konten Empty State | Required |
| Visual Element | Featured Icon, Illustration, atau File Type Icon | Required sesuai variant |
| Title | Menjelaskan kondisi utama | Required |
| Description | Memberikan informasi tambahan | Mengikuti komponen dan konteks |
| Action Button | Memberikan tindakan berikutnya | Optional, jika didukung |

### 5.2 Visual Element

AI MUST:

- Menggunakan visual resmi GEMS.
- Memilih jenis Icon sesuai konteks.
- Menggunakan ukuran resmi.
- Mempertahankan posisi dan styling resmi.

AI MUST NOT:

- Menggunakan ikon eksternal.
- Membuat ilustrasi custom.
- Mengubah warna visual secara manual.
- Mengubah proporsi visual di luar GEMS.

### 5.3 Title

Title harus menjelaskan kondisi data secara langsung.

**Examples:**

- Belum Ada Data
- Belum Ada Pesanan Tamu
- Belum Ada Jadwal Transportasi
- Belum Ada Rekap Makanan
- Belum Ada Dokumen
- Tidak Ada Hasil Pencarian

**Rules:**

- MUST menggunakan typography resmi.
- MUST sesuai dengan konteks fitur.
- SHOULD singkat dan mudah dipahami.
- MUST NOT menggunakan judul generik jika konteks spesifik tersedia.

### 5.4 Description

Description menjelaskan kondisi atau tindakan berikutnya.

**Examples:**

- Data yang ditambahkan akan ditampilkan di sini.
- Pesanan tamu yang dibuat akan muncul pada halaman ini.
- Jadwal transportasi akan ditampilkan setelah tersedia.
- Coba gunakan kata kunci lain untuk menemukan data.
- Belum ada dokumen yang ditambahkan.

**Rules:**

- MUST sesuai dengan kondisi data.
- SHOULD menjelaskan informasi yang dibutuhkan pengguna.
- MUST NOT memberikan informasi yang tidak benar.
- MUST NOT menjanjikan tindakan otomatis yang tidak didukung sistem.

### 5.5 Action Button

Action Button digunakan ketika pengguna dapat melakukan tindakan untuk mengatasi kondisi kosong.

**Examples:**

- Tambah Data
- Buat Pesanan
- Unggah Dokumen
- Reset Filter
- Coba Kata Kunci Lain

**Rules:**

- MUST menggunakan Button resmi GEMS.
- MUST mengikuti action hierarchy resmi.
- MUST memiliki tujuan yang jelas.
- MUST NOT menambahkan Button jika pengguna tidak memiliki akses atau kemampuan melakukan tindakan.
- MUST NOT membuat Button custom.

---

## 6. Empty State Conditions & States

Kondisi pada bagian ini merupakan application data states, bukan nama variant visual Figma yang sudah diverifikasi.

### 6.1 State Matrix

| State | Trigger | Expected Behavior |
|---|---|---|
| Initial Empty | Belum pernah ada data | Menjelaskan bahwa data belum tersedia |
| No Data | Dataset kosong | Menampilkan informasi tidak ada data |
| No Search Results | Pencarian tidak menemukan hasil | Menjelaskan hasil pencarian kosong |
| No Filter Results | Filter tidak menemukan data | Menjelaskan tidak ada data sesuai filter |
| No Documents | Belum ada file | Menjelaskan belum ada dokumen |
| No Activity | Belum ada aktivitas | Menjelaskan riwayat masih kosong |
| Empty Section | Bagian tertentu tidak memiliki data | Menampilkan Empty State pada area terkait |
| Populated | Data tersedia | Empty State disembunyikan |

### 6.2 Initial Empty State

Digunakan ketika pengguna belum pernah membuat data pada suatu fitur.

**Rules:**

- MUST menggunakan Empty State resmi.
- MUST menjelaskan bahwa belum ada data.
- SHOULD memberikan arahan tindakan awal jika tersedia.
- MUST NOT menampilkan pesan kegagalan.
- MUST NOT menambahkan CTA tanpa kebutuhan.

### 6.3 No Data State

Digunakan ketika sistem berhasil memuat data tetapi dataset kosong.

**Rules:**

- MUST menggunakan Empty State resmi.
- MUST menggunakan pesan sesuai jenis data.
- MUST NOT menampilkan Loading State.
- MUST NOT menampilkan Error State.
- MUST NOT membuat ilustrasi custom.

### 6.4 No Search Results State

Digunakan ketika pencarian selesai tetapi tidak menghasilkan data.

**Rules:**

- MUST menjelaskan bahwa pencarian tidak menemukan hasil.
- SHOULD menyarankan perubahan kata kunci.
- MAY menyediakan tindakan reset pencarian jika didukung.
- MUST NOT menyatakan bahwa seluruh data belum tersedia.
- MUST NOT menghapus query pengguna secara otomatis.

**Example:**

Title: Tidak Ada Hasil Pencarian

Description: Tidak ditemukan data yang sesuai. Coba gunakan kata kunci lain.

### 6.5 No Filter Results State

Digunakan ketika filter aktif tetapi tidak ada data yang memenuhi kriteria.

**Rules:**

- MUST menjelaskan bahwa tidak ada data sesuai filter.
- SHOULD memberikan arahan untuk menyesuaikan filter.
- MAY menyediakan Reset Filter jika tersedia.
- MUST NOT menyatakan dataset utama kosong tanpa verifikasi.
- MUST NOT menghapus filter otomatis tanpa tindakan pengguna.

**Example:**

Title: Tidak Ada Data yang Sesuai

Description: Coba ubah atau reset filter untuk menampilkan data lainnya.

### 6.6 No Documents State

Digunakan ketika daftar dokumen atau lampiran kosong.

**Rules:**

- SHOULD mempertimbangkan `Icon=File type icon`.
- MUST menggunakan ikon resmi.
- MUST menggunakan judul sesuai konteks dokumen.
- MAY menyediakan Unggah Dokumen jika pengguna memiliki izin.

**Example:**

Title: Belum Ada Dokumen

Description: Dokumen yang ditambahkan akan ditampilkan di sini.

### 6.7 No Activity State

Digunakan ketika belum ada riwayat atau aktivitas.

**Rules:**

- MUST menjelaskan bahwa aktivitas belum tersedia.
- MUST NOT membuat data aktivitas palsu.
- MUST NOT menambahkan CTA jika tidak relevan.

**Example:**

Title: Belum Ada Riwayat Aktivitas

Description: Aktivitas yang dilakukan akan tercatat di halaman ini.

### 6.8 Empty Section State

Digunakan ketika halaman detail memiliki beberapa bagian dan salah satunya kosong.

**Rules:**

- MUST menampilkan Empty State hanya pada bagian terkait.
- MUST mempertahankan konten lain yang tersedia.
- MUST menggunakan Size sesuai container.
- MUST NOT mengganti seluruh halaman menjadi Empty State apabila hanya satu bagian yang kosong.

### 6.9 Populated State

Digunakan ketika data tersedia.

**Rules:**

- MUST menampilkan konten normal.
- MUST menyembunyikan Empty State pada area yang telah memiliki data.
- MUST NOT menampilkan Empty State bersamaan dengan data normal untuk konteks yang sama.

---

## 7. Empty State in Data Tables

### 7.1 When to Use

Digunakan ketika tabel berhasil dimuat tetapi tidak memiliki baris data.

### 7.2 Layout Rules

AI MUST:

1. Mempertahankan struktur Data Table resmi GEMS.
2. Menggunakan Empty State resmi di area konten kosong.
3. Mempertahankan Table Header jika pattern resmi mengharuskannya.
4. Menggunakan ukuran Empty State yang sesuai.
5. Mempertahankan filter dan search yang relevan.
6. Mengikuti layout resmi.

AI MUST NOT:

1. Membuat Empty State manual di dalam tabel.
2. Menghapus struktur tabel tanpa kebutuhan.
3. Menampilkan baris dummy sebagai pengganti Empty State.
4. Menggunakan Loading State untuk dataset kosong.

---

## 8. Empty State in Lists & Cards

### 8.1 When to Use

Digunakan ketika suatu daftar atau kumpulan Card tidak memiliki item.

### 8.2 Rules

AI MUST:

- Menggunakan Empty State resmi.
- Mempertahankan container dan struktur halaman.
- Memilih ukuran yang sesuai.
- Menggunakan pesan berdasarkan jenis daftar.
- Menyediakan CTA hanya jika relevan.

AI MUST NOT:

- Membuat Card kosong sebagai placeholder permanen.
- Membuat visual Empty State custom.
- Menampilkan data dummy sebagai kondisi final.

---

## 9. Empty State in Search & Filter

### 9.1 Search Empty State

**Condition:** Query pencarian tidak menghasilkan data.

**Rules:**

- MUST mempertahankan input pencarian.
- MUST menggunakan pesan khusus hasil pencarian.
- MUST menggunakan Empty State resmi.
- SHOULD membantu pengguna memperbaiki pencarian.

### 9.2 Filter Empty State

**Condition:** Filter aktif tetapi hasil kosong.

**Rules:**

- MUST mempertahankan filter yang dipilih.
- MUST menjelaskan bahwa hasil filter kosong.
- MAY menyediakan Reset Filter.
- MUST menggunakan Button resmi jika CTA tersedia.

### 9.3 Important Distinction

AI MUST membedakan:

**Dataset Empty:**

Tidak ada data sama sekali.

**Search Empty:**

Data mungkin tersedia, tetapi tidak cocok dengan query.

**Filter Empty:**

Data mungkin tersedia, tetapi tidak memenuhi filter.

Ketiga kondisi tersebut MUST menggunakan wording yang sesuai.

---

## 10. Empty State UX Writing

### 10.1 General Rules

AI MUST:

1. Menggunakan bahasa yang jelas.
2. Mengikuti terminologi HSD/BRD.
3. Menjelaskan kondisi data secara spesifik.
4. Menggunakan deskripsi yang relevan.
5. Menghindari pesan yang menyalahkan pengguna.
6. Menyesuaikan CTA dengan kemampuan pengguna.

AI MUST NOT:

1. Menggunakan pesan generik untuk seluruh fitur.
2. Menggunakan wording error untuk kondisi tanpa data.
3. Menampilkan instruksi yang tidak dapat dilakukan.
4. Menambahkan informasi yang tidak didukung sistem.

### 10.2 Recommended Wording

| Context | Title | Description |
|---|---|---|
| General | Belum Ada Data | Data yang ditambahkan akan ditampilkan di sini. |
| Guest Order | Belum Ada Pesanan Tamu | Pesanan tamu yang dibuat akan muncul pada halaman ini. |
| Transport | Belum Ada Jadwal Transportasi | Jadwal transportasi akan ditampilkan setelah tersedia. |
| Meals Report | Belum Ada Rekap Makanan | Rekap makanan akan ditampilkan setelah data tersedia. |
| Documents | Belum Ada Dokumen | Dokumen yang ditambahkan akan muncul di sini. |
| Search | Tidak Ada Hasil Pencarian | Coba gunakan kata kunci lain. |
| Filter | Tidak Ada Data yang Sesuai | Coba ubah filter untuk melihat data lainnya. |
| Activity | Belum Ada Riwayat Aktivitas | Riwayat aktivitas akan ditampilkan di sini. |

Contoh wording merupakan panduan konten dan dapat disesuaikan dengan kebutuhan aplikasi.

---

## 11. Responsive Behavior

### 11.1 Desktop

AI MUST:

- Menggunakan instance Empty State resmi.
- Memilih Size sesuai container.
- Mempertahankan alignment resmi.
- Menggunakan typography dan spacing GEMS.
- Mengikuti layout halaman.

### 11.2 Mobile

AI MUST:

- Menggunakan komponen Empty State resmi.
- Memilih Size yang sesuai.
- Menjaga keterbacaan Title dan Description.
- Memastikan CTA dapat digunakan.
- Mengikuti responsive behavior resmi.

### 11.3 Responsive Restrictions

AI MUST NOT:

1. Membuat layout mobile custom tanpa acuan.
2. Mengubah ukuran ilustrasi di luar properties.
3. Mengubah typography secara manual.
4. Membuat responsive variant baru tanpa persetujuan.
5. Memotong Title atau Description sehingga informasi penting hilang.

---

## 12. AI Decision Logic

AI MUST mengikuti urutan berikut.

### Step 1 — Identify Data Condition

Periksa kondisi data:

- Loading.
- Success with Data.
- Success without Data.
- Search Empty.
- Filter Empty.
- Error.

### Step 2 — Determine Empty State Necessity

Jika data berhasil dimuat tetapi kosong, gunakan Empty State.

Jika data masih dimuat, gunakan Loading State.

Jika permintaan gagal, gunakan Error State.

### Step 3 — Retrieve Official Component

AI MUST mengakses Empty State resmi GEMS Design System.

### Step 4 — Select Icon Variant

Pilih:

- Featured icon.
- Illustration.
- File type icon.

AI MUST memilih variant resmi sesuai konteks.

### Step 5 — Select Size

Pilih:

- sm.
- md.
- lg.

AI MUST mempertimbangkan area penempatan dan aturan GEMS.

### Step 6 — Configure Content

Sesuaikan:

- Title.
- Description.
- Action Button jika tersedia dan diperlukan.

### Step 7 — Apply Design System

AI MUST menggunakan:

- Empty State resmi.
- Typography resmi.
- Color tokens resmi.
- Spacing resmi.
- Button resmi jika diperlukan.
- Icon atau Illustration resmi.

### Step 8 — Validate Data Logic

Pastikan:

- Empty State muncul hanya ketika kondisi sesuai.
- Loading dan Error tidak disalahartikan sebagai Empty State.
- Search Empty dan Filter Empty menggunakan pesan yang benar.
- Empty State hilang ketika data tersedia.

### Step 9 — Validate Against GEMS

AI MUST memastikan:

1. Instance resmi digunakan.
2. Icon variant sesuai.
3. Size sesuai.
4. Visual asset resmi.
5. Typography sesuai.
6. Color tokens sesuai.
7. Spacing sesuai.
8. Alignment sesuai.
9. CTA menggunakan Button resmi.
10. Tidak ada visual custom.

### Step 10 — Request Human Approval

Jika kebutuhan tidak didukung komponen resmi, AI MUST meminta Human Approval sebelum membuat alternatif.

---

## 13. AI Restrictions

AI MUST NOT:

1. Membuat Empty State custom jika komponen resmi tersedia.
2. Menggunakan komponen dari library lain.
3. Mengganti instance resmi dengan Frame custom.
4. Membuat ilustrasi custom.
5. Menggunakan ikon eksternal.
6. Membuat Size baru.
7. Membuat Icon variant baru.
8. Mengubah typography di luar GEMS.
9. Mengubah warna di luar GEMS.
10. Mengubah spacing secara manual.
11. Mengubah struktur komponen resmi.
12. Menggunakan Empty State sebagai Loading State.
13. Menggunakan Empty State sebagai Error State.
14. Menampilkan pesan generik untuk seluruh kondisi.
15. Menampilkan data dummy sebagai pengganti Empty State.
16. Membuat CTA yang tidak relevan.
17. Menggunakan Button custom.
18. Mengabaikan role access.
19. Menghapus filter atau search otomatis.
20. Mengganti seluruh halaman ketika hanya satu section kosong.
21. Menggunakan visual yang tidak sesuai konteks.
22. Membuat responsive variant baru tanpa persetujuan.
23. Mengklaim desain sesuai GEMS tanpa verifikasi.

---

## 14. Official GEMS Design System Component

### 14.1 Component Reference

**Component Name:** Empty State  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=398-2239

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `398:2239`

### 14.2 Verified Component Configurations

**Icon:**
- Featured icon
- Illustration
- File type icon

**Size:**
- sm
- md
- lg

**Total:** 9 configurations.

### 14.3 Mandatory Component Usage

AI MUST:

1. Mengakses komponen Empty State resmi.
2. Menggunakan instance resmi GEMS.
3. Memilih Icon dan Size yang tersedia.
4. Mempertahankan visual properties resmi.
5. Menggunakan Title dan Description sesuai konteks.
6. Menggunakan Button resmi apabila CTA diperlukan.
7. Mengikuti data state yang benar.
8. Mempertahankan koneksi library apabila didukung.
9. Memvalidasi hasil implementasi terhadap sumber resmi.

### 14.4 Component Verification

Sebelum implementasi, AI MUST memeriksa:

- Component Name.
- Available Variants.
- Component Properties.
- Icon Type.
- Size.
- Typography.
- Colors.
- Spacing.
- Alignment.
- Action Button Support.
- Responsive Behavior.

Jika suatu properti tidak dapat diverifikasi, AI MUST NOT mengarang spesifikasinya.

### 14.5 Final AI Instruction

**AI MUST retrieve and reuse the official GEMS Empty State component from the specified Figma source whenever the integration supports it.**

AI MUST select a supported Icon and Size configuration, preserve the official component structure, and configure content according to the application data condition and approved HSD/BRD requirements.

AI MUST use official GEMS components and tokens for all supported elements.

AI MUST NOT recreate Empty State manually, invent unsupported visual variants, or introduce custom styling without Human Approval.

**GEMS Design System is the single source of truth for all Empty State visual specifications.**
