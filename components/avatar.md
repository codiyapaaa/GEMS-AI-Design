# Avatar — GEMS AI Design Guidelines

## 1. Purpose & Core Principles


Avatar merupakan komponen identitas visual yang digunakan untuk merepresentasikan individu melalui foto profil, inisial nama, atau placeholder.

Komponen Avatar digunakan untuk mempermudah identifikasi pengguna pada berbagai konteks antarmuka, seperti Data Table, List, Card, Header, Profile, Notification, dan kelompok anggota.

Dalam GEMS Design System, Avatar terdiri dari beberapa jenis komponen yang memiliki fungsi, ukuran, dan variasi masing-masing.

**Tujuan penggunaan:**

- Mempermudah identifikasi individu.
- Menampilkan identitas pengguna secara konsisten.
- Mendukung representasi identitas ketika foto tidak tersedia.
- Memperkuat informasi nama pada tabel, daftar, dan kartu.
- Mendukung tampilan identitas individu maupun kelompok.
- Menampilkan atribut identitas apabila diperlukan.

**Aturan utama:**

- AI MUST menggunakan komponen Avatar resmi GEMS Design System.
- AI MUST menentukan penggunaan Avatar berdasarkan konteks UI dan kebutuhan HSD/BRD.
- AI MUST menggunakan variant dan ukuran yang tersedia pada GEMS.
- AI MUST NOT membuat komponen Avatar baru apabila komponen resmi sudah tersedia.
- AI MUST NOT menggunakan Avatar sebagai elemen dekoratif tanpa fungsi identitas.

---

## 2. Component Types

GEMS Design System menyediakan beberapa jenis komponen Avatar.

| Component | Description | Usage |
|---|---|---|
| Avatar | Komponen identitas individu | Tabel, daftar, header, identitas pengguna |
| Avatar Label Group | Avatar dengan informasi teks | Nama pengguna, PIC, anggota, identitas pada list/card |
| Avatar Group | Kumpulan beberapa Avatar | Anggota tim, peserta, kolaborator |
| Avatar Profile Photo | Foto profil dengan ukuran lebih besar | Halaman profil dan detail pengguna |
| Avatar Image | Aset gambar internal Avatar | Pengaturan sumber gambar Avatar |
| Avatar Add Button | Kontrol menambahkan anggota | Daftar anggota dan kelompok pengguna |

### Component Selection Rules

- AI MUST memilih jenis komponen berdasarkan kebutuhan informasi.
- AI SHOULD menggunakan Avatar Label Group ketika identitas perlu ditampilkan bersama nama.
- AI MUST menggunakan Avatar Group ketika desain membutuhkan representasi beberapa anggota dalam satu kelompok.
- AI SHOULD menggunakan Avatar Profile Photo untuk identitas utama pada halaman profil.
- AI MUST menggunakan Avatar Add Button hanya untuk tindakan penambahan anggota.
- AI MUST NOT menggunakan Avatar Image sebagai pengganti komponen Avatar utama tanpa alasan teknis yang sesuai.

---

## 3. Component Properties & Variants

### 3.1 Avatar

| Property | Available Values |
|---|---|
| Size | `xs`, `sm`, `md`, `lg`, `xl`, `2xl` |
| Placeholder | `True`, `False` |
| Text | `True`, `False` |
| Status icon | `False`, `Online indicator`, `Company`, `Verified` |

**Ukuran resmi:**

| Size | Dimension |
|---|---|
| `xs` | 24 × 24 px |
| `sm` | 32 × 32 px |
| `md` | 40 × 40 px |
| `lg` | 48 × 48 px |
| `xl` | 56 × 56 px |
| `2xl` | 64 × 64 px |

**Kombinasi tampilan yang didukung:**

| Placeholder | Text | Status icon |
|---|---|---|
| `False` | `False` | False, Online indicator, Company, Verified |
| `False` | `True` | False, Online indicator, Company |
| `True` | `False` | False, Online indicator, Company |

Kombinasi di atas mengikuti variasi yang teridentifikasi pada komponen GEMS. AI MUST memverifikasi variant aktual sebelum implementasi.

