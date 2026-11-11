# GEMS Design System — Input Guidelines

**Document:** `components/input.md`  
**Version:** 1.0 — Final  
**Scope:** Input Field, Textarea Input Field, Input Dropdown, Date & Time Picker  
**Platform:** GEMS Web Application

## 1. Purpose & Source of Truth

Dokumen ini adalah **satu sumber aturan untuk seluruh keluarga komponen input GEMS**. AI menggunakan HSD/BRD untuk menentukan data, aturan bisnis, hak akses, format, dan alur; menggunakan GEMS Figma Design System untuk memilih komponen, variant, state, dan visual. Jika keduanya belum menentukan perilaku, AI MUST meminta Human Approval, bukan menciptakan aturan sendiri.

**Core principle:** Pilih kontrol berdasarkan jenis data dan cara interaksi, bukan kemiripan visual. **Nama `Type`, `State`, `Size`, dan `Destructive` di bawah mempertahankan penamaan komponen Figma; jangan menormalisasi nama state lintas komponen.**

## 2. Component Selection Matrix

| Kebutuhan pengguna | Komponen GEMS | Alasan | Contoh ilustratif |
|---|---|---|---|
| Memasukkan satu baris teks/angka | Input Field | Input bebas satu nilai | Nama, nomor identitas |
| Menulis teks lebih panjang/multiline | Textarea Input Field | Mendukung beberapa baris | Catatan, deskripsi |
| Memilih dari opsi yang tersedia | Input Dropdown | Pilihan terstruktur | Lokasi, kategori |
| Memilih opsi dengan pencarian | Input Dropdown — Search | Menemukan pilihan dalam daftar | Pilih karyawan |
| Memilih banyak opsi yang ditampilkan sebagai tag | Input Dropdown — Tags | Pilihan multi-value *jika didukung kebutuhan dan komponen* | Kategori |
| Mengetik beberapa nilai sebagai tag | Input Field — Tags | Input multi-value | Kata kunci |
| Memilih tanggal | Date & Time Picker | Interaksi kalender | Tanggal kunjungan |
| Memilih waktu | Date & Time Picker | Interaksi pemilihan jam | Jam keberangkatan |
| Memilih tanggal dan waktu | Date & Time Picker | Kombinasi input sesuai desain yang tersedia | Check-in terjadwal |

- MUST memilih komponen sesuai requirement HSD/BRD.
- MUST NOT mengganti Dropdown dengan Input Field hanya karena keduanya berbentuk field.
- MUST NOT mengganti Date & Time Picker dengan Input teks bebas tanpa persetujuan.
- SHOULD memisahkan label, helper text, dan error message secara jelas.

## 3. Input Field

**Figma:** https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=219-5292

### 3.1 Properties

| Property | Nilai resmi |
|---|---|
| Size | `sm`, `md` |
| Type | `Default`, `Icon leading`, `Leading dropdown`, `Trailing dropdown`, `Leading text`, `Payment input`, `Tags`, `Trailing button` |
| State | `Placeholder`, `Filled`, `Focused`, `Disabled` |
| Destructive | `False`, `True` |

### 3.2 Type Usage Matrix

| Type | Gunakan ketika | Hindari ketika | Contoh ilustratif |
|---|---|---|---|
| Default | Teks/angka sederhana satu baris | Dibutuhkan affordance khusus | Nama lengkap |
| Icon leading | Ikon awal membantu memahami konteks | Ikon hanya dekorasi | Pencarian sederhana |
| Leading dropdown | Ada pilihan di depan nilai input | Pilihan tidak berkaitan langsung | Kode negara + nomor |
| Trailing dropdown | Pilihan di belakang nilai input | Pilihan seharusnya field mandiri | Nilai + satuan |
| Leading text | Prefiks tetap tidak diedit sebagai nilai utama | Prefiks harus diketik pengguna | `Rp` + nominal |
| Payment input | Pola input pembayaran GEMS diperlukan | Semua input angka biasa | Informasi pembayaran |
| Tags | Pengguna memasukkan beberapa nilai/tag | Hanya satu nilai | Kata kunci |
| Trailing button | Ada aksi langsung terhadap nilai field | Aksi untuk keseluruhan form | Kode + tombol aksi |

### 3.3 Size Rules

