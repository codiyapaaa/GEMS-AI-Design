# GEMS Design System — Toggle Guidelines

**Document:** `components/toggle.md`  
**Version:** 1.3 — Final  
**Component:** Toggle  
**Platform:** GEMS Web Application  
**Primary Design Source:** GEMS Design System (Figma)  
**Business Requirement Source:** HSD / BRD

---

## 1. Purpose & Core Principles

Toggle merupakan komponen interaktif berbentuk switch yang digunakan untuk mengaktifkan atau menonaktifkan suatu pengaturan, fitur, preferensi, atau kondisi data yang memiliki dua nilai (*binary state*).

Contoh kondisi:

- Aktif / Nonaktif
- On / Off
- Tampilkan / Sembunyikan
- Enabled / Disabled sebagai nilai pengaturan, bukan interaction state komponen

### 1.1 Core Principles

1. Toggle digunakan untuk mengubah kondisi biner yang dapat dipertahankan.
2. Toggle bukan pengganti Button untuk tindakan sekali pakai.
3. Toggle harus merepresentasikan nilai aktual dari data atau pengaturan.
4. Perubahan Toggle harus mengikuti mekanisme penyimpanan dan validasi yang ditentukan HSD/BRD.
5. Komponen, variants, dan visual harus mengikuti GEMS Design System.

### 1.2 AI Rules

- MUST menggunakan komponen Toggle resmi GEMS.
- MUST membaca HSD/BRD sebelum menentukan penggunaan Toggle.
- MUST mempertahankan konsistensi visual dan interaction pattern GEMS.
- MUST NOT membuat aturan bisnis atau behavior baru tanpa persetujuan.
- MUST NOT menganggap semua kebutuhan dengan dua pilihan otomatis menggunakan Toggle.

---

## 2. When to Use Toggle

### 2.1 Recommended Usage

| Context | When to Use | Example | Reason |
|---|---|---|---|
| Settings | Mengaktifkan atau menonaktifkan pengaturan | Aktifkan Notifikasi | Mengubah kondisi pengaturan |
| Feature Configuration | Mengaktifkan atau menonaktifkan fitur | Aktifkan Pengingat | Mengontrol kondisi fitur |
| Visibility Settings | Mengatur visibilitas elemen | Tampilkan Informasi Tambahan | Mengubah kondisi tampil/sembunyi |
| System Configuration | Mengaktifkan atau menonaktifkan konfigurasi | Aktifkan Integrasi | Mengontrol konfigurasi sistem |
| Form Settings | Mengisi nilai pengaturan biner dalam form | Aktifkan Pengingat Otomatis | Menentukan nilai pengaturan |
| Table Row Settings | Mengubah pengaturan biner pada item tabel | Aktifkan Konfigurasi | Mengontrol kondisi per item |
| Data Activation Status | Mengatur status aktif/nonaktif suatu record | Status Aktif | Mengontrol kondisi aktif data |

**Important:** Contoh di atas merupakan pola penggunaan. Keberadaan fitur, hak akses, dan behavior aktual tetap harus mengikuti HSD/BRD.

### 2.2 When NOT to Use Toggle

| Requirement | Reason | Recommended Component |
|---|---|---|
| Menyimpan data | Merupakan tindakan sekali pakai | Button |
| Menghapus data | Merupakan aksi destruktif | Button |
| Mengirim pengajuan | Merupakan aksi submit | Button |
| Mengonfirmasi tindakan | Membutuhkan keputusan eksplisit | Button / Modal |
| Memilih beberapa item | Merupakan multi-selection | Checkbox |
| Memilih satu dari beberapa opsi | Merupakan single-selection | Radio Button / Dropdown |
| Menyetujui atau menolak permintaan | Merupakan keputusan workflow | Button / Approved Workflow |
| Mengubah status proses bertahap | Memiliki aturan transisi bisnis | Control sesuai HSD/BRD |

### 2.3 Toggle Selection Rules