### 3.2 Avatar Label Group

| Property | Available Values |
|---|---|
| Size | `sm`, `md`, `lg`, `xl` |
| Status icon | `False`, `Online indicator`, `Company`, `Verified` |

Komponen ini digunakan ketika Avatar dan informasi nama ditampilkan sebagai satu kesatuan.

### 3.3 Avatar Group

| Property | Available Values |
|---|---|
| Size | `xs`, `sm`, `md` |

Komponen ini digunakan untuk menampilkan beberapa identitas dalam ruang terbatas.

### 3.4 Avatar Profile Photo

| Property | Available Values |
|---|---|
| Size | `sm`, `md`, `lg` |
| Placeholder | `True`, `False` |
| Text | `True`, `False`, sesuai kombinasi resmi |

**Ukuran resmi:**

| Size | Dimension |
|---|---|
| `sm` | 72 × 72 px |
| `md` | 96 × 96 px |
| `lg` | 160 × 160 px |

**Kombinasi yang tersedia:**

- Foto: `Placeholder=False`, `Text=False`
- Placeholder tanpa inisial: `Placeholder=True`, `Text=False`
- Placeholder dengan inisial: `Placeholder=True`, `Text=True`

### 3.5 Avatar Image

| Property | Available Values |
|---|---|
| Type | `Square`, `Portrait` |

### 3.6 Avatar Add Button

| Property | Available Values |
|---|---|
| Size | `xs`, `sm`, `md` |
| State | `Default`, `Hover`, `Focus`, `Disabled` |

**Ukuran resmi:**

| Size | Dimension |
|---|---|
| `xs` | 24 × 24 px |
| `sm` | 32 × 32 px |
| `md` | 40 × 40 px |

**Aturan:**

- AI MUST menggunakan properti dan nilai yang tersedia.
- AI MUST NOT menggabungkan property menjadi kombinasi yang tidak didukung.
- AI MUST NOT membuat ukuran, warna, atau state tambahan tanpa persetujuan.

---

## 4. When to Use

### 4.1 Data Table — Web

Gunakan Avatar pada kolom yang merepresentasikan identitas individu.

**Contoh penggunaan:**

- Nama Pengguna
- Nama Karyawan
- Nama Penanggung Jawab
- Nama Anggota
- Nama Individu lainnya

**Pola yang dianjurkan:**

`Avatar + Nama`

**Aturan:**

- AI SHOULD memprioritaskan Avatar + Nama untuk kolom identitas individu.
- AI MUST menampilkan nama sebagai teks utama.
- AI MUST menjaga ukuran dan alignment Avatar konsisten pada seluruh baris.
- AI MUST mengikuti pola Data Table GEMS jika telah ditentukan.
- AI MUST NOT menambahkan Avatar pada kolom nama dokumen, lokasi, atau kategori.

### 4.2 List & Card — Web

Gunakan Avatar ketika daftar atau kartu menampilkan informasi individu.

**Contoh penggunaan:**

- Daftar pengguna.
- Daftar anggota.
- Kartu penanggung jawab.
- Informasi pemilik aktivitas.

**Pola yang dianjurkan:**

`Avatar + Nama + Informasi Pendukung`

**Aturan:**

- AI SHOULD menggunakan Avatar Label Group jika struktur komponen sesuai.
- AI MUST mempertahankan nama sebagai informasi utama.
- AI MUST NOT menambahkan informasi pendukung yang tidak tersedia.

### 4.3 List & Card — Mobile

Gunakan Avatar pada daftar atau kartu Mobile yang menampilkan identitas individu.

**Contoh penggunaan:**

- Daftar pengguna.
- Daftar peserta.
- Daftar penanggung jawab.
- Kartu identitas.
- Riwayat aktivitas individu.

**Pola yang dianjurkan:**

`Avatar + Nama + Informasi Pendukung`

**Aturan:**

- AI SHOULD memprioritaskan Avatar + Nama pada list/card individu.
- AI MUST menjaga keterbacaan nama pada layar kecil.
- AI MUST menggunakan ukuran resmi yang sesuai dengan kepadatan tampilan.
- AI MUST mempertahankan fallback foto.
- AI MUST NOT menghilangkan nama penting untuk memberikan ruang pada Avatar.
- AI MUST mengikuti layout Mobile resmi apabila telah ditentukan.