| Size | Penggunaan | Aturan |
|---|---|---|
| `sm` | Form ringkas sesuai layout GEMS | MUST memakai instance/token resmi |
| `md` | Form standar sesuai layout GEMS | MUST memakai instance/token resmi |

MUST NOT menyimpulkan tinggi/padding CSS dari ukuran frame dokumentasi Figma. MUST mempertahankan konsistensi ukuran dalam kelompok form kecuali layout mengharuskan lain.

### 3.4 State Matrix

| State | Kondisi | Perilaku | Editable |
|---|---|---|---|
| Placeholder | Belum ada nilai | Menampilkan placeholder | Ya |
| Filled | Sudah berisi dan tidak fokus | Menampilkan nilai normal | Ya |
| Focused | Sedang menerima fokus | Visual fokus resmi GEMS | Ya |
| Disabled | Interaksi tidak tersedia | Visual disabled resmi GEMS | Tidak |

- MUST mempertahankan nilai pengguna ketika fokus berpindah.
- MUST mendukung indikator fokus keyboard.
- MUST NOT menggunakan Disabled untuk menampilkan error.
- MUST NOT membuat `Success` State; setelah validasi berhasil kembali ke `Filled`, `Focused`, atau `Placeholder` sesuai kondisi.

### 3.5 Destructive & Validation

| Kondisi | State | Destructive | Perilaku |
|---|---|---|---|
| Kosong normal | Placeholder | False | Placeholder normal |
| Terisi normal | Filled | False | Nilai normal |
| Fokus normal | Focused | False | Visual fokus |
| Kosong tetapi error | Placeholder | True | Visual error resmi GEMS |
| Terisi tetapi error | Filled | True | Nilai tetap ada; visual error |
| Fokus dengan error | Focused | True | Visual error/fokus sesuai GEMS |
| Error selesai diperbaiki | Sesuai kondisi | False | Kembali normal tanpa indikator sukses baru |
| Disabled | Disabled | False | Non-interaktif |

`Destructive` adalah **property**, bukan tambahan `State`. MUST menggunakan pesan validasi yang jelas berdasarkan HSD/BRD; MUST NOT menghapus nilai ketika error; MUST NOT menambah border hijau atau ikon centang untuk sukses.

## 4. Textarea Input Field

**Figma:** https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-4425

### 4.1 Properties

| Property | Nilai resmi |
|---|---|
| Type | `Default`, `Tags` |
| State | `Placeholder`, `Default`, `Focused`, `Disabled` |
| Destructive | `False`, `True` |

**Penting:** Textarea menggunakan `State=Default`, **bukan** `Filled` seperti Input Field. Tidak ada properti `Size` yang teridentifikasi pada kumpulan variant Textarea rujukan ini; AI MUST NOT mengada-adakan `sm/md` untuk Textarea.

### 4.2 Type Usage

| Type | Kapan digunakan | Contoh ilustratif |
|---|---|---|
| Default | Catatan, deskripsi, atau teks multiline | Catatan kunjungan |
| Tags | Konten berbentuk tag sesuai kemampuan komponen | Daftar tag dalam area input |

### 4.3 State & Error Matrix

| State | Kondisi | Destructive=False | Destructive=True |
|---|---|---|---|
| Placeholder | Belum diisi | Tampilan placeholder | Placeholder error |
| Default | Area tidak fokus | Tampilan normal | Tampilan error |
| Focused | Area sedang fokus | Tampilan fokus | Tampilan error saat fokus |
| Disabled | Tidak dapat diedit | Tampilan disabled | Tidak tersedia sebagai kombinasi variant pada referensi yang ditinjau |

- MUST memakai `Default` untuk tampilan normal setelah pengguna selesai mengisi dan keluar dari fokus.
- MUST mempertahankan line breaks/teks pengguna selama editing.
- MUST NOT menciptakan `Filled`, `Success`, atau indikator sukses baru untuk Textarea.
- MUST NOT mengasumsikan `Destructive=True` tersedia pada `Disabled` bila tidak ada variant resminya.
- SHOULD menggunakan Textarea untuk teks multiline, bukan memaksa Input Field satu baris.

## 5. Input Dropdown

**Figma:** https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-4695  
**Relevant frame:** `Input dropdown` (`240:5034`)

### 5.1 Properties

