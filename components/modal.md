# GEMS Design System — Modal Guidelines

## 1. Purpose

Modal merupakan komponen dialog yang digunakan untuk meminta konfirmasi, memberikan peringatan, atau memfasilitasi keputusan pengguna sebelum suatu tindakan dijalankan.

Modal digunakan ketika pengguna perlu memahami tindakan dan konsekuensinya tanpa meninggalkan konteks halaman yang sedang digunakan.

**Core Principle:**

> AI MUST menggunakan komponen Modal resmi GEMS Design System beserta seluruh komponen pendukung yang tersedia. AI hanya boleh memilih variant dan mengubah konten atau component properties yang didukung, bukan membuat desain Modal baru.

### 1.1 Mandatory Design System Compliance

AI MUST:

1. Menggunakan komponen Modal resmi GEMS Design System.
2. Menggunakan instance dari component library apabila tersedia.
3. Mempertahankan struktur dan visual properties resmi.
4. Menggunakan Button, Input, Textarea, Icon, dan komponen pendukung resmi GEMS.
5. Memilih pattern sesuai tujuan dan konsekuensi tindakan.
6. Mengikuti HSD/BRD untuk menentukan kebutuhan dan alur interaksi.
7. Menggunakan component properties resmi untuk perubahan yang didukung.
8. Memastikan setiap Modal mengikuti hierarchy dan UX pattern GEMS.

AI MUST NOT:

1. Membuat Modal custom apabila komponen resmi tersedia.
2. Menggunakan komponen dari library lain.
3. Membuat ikon, warna, variant, atau visual state baru.
4. Mengubah struktur internal komponen secara manual.
5. Mengganti instance resmi dengan Frame custom.
6. Mengubah ukuran, spacing, radius, shadow, atau typography di luar GEMS.
7. Membuat pola interaksi baru tanpa Human Approval.

---

## 2. Modal Types & Usage Hierarchy

### 2.1 Available Patterns

Berdasarkan contoh visual GEMS yang diberikan, Confirmation Modal memiliki beberapa pola penggunaan.

| Pattern | Visual Meaning | Primary Action |
|---|---|---|
| Positive Confirmation | Hijau | Simpan, Setujui |
| Warning Confirmation | Oranye | Keluar, Batalkan, Minta Revisi |
| Destructive Confirmation | Merah | Hapus, Tolak |
| Confirmation with Input | Mengikuti konteks tindakan | Setujui, Tolak, Minta Revisi |

Pattern di atas merupakan klasifikasi penggunaan berdasarkan contoh visual. Nama variant teknis tetap mengikuti component set Figma resmi.

### 2.2 Modal Usage Matrix

| Pattern | When to Use | When Not to Use |
|---|---|---|
| Positive | Tindakan menyimpan, menyetujui, atau melanjutkan proses positif | Penghapusan, penolakan, atau tindakan berisiko |
| Warning | Tindakan yang perlu dipertimbangkan karena konsekuensi atau perubahan proses | Tindakan positif tanpa risiko khusus |
| Destructive | Penghapusan data atau penolakan | Menyimpan atau menyetujui data |
| With Input | Keputusan membutuhkan catatan atau alasan | Keputusan tanpa kebutuhan input tambahan |

### 2.3 General Selection Rules

- MUST menentukan pattern berdasarkan makna tindakan.
- MUST menggunakan warna dan ikon yang sesuai dengan pattern GEMS.
- MUST mempertahankan struktur Confirmation Modal resmi.
- MUST menggunakan Button hierarchy sesuai GEMS.
- MUST NOT menentukan warna hanya berdasarkan preferensi visual.
- MUST NOT membuat variant baru untuk setiap jenis tindakan.
- MUST NOT menambahkan Modal apabila tidak dibutuhkan dalam user flow.

---

## 3. Positive Confirmation Modal

### 3.1 Definition

