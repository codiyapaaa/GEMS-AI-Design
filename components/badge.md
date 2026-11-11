# GEMS Design System — Badge Guidelines

## 1. Purpose & Core Principles

Badge merupakan komponen visual ringkas yang digunakan untuk menyampaikan status, kategori, kondisi, atau informasi singkat mengenai suatu data, proses, atau entitas.

Badge membantu pengguna mengenali informasi penting dengan cepat tanpa harus membaca seluruh detail data.

### 1.1 Primary Purposes

- Menampilkan status proses atau workflow.
- Menampilkan status aktif/nonaktif suatu data.
- Menampilkan kategori atau klasifikasi.
- Menampilkan kondisi operasional.
- Menampilkan label atau metadata singkat.
- Membedakan informasi berdasarkan makna semantik yang telah ditentukan.

### 1.2 Core Principles

1. Badge berfungsi sebagai indikator informasi, bukan aksi utama.
2. Teks Badge harus menyampaikan makna yang jelas.
3. Warna Badge harus mengikuti konteks bisnis dan aturan semantik.
4. Visual Badge harus menggunakan variant resmi GEMS.
5. Badge tidak boleh menjadi satu-satunya cara menyampaikan informasi penting.
6. Badge harus konsisten untuk status atau kondisi yang memiliki makna sama dalam satu sistem.

### 1.3 AI Rules

- MUST menggunakan komponen Badge resmi GEMS.
- MUST menentukan label berdasarkan HSD/BRD.
- MUST menggunakan warna dan Type yang sesuai dengan konteks.
- MUST NOT membuat status atau kategori baru tanpa requirement.
- MUST NOT menentukan warna hanya berdasarkan preferensi estetika.
- MUST NOT menggunakan Badge sebagai pengganti Button atau Toggle.

---

## 2. When to Use Badge

### 2.1 Recommended Usage

| Context | When to Use | Example |
|---|---|---|
| Workflow Status | Menampilkan tahapan proses | Draft, Proposed, Processed, Finished |
| Approval Status | Menampilkan hasil atau kondisi persetujuan | Menunggu Persetujuan, Disetujui, Ditolak |
| Data Activation | Menampilkan kondisi aktif/nonaktif | Aktif, Nonaktif |
| Operational Status | Menampilkan kondisi operasional | Tersedia, Digunakan, Dalam Perbaikan |
| Accommodation Status | Menampilkan kondisi akomodasi | Terisi, Kosong, Reservasi |
| Transport Status | Menampilkan kondisi perjalanan atau penempatan | Draft, Siap Ditempatkan |
| Meal Management | Menampilkan status pesanan atau laporan | Draft, Proposed, Finished |
| Category | Menampilkan kategori data | Staff, Non-Staff |
| Metadata | Menampilkan informasi singkat | Internal, Eksternal |

Status dan label aktual mengikuti kebutuhan HSD/BRD.

### 2.2 When NOT to Use Badge

| Requirement | Reason | Recommended Component |
|---|---|---|
| Menyimpan data | Badge bukan kontrol aksi utama | Button |
| Mengaktifkan fitur | Membutuhkan kontrol biner | Toggle |
| Memilih beberapa data | Membutuhkan selection control | Checkbox |
| Memilih satu opsi | Membutuhkan input pilihan | Radio Button / Dropdown |
| Menampilkan pesan kesalahan lengkap | Membutuhkan penjelasan dan tindakan | Alert |
| Menampilkan notifikasi sementara | Membutuhkan feedback sistem | Notification / Toast |
| Mengubah status workflow | Membutuhkan aksi dan validasi | Button atau workflow control sesuai HSD/BRD |

### 2.3 Selection Rules

- MUST menggunakan Badge untuk menyampaikan informasi ringkas.
- SHOULD menggunakan Badge pada tabel ketika status perlu mudah dipindai.
- SHOULD menggunakan Badge pada halaman detail untuk menampilkan kondisi data.
- MUST NOT menggunakan Badge sebagai satu-satunya kontrol perubahan status.
- MUST NOT menganggap semua Badge dapat diklik.
- MUST mengikuti HSD/BRD apabila suatu label memiliki interaksi khusus.