| Property | Nilai resmi yang teridentifikasi |
|---|---|
| Type | `Default`, `Icon leading`, `Avatar leading`, `Dot leading`, `Search`, `Tags` |
| State | `Placeholder`, `Default`, `Focused`, `Open`, `Disabled` |

Jangan menambahkan properti `Destructive` atau `Size` ke Dropdown tanpa bukti pada komponen Figma terkait. `Open` merupakan state Dropdown, bukan Input Field.

### 5.2 Type Usage Matrix

| Type | Gunakan ketika | Contoh ilustratif |
|---|---|---|
| Default | Memilih dari daftar pilihan biasa | Lokasi kerja |
| Icon leading | Pilihan memiliki ikon pendukung | Kategori berikon |
| Avatar leading | Pilihan perlu dikenali dengan avatar | Pilih anggota tim |
| Dot leading | Pilihan menampilkan indikator titik yang bermakna | Pilih status berkode warna jika disetujui |
| Search | Daftar perlu ditelusuri lewat pencarian | Cari karyawan |
| Tags | Beberapa pilihan ditampilkan sebagai tag sesuai komponen | Pilih kategori |

### 5.3 State Matrix

| State | Kondisi | Behavior |
|---|---|---|
| Placeholder | Belum ada pilihan | Placeholder terlihat |
| Default | Dropdown tertutup dalam tampilan normal | Pilihan saat ini dapat ditampilkan |
| Focused | Mendapat fokus | Indikator fokus resmi GEMS |
| Open | Daftar pilihan terbuka | Menampilkan panel opsi sesuai variant |
| Disabled | Tidak dapat digunakan | Tidak membuka daftar atau mengubah nilai |

- MUST menggunakan `Open` ketika panel pilihan dibuka, jika variant terkait mendukungnya.
- MUST mempertahankan nilai terpilih setelah panel ditutup.
- MUST NOT mengasumsikan `Open` selalu menampilkan panel dengan tinggi sama: variant `Search`, `Tags`, `Avatar leading`, dan `Dot leading` dapat berbeda dari `Default`.
- MUST mengikuti HSD/BRD untuk sumber opsi, single/multiple selection, opsi kosong, pencarian, dan aturan disabled.
- SHOULD menjaga interaksi keyboard, fokus, dan keterbacaan opsi.
- MUST NOT membuat search, multi-select, atau grouping opsi bila kebutuhan dan komponen tidak mendukung.

## 6. Date & Time Picker

**Main component:** https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1146-1678  
**Supporting components:** https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1146-1533

### 6.1 Main Component Properties

| Property | Nilai yang teridentifikasi |
|---|---|
| Type | `Default`, `Date Open`, `Time Open` |
| State | `Default`, `Disabled` (pada kombinasi yang terlihat) |

**Penting:** `Date Open` dan `Time Open` adalah **Type** pada komponen utama yang ditinjau, bukan State baru. Tidak ada dasar untuk menambahkan `Focused`, `Filled`, atau `Success` sebagai property State resmi komponen ini. `Disabled` yang teridentifikasi adalah `State=Disabled, Type=Default`; kombinasi lain tidak boleh diasumsikan tersedia.

### 6.2 Supporting Elements

| Element | Variasi/struktur terlihat | Peran |
|---|---|---|
| Calendar | Calendar component | Memilih tanggal |
| Day cell | `Selected`, `Today`, `default` | Penanda tanggal pada kalender |
| Select Time | `Version=Default`, `Version=V2` | Memilih waktu |
| Clock | `default`, `input` | Elemen pengaturan waktu |
| Time Type | `AM Selected`, `PM Selected` | Pilihan AM/PM bila pola tersebut digunakan |

Variant elemen pendukung bukan otomatis property milik komponen Date & Time Picker utama.

### 6.3 Context & Behavior Matrix

| Kebutuhan | Pola yang dipilih | Catatan |
|---|---|---|
| Input tanggal | Date picker / `Date Open` sesuai komponen | Calendar untuk memilih tanggal |
| Input jam | Time picker / `Time Open` sesuai komponen | Gunakan pola pemilihan waktu resmi |
| Input tanggal dan jam | Kombinasi Date & Time Picker yang didukung | Jangan menciptakan UI gabungan baru tanpa persetujuan |
| Input rentang tanggal | Pola/range yang benar-benar tersedia atau disetujui | Jangan mengasumsikan range picker otomatis tersedia |
| Input waktu manual | Mekanisme input yang didukung GEMS dan requirement | Jangan memaksa pemilihan otomatis/current time |

