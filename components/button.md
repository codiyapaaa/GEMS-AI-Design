# GEMS Design System — Button Guidelines

## 1. Purpose

Button merupakan komponen interaktif yang digunakan untuk menjalankan tindakan pengguna, seperti membuat, menyimpan, mengubah, menghapus, mengirim, membatalkan, mengonfirmasi, dan menghentikan proses.

Pemilihan Button MUST mempertimbangkan:

- Prioritas tindakan.
- Konteks halaman atau komponen.
- Dampak tindakan terhadap data atau proses.
- Hubungan dengan tombol lain dalam satu kelompok aksi.
- Variant dan state resmi GEMS Design System.

**Core Principle:**

> Button hierarchy ditentukan berdasarkan konteks dan prioritas tindakan, bukan hanya berdasarkan label tombol.

AI MUST menggunakan komponen Button resmi GEMS dan MUST NOT membuat variant, warna, atau visual state baru tanpa Human Approval.

---

## 2. Button Variants & Hierarchy

### 2.1 Available Variants

| Variant | Visual Hierarchy | Purpose |
|---|---|---|
| Primary | Highest | Aksi utama dengan penekanan tertinggi |
| Secondary Color | Medium | Aksi kontekstual dengan penekanan warna |
| Secondary Gray | Medium | Aksi pendukung atau utilitas netral |
| Tertiary Color | Low | Aksi tambahan berwarna; implementasi spesifik belum ditetapkan |
| Tertiary Gray | Low | Aksi tambahan netral |
| Link Color | Text-based | Aksi berbasis teks berwarna; aturan detail belum ditetapkan |
| Link Gray | Text-based | Aksi berbasis teks netral; aturan detail belum ditetapkan |

**Scope V1.0:** Aturan implementasi yang disepakati meliputi Primary, Secondary Color, Secondary Gray, dan Tertiary Gray. Tertiary Color hanya dijelaskan pada tingkat prinsip; Link Color dan Link Gray tidak diberikan aturan penggunaan spesifik dalam versi ini. AI MUST NOT mengarang aturan untuk variant yang belum diatur.

### 2.2 Button Usage Matrix

| Variant | When to Use | When Not to Use | Example |
|---|---|---|---|
| Primary | Aksi utama dalam kelompok tindakan | Aksi pendukung dengan prioritas rendah | Simpan, Buat Pesanan, Konfirmasi |
| Secondary Color | Aksi kontekstual yang membutuhkan penekanan warna tanpa solid fill | Aksi netral yang cukup menggunakan Secondary Gray | Ubah Pesanan, Hapus, Stop Charging |
| Secondary Gray | Aksi pendukung, pembatalan, navigasi, atau utilitas | Aksi utama yang membutuhkan penekanan tertinggi | Batal, Kembali, Edit, Ekspor Data |
| Tertiary Color | Aksi tambahan berwarna dengan penekanan rendah; penerapan spesifik memerlukan arahan | Aksi utama atau konfirmasi penting | Belum ditetapkan |
| Tertiary Gray | Aksi tambahan netral dengan penekanan rendah | Aksi utama atau tindakan yang perlu ditonjolkan | Aksi tambahan netral sesuai konteks |

**Rules:**

- MUST menentukan hierarchy berdasarkan konteks.
- MUST menggunakan variant resmi GEMS.
- MUST menjaga konsistensi hierarchy dalam satu kelompok tindakan.
- SHOULD menggunakan satu aksi utama yang paling menonjol dalam satu kelompok, kecuali terdapat pattern khusus yang disetujui.
- MUST NOT menggunakan Primary untuk semua tombol pada halaman.
- MUST NOT menentukan variant hanya berdasarkan kata kerja seperti Edit atau Hapus.

---

## 3. Primary Button

### 3.1 Definition

Primary Button digunakan untuk tindakan dengan prioritas tertinggi dalam satu kelompok aksi.

### 3.2 When to Use

- Menyimpan data atau perubahan.
- Membuat data baru.
- Mengirim pengajuan atau laporan.
- Mengonfirmasi tindakan utama.
- Menjalankan aksi utama pada halaman.

### 3.3 Examples

| Context | Button Label | Variant |
|---|---|---|
| Form tambah data | Simpan | Primary |
| Form pesanan | Buat Pesanan | Primary |
| Pengajuan | Kirim Pengajuan | Primary |
| Modal konfirmasi | Konfirmasi | Primary |
| Page Header | Ubah Data Aset | Primary |

### 3.4 Rules