Positive Confirmation Modal digunakan untuk mengonfirmasi tindakan yang memiliki tujuan positif, seperti menyimpan data atau menyetujui permintaan.

### 3.2 When to Use

- Menyimpan data.
- Menyimpan perubahan.
- Menyetujui permintaan.
- Mengonfirmasi tindakan positif.
- Melanjutkan proses yang membutuhkan konfirmasi.

### 3.3 Visual Pattern

Berdasarkan contoh visual:

- Status color: Green.
- Status icon: Question mark dalam lingkaran hijau.
- Primary Button: Green Solid.
- Secondary Button: Neutral Outline.
- Modal Container: Mengikuti komponen resmi GEMS.
- Decorative Elements: Mengikuti struktur resmi.

### 3.4 Examples

| Context | Modal Title | Secondary Action | Primary Action |
|---|---|---|---|
| Save Data | Simpan Data? | Batal | Ya, Simpan |
| Approval | Konfirmasi Persetujuan | Batal | Ya, Setujui |
| Approval with Note | Konfirmasi Persetujuan | Batal | Ya, Setujui |

### 3.5 Rules

AI MUST:

1. Menggunakan Modal resmi GEMS.
2. Menggunakan visual Positive Confirmation yang tersedia.
3. Menggunakan ikon positif resmi.
4. Menggunakan Green Solid Button resmi untuk aksi utama sesuai pattern.
5. Menggunakan Button netral untuk pembatalan.
6. Menyesuaikan judul dan deskripsi dengan tindakan.
7. Menjalankan tindakan hanya setelah konfirmasi.

AI MUST NOT:

1. Membuat warna hijau custom.
2. Menggunakan visual destructive.
3. Mengganti ikon dengan ikon custom.
4. Mengubah posisi Button.
5. Membuat Modal baru untuk approval apabila pattern yang tersedia dapat digunakan.

---

## 4. Warning Confirmation Modal

### 4.1 Definition

Warning Confirmation Modal digunakan untuk mengonfirmasi tindakan yang membutuhkan perhatian karena berpotensi menyebabkan perubahan, pembatalan, atau hilangnya data yang belum disimpan.

### 4.2 When to Use

- Keluar dari form dengan perubahan belum disimpan.
- Membatalkan proses.
- Meminta revisi.
- Mengonfirmasi tindakan yang memiliki konsekuensi.
- Menghentikan atau mengubah proses tertentu apabila pattern GEMS sesuai.

### 4.3 Visual Pattern

Berdasarkan contoh visual:

- Status color: Orange.
- Status icon: Question mark atau ikon kontekstual resmi berwarna oranye.
- Primary Button: Orange Solid.
- Secondary Button: Neutral Outline.
- Modal Container: Mengikuti komponen resmi GEMS.
- Decorative Elements: Mengikuti struktur resmi.

### 4.4 Examples

| Context | Modal Title | Secondary Action | Primary Action |
|---|---|---|---|
| Exit Form | Keluar Dari Penambahan Data? | Kembali | Ya, Batalkan |
| Revision | Konfirmasi Revisi | Batal | Ya, Minta Revisi |
| Revision with Reason | Konfirmasi Permintaan Revisi | Batal | Ya, Minta Revisi |

### 4.5 Rules

AI MUST:

1. Menggunakan Warning Confirmation Modal resmi.
2. Menggunakan warna dan ikon oranye sesuai GEMS.
3. Menjelaskan konsekuensi tindakan.
4. Menggunakan Orange Solid Button resmi apabila sesuai pattern.
5. Memberikan pilihan kembali atau membatalkan tindakan.
6. Mempertahankan data apabila pengguna memilih kembali.
7. Menggunakan konten sesuai HSD/BRD.

AI MUST NOT:

1. Menggunakan Green Solid untuk tindakan warning.
2. Menggunakan Red Solid secara otomatis untuk semua pembatalan.
3. Menghapus data sebelum konfirmasi.
4. Membuat warning icon custom.
5. Mengubah struktur Modal resmi.