### 6.4 Date Rules

- MUST mengikuti HSD/BRD untuk format tanggal, tanggal minimum/maksimum, rentang, dan hari yang tidak dapat dipilih.
- MUST NOT membatasi tanggal lampau atau mendatang tanpa requirement.
- MUST NOT otomatis memilih tanggal hari ini tanpa requirement.
- MUST membedakan penanda `Today` dari `Selected` pada kalender.
- SHOULD menampilkan nilai tanggal terpilih dengan format yang konsisten.

### 6.5 Time Rules

- MUST mengikuti HSD/BRD untuk input jam, menit, dan format waktu.
- MUST NOT memaksa format 12 jam atau 24 jam tanpa dasar requirement dan pattern resmi.
- MUST NOT otomatis mengisi waktu saat ini tanpa requirement.
- MUST NOT menyimpulkan waktu kedatangan/keberangkatan dari tanggal saja.
- MUST mengikuti komponen GEMS ketika membutuhkan AM/PM, Clock, atau Select Time.
- MUST NOT membatasi jam yang dapat dipilih tanpa requirement.

### 6.6 Disabled & Open Behavior

- MUST menggunakan tampilan `Disabled` resmi jika interaksi tidak tersedia.
- MUST NOT memungkinkan perubahan nilai saat disabled.
- MUST menggunakan Type `Date Open` / `Time Open` yang relevan untuk kondisi picker terbuka.
- MUST NOT menambah state baru hanya untuk mendeskripsikan popup kalender atau jam.

## 7. Shared Validation & Error Handling

| Situation | Requirement | Rule |
|---|---|---|
| Field wajib kosong | HSD/BRD menetapkan required | Tampilkan pesan validasi yang spesifik |
| Format tidak sesuai | Ada format yang disyaratkan | Pertahankan nilai; jelaskan format yang benar |
| Nilai di luar batas | Ada batas dari requirement | Jelaskan batas yang diperbolehkan |
| Tanggal/jam tidak valid | Ada aturan tanggal/jam | Jelaskan apa yang harus diperbaiki |
| Error Input Field/Textarea | Property `Destructive` tersedia | Gunakan `Destructive=True` sesuai variant |
| Error Dropdown/Date & Time | Property error belum teridentifikasi pada referensi ini | Gunakan pattern validasi GEMS yang terverifikasi; jangan membuat property/visual baru |
| Validasi berhasil | Error selesai | Kembali ke tampilan normal; tanpa success border/icon baru |

**Contoh pesan (bukan aturan bisnis):** “Nama lengkap wajib diisi.”; “Pilih tanggal kunjungan.”; “Masukkan jam keberangkatan.”; “Pilih salah satu lokasi.”

- MUST NOT menghapus nilai pengguna karena error.
- MUST NOT mengubah data secara diam-diam.
- MUST NOT membuat `Success` State lintas komponen.
- SHOULD meletakkan pesan error dekat field dan menggunakan terminologi yang mudah dipahami.

## 8. Labels, Placeholder, Helper Text

- MUST menggunakan label yang spesifik dan konsisten dengan HSD/BRD.
- MUST NOT mengandalkan placeholder sebagai satu-satunya label field penting.
- SHOULD menggunakan placeholder singkat untuk contoh format, bukan paragraf instruksi.
- SHOULD menggunakan helper text untuk menjelaskan format atau konsekuensi yang tidak jelas.
- MUST mengikuti pattern required/optional GEMS dan requirement bisnis; jangan mengasumsikan field wajib.
- MUST menjaga pesan error tetap jelas dan dapat dihubungkan ke field terkait.

## 9. Contextual Input Patterns