- MUST menggunakan Toggle untuk kondisi biner yang sesuai.
- MUST memastikan pengguna memahami apa yang diaktifkan atau dinonaktifkan.
- MUST menggunakan Toggle untuk status aktif/nonaktif data jika pola tersebut ditetapkan dalam desain atau requirement.
- MUST NOT menggunakan Toggle untuk aksi Simpan, Hapus, Kirim, atau Konfirmasi.
- MUST NOT mengganti status workflow menjadi Toggle tanpa persetujuan.
- SHOULD menggunakan label yang menjelaskan fungsi atau objek yang dikendalikan.

---

## 3. Toggle Component Structure

GEMS Design System menyediakan komponen Toggle utama dan komponen dasar switch.

| Component | Purpose | Figma Reference |
|---|---|---|
| Toggle | Komponen lengkap, termasuk opsi dengan teks pendamping | [View Toggle Design](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-6121) |
| `_Toggle base` | Komponen switch dasar tanpa teks | [View Toggle Base Design](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-18337) |

### 3.1 Component Properties

| Property | Available Values | Purpose |
|---|---|---|
| `Pressed` | `True`, `False` | Menentukan nilai aktif/nonaktif |
| `Size` | `xs`, `sm`, `md` | Menentukan ukuran switch |
| `Text` | `True`, `False` | Menampilkan atau menyembunyikan teks pendamping |
| `State` | `Default`, `Hover`, `Focus`, `Disabled` | Menentukan kondisi interaksi |

### 3.2 Property Rules

- `Pressed` menentukan nilai Toggle.
- `State` menentukan kondisi interaksi Toggle.
- `Size` menentukan dimensi switch.
- `Text` menentukan keberadaan teks pendamping pada komponen Toggle utama.
- Komponen `_Toggle base` tidak memiliki property `Text`.
- `Focus` merupakan penamaan State resmi Figma GEMS, bukan `Focused`.

---

## 4. Toggle Variants & Sizes

### 4.1 Available Sizes

| Size | Switch Dimensions | Recommended Usage |
|---|---|---|
| `xs` | 32 × 16 px | Area ringkas tanpa teks |
| `sm` | 36 × 20 px | Tabel atau pengaturan ringkas |
| `md` | 44 × 24 px | Form atau halaman pengaturan standar |

Dimensi tersebut merujuk pada visual switch, bukan keseluruhan area interaksi.

### 4.2 Text Variants

| Text | Available Sizes | Usage |
|---|---|---|
| `False` | `xs`, `sm`, `md` | Label tersedia secara terpisah |
| `True` | `sm`, `md` | Teks pendamping berada dalam komponen |

Kombinasi `Size=xs, Text=True` tidak teridentifikasi pada variants resmi yang diperiksa.

### 4.3 Variant Selection Rules

- MUST menggunakan ukuran resmi `xs`, `sm`, atau `md`.
- MUST NOT membuat ukuran custom tanpa persetujuan.
- MUST menggunakan kombinasi `Text` dan `Size` yang tersedia.
- SHOULD mempertahankan konsistensi ukuran dalam kelompok pengaturan yang sama.
- SHOULD mempertimbangkan keterbacaan dan area interaksi ketika menggunakan ukuran kecil.
- MUST NOT mengubah dimensi atau proporsi switch di luar GEMS.

---

## 5. Toggle Pressed Conditions

`Pressed` merepresentasikan nilai biner yang dikendalikan oleh Toggle.

### 5.1 Pressed Matrix

| Pressed | Meaning | Visual | Interaction |
|---|---|---|---|
| `False` | Off / Nonaktif | Visual Off resmi GEMS | Dapat diubah jika enabled |
| `True` | On / Aktif | Visual On resmi GEMS | Dapat diubah jika enabled |

### 5.2 Pressed=False

**When to Use:** Nilai pengaturan atau data berada dalam kondisi nonaktif.

**Rules:**

- MUST menampilkan visual Off resmi GEMS.
- MUST mempertahankan nilai sampai terjadi perubahan yang valid.
- MUST NOT menganggap `Pressed=False` sebagai `State=Disabled`.

### 5.3 Pressed=True

**When to Use:** Nilai pengaturan atau data berada dalam kondisi aktif.

**Rules:**

- MUST menampilkan visual On resmi GEMS.
- MUST mempertahankan nilai sampai terjadi perubahan yang valid.
- MUST NOT menganggap `Pressed=True` sebagai Hover atau Focus.