---

## 5. Destructive Confirmation Modal

### 5.1 Definition

Destructive Confirmation Modal digunakan untuk mengonfirmasi tindakan negatif yang memiliki dampak signifikan, seperti menghapus data atau menolak permintaan.

### 5.2 When to Use

- Menghapus data.
- Menghapus data secara permanen.
- Menolak permintaan.
- Menolak laporan.
- Menjalankan tindakan negatif yang membutuhkan konfirmasi.

### 5.3 Visual Pattern

Berdasarkan contoh visual:

- Status color: Red.
- Status icon: Trash, Question mark, atau X sesuai pattern yang digunakan.
- Primary Button: Red Solid.
- Secondary Button: Neutral Outline.
- Modal Container: Mengikuti komponen resmi GEMS.
- Decorative Elements: Mengikuti struktur resmi.

### 5.4 Examples

| Context | Modal Title | Secondary Action | Primary Action |
|---|---|---|---|
| Delete Data | Konfirmasi Hapus | Batal | Ya, Hapus |
| Reject Request | Konfirmasi Penolakan | Batal | Ya, Tolak |
| Reject Report | Konfirmasi Penolakan Laporan | Batal | Tolak |

### 5.5 Rules

AI MUST:

1. Menggunakan Modal resmi GEMS.
2. Menggunakan visual Destructive Confirmation yang tersedia.
3. Menggunakan ikon merah sesuai konteks dan pattern resmi.
4. Menggunakan Red Solid Button resmi apabila sesuai pattern.
5. Menjelaskan konsekuensi penghapusan atau penolakan.
6. Menyediakan tindakan pembatalan.
7. Menjalankan tindakan hanya setelah konfirmasi.

AI MUST NOT:

1. Menggunakan warna hijau untuk tindakan destructive.
2. Membuat ikon merah custom.
3. Menghapus data sebelum konfirmasi.
4. Menggunakan destructive pattern untuk tindakan positif.
5. Mengubah struktur atau visual komponen resmi.

---

## 6. Confirmation Modal with Input

### 6.1 Definition

Confirmation Modal with Input merupakan Confirmation Modal yang memiliki field tambahan untuk mengumpulkan informasi sebelum pengguna mengonfirmasi tindakan.

Pattern ini tetap menggunakan struktur Confirmation Modal resmi GEMS.

### 6.2 When to Use

- Persetujuan dengan catatan.
- Penolakan dengan alasan.
- Permintaan revisi dengan alasan.
- Tindakan lain yang membutuhkan informasi tambahan sesuai HSD/BRD.

### 6.3 Input Usage Matrix

| Context | Input | Required | Primary Action |
|---|---|---|---|
| Approval with Note | Catatan Persetujuan | Mengikuti HSD/BRD | Ya, Setujui |
| Rejection with Reason | Alasan Penolakan | Ya, sesuai contoh | Tolak |
| Revision with Reason | Alasan Revisi | Ya, sesuai contoh | Ya, Minta Revisi |

### 6.4 Component Structure

AI MUST mempertahankan urutan konten yang ditunjukkan pada contoh GEMS:

1. Status Icon.
2. Close Button.
3. Modal Title.
4. Modal Description.
5. Input Label.
6. Input atau Textarea.
7. Footer Actions.

### 6.5 Input Rules

AI MUST:

1. Menggunakan Input atau Textarea resmi GEMS.
2. Menggunakan label yang jelas.
3. Menampilkan required indicator apabila field wajib.
4. Menggunakan validation pattern resmi.
5. Mempertahankan nilai input saat validasi gagal.
6. Menempatkan field di antara deskripsi dan Footer.
7. Mengikuti spacing dan layout resmi GEMS.
8. Menggunakan warna aksi utama sesuai konteks.

AI MUST NOT:

1. Membuat Input atau Textarea custom.
2. Mengubah struktur Modal.
3. Menghilangkan field wajib.
4. Mengirim data ketika validasi gagal.
5. Menggunakan warna aksi yang tidak sesuai.
6. Membuat Form Modal baru jika Confirmation Modal resmi dapat memenuhi kebutuhan.

---

## 7. Modal Structure & Component Anatomy

### 7.1 Component Anatomy

Berdasarkan contoh visual GEMS:

| Element | Function | Usage |
|---|---|---|
| Overlay / Backdrop | Memisahkan Modal dari halaman utama | Mengikuti GEMS |
| Modal Container | Membungkus konten dialog | Required |
| Status Icon | Menunjukkan makna tindakan | Required pada pattern yang ditampilkan |
| Decorative Circles | Elemen visual di sekitar ikon | Mengikuti komponen resmi |
| Close Button | Menutup Modal | Ditampilkan pada contoh |
| Title | Menjelaskan tujuan tindakan | Required |
| Description | Menjelaskan tindakan atau konsekuensi | Required pada contoh |
| Input Area | Mengumpulkan informasi tambahan | Optional |
| Footer | Menampung tindakan | Required |
| Secondary Button | Membatalkan atau kembali | Required pada contoh |
| Primary Button | Mengonfirmasi tindakan | Required pada contoh |

### 7.2 Modal Container

- MUST menggunakan container resmi GEMS.
- MUST mengikuti ukuran dan radius resmi.
- MUST mengikuti shadow dan background resmi.
- MUST mempertahankan layout internal.
- MUST NOT membuat container custom.
- MUST NOT mengubah ukuran secara manual di luar properties yang tersedia.

### 7.3 Status Icon

- MUST menggunakan ikon resmi GEMS.
- MUST menggunakan warna sesuai makna tindakan.
- MUST mempertahankan dekorasi lingkaran yang tersedia.
- MUST NOT membuat ikon baru.
- MUST NOT mengubah ukuran atau posisi ikon secara sembarangan.

### 7.4 Close Button

- MUST menggunakan Close Button resmi.
- MUST mengikuti posisi kanan atas seperti contoh.
- MUST mengikuti aturan penutupan sesuai konteks.
- MUST NOT menghilangkan Close Button tanpa dasar pattern resmi.

### 7.5 Title & Description

- MUST menggunakan typography resmi.
- MUST mempertahankan alignment sesuai komponen.
- MUST menggunakan teks sesuai tindakan.
- SHOULD menjaga judul singkat.
- MUST menjelaskan konsekuensi ketika diperlukan.
- MUST NOT menyalin teks contoh yang tidak sesuai konteks.

### 7.6 Footer Actions

- MUST menggunakan Button resmi GEMS.
- MUST mengikuti layout dua tombol pada pattern yang ditampilkan.
- MUST menempatkan tindakan pendukung di kiri.
- MUST menempatkan tindakan utama di kanan.
- MUST menggunakan warna aksi utama sesuai pattern.
- MUST NOT membuat Button custom.
- MUST NOT mengubah urutan tindakan tanpa pattern yang disetujui.

---

## 8. Modal States

Modal memiliki beberapa kondisi fungsional yang perlu ditangani oleh AI.

| State | Trigger | Expected Behavior |
|---|---|---|
| Closed | Modal belum dibuka | Modal tidak terlihat |
| Open / Default | Pengguna membuka Modal | Modal dan overlay ditampilkan |
| Focused | Pengguna menggunakan keyboard | Fokus terlihat pada elemen aktif |
| Processing | Pengguna mengonfirmasi tindakan | Sistem memproses permintaan |
| Validation Error | Input tidak valid | Menampilkan pesan validasi |
| Request Error | Permintaan gagal | Menampilkan feedback kegagalan |
| Completed | Permintaan berhasil | Menjalankan success flow |

State tersebut merupakan kebutuhan perilaku. Visual state spesifik MUST mengikuti komponen resmi GEMS yang tersedia.

### 8.1 Closed State