### 4.4 Header & Account Menu

Gunakan Avatar untuk menampilkan identitas akun aktif.

**Pola:**

`Avatar` atau `Avatar + Nama`

**Aturan:**

- AI MUST menggunakan identitas akun aktif.
- AI MUST mempertahankan fallback.
- AI MUST NOT menjadikan Avatar clickable tanpa fungsi yang ditentukan.

### 4.5 Profile & Detail Page

Gunakan Avatar Profile Photo ketika identitas pengguna menjadi elemen utama.

**Aturan:**

- AI SHOULD menggunakan Avatar Profile Photo untuk foto profil berukuran besar.
- AI MUST menggunakan foto valid atau fallback.
- AI MUST NOT menambahkan fitur unggah atau ubah foto tanpa requirement.

### 4.6 Team & Member Group

Gunakan Avatar Group ketika beberapa individu ditampilkan sebagai satu kelompok.

**Aturan:**

- AI MUST menggunakan data anggota yang valid.
- AI MUST mengikuti susunan dan spacing resmi GEMS.
- AI MUST NOT menambahkan anggota fiktif.
- AI MUST NOT membuat pola overflow baru tanpa persetujuan.

### 4.7 Activity & Notification

Gunakan Avatar apabila aktivitas atau pemberitahuan memiliki identitas individu yang relevan.

**Aturan:**

- AI MUST menggunakan identitas pelaku atau pengirim yang sesuai.
- AI MUST NOT menambahkan Avatar pada notifikasi sistem yang tidak membutuhkan identitas individu.
- AI MUST mengikuti komponen Notification resmi GEMS.

### 4.8 Member Addition

Gunakan Avatar Add Button ketika pengguna dapat menambahkan anggota.

**Aturan:**

- AI MUST menggunakan Avatar Add Button resmi.
- AI MUST mengikuti hak akses.
- AI MUST NOT menggunakan komponen ini sebagai tombol tambah umum.

---

## 5. When NOT to Use

Avatar tidak digunakan ketika informasi tidak membutuhkan identitas visual individu.

| Context | Reason | Alternative |
|---|---|---|
| Status proses | Bukan identitas individu | Badge |
| Pesan kesalahan | Merupakan feedback sistem | Alert / Notification |
| Nama dokumen | Bukan identitas individu | Teks / Icon |
| Nama lokasi | Bukan identitas individu | Teks / Icon |
| Navigasi | Tidak merepresentasikan identitas | Icon |
| Ilustrasi | Bukan identitas pengguna | Image |
| Tambah data umum | Tidak berkaitan dengan anggota | Button |

**AI Rules:**

- AI MUST NOT menggunakan Avatar hanya karena terdapat teks nama.
- AI MUST membedakan nama individu dan nama objek.
- AI MUST NOT menggantikan Badge, Icon, Button, atau Notification dengan Avatar.
- AI MUST NOT menambahkan Avatar tanpa kebutuhan identitas yang jelas.

---

## 6. Content States & Fallback

Avatar memiliki beberapa kondisi berdasarkan ketersediaan foto dan nama.

### 6.1 Image Available

**Kondisi:** Foto profil tersedia dan valid.

**Tampilan:** Avatar menampilkan foto profil.

**Aturan:**

- AI MUST menggunakan foto yang sesuai dengan identitas.
- AI MUST mempertahankan proporsi gambar.
- AI MUST menyediakan fallback jika gambar gagal dimuat.

### 6.2 Image Unavailable — Initials Available

**Kondisi:** Foto tidak tersedia, tetapi nama valid tersedia.

**Tampilan:** Avatar menampilkan inisial nama.

**Contoh:**

| Nama | Inisial |
|---|---|
| Amanda Aprilia | AA |
| Muhammad Yusron | MY |
| Silvia | S |

**Aturan:**