### 5.4 Pressed vs State

| Pressed | State | Meaning |
|---|---|---|
| False | Default | Off, kondisi normal |
| True | Default | On, kondisi normal |
| False | Hover | Off, pointer hover |
| True | Hover | On, pointer hover |
| False | Focus | Off, menerima fokus |
| True | Focus | On, menerima fokus |
| False | Disabled | Off, tidak dapat diubah |
| True | Disabled | On, tidak dapat diubah |

**Important:** Toggle yang Disabled tetap dapat memperlihatkan nilai aktif atau nonaktif sesuai data.

---

## 6. Toggle States & Behavior

### 6.1 State Overview

| State | Trigger | Visual Behavior | Can Change Value? |
|---|---|---|---|
| `Default` | Tidak ada interaksi khusus | Visual normal GEMS | Yes |
| `Hover` | Pointer berada di area Toggle | Visual Hover GEMS | Yes |
| `Focus` | Toggle menerima fokus | Focus indicator GEMS | Yes |
| `Disabled` | Interaksi tidak diizinkan | Visual Disabled GEMS | No |

### 6.2 Default State

**When to Use:** Toggle berada dalam kondisi normal dan tersedia untuk interaksi.

**Behavior:**

- Menampilkan nilai berdasarkan `Pressed`.
- Dapat diaktifkan melalui pointer atau keyboard.
- Tidak menampilkan visual Hover atau Focus jika kondisi tersebut tidak terjadi.

**AI Rules:**

- MUST menggunakan variant `State=Default`.
- MUST mempertahankan nilai yang sedang berlaku.
- MUST NOT menampilkan visual Hover atau Focus secara permanen.

### 6.3 Hover State

**When to Use:** Pointer berada di area interaksi Toggle.

**Behavior:**

- Visual berubah menjadi Hover sesuai GEMS.
- Nilai `Pressed` tidak berubah.
- Ketika pointer keluar, visual kembali sesuai kondisi interaksi yang berlaku.

**AI Rules:**

- MUST menggunakan variant `State=Hover`.
- MUST NOT mengubah nilai hanya karena Hover.
- MUST NOT membuat visual Hover custom.

### 6.4 Focus State

**When to Use:** Toggle menerima fokus melalui keyboard atau mekanisme fokus lainnya.

**Behavior:**

- Menampilkan indikator Focus resmi.
- Nilai `Pressed` tidak berubah hanya karena menerima fokus.
- Pengguna dapat mengubah nilai melalui interaksi keyboard yang didukung.

**AI Rules:**

- MUST menggunakan variant `State=Focus`.
- MUST mempertahankan indikator fokus yang terlihat.
- MUST NOT menghilangkan indikator fokus tanpa pengganti yang sesuai.
- MUST NOT mengganti penamaan Figma State menjadi `Focused`.

### 6.5 Disabled State

**When to Use:**

- Pengguna tidak memiliki izin untuk mengubah pengaturan.
- Fitur belum tersedia.
- Prasyarat perubahan belum terpenuhi.
- Kondisi proses tidak memungkinkan perubahan berdasarkan HSD/BRD.

**Behavior:**

- Menampilkan visual Disabled resmi.
- Tidak menerima perubahan melalui interaksi pengguna.
- Tetap memperlihatkan nilai `Pressed=True` atau `Pressed=False` sesuai data.

**AI Rules:**

- MUST menggunakan variant `State=Disabled`.
- MUST NOT menjalankan perubahan ketika Disabled.
- MUST NOT mengubah nilai tersimpan hanya karena Disabled.
- SHOULD memberikan penjelasan jika alasan Disabled tidak jelas.
- MUST mengikuti aturan hak akses mengenai apakah Toggle ditampilkan Disabled atau disembunyikan.

---

## 7. Toggle Interaction Behavior

### 7.1 Basic Interaction

| User Action | Expected Behavior |
|---|---|
| Klik Toggle Off | Berubah menjadi On jika diizinkan |
| Klik Toggle On | Berubah menjadi Off jika diizinkan |
| Hover | Visual Hover, nilai tetap |
| Keyboard Focus | Visual Focus, nilai tetap |
| Aktivasi keyboard | Mengubah nilai jika enabled |
| Klik Disabled Toggle | Tidak terjadi perubahan |