- MUST menyembunyikan Modal.
- MUST mengembalikan interaksi halaman sesuai kondisi normal.
- MUST NOT meninggalkan overlay aktif setelah Modal ditutup.

### 8.2 Open / Default State

- MUST menampilkan Modal resmi.
- MUST menggunakan overlay GEMS.
- MUST memusatkan perhatian pengguna pada dialog.
- MUST mengikuti struktur konten resmi.
- MUST NOT mengubah data sebelum pengguna menjalankan tindakan.

### 8.3 Focused State

- MUST mendukung navigasi keyboard.
- MUST menggunakan focus indicator resmi GEMS.
- SHOULD memindahkan fokus ke dialog ketika dibuka.
- SHOULD menjaga fokus tetap berada dalam dialog selama aktif.
- SHOULD mengembalikan fokus ke elemen pemicu setelah ditutup.
- MUST NOT menghilangkan focus indicator.

### 8.4 Processing State

- MUST mencegah submit berulang.
- MUST menggunakan loading state resmi GEMS apabila tersedia.
- MUST mempertahankan konteks tindakan.
- MUST NOT menganggap proses berhasil sebelum menerima hasil sukses.
- MUST NOT membuat loading visual baru tanpa persetujuan.

### 8.5 Validation Error State

- MUST memvalidasi seluruh field wajib.
- MUST menampilkan pesan kesalahan sesuai GEMS.
- MUST mempertahankan data input yang valid.
- MUST NOT menjalankan submit ketika validasi gagal.
- MUST NOT menutup Modal otomatis.

### 8.6 Request Error State

- MUST memberikan feedback bahwa tindakan gagal.
- SHOULD menyediakan mekanisme mencoba kembali jika relevan.
- MUST mempertahankan data yang diperlukan untuk retry.
- MUST NOT menampilkan pesan sukses ketika permintaan gagal.

### 8.7 Completed State

- MUST mengikuti success flow HSD/BRD.
- MAY menutup Modal dan menampilkan Toast sesuai pattern GEMS.
- MUST memperbarui tampilan data berdasarkan hasil proses.
- MUST NOT menambahkan Success Modal baru tanpa kebutuhan.

---

## 9. Contextual Modal Patterns

### 9.1 Save Data

**Pattern:** Positive Confirmation

| Element | Configuration |
|---|---|
| Title | Simpan Data? |
| Description | Data yang telah diisi akan disimpan dan ditambahkan ke sistem. |
| Status Color | Green |
| Secondary Button | Batal |
| Primary Button | Ya, Simpan |
| Primary Button Visual | Green Solid |

**Rules:**

- MUST menggunakan Positive Confirmation resmi.
- MUST menggunakan Green Solid Button resmi.
- MUST menjalankan penyimpanan setelah konfirmasi.
- MUST NOT menggunakan destructive visual.

### 9.2 Exit Form

**Pattern:** Warning Confirmation

| Element | Configuration |
|---|---|
| Title | Keluar Dari Penambahan Data? |
| Description | Data yang belum disimpan akan hilang jika Anda keluar dari halaman ini. |
| Status Color | Orange |
| Secondary Button | Kembali |
| Primary Button | Ya, Batalkan |
| Primary Button Visual | Orange Solid |

**Rules:**

- MUST menggunakan Warning Confirmation resmi.
- MUST menjelaskan konsekuensi data belum disimpan.
- MUST mempertahankan data jika pengguna memilih Kembali.
- MUST NOT membuang perubahan sebelum pengguna mengonfirmasi.

### 9.3 Delete Data

**Pattern:** Destructive Confirmation

| Element | Configuration |
|---|---|
| Title | Konfirmasi Hapus |
| Description | Data yang dihapus akan terhapus secara permanen dan tidak dapat dipulihkan. |
| Status Color | Red |
| Status Icon | Trash |
| Secondary Button | Batal |
| Primary Button | Ya, Hapus |
| Primary Button Visual | Red Solid |