- AI SHOULD menggunakan maksimal dua inisial.
- AI SHOULD menggunakan huruf pertama nama pertama dan terakhir.
- AI MUST menggunakan data nama yang valid.
- AI MUST menjaga konsistensi format.

### 6.3 Image & Name Unavailable

**Kondisi:** Foto dan nama valid tidak tersedia.

**Tampilan:** Avatar menggunakan placeholder resmi GEMS.

**Aturan:**

- AI MUST menggunakan placeholder resmi.
- AI MUST NOT menggunakan gambar acak.
- AI MUST NOT menampilkan broken image atau nilai `null`.

### 6.4 Image Loading

**Kondisi:** Foto sedang dimuat.

**Perilaku:**

- Ukuran container tetap stabil.
- Gunakan fallback atau loading treatment yang telah disetujui.
- Tampilkan foto setelah berhasil dimuat.

**Aturan:**

- AI MUST menjaga layout agar tidak bergeser.
- AI MUST NOT membuat loading variant baru jika tidak tersedia pada GEMS.

### 6.5 Image Error

**Kondisi:** Foto gagal dimuat.

**Perilaku:**

- Gunakan inisial jika nama tersedia.
- Gunakan placeholder jika nama tidak tersedia.
- Jangan menampilkan broken image.

### 6.6 Fallback Priority

| Priority | Condition | Display |
|---|---|---|
| 1 | Foto valid tersedia | Image |
| 2 | Foto tidak tersedia, nama valid | Initials |
| 3 | Foto dan nama tidak tersedia | Placeholder |

**AI MUST menggunakan urutan fallback ini secara konsisten pada Web dan Mobile**, kecuali terdapat aturan produk yang telah disetujui.

---

## 7. Status Indicators

Avatar dapat menampilkan indikator atribut identitas menggunakan variasi resmi GEMS.

| Indicator | Usage |
|---|---|
| `False` | Tidak menampilkan indikator |
| `Online indicator` | Menampilkan status online |
| `Company` | Menampilkan atribut perusahaan |
| `Verified` | Menampilkan status verifikasi |

### Usage Rules

- AI MUST menggunakan indikator berdasarkan data aktual.
- AI MUST NOT menampilkan Online indicator tanpa informasi presence.
- AI MUST NOT menampilkan Verified tanpa status verifikasi.
- AI MUST NOT menambahkan Company indicator tanpa kebutuhan.
- AI MUST NOT menggunakan status indicator sebagai pengganti Badge untuk status workflow.
- AI MUST menggunakan kombinasi indicator yang didukung oleh variant GEMS.

**Catatan:** Pada Avatar utama, variasi `Verified` yang teridentifikasi tersedia pada Avatar bergambar. AI tidak boleh mengasumsikan bahwa indikator ini tersedia pada seluruh kondisi inisial atau placeholder.

---

## 8. Interaction States & Behavior

### 8.1 Static Avatar

Avatar digunakan hanya untuk menampilkan identitas.

**Behavior:**

- Tidak memiliki aksi.
- Tidak membuka halaman.
- Tidak memberikan affordance seolah dapat diklik.

### 8.2 Interactive Avatar

Avatar dapat digunakan sebagai pemicu navigasi jika kebutuhan sistem secara eksplisit mengharuskannya.

**Behavior:**

- Membuka profil atau detail yang relevan.
- Mendukung keyboard.
- Menampilkan fokus sesuai pola interaksi yang disetujui.

**Rules:**

- AI MUST NOT menjadikan semua Avatar clickable.
- AI MUST memiliki tujuan interaksi yang jelas.
- AI MUST menggunakan pola interaksi resmi yang tersedia.
- AI MUST NOT membuat navigasi tanpa requirement.

### 8.3 Avatar Add Button States

| State | Behavior |
|---|---|
| `Default` | Kontrol siap digunakan |
| `Hover` | Memberikan feedback saat pointer diarahkan |
| `Focus` | Menampilkan indikator fokus |
| `Disabled` | Tidak dapat digunakan |

**Rules:**

- AI MUST menggunakan state resmi GEMS.
- AI MUST mengikuti permission pengguna.
- AI MUST menyediakan accessible name.
- AI MUST NOT membuat state tambahan tanpa persetujuan.