### 7.2 Save Behavior

Toggle dapat menggunakan dua pola penyimpanan sesuai requirement.

| Pattern | Behavior | When to Use |
|---|---|---|
| Immediate Update | Perubahan diproses setelah Toggle diaktifkan | Jika HSD/BRD menetapkan perubahan langsung |
| Form Submission | Nilai berubah pada form, kemudian disimpan melalui Button | Jika HSD/BRD menggunakan mekanisme Simpan |

**AI Rules:**

- MUST mengikuti pola penyimpanan HSD/BRD.
- MUST NOT mengasumsikan seluruh Toggle menggunakan auto-save.
- MUST NOT menambahkan tombol Simpan jika requirement menggunakan immediate update.
- MUST NOT menghapus tombol Simpan jika requirement menggunakan form submission.
- MUST memberikan feedback yang sesuai jika perubahan gagal.

### 7.3 Initial Value

- MUST menggunakan nilai awal berdasarkan data atau requirement.
- MUST NOT mengatur seluruh Toggle menjadi Off secara otomatis.
- MUST mempertahankan nilai tersimpan setelah reload jika sistem memang menyimpan pengaturan tersebut.
- MUST NOT mengubah data tanpa tindakan pengguna atau aturan sistem yang sah.

---

## 8. Toggle vs Other Components

| User Requirement | Correct Component | Explanation |
|---|---|---|
| Aktifkan notifikasi | Toggle | Mengubah preferensi biner |
| Aktifkan status data | Toggle, jika ditetapkan dalam requirement | Mengubah status aktif/nonaktif |
| Pilih beberapa kategori | Checkbox | Multi-selection |
| Pilih satu lokasi | Dropdown | Single-selection |
| Pilih Ya/Tidak dalam pertanyaan formulir | Radio Button atau kontrol yang disetujui | Jawaban eksplisit, bukan selalu pengaturan |
| Simpan perubahan | Button | Menjalankan tindakan |
| Hapus data | Button | Aksi destruktif |
| Setujui pengajuan | Button | Keputusan workflow |
| Ubah status proses | Berdasarkan HSD/BRD | Dapat memiliki validasi dan tahapan khusus |

**Important:** Tidak semua kebutuhan dengan dua nilai harus menggunakan Toggle.

---

## 9. Contextual Toggle Patterns

Contoh berikut merupakan ilustrasi penggunaan komponen. AI MUST memvalidasi konteks, hak akses, dan behavior terhadap HSD/BRD.

### 9.1 Notification Settings

| Element | Configuration |
|---|---|
| Label | Aktifkan Notifikasi |
| Size | `sm` atau `md` |
| Text | True |
| Pressed | Sesuai data |
| State | Default |

**Behavior:** Mengaktifkan atau menonaktifkan pengaturan notifikasi.

### 9.2 Feature Configuration

| Element | Configuration |
|---|---|
| Label | Aktifkan Fitur |
| Size | `md` |
| Text | True |
| Pressed | Sesuai data |
| State | Default / Disabled |

**Behavior:** Mengubah kondisi fitur apabila pengguna memiliki izin.

### 9.3 Table Row Settings

| Element | Configuration |
|---|---|
| Context | Pengaturan per item pada tabel |
| Size | `xs` atau `sm` |
| Text | False |
| Pressed | Sesuai data |
| State | Default / Disabled |

**Behavior:** Mengubah pengaturan biner untuk item tertentu.

**Restriction:** MUST NOT mengubah status workflow kompleks melalui Toggle tanpa aturan bisnis yang jelas.

### 9.4 Visibility Settings

| Element | Configuration |
|---|---|
| Label | Tampilkan Informasi Tambahan |
| Size | `sm` atau `md` |
| Text | True |
| Pressed | Sesuai nilai visibilitas |
| State | Default |

**Behavior:** Mengatur apakah informasi tertentu ditampilkan.

### 9.5 Disabled Settings

| Element | Configuration |
|---|---|
| Label | Aktifkan Integrasi |
| Size | `sm` atau `md` |
| Text | True |
| Pressed | True / False sesuai data |
| State | Disabled |