**Rules:**

- MUST menggunakan Destructive Confirmation resmi.
- MUST menggunakan ikon Trash resmi sesuai pattern.
- MUST menjelaskan konsekuensi permanen hanya jika penghapusan memang tidak dapat dipulihkan.
- MUST NOT menjalankan penghapusan sebelum konfirmasi.

### 9.4 Approval

**Pattern:** Positive Confirmation

| Element | Configuration |
|---|---|
| Title | Konfirmasi Persetujuan |
| Description | Apakah Anda yakin ingin menyetujui permintaan ini? |
| Status Color | Green |
| Secondary Button | Batal |
| Primary Button | Ya, Setujui |
| Primary Button Visual | Green Solid |

**Rules:**

- MUST menggunakan Positive Confirmation resmi.
- MUST menggunakan visual positif.
- MUST menjalankan approval setelah konfirmasi.
- MUST NOT menggunakan destructive visual.

### 9.5 Approval with Note

**Pattern:** Positive Confirmation with Input

| Element | Configuration |
|---|---|
| Title | Konfirmasi Persetujuan |
| Description | Apakah Anda yakin ingin menyetujui permintaan ini? |
| Status Color | Green |
| Input Label | Catatan Persetujuan |
| Input | Input resmi GEMS |
| Secondary Button | Batal |
| Primary Button | Ya, Setujui |

**Rules:**

- MUST menggunakan komponen input resmi.
- MUST mengikuti required state berdasarkan HSD/BRD.
- MUST mempertahankan struktur Modal.
- MUST NOT membuat Form Modal custom.

### 9.6 Rejection

**Pattern:** Destructive Confirmation

| Element | Configuration |
|---|---|
| Title | Konfirmasi Penolakan |
| Description | Apakah Anda yakin ingin menolak permintaan ini? |
| Status Color | Red |
| Secondary Button | Batal |
| Primary Button | Ya, Tolak |
| Primary Button Visual | Red Solid |

**Rules:**

- MUST menggunakan Destructive Confirmation resmi.
- MUST menggunakan visual merah sesuai pattern.
- MUST menjalankan penolakan setelah konfirmasi.
- MUST NOT menggunakan Green Solid.

### 9.7 Rejection with Reason

**Pattern:** Destructive Confirmation with Input

| Element | Configuration |
|---|---|
| Title | Konfirmasi Penolakan Laporan |
| Description | Apakah Anda yakin ingin menolak laporan pengelolaan? |
| Status Color | Red |
| Input Label | Alasan Penolakan |
| Required | Yes |
| Input | Textarea resmi GEMS |
| Secondary Button | Batal |
| Primary Button | Tolak |

**Rules:**

- MUST menggunakan Textarea resmi GEMS.
- MUST menampilkan required indicator.
- MUST memvalidasi alasan sebelum submit.
- MUST mempertahankan input ketika validasi gagal.
- MUST NOT mengirim penolakan tanpa alasan jika diwajibkan.

### 9.8 Revision Request

**Pattern:** Warning Confirmation

| Element | Configuration |
|---|---|
| Title | Konfirmasi Revisi |
| Description | Apakah Anda yakin ingin meminta revisi pada data ini? |
| Status Color | Orange |
| Secondary Button | Batal |
| Primary Button | Ya, Minta Revisi |
| Primary Button Visual | Orange Solid |

**Rules:**

- MUST menggunakan Warning Confirmation resmi.
- MUST menggunakan visual oranye.
- MUST menjaga kesesuaian teks dengan tindakan revisi.
- MUST NOT menggunakan deskripsi penolakan untuk tindakan revisi.

### 9.9 Revision Request with Reason

**Pattern:** Warning Confirmation with Input

| Element | Configuration |
|---|---|
| Title | Konfirmasi Permintaan Revisi |
| Description | Apakah Anda yakin ingin meminta revisi pada data ini? |
| Status Color | Orange |
| Input Label | Alasan Revisi |
| Required | Yes |
| Input | Textarea resmi GEMS |
| Secondary Button | Batal |
| Primary Button | Ya, Minta Revisi |