- MUST digunakan untuk tindakan dengan prioritas tertinggi.
- SHOULD dibatasi pada satu Primary dalam satu kelompok aksi.
- MAY menggunakan warna positif atau negatif apabila sesuai dengan pattern GEMS yang disetujui.
- MUST menggunakan visual resmi GEMS.
- MUST NOT digunakan untuk semua aksi tanpa mempertimbangkan hierarchy.

---

## 4. Secondary Color Button

### 4.1 Definition

Secondary Color merupakan Button dengan penekanan warna dan tampilan outline, digunakan untuk tindakan kontekstual yang perlu terlihat jelas tetapi tidak membutuhkan tampilan solid.

### 4.2 When to Use

- Tindakan membutuhkan penekanan warna.
- Aksi berada pada konteks tertentu, seperti tabel atau halaman detail.
- Aksi memiliki konsekuensi yang perlu dibedakan secara visual.
- Tampilan solid terlalu dominan dalam kelompok aksi tersebut.

### 4.3 Examples

| Context | Button Label | Visual |
|---|---|---|
| Table Row | Ubah Pesanan | Colored Outline |
| Detail Page | Hapus | Red Outline |
| Live Charging Session | Stop Charging | Red Outline |

### 4.4 Rules

- MUST menggunakan warna yang tersedia pada GEMS.
- MUST menggunakan variant outline sesuai komponen.
- MUST NOT otomatis mengubah seluruh aksi negatif menjadi solid red.
- MUST NOT menggunakan Secondary Color untuk semua aksi pendukung.
- SHOULD menggunakan Secondary Gray untuk tindakan netral.

---

## 5. Secondary Gray Button

### 5.1 Definition

Secondary Gray merupakan Button netral yang digunakan untuk aksi pendukung, pembatalan, navigasi, atau utilitas.

### 5.2 When to Use

- Membatalkan tindakan.
- Kembali ke halaman sebelumnya.
- Mengedit data ketika aksi tersebut tidak menjadi prioritas utama.
- Mengekspor atau mengunduh data.
- Menjalankan aksi utilitas yang berdiri sendiri.

### 5.3 Examples

| Context | Button Label | Variant |
|---|---|---|
| Modal | Batal | Secondary Gray |
| Navigation | Kembali | Secondary Gray |
| Page Header | Ekspor Data | Secondary Gray |
| Detail Page | Edit Pesanan | Secondary Gray |
| Live Charging Session | Edit | Secondary Gray |
| Utility | Unduh Kode QR | Secondary Gray |

### 5.4 Rules

- SHOULD menjadi pasangan default untuk Primary.
- MAY digunakan tanpa Primary.
- MUST mempertahankan visual netral sesuai GEMS.
- MUST NOT otomatis diganti menjadi Secondary Color hanya karena tindakan mengubah data.
- MUST NOT memaksakan Primary untuk aksi utilitas.

---

## 6. Tertiary Color Button

### 6.1 Definition

Tertiary Color digunakan untuk aksi tambahan yang memerlukan penekanan warna lebih rendah dibandingkan Primary dan Secondary.

### 6.2 When to Use

Secara prinsip, digunakan ketika:

- Aksi bersifat tambahan.
- Aksi perlu dikenali melalui warna.
- Aksi tidak memerlukan tampilan solid atau outline yang dominan.

### 6.3 Rules

- MUST menggunakan variant resmi Tertiary Color.
- MUST mempertahankan hierarchy di bawah Primary dan Secondary.
- MUST NOT digunakan untuk aksi utama.
- MUST NOT digunakan sebagai pengganti konfirmasi penting tanpa pattern yang disetujui.
- MUST meminta arahan manusia untuk contoh implementasi yang belum ditetapkan.

---

## 7. Tertiary Gray Button

### 7.1 Definition

Tertiary Gray digunakan untuk aksi tambahan yang bersifat netral dan memiliki prioritas visual rendah.

### 7.2 When to Use

- Aksi bukan prioritas utama.
- Aksi tidak membutuhkan penekanan warna.
- Tampilan Secondary Gray terlalu dominan untuk konteks tersebut.

### 7.3 Rules

- MUST menggunakan variant resmi Tertiary Gray.
- MUST mempertahankan penekanan visual rendah.
- MUST NOT digunakan untuk aksi utama.
- MUST NOT digunakan ketika tindakan memerlukan penekanan tinggi.
- MUST mengikuti konteks penggunaan dan hierarchy GEMS.

---

## 8. Button States

Button GEMS memiliki empat state utama:

| State | Trigger | Visual Behavior | Interaction |
|---|---|---|---|
| Default | Tombol aktif tanpa interaksi khusus | Tampilan normal sesuai variant | Enabled |
| Hover | Pointer berada di atas tombol | Tampilan Hover sesuai GEMS | Enabled |
| Focused | Tombol menerima fokus | Visual Focused sesuai GEMS | Enabled |
| Disabled | Aksi tidak tersedia | Tampilan Disabled sesuai GEMS | Not interactive |

### 8.1 Default State

**When to Use:** Tombol tersedia dan siap digunakan.

**Behavior:**

- Menampilkan visual normal sesuai variant.
- Menampilkan label dan ikon apabila tersedia.
- Dapat menerima interaksi.

**Rules:**

- MUST menggunakan Default State resmi GEMS.
- MUST menjalankan aksi sesuai label.
- MUST NOT menggunakan visual Hover atau Focused secara permanen.

### 8.2 Hover State

**When to Use:** Pointer pengguna berada di atas tombol.

**Behavior:**

- Menampilkan perubahan visual Hover.
- Tidak mengubah label atau tujuan aksi.
- Kembali ke tampilan normal ketika pointer meninggalkan tombol, selama tidak ada state lain yang aktif.

**Rules:**

- MUST menggunakan Hover State resmi GEMS.
- MUST NOT membuat warna Hover custom.
- MUST NOT menganggap Hover sebagai aksi klik.

### 8.3 Focused State

**When to Use:** Tombol menerima fokus melalui keyboard atau mekanisme fokus lainnya.

**Behavior:**

- Menampilkan visual Focused.
- Tombol tetap dapat diaktifkan.
- Focus indicator tetap terlihat selama kondisi fokus berlaku.

**Rules:**

- MUST menggunakan Focused State resmi GEMS.
- MUST mempertahankan aksesibilitas keyboard.
- MUST NOT menghilangkan indikator fokus tanpa pengganti yang sesuai.

### 8.4 Disabled State

**When to Use:**

- Syarat tindakan belum terpenuhi.
- Aksi belum tersedia pada status proses saat ini.
- Aturan bisnis membatasi tindakan.
- Pengguna tidak memiliki izin untuk menjalankan tindakan, apabila pattern akses memang menampilkan tombol disabled.

**Behavior:**

- Menampilkan visual Disabled.
- Tidak menjalankan aksi.
- Tidak memberikan respons aktivasi yang menyerupai tombol aktif.

**Rules:**

- MUST menggunakan Disabled State resmi GEMS.
- MUST NOT menjalankan aksi ketika Disabled.
- SHOULD memberikan penjelasan apabila alasan Disabled tidak jelas.
- MUST NOT menggunakan Disabled sebagai pengganti pesan validasi form.

---

## 9. Contextual Button Patterns

### 9.1 Form Actions

**Case:** Batal + Simpan

| Button | Variant | Priority |
|---|---|---|
| Batal | Secondary Gray | Supporting |
| Simpan | Primary | Main |

**Rules:**

- SHOULD menggunakan kombinasi Secondary Gray + Primary.
- MUST memberikan prioritas visual tertinggi kepada Simpan.

### 9.2 Positive Confirmation

**Case:** Batal + Konfirmasi

| Button | Variant |
|---|---|
| Batal | Secondary Gray |
| Konfirmasi | Primary — Green Solid |

**Rules:**

- MUST menggunakan visual positif yang disetujui dalam GEMS.
- MUST menjaga perbedaan hierarchy antara Batal dan Konfirmasi.

### 9.3 Negative Confirmation

**Case:** Batal + Konfirmasi Penolakan

| Button | Variant |
|---|---|
| Batal | Secondary Gray |
| Konfirmasi | Primary — Red Solid |

**Rules:**

- MUST menggunakan visual negatif sesuai pattern yang disetujui.
- MUST NOT menggunakan visual positif untuk konfirmasi tindakan negatif.

### 9.4 Approval Decision

**Case:** Tolak + Setujui

| Button | Visual |
|---|---|
| Tolak | Red Solid |
| Setujui | Green Solid |

**Rules:**

- MAY menggunakan dua tombol solid pada konteks keputusan approval yang telah disetujui.
- MUST mempertahankan perbedaan makna tindakan.
- MUST NOT menerapkan pola dua tombol solid secara otomatis pada semua form.

**Scope:** Bagian ini hanya mendokumentasikan visual Button, bukan UX Flow Approval.

### 9.5 Page Header Actions

**Case:** Ekspor Data + Ubah Data Aset

| Button | Variant |
|---|---|
| Ekspor Data | Secondary Gray |
| Ubah Data Aset | Primary |

**Rules:**