**Behavior:** Nilai terlihat tetapi tidak dapat diubah.

### 9.6 Data Activation Status

**When to Use:**

Toggle dapat digunakan pada form tambah/edit data atau halaman pengaturan untuk menentukan apakah suatu record berstatus aktif atau nonaktif.

**Example:** ISS Registrasi Asset — Status Aktif.

| Element | Configuration |
|---|---|
| Field Label | Status |
| Toggle Label | Status Aktif |
| Component | Toggle |
| Pressed | `True` untuk aktif, `False` untuk nonaktif |
| State | Default, Hover, Focus, atau Disabled |
| Size | Mengikuti variant GEMS yang digunakan |
| Save Behavior | Mengikuti mekanisme penyimpanan form sesuai HSD/BRD |

**Interaction Behavior:**

- Ketika `Pressed=True`, data direpresentasikan sebagai aktif.
- Ketika `Pressed=False`, data direpresentasikan sebagai nonaktif.
- Perubahan nilai Toggle tidak otomatis berarti data langsung tersimpan.
- Jika Toggle berada dalam form dengan tombol Simpan, nilai mengikuti proses penyimpanan form.
- Jika pengguna tidak memiliki hak untuk mengubah status, gunakan kondisi Disabled atau aturan tampilan sesuai HSD/BRD.

**AI Rules:**

- MUST menggunakan Toggle untuk status aktif/nonaktif data apabila pola tersebut ditentukan dalam desain atau requirement.
- MUST membedakan status aktif/nonaktif data dari status workflow.
- MUST menggunakan nilai awal sesuai data yang tersedia.
- MUST NOT mengasumsikan perubahan status langsung disimpan.
- MUST NOT mengubah status workflow kompleks menjadi Toggle tanpa persetujuan.

**Design Reference:**