**Rules:**

- MUST menggunakan Textarea resmi.
- MUST menampilkan required indicator.
- MUST memvalidasi alasan revisi.
- MUST menggunakan visual oranye.
- MUST NOT membuat Modal baru untuk kebutuhan alasan revisi.

---

## 10. Modal Labels & UX Writing

### 10.1 General Rules

- MUST menggunakan label yang jelas dan berorientasi tindakan.
- MUST menggunakan terminologi sesuai HSD/BRD.
- MUST menjaga konsistensi Title, Description, dan Button.
- SHOULD menggunakan kalimat singkat.
- MUST menjelaskan konsekuensi tindakan apabila relevan.
- MUST NOT menggunakan label ambigu.
- MUST NOT menyalin wording dari pattern berbeda tanpa penyesuaian.

### 10.2 Label Examples

| Action | Modal Title | Primary Button |
|---|---|---|
| Save | Simpan Data? | Ya, Simpan |
| Approval | Konfirmasi Persetujuan | Ya, Setujui |
| Delete | Konfirmasi Hapus | Ya, Hapus |
| Reject | Konfirmasi Penolakan | Ya, Tolak |
| Request Revision | Konfirmasi Revisi | Ya, Minta Revisi |
| Exit Form | Keluar Dari Penambahan Data? | Ya, Batalkan |

### 10.3 Content Consistency Rules

AI MUST memastikan:

1. Title sesuai tindakan.
2. Description menjelaskan tindakan yang sama.
3. Primary Button menjalankan tindakan yang dijelaskan.
4. Secondary Button memiliki makna yang jelas.
5. Warna dan ikon sesuai makna tindakan.
6. Required Input sesuai kebutuhan bisnis.

---

## 11. Modal Selection Rules for AI

AI MUST mengikuti urutan berikut:

### Step 1 — Identify Action

Identifikasi tindakan berdasarkan HSD/BRD.

### Step 2 — Determine Modal Necessity

Tentukan apakah tindakan membutuhkan konfirmasi.

AI MUST NOT menambahkan Modal secara otomatis untuk seluruh aksi.

### Step 3 — Determine Action Meaning

Klasifikasikan tindakan:

- Positive.
- Warning.
- Destructive.

### Step 4 — Determine Input Requirement

Periksa apakah tindakan membutuhkan:

- Catatan.
- Alasan.
- Input tambahan.

Jika tidak diperlukan, AI MUST NOT menambahkan field baru.

### Step 5 — Retrieve Official Modal

AI MUST mengakses komponen Modal resmi GEMS Design System.

### Step 6 — Select Supported Variant

AI MUST memeriksa variant dan component properties.

AI MUST NOT menganggap klasifikasi fungsional sebagai nama variant Figma.

### Step 7 — Configure Visual Pattern

Gunakan:

- Status Icon resmi.
- Status Color resmi.
- Modal Container resmi.
- Typography resmi.
- Footer resmi.
- Button resmi.

### Step 8 — Configure Content

Sesuaikan:

- Title.
- Description.
- Input Label.
- Input Content.
- Button Labels.

### Step 9 — Apply Interaction States

Pastikan:

- Open.
- Close.
- Focused.
- Processing.
- Validation Error.
- Request Error.
- Completed.

### Step 10 — Validate Against GEMS

AI MUST memastikan:

1. Modal merupakan instance resmi.
2. Variant tersedia dalam GEMS.
3. Status Icon sesuai.
4. Status Color sesuai.
5. Container sesuai.
6. Typography sesuai.
7. Button hierarchy benar.
8. Input menggunakan komponen resmi.
9. Struktur tidak diubah.
10. Interaksi sesuai HSD/BRD.

### Step 11 — Request Human Approval