---

## 3. Badge Component Structure

GEMS Design System menyediakan beberapa tipe visual Badge.

| Type | Description | Recommended Usage |
|---|---|---|
| `Pill color` | Badge berbentuk pill dengan warna semantik | Status dan label ringkas |
| `Pill outline` | Badge berbentuk pill dengan outline | Label atau metadata dengan penekanan lebih ringan |
| `Badge color` | Badge berwarna dengan bentuk non-pill | Status, kategori, dan informasi ringkas |
| `Badge modern` | Variant Badge dengan gaya modern | Konteks yang menggunakan gaya tersebut pada desain |

### 3.1 Official Properties

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Type` | `Pill color`, `Pill outline`, `Badge color`, `Badge modern` |
| `Icon` | `False`, `Dot`, `X close`, `Icon trailing`, `Icon leading`, `Text leading`, `Only`, `Country`, `Avatar` |
| `Color` | `Gray`, `Brand`, `Error`, `Warning`, `Success`, `Blue gray`, `Blue light`, `Blue`, `Indigo`, `Purple`, `Pink`, `Orange` |

### 3.2 Component Rules

- MUST menggunakan Type resmi GEMS.
- MUST menggunakan kombinasi property yang tersedia pada komponen GEMS.
- MUST NOT membuat Type custom tanpa Human Approval.
- SHOULD mempertahankan satu Type yang konsisten dalam kelompok status yang sama.
- MUST mengikuti struktur, ukuran, warna, dan visual GEMS Design System.

---

## 4. Badge Types & Selection

### 4.1 Pill Color

**When to Use:**

Digunakan ketika informasi membutuhkan label ringkas dengan bentuk pill dan penekanan visual berwarna.

**Recommended Context:**

- Workflow status.
- Operational status.
- Status aktif/nonaktif.
- Label kategori.

**AI Rules:**

- MUST mengikuti warna resmi GEMS.
- SHOULD digunakan secara konsisten dalam satu kelompok data.
- MUST NOT menggunakan warna berbeda untuk status bermakna sama tanpa aturan khusus.

### 4.2 Pill Outline

**When to Use:**

Digunakan ketika label memerlukan penekanan visual lebih ringan melalui outline.

**Recommended Context:**

- Metadata.
- Kategori.
- Informasi sekunder.
- Label yang tidak perlu mendominasi tampilan.

**AI Rules:**

- MUST menggunakan outline dan warna resmi GEMS.
- MUST menjaga keterbacaan teks.
- MUST NOT menganggap Pill Outline selalu memiliki prioritas informasi lebih rendah; makna tetap mengikuti konteks.

### 4.3 Badge Color

**When to Use:**

Digunakan ketika desain membutuhkan Badge berwarna dengan bentuk non-pill.

**Recommended Context:**

- Status pada tabel.
- Kategori data.
- Label informasi.
- Penanda kondisi.

**AI Rules:**

- MUST menggunakan variant resmi GEMS.
- SHOULD mempertahankan bentuk yang konsisten dalam satu kelompok informasi.
- MUST NOT mengubah bentuk hanya berdasarkan preferensi estetika.

### 4.4 Badge Modern

**When to Use:**

Digunakan ketika halaman atau komponen membutuhkan gaya Badge Modern.

**AI Rules:**

- MUST mengikuti struktur variant yang tersedia.
- MUST NOT menganggap Badge Modern sebagai pilihan default untuk seluruh status.
- SHOULD mengutamakan konsistensi dengan pola GEMS.

---

## 5. Badge Sizes

### 5.1 Available Sizes

| Size | Recommended Context |
|---|---|
| `sm` | Tabel, daftar, atau area ringkas |
| `md` | Card, detail data, atau informasi standar |
| `lg` | Konteks yang membutuhkan Badge lebih menonjol |

Ukuran dan dimensi aktual mengikuti variant GEMS.

### 5.2 Size Selection Rules

- MUST menggunakan `sm`, `md`, atau `lg`.
- MUST NOT membuat ukuran custom tanpa persetujuan.
- SHOULD menggunakan ukuran konsisten dalam satu tabel.
- SHOULD mempertimbangkan kepadatan informasi dan hierarki visual.
- MUST NOT memperbesar Badge hanya untuk menarik perhatian tanpa alasan informasi.

---

## 6. Badge Colors & Semantic Meaning

Warna Badge membantu pengguna mengenali informasi, tetapi makna bisnis tidak boleh ditentukan hanya berdasarkan warna.

### 6.1 Available Color Variants

| Color | General Semantic Guidance |
|---|---|
| `Gray` | Netral, informasi umum, atau status tanpa penekanan khusus |
| `Brand` | Identitas brand atau penekanan yang ditetapkan sistem |
| `Error` | Kondisi gagal, kesalahan, atau masalah yang relevan |
| `Warning` | Kondisi yang memerlukan perhatian atau kewaspadaan |
| `Success` | Kondisi berhasil atau selesai jika sesuai definisi bisnis |
| `Blue gray` | Informasi netral atau klasifikasi |
| `Blue light` | Informasi atau klasifikasi dengan warna biru muda |
| `Blue` | Informasi atau kondisi yang dipetakan ke biru |
| `Indigo` | Kategori atau kondisi yang dipetakan ke indigo |
| `Purple` | Kategori atau kondisi yang dipetakan ke ungu |
| `Pink` | Kategori atau kondisi yang dipetakan ke pink |
| `Orange` | Kategori atau kondisi yang dipetakan ke oranye |

### 6.2 Semantic Mapping Rules

- MUST mengambil status dari HSD/BRD.
- MUST menggunakan warna resmi GEMS.
- MUST menjaga konsistensi pemetaan status dan warna.
- MUST NOT menganggap semua status `Finished` otomatis menggunakan `Success` tanpa memeriksa aturan bisnis.
- MUST NOT menganggap semua status `Draft` otomatis menggunakan `Gray` tanpa memeriksa aturan bisnis.
- MUST NOT menggunakan `Error` untuk kondisi yang bukan kesalahan hanya karena terlihat mencolok.
- SHOULD menggunakan makna semantik yang konsisten dan meminta validasi untuk mapping yang belum ditentukan.

### 6.3 Status-to-Color Mapping

Untuk setiap proyek, AI SHOULD menyusun mapping sebelum membuat desain.

| Status | Business Meaning | Badge Color | Validation |
|---|---|---|---|
| Draft | Berdasarkan HSD/BRD | Berdasarkan mapping bisnis | Required |
| Proposed | Berdasarkan HSD/BRD | Berdasarkan mapping bisnis | Required |
| Processed | Berdasarkan HSD/BRD | Berdasarkan mapping bisnis | Required |
| Finished | Berdasarkan HSD/BRD | Berdasarkan mapping bisnis | Required |
| Aktif | Berdasarkan HSD/BRD | Berdasarkan mapping bisnis | Required |
| Nonaktif | Berdasarkan HSD/BRD | Berdasarkan mapping bisnis | Required |

AI MUST NOT menganggap tabel ini sebagai penetapan warna final.

---

## 7. Badge Icon Variants

### 7.1 Available Icon Properties

| Icon | Description | Recommended Usage |
|---|---|---|
| `False` | Tanpa ikon | Status atau label sederhana |
| `Dot` | Indikator titik | Status ringkas |
| `X close` | Ikon close | Variant dengan fungsi close sesuai requirement |
| `Icon trailing` | Ikon di belakang teks | Informasi dengan ikon pendamping |
| `Icon leading` | Ikon di depan teks | Informasi dengan ikon pendamping |
| `Text leading` | Elemen teks tambahan di depan | Label dengan informasi pendahulu |
| `Only` | Variant ikon saja | Penggunaan yang didukung GEMS |
| `Country` | Elemen negara | Label negara atau konteks geografis |
| `Avatar` | Elemen avatar | Label berkaitan dengan identitas atau entitas |

### 7.2 Icon Selection Rules

- MUST menggunakan variant Icon resmi GEMS.
- MUST NOT menambahkan ikon dekoratif tanpa tujuan informasi.
- SHOULD menggunakan `Icon=False` untuk status sederhana jika ikon tidak diperlukan.
- SHOULD menggunakan `Dot` jika status memerlukan indikator titik.
- MUST NOT menganggap `X close` selalu berarti Badge dapat dihapus.
- MUST NOT menambahkan behavior klik atau close hanya berdasarkan keberadaan ikon.
- MUST memastikan Badge icon-only memiliki nama aksesibel yang menjelaskan maknanya.

---

## 8. Badge States & Interaction Behavior

### 8.1 Default Behavior

Badge status umumnya bersifat informatif dan tidak mengubah data ketika diklik.

**Expected Behavior:**

- Menampilkan label berdasarkan nilai aktual.
- Menampilkan warna dan Type sesuai mapping.
- Memperbarui informasi ketika nilai data berubah.
- Tidak menjalankan aksi tanpa requirement eksplisit.

### 8.2 Informational Badge

| User Action | Expected Behavior |
|---|---|
| Melihat Badge | Pengguna memahami label dan kondisi |
| Hover | Tidak otomatis memicu aksi |
| Klik | Tidak otomatis mengubah status |
| Data berubah | Label dan warna mengikuti nilai baru |
| Data tidak tersedia | Mengikuti aturan fallback HSD/BRD |

### 8.3 Interactive Badge

Beberapa variant Badge memiliki elemen yang secara visual memungkinkan interaksi, seperti `X close`.

Interaksi tersebut hanya boleh digunakan jika:

1. Variant mendukung pola tersebut.
2. HSD/BRD menetapkan interaksi.
3. Konsekuensi tindakan jelas.
4. Perilaku keyboard dan aksesibilitas ditangani.

**AI Rules:**

- MUST NOT membuat seluruh Badge clickable.
- MUST NOT mengubah status ketika Badge diklik tanpa requirement.
- MUST NOT mengasumsikan semua Badge dengan ikon close dapat dihapus.
- MUST mengikuti behavior yang disetujui untuk Badge interaktif.

---

## 9. Contextual Badge Patterns

### 9.1 Workflow Status

**When to Use:**

Menampilkan tahapan proses bisnis pada tabel, card, atau halaman detail.

**Example Labels:**

- Draft
- Proposed
- Processed
- Finished

**AI Rules:**

- MUST mengikuti status workflow dari HSD/BRD.
- MUST menjaga konsistensi label dan warna.
- MUST NOT mengubah tahapan workflow.
- MUST NOT menggunakan Badge sebagai tombol transisi status.

### 9.2 Approval Status

**When to Use:**

Menampilkan status keputusan atau proses persetujuan apabila modul memiliki approval.

**Example Labels:**

- Menunggu Persetujuan
- Disetujui
- Ditolak

**AI Rules:**

- MUST mengikuti workflow persetujuan aktual.
- MUST NOT menambahkan status approval ke modul yang tidak menggunakannya.
- MUST NOT menganggap Badge sebagai tombol Approve atau Reject.

### 9.3 Data Activation Status

**When to Use:**

Menampilkan apakah data berstatus aktif atau nonaktif.

| Element | Configuration |
|---|---|
| Component | Badge |
| Label | Aktif / Nonaktif |
| Color | Sesuai mapping bisnis menggunakan warna GEMS |
| Behavior | Informational |

**Important:**

Badge menampilkan status, sedangkan Toggle dapat digunakan untuk mengubah status jika diizinkan.

### 9.4 Accommodation Status

**When to Use:**

Menampilkan kondisi kamar, mess, penghuni, atau proses akomodasi.

**Example Labels:**

- Terisi
- Kosong
- Reservasi

**AI Rules:**

- MUST menggunakan status yang tersedia pada HSD/BRD.
- MUST membedakan status kamar dari status pengajuan.
- MUST menjaga konsistensi warna berdasarkan makna status.
- MUST NOT menciptakan status baru berdasarkan asumsi.

### 9.5 Transport Status

**When to Use:**

Menampilkan kondisi penempatan penumpang atau perjalanan.

**Example Labels:**

- Draft
- Siap Ditempatkan
- Sudah Lengkap

**AI Rules:**

- MUST mengikuti status yang ditentukan HSD/BRD.
- MUST membedakan status kelengkapan data, penempatan, dan perjalanan.
- MUST NOT menyederhanakan seluruh status transport menjadi Aktif/Nonaktif.

### 9.6 Category Badge

**When to Use:**

Menampilkan kategori yang bukan merupakan status workflow.

**Example Labels:**

- Staff
- Non-Staff
- Internal
- Eksternal

**AI Rules:**

- MUST membedakan kategori dari status.
- MUST menggunakan warna resmi GEMS berdasarkan mapping yang ditetapkan.
- MUST NOT menggunakan warna Error/Warning untuk kategori biasa tanpa alasan semantik.

### 9.7 Badge in Table

**When to Use:**

Menampilkan status atau kategori pada kolom tabel.

**AI Rules:**

- SHOULD menggunakan ukuran konsisten.
- MUST mempertahankan keterbacaan label.
- MUST menjaga alignment sesuai desain tabel GEMS.
- MUST NOT menggunakan Badge sebagai pengganti action menu.
- SHOULD memastikan label mudah dipahami saat tabel memiliki banyak data.

### 9.8 Badge in Detail Page

**When to Use:**

Menampilkan status utama atau kategori data pada halaman detail.

**AI Rules:**

- SHOULD menempatkan Badge dekat informasi yang dijelaskan.
- MUST mempertahankan konsistensi label dan warna dengan halaman daftar.
- MUST NOT menggunakan label berbeda untuk status yang sama tanpa ketentuan bisnis.

---

## 10. Badge Labels & Content

### 10.1 Label Rules

- MUST menggunakan label sesuai HSD/BRD.
- MUST menggunakan istilah yang konsisten antarhalaman.
- MUST NOT membuat singkatan yang tidak dipahami pengguna.
- SHOULD menggunakan teks singkat dan mudah dipindai.
- SHOULD menghindari label panjang yang mengganggu layout.
- MUST NOT mengubah makna status hanya untuk mempersingkat teks.

### 10.2 Language Consistency

Jika produk menggunakan Bahasa Indonesia:

- SHOULD menggunakan label Bahasa Indonesia.
- MUST mempertahankan istilah khusus jika HSD/BRD menetapkannya.
- MUST NOT mencampur bahasa secara tidak konsisten.

### 10.3 Unknown Status

Jika data status tidak tersedia:

- MUST mengikuti fallback yang ditetapkan HSD/BRD.
- MUST NOT otomatis menggunakan status `Draft`, `Nonaktif`, atau `Error`.
- SHOULD menggunakan label netral jika fallback disetujui.
- MUST NOT menampilkan status palsu.

---

## 11. Accessibility Rules

- MUST memastikan teks Badge dapat dibaca dengan jelas.
- MUST memastikan status tidak hanya dibedakan melalui warna.
- MUST mempertahankan label yang menjelaskan makna status.
- SHOULD menjaga kontras teks dan latar sesuai standar aksesibilitas.
- SHOULD menghindari kombinasi warna yang sulit dibedakan.
- MUST memberikan accessible name untuk variant icon-only.
- MUST menyediakan interaksi keyboard yang sesuai jika Badge memiliki fungsi interaktif.
- MUST NOT menggunakan Badge informatif sebagai elemen fokus keyboard tanpa kebutuhan interaksi.

---

## 12. AI Badge Selection Workflow

1. **Read HSD/BRD:** Identifikasi status, kategori, atau informasi yang perlu ditampilkan.
2. **Determine Purpose:** Tentukan apakah Badge digunakan untuk workflow, kondisi, kategori, atau metadata.
3. **Validate Component:** Pastikan Badge lebih tepat dibanding Button, Toggle, Alert, atau komponen lainnya.
4. **Select Official Type:** Pilih `Pill color`, `Pill outline`, `Badge color`, atau `Badge modern`.
5. **Select Size:** Gunakan `sm`, `md`, atau `lg`.
6. **Select Icon:** Gunakan variant GEMS yang tersedia dan relevan.
7. **Determine Color:** Gunakan warna GEMS berdasarkan mapping semantik yang disetujui.
8. **Set Label:** Gunakan istilah resmi HSD/BRD.
9. **Define Behavior:** Tentukan apakah Badge informatif atau memiliki interaksi yang disetujui.
10. **Verify Consistency:** Periksa penggunaan Badge pada tabel, card, dan halaman detail.
11. **Verify Figma:** Pastikan kombinasi property sesuai komponen resmi GEMS.
12. **Human Approval:** Minta persetujuan untuk mapping, variant, atau behavior baru yang belum ditentukan.

---

## 13. AI Restrictions

AI MUST NOT:

1. Membuat Type Badge baru tanpa persetujuan.
2. Membuat Size di luar `sm`, `md`, atau `lg`.
3. Membuat warna custom di luar GEMS tanpa persetujuan.
4. Menggunakan kombinasi property yang tidak tersedia pada GEMS.
5. Menggunakan warna berdasarkan estetika semata.
6. Menentukan status baru tanpa HSD/BRD.
7. Mengubah label status bisnis tanpa persetujuan.
8. Menganggap semua status selesai otomatis berwarna Success.
9. Menganggap semua status Draft otomatis berwarna Gray.
10. Menggunakan Error untuk kategori biasa tanpa alasan semantik.
11. Menganggap seluruh Badge clickable.
12. Menganggap ikon `X close` otomatis dapat menghapus data.
13. Menggunakan Badge untuk aksi Simpan, Hapus, atau Kirim.
14. Menggunakan Badge sebagai pengganti Toggle untuk perubahan status aktif/nonaktif.
15. Menggunakan Badge sebagai pengganti Alert untuk pesan kesalahan lengkap.
16. Mengubah workflow atau hak akses berdasarkan tampilan Badge.
17. Menyampaikan status hanya melalui warna tanpa label yang jelas.
18. Membuat behavior baru tanpa Human Approval.
19. Mengabaikan mapping status dan warna yang sudah disetujui.

---

## 14. Implementation Requirements

### 14.1 Source of Truth

| Source | Responsibility |
|---|---|
| HSD / BRD | Definisi status, kategori, workflow, dan hak akses |
| GEMS Design System | Type, Size, Icon, Color, dan visual komponen |
| Human Approval | Persetujuan perubahan yang belum tercakup |

### 14.2 Final AI Instruction

When generating UI/UX designs, AI MUST:

1. Read the HSD/BRD to identify the correct status or category.
2. Use the official GEMS Badge component.
3. Select supported Type, Size, Icon, and Color variants.
4. Apply approved semantic status-to-color mapping.
5. Use accurate labels from business requirements.
6. Preserve consistency across tables, cards, and detail pages.
7. Treat informational Badges as non-interactive by default.
8. Avoid inventing new statuses, business rules, or interaction behaviors.
9. Request Human Approval before introducing new variants or semantic mappings.

---

## 15. Official Figma Reference

| Component | Purpose | Figma Design |
|---|---|---|
| GEMS Badge | Komponen dan variants Badge resmi | [Open GEMS Badge Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=345-6118&t=oti8QS9H602K2cYU-1) |