---

## 9. Layout & Responsive Guidelines

### 9.1 Web

- AI MUST menggunakan ukuran Avatar sesuai kepadatan tampilan.
- AI MUST menjaga alignment dengan nama.
- AI MUST menjaga konsistensi ukuran antarbaris tabel.
- AI MUST mengikuti spacing dan layout resmi GEMS.

### 9.2 Mobile

- AI MUST mempertimbangkan Avatar pada list/card yang merepresentasikan individu.
- AI MUST menjaga nama tetap terbaca.
- AI MUST menggunakan ukuran resmi yang sesuai.
- AI MUST mempertahankan fallback.
- AI MUST memastikan kontrol interaktif tetap mudah digunakan.

### 9.3 Cross-Platform Consistency

- Identitas yang sama harus menggunakan sumber foto dan nama yang sama.
- Fallback harus konsisten.
- Ukuran dapat berbeda berdasarkan layout.
- Status indicator mengikuti data yang sama.
- AI MUST NOT mengubah representasi identitas hanya karena perbedaan platform.

---

## 10. Accessibility Guidelines

### 10.1 Visual Accessibility

- AI MUST menjaga kontras inisial.
- AI MUST menjaga keterbacaan nama.
- AI MUST NOT mengandalkan foto sebagai satu-satunya informasi identitas.
- AI MUST NOT mengandalkan warna status saja.

### 10.2 Screen Reader

- Avatar informatif harus memiliki representasi teks yang sesuai.
- Jika nama sudah ditampilkan sebagai teks, hindari pembacaan nama yang berulang.
- Avatar dekoratif dalam komponen identitas dapat disembunyikan dari pembaca layar jika nama sudah tersedia.
- Avatar interaktif harus memiliki nama aksesibel.

### 10.3 Keyboard Accessibility

- Avatar interaktif harus dapat diakses dengan keyboard.
- Fokus harus terlihat.
- Avatar statis tidak boleh menerima fokus tanpa kebutuhan.
- Avatar Add Button harus memiliki label tindakan yang jelas.

### 10.4 Status Accessibility

- Makna indikator harus dapat dipahami tanpa hanya mengandalkan warna.
- Informasi status harus tersedia dalam bentuk yang dapat diakses.

---

## 11. AI Decision Logic

AI harus mengikuti urutan keputusan berikut ketika menentukan penggunaan Avatar.

### Step 1 — Identify Identity Context

Periksa apakah data merepresentasikan individu atau kelompok individu.

- Jika ya, lanjutkan evaluasi Avatar.
- Jika tidak, gunakan komponen lain yang sesuai.

### Step 2 — Identify UI Context

| UI Context | Recommended Component |
|---|---|
| Web Data Table — Person Name | Avatar + Nama |
| Web User List | Avatar Label Group |
| Web Person Card | Avatar Label Group |
| Mobile Person List | Avatar Label Group |
| Mobile Person Card | Avatar Label Group |
| Header / Account Menu | Avatar |
| Profile / Detail | Avatar Profile Photo |
| Multiple Members | Avatar Group |
| Add Member | Avatar Add Button |

### Step 3 — Select Official Variant

- Periksa jenis komponen.
- Periksa ukuran yang tersedia.
- Periksa kombinasi property.
- Periksa indikator yang didukung.
- Jangan membuat variasi baru.

### Step 4 — Determine Avatar Content

| Condition | Display |
|---|---|
| Foto valid tersedia | Image |
| Foto tidak tersedia, nama valid | Initials |
| Foto dan nama tidak tersedia | Placeholder |
| Foto gagal dimuat, nama valid | Initials |
| Foto gagal dimuat, nama tidak tersedia | Placeholder |

### Step 5 — Determine Interaction

- Jika hanya menampilkan identitas, gunakan Static Avatar.
- Jika membuka profil, gunakan pola interaktif yang didukung.
- Jika menambahkan anggota, gunakan Avatar Add Button.
- Jika tidak ada kebutuhan interaksi, jangan membuat Avatar clickable.

### Step 6 — Validate Output

Sebelum menghasilkan desain, AI MUST memeriksa:

1. Kesesuaian komponen dengan GEMS.
2. Kesesuaian penggunaan dengan HSD/BRD.
3. Ukuran dan variant resmi.
4. Kebenaran identitas.
5. Fallback foto.
6. Kesesuaian status indicator.
7. Kesesuaian Web/Mobile.
8. Aksesibilitas.
9. Kebutuhan interaksi dan permission.

---

## 12. AI Implementation Rules

### 12.1 Mandatory Rules

AI MUST:

1. Menggunakan komponen Avatar resmi GEMS Design System.
2. Memilih jenis Avatar sesuai konteks.
3. Memprioritaskan Avatar + Nama pada kolom identitas individu di tabel Web jika sesuai dengan pola GEMS.
4. Mempertimbangkan Avatar + Nama pada list/card Mobile yang menampilkan individu.
5. Menggunakan ukuran dan variasi resmi.
6. Menggunakan identitas yang sesuai dengan data.
7. Menyediakan fallback ketika foto tidak tersedia.
8. Menggunakan indikator berdasarkan data valid.
9. Menjaga konsistensi Web dan Mobile.
10. Memenuhi kebutuhan aksesibilitas.
11. Mengikuti HSD/BRD dan permission sistem.
12. Meminta persetujuan untuk pola baru yang belum didukung.

### 12.2 Prohibited Rules

AI MUST NOT:

1. Membuat komponen Avatar custom tanpa persetujuan.
2. Menggunakan ukuran di luar GEMS.
3. Membuat kombinasi property yang tidak tersedia.
4. Membuat foto pengguna nyata secara fiktif.
5. Menggunakan gambar individu yang tidak sesuai.
6. Menampilkan gambar rusak.
7. Menghilangkan fallback.
8. Menampilkan status tanpa data valid.
9. Menggunakan Avatar untuk menggantikan status workflow.
10. Menjadikan semua Avatar clickable.
11. Membuat interaksi baru tanpa requirement.
12. Menggunakan Avatar Add Button sebagai tombol tambah umum.
13. Menambahkan anggota fiktif pada Avatar Group.
14. Membuat pola overflow baru tanpa persetujuan.
15. Menghilangkan nama penting hanya untuk menampilkan foto.
16. Mengabaikan pola identitas pada Mobile.
17. Menggunakan Avatar untuk data nonindividu tanpa kebutuhan identitas yang relevan.

### 12.3 Source of Truth

| Source | Responsibility |
|---|---|
| GEMS Design System | Komponen, variant, ukuran, state, dan spesifikasi visual |
| HSD / BRD | Kebutuhan identitas, alur bisnis, data, dan permission |
| System Data | Foto, nama, status, dan atribut identitas aktual |
| Human Approval | Persetujuan perubahan atau penambahan pola yang belum didukung |

### 12.4 Final AI Instruction

AI MUST menggunakan komponen Avatar resmi GEMS Design System ketika desain membutuhkan representasi identitas individu atau kelompok.

Untuk tabel Web yang menampilkan nama individu, AI SHOULD memprioritaskan pola Avatar + Nama. Untuk daftar dan kartu Mobile yang menampilkan identitas individu, AI SHOULD mempertimbangkan pola yang sama.

AI MUST memilih komponen berdasarkan konteks, menggunakan variant resmi, menjaga keterbacaan nama, menerapkan fallback foto, serta mempertahankan konsistensi pada Web dan Mobile.

AI MUST NOT membuat komponen, variant, state, ukuran, atau interaksi baru di luar GEMS tanpa persetujuan manusia yang berwenang.

---

## 13. Official GEMS Design System — Component Specifications

| Component | Official GEMS Component |
|---|---|
| Avatar | [GEMS Avatar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-3857) |
| Avatar Group | [GEMS Avatar Group](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-30704) |
| Avatar Label Group | [GEMS Avatar Label Group](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-30580) |
| Avatar Profile Photo | [GEMS Avatar Profile Photo](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-30661) |
| Avatar Image | [GEMS Avatar Image](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-4089) |
| Avatar Add Button | [GEMS Avatar Add Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-4120) |