Jika pattern, variant, atau component properties tidak tersedia, AI MUST meminta Human Approval sebelum membuat solusi baru.

---

## 12. AI Restrictions

AI MUST NOT:

1. Membuat Modal custom ketika komponen resmi tersedia.
2. Menggunakan Modal dari library lain.
3. Mengganti instance Modal dengan Frame custom.
4. Mengubah struktur internal Modal.
5. Mengubah ukuran di luar variant resmi.
6. Mengubah spacing, radius, shadow, atau typography di luar GEMS.
7. Membuat warna atau ikon custom.
8. Membuat variant baru tanpa Human Approval.
9. Mengubah posisi Status Icon.
10. Menghilangkan decorative elements resmi.
11. Mengubah posisi Close Button tanpa acuan.
12. Mengubah susunan Footer tanpa acuan.
13. Menggunakan Button custom.
14. Menggunakan Input atau Textarea custom.
15. Menggunakan Green Solid untuk tindakan destructive.
16. Menggunakan Red Solid untuk tindakan positive.
17. Menggunakan Orange Solid untuk tindakan positive tanpa dasar pattern.
18. Menambahkan Modal pada seluruh tindakan.
19. Membuat Confirmation Modal baru untuk setiap konteks bisnis.
20. Menambahkan input tanpa kebutuhan HSD/BRD.
21. Menghilangkan required field.
22. Menjalankan submit ketika validasi gagal.
23. Menjalankan aksi sebelum konfirmasi jika diwajibkan.
24. Menutup Modal secara otomatis ketika validasi gagal.
25. Mengabaikan keyboard focus dan aksesibilitas.
26. Mengubah alur bisnis berdasarkan preferensi visual.
27. Menganggap contoh visual sebagai izin membuat variant baru.
28. Mengklaim desain sesuai GEMS tanpa memeriksa komponen resmi.

---

## 13. Official GEMS Design System Component

### 13.1 Component Reference

**Component Name:** Modal  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-26550

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `240:26550`

### 13.2 Official Component Usage Rules

AI MUST:

1. Mengakses komponen Modal resmi GEMS.
2. Menggunakan instance resmi apabila tersedia.
3. Memeriksa component set, variant, dan properties.
4. Memilih visual pattern sesuai konteks tindakan.
5. Mempertahankan struktur dan visual properties resmi.
6. Menggunakan seluruh komponen pendukung resmi GEMS.
7. Mempertahankan koneksi library apabila didukung.
8. Memvalidasi hasil implementasi terhadap komponen resmi.

AI MUST NOT:

1. Membuat Modal custom.
2. Menggunakan komponen dari library lain.
3. Membuat variant atau visual state baru tanpa persetujuan.
4. Mengganti instance resmi dengan Frame custom.
5. Mengubah ukuran, warna, radius, spacing, atau typography di luar GEMS.
6. Membuat interaksi baru yang bertentangan dengan HSD/BRD.

### 13.3 Component Verification

Sebelum implementasi, AI MUST memverifikasi:

- Component Name.
- Component Set.
- Available Variants.
- Component Properties.
- Supported Sizes.
- Status Icon.
- Status Color.
- Header Structure.
- Body Structure.
- Footer Structure.
- Button Configuration.
- Input Configuration.
- Interaction States.

Jika suatu properti tidak dapat diverifikasi, AI MUST NOT mengarang nilainya.

### 13.4 Final AI Instruction

**AI MUST retrieve and reuse the official GEMS Modal component from the specified Figma source whenever the integration supports it.**

AI MUST use official GEMS components for all supported elements inside the Modal, including Buttons, Inputs, Textareas, Icons, and other reusable components.

AI MUST preserve the official structure, use supported variants and properties, and configure content according to approved HSD/BRD requirements.

AI MUST NOT recreate the Modal visually from scratch, invent unsupported variants, or introduce custom design properties without Human Approval.

**GEMS Design System is the single source of truth for all Modal visual specifications.**