- SHOULD menggunakan Primary untuk aksi utama halaman.
- SHOULD menggunakan Secondary Gray untuk aksi pendukung.
- MUST menentukan hierarchy berdasarkan konteks halaman.

### 9.6 Table Row Actions

**Case:** Ubah Pesanan

| Button | Variant |
|---|---|
| Ubah Pesanan | Secondary Color |

**Rules:**

- MAY menggunakan Secondary Color untuk aksi baris tabel.
- MUST NOT menganggap semua aksi Edit sebagai Primary.

### 9.7 Detail Page Actions

**Case:** Hapus + Edit Pesanan

| Button | Variant |
|---|---|
| Hapus | Secondary Color — Red Outline |
| Edit Pesanan | Secondary Gray |

**Rules:**

- MAY menggunakan Secondary Color dan Secondary Gray secara bersamaan.
- MUST NOT memaksakan Primary jika tidak ada aksi yang membutuhkan hierarchy tersebut.

### 9.8 Active Process Actions

**Case:** Live Charging Session

| Button | Variant | Context |
|---|---|---|
| Edit | Secondary Gray | Mengubah informasi terkait sesi |
| Stop Charging | Secondary Color — Red Outline | Menghentikan proses charging aktif |

**Rules:**

- MAY menggunakan Secondary Gray untuk aksi Edit.
- MAY menggunakan Secondary Color Red Outline untuk menghentikan proses aktif.
- MUST NOT otomatis menggunakan tombol solid merah untuk semua tindakan penghentian proses.

### 9.9 Standalone Utility Actions

**Case:** Unduh Kode QR

| Button | Variant |
|---|---|
| Unduh Kode QR | Secondary Gray |

**Rules:**

- MAY menggunakan Secondary Gray secara mandiri.
- MUST NOT memaksakan Primary apabila aksi bersifat utilitas.

---

## 10. Button Labels

### 10.1 General Rules

- MUST menggunakan label yang jelas dan berorientasi tindakan.
- MUST menggunakan terminologi sesuai HSD/BRD.
- SHOULD menggunakan label singkat.
- SHOULD menjaga konsistensi penamaan pada seluruh aplikasi.
- MUST NOT menggunakan label ambigu apabila tindakan membutuhkan penjelasan spesifik.

### 10.2 Label Examples

| Action | Recommended Label |
|---|---|
| Menyimpan perubahan | Simpan Perubahan |
| Membuat pesanan | Buat Pesanan |
| Mengirim pengajuan | Kirim Pengajuan |
| Menghapus data | Hapus |
| Membatalkan tindakan | Batal |
| Mengekspor data | Ekspor Data |
| Mengunduh QR | Unduh Kode QR |
| Menghentikan charging | Stop Charging |

---

## 11. Button Selection Rules for AI

AI MUST mengikuti urutan pengambilan keputusan berikut:

**Step 1 — Identify Action**

Identifikasi tindakan berdasarkan HSD/BRD.

**Step 2 — Identify Context**

Tentukan lokasi Button: Form, Modal, Page Header, Detail Page, Table Row, Card, Active Process, atau Utility Area.

**Step 3 — Determine Priority**

Tentukan apakah tindakan merupakan Main Action, Supporting Action, Contextual Action, atau Additional Action.

**Step 4 — Select Variant**

Pilih variant berdasarkan Button Usage Matrix dan Contextual Button Patterns.

**Step 5 — Apply State**

Gunakan Default, Hover, Focused, atau Disabled sesuai kondisi interaksi.

**Step 6 — Validate Against GEMS**

Pastikan variant, warna, state, dan komposisi sesuai komponen resmi GEMS.

**Step 7 — Request Human Approval When Needed**

Jika tidak ditemukan pattern yang sesuai atau dibutuhkan perubahan pada hierarchy atau visual, AI MUST meminta persetujuan manusia sebelum membuat aturan baru.

---

## 12. AI Restrictions

AI MUST NOT:

1. Membuat variant Button baru tanpa Human Approval.
2. Mengubah warna atau visual state di luar GEMS.
3. Menggunakan Primary untuk seluruh tindakan.
4. Menganggap semua aksi Edit harus Primary.
5. Menganggap semua aksi Hapus harus Red Solid.
6. Menggunakan Secondary Color untuk semua aksi pendukung.
7. Menghilangkan Focused State.
8. Menjalankan aksi pada Disabled Button.
9. Mengubah alur bisnis hanya berdasarkan pilihan Button.
10. Menganggap contoh kontekstual sebagai aturan universal tanpa memeriksa kebutuhan halaman.

---

## 13. Figma Reference

**Source:** GEMS Design System

[Open Button Component in Figma](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=294-4425)