| Case | Data | Recommended component | Important constraint |
|---|---|---|---|
| Registrasi | Nama | Input Field — Default | Required mengikuti HSD/BRD |
| Pencarian | Kata kunci bebas | Input Field — Icon leading atau Dropdown — Search | Bedakan free text dan pilihan daftar |
| Catatan | Uraian multiline | Textarea — Default | Jangan pakai single-line input |
| Form lokasi | Pilih lokasi | Dropdown — Default | Opsi dari sumber resmi |
| Form penanggung jawab | Pilih orang | Dropdown — Avatar leading jika cocok | Jangan membuat avatar wajib |
| Form kategori | Pilih beberapa kategori | Dropdown — Tags jika didukung | Multi-select harus ada dasar |
| Form nominal | Nilai berprefiks | Input Field — Leading text | Prefiks/format sesuai requirement |
| Form nomor telepon | Kode negara + nomor | Input Field — Leading dropdown | Hanya jika perlu kode negara |
| Jadwal kunjungan | Tanggal | Date & Time Picker — Date Open | Batas tanggal sesuai requirement |
| Jadwal transport | Jam berangkat | Date & Time Picker — Time Open | Jam tidak boleh diasumsikan dari tanggal |
| Akomodasi | Tanggal dan jam check-in | Date & Time Picker yang didukung | Boleh manual jika HSD/BRD mengharuskan |
| Periode laporan | Rentang tanggal | Pattern range yang telah disetujui | Jangan invent range picker |

Contoh hanya ilustratif; bukan persetujuan otomatis terhadap flow atau aturan bisnis tertentu.

## 10. Accessibility & Interaction

- MUST menjaga indikator fokus yang terlihat sesuai komponen GEMS.
- SHOULD mendukung navigasi keyboard dan pembacaan label/error yang dapat diakses.
- MUST membedakan field editable, disabled, dan error.
- MUST NOT mengandalkan warna saja untuk menjelaskan kesalahan bila pesan teks diperlukan.
- SHOULD menjaga urutan fokus yang logis dalam form dan popup.
- MUST mengikuti pattern interaksi komponen resmi, termasuk opsi Dropdown dan Calendar.

## 11. AI Selection Workflow

1. **Read HSD/BRD:** Identifikasi data, sumber opsi, required/optional, hak akses, format, rentang, dan alur.
2. **Select family:** Pilih Input Field, Textarea, Dropdown, atau Date & Time Picker.
3. **Select official Type:** Gunakan nama Type yang benar-benar tersedia pada komponen terpilih.
4. **Select supported properties:** Gunakan hanya Size, State, Destructive, atau Type yang ada pada keluarga komponen itu.
5. **Apply contextual behavior:** Tentukan input bebas vs pilihan, tanggal vs jam, single vs multi, serta interaksi disabled berdasarkan requirement.
6. **Apply validation:** Gunakan visual error resmi yang terverifikasi; jangan menyamakan semua komponen.
7. **Check Figma:** Verifikasi instance, struktur, visual, dan behavior terhadap referensi resmi.
8. **Escalate:** Jika komponen/variant/flow tidak tersedia atau ambigu, minta Human Approval sebelum implementasi.

## 12. AI Restrictions

AI MUST NOT:

1. Menciptakan Type, State, Size, atau property baru tanpa Human Approval.
2. Menganggap `Filled` pada Input Field berlaku untuk Textarea, Dropdown, atau Date & Time Picker.
3. Menganggap `Open` pada Dropdown adalah state semua input.
4. Menganggap `Date Open`/`Time Open` adalah State, padahal tercatat sebagai Type pada komponen utama.
5. Menambahkan Success State, border hijau, atau check icon untuk nilai valid.
6. Menambahkan `Destructive` pada komponen yang belum terverifikasi memiliki property tersebut.
7. Menentukan format, required, batas karakter, tanggal, atau waktu tanpa dasar HSD/BRD.
8. Mengisi tanggal/jam saat ini secara otomatis tanpa requirement.
9. Menghapus atau mengubah nilai pengguna diam-diam setelah validasi.
10. Mengubah business flow, user flow, hak akses, atau aturan approval tanpa persetujuan manusia berwenang.
11. Menganggap semua contoh kontekstual sebagai ketentuan wajib.
12. Menggunakan file placeholder sebagai sumber guideline yang sudah disetujui.

## 13. Official Figma References

| Family | Reference |
|---|---|
| Input Field | https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=219-5292 |
| Textarea Input Field | https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-4425 |
| Input Dropdown | https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-4695 |
| Date & Time Picker | https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1146-1678 |
| Date & Time supporting elements | https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1146-1533 |

**Implementation requirement:** HSD/BRD governs business requirements; GEMS governs design component variants and visuals; proposed new flows or component behaviors require authorized Human Approval.