[View ISS Registrasi Asset — Status Aktif](https://www.figma.com/design/v3ggUUZOrTe6dh9wJ21Hcy/ISS-Registrasi-Asset?node-id=365-92063)

---

## 10. Labels & Supporting Text

### 10.1 Label Rules

- MUST menggunakan label yang menjelaskan pengaturan atau objek yang dikendalikan.
- MUST menggunakan terminologi HSD/BRD.
- MUST NOT menggunakan label ambigu tanpa konteks.
- SHOULD menggunakan label singkat dan mudah dipahami.

### 10.2 Label Examples

| Context | Recommended Label |
|---|---|
| Notification | Aktifkan Notifikasi |
| Feature | Aktifkan Fitur |
| Visibility | Tampilkan Informasi Tambahan |
| Reminder | Aktifkan Pengingat |
| Integration | Aktifkan Integrasi |
| Data Activation | Status Aktif |

### 10.3 Supporting Description

Supporting description dapat digunakan apabila konsekuensi pengaturan perlu dijelaskan.

| Label | Supporting Description |
|---|---|
| Aktifkan Notifikasi | Terima pemberitahuan ketika terdapat pembaruan data. |
| Aktifkan Pengingat | Tampilkan pengingat untuk jadwal yang akan datang. |
| Status Aktif | Tentukan apakah data dapat digunakan sesuai aturan sistem. |

**Important:** Supporting description merupakan contoh wording dan harus disesuaikan dengan fungsi aktual pada HSD/BRD.

---

## 11. Accessibility Rules

- MUST memiliki label atau accessible name yang jelas.
- MUST memastikan nilai On/Off dapat dipahami tanpa hanya mengandalkan warna.
- MUST mempertahankan indikator Focus.
- MUST mendukung interaksi keyboard sesuai pola switch.
- MUST memastikan Disabled tidak dapat diubah melalui keyboard atau pointer.
- SHOULD memastikan area interaksi memadai, termasuk pada ukuran `xs`.
- SHOULD mengomunikasikan nilai aktif/nonaktif kepada teknologi bantu.
- SHOULD memastikan label dan deskripsi mendukung pemahaman pengguna terhadap konsekuensi perubahan.

---

## 12. AI Toggle Selection Workflow

1. **Read HSD/BRD:** Identifikasi apakah kebutuhan merupakan pengaturan biner atau status aktif/nonaktif data.
2. **Check Suitability:** Pastikan Toggle lebih tepat daripada Button, Checkbox, Radio Button, atau Dropdown.
3. **Select Official Component:** Gunakan Toggle GEMS.
4. **Select Size:** Pilih `xs`, `sm`, atau `md` sesuai variant.
5. **Select Text:** Tentukan `Text=True` atau `Text=False` sesuai kombinasi resmi.
6. **Set Pressed:** Gunakan nilai True/False berdasarkan data.
7. **Set State:** Pilih Default, Hover, Focus, atau Disabled sesuai kondisi interaksi.
8. **Define Save Behavior:** Tentukan immediate update atau form submission sesuai HSD/BRD.
9. **Verify Figma:** Pastikan visual dan variant sesuai GEMS Design System.
10. **Human Approval:** Minta persetujuan apabila diperlukan perubahan komponen, aturan bisnis, atau user flow.

---

## 13. AI Restrictions

AI MUST NOT:

1. Membuat variant Toggle baru tanpa persetujuan.
2. Membuat ukuran di luar `xs`, `sm`, atau `md`.
3. Menggunakan `Size=xs, Text=True` sebagai kombinasi resmi tanpa bukti.
4. Mengubah nama property `Pressed` menjadi `Checked` pada dokumentasi variant Figma.
5. Mengubah nama State `Focus` menjadi `Focused`.
6. Menganggap `Pressed=False` sebagai Disabled.
7. Mengubah nilai Toggle hanya karena Hover atau Focus.
8. Mengasumsikan semua Toggle menggunakan auto-save.
9. Mengasumsikan semua Toggle memerlukan tombol Simpan.
10. Menentukan nilai awal tanpa data atau requirement.
11. Menggunakan Toggle untuk aksi Hapus, Simpan, Kirim, atau Konfirmasi.
12. Menggunakan Toggle untuk workflow approval tanpa requirement.
13. Mengubah business flow atau hak akses tanpa Human Approval.
14. Membuat visual, warna, atau dimensi baru di luar GEMS.
15. Menganggap contoh kontekstual sebagai requirement bisnis universal.
16. Menggunakan Toggle untuk status workflow kompleks tanpa aturan transisi yang jelas.
17. Mengasumsikan perubahan status aktif/nonaktif data langsung tersimpan tanpa ketentuan HSD/BRD.

---

## 14. Official Figma References

| Reference | Purpose | Figma Design |
|---|---|---|
| GEMS Toggle Overview | Dokumentasi keseluruhan Toggle | [Open Toggle Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-17422) |
| GEMS Toggle Base | Base switch variants | [Open Toggle Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-18337) |
| GEMS Toggle | Toggle variants termasuk Text | [Open Toggle Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-6121) |
| ISS Registrasi Asset | Contoh implementasi Status Aktif | [Open Status Aktif Design](https://www.figma.com/design/v3ggUUZOrTe6dh9wJ21Hcy/ISS-Registrasi-Asset?node-id=365-92063) |

---

## 15. Implementation Requirements

### 15.1 Source of Truth

| Source | Responsibility |
|---|---|
| HSD / BRD | Business requirements, role access, validation, dan workflow |
| GEMS Design System | Komponen, variants, ukuran, dan visual |
| Approved Product Designs | Referensi implementasi kontekstual |
| Human Approval | Persetujuan perubahan atau penambahan yang belum tercakup |

### 15.2 Final AI Instruction

When generating UI/UX designs, AI MUST:

1. Read and understand the HSD/BRD.
2. Determine whether Toggle is appropriate for the required interaction.
3. Use the official GEMS Toggle component and supported variants.
4. Apply the correct `Pressed`, `Size`, `Text`, and `State` properties.
5. Follow the defined interaction and save behavior.
6. Preserve business rules, permissions, and workflow.
7. Use approved product examples as contextual references without treating them as universal requirements.
8. Request Human Approval before introducing new components, variants, or business behavior.

**Final Principle:** HSD/BRD defines what the system must do. GEMS Design System defines how the interface must be designed. AI must respect both sources and must not introduce unapproved changes.
