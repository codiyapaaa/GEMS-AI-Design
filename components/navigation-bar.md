# GEMS Design System — Navigation Bar Guidelines

## 1. Purpose

Navigation Bar (Navbar) merupakan komponen navigasi yang membantu pengguna mengakses informasi, fitur, atau tindakan pada bagian atas aplikasi.

Navbar merupakan bagian dari struktur navigasi aplikasi dan harus memiliki hubungan yang konsisten dengan Sidebar, konten halaman, serta navigasi lainnya.

**Core Principle:**

> AI MUST menggunakan komponen Navbar resmi GEMS Design System. AI MUST memilih konfigurasi resmi berdasarkan status Navbar dan Sidebar, serta mempertahankan seluruh visual properties dan interaction patterns yang tersedia.

### 1.1 Mandatory Design System Compliance

AI MUST:

1. Menggunakan instance Navbar resmi GEMS.
2. Memilih variant dan component properties resmi.
3. Mempertahankan struktur komponen.
4. Menggunakan typography, warna, spacing, dan ukuran resmi.
5. Menggunakan Icon dan Button resmi GEMS.
6. Mengikuti layout dan interaction patterns GEMS.
7. Menyesuaikan konfigurasi dengan kondisi Sidebar.
8. Mengikuti HSD/BRD untuk menentukan konten dan tindakan.
9. Memastikan konsistensi Navbar pada seluruh halaman yang menggunakan layout serupa.

AI MUST NOT:

1. Membuat Navbar custom jika komponen resmi tersedia.
2. Menggunakan Navbar dari library lain.
3. Mengganti instance resmi dengan Frame custom.
4. Membuat variant baru tanpa Human Approval.
5. Mengubah typography, warna, spacing, atau ukuran di luar GEMS.
6. Mengubah struktur internal komponen secara manual.
7. Membuat Icon atau Button custom.
8. Mengabaikan hubungan Navbar dengan Sidebar.

---

## 2. Official Navbar Variants

### 2.1 Verified Component Properties

Berdasarkan metadata GEMS Design System, Navbar memiliki dua properties:

| Property | Available Values |
|---|---|
| Open | true, false |
| Sidebar | Open, Closed |

Tersedia empat konfigurasi resmi:

| Configuration | Open | Sidebar |
|---|---|---|
| 1 | true | Open |
| 2 | true | Closed |
| 3 | false | Open |
| 4 | false | Closed |

### 2.2 Open Property

**Property:** `Open`

Available values:

- `true`
- `false`

Property ini mengontrol salah satu kondisi internal Navbar sesuai definisi komponen resmi.

**Rules:**

- MUST menggunakan nilai Boolean resmi.
- MUST mengikuti kondisi komponen yang sedang digunakan.
- MUST mempertahankan visual sesuai variant.
- MUST NOT mengubah nilai tanpa alasan interaksi yang valid.
- MUST NOT mengasumsikan bahwa `Open` selalu berarti Sidebar terbuka.

**Important:**

Makna detail `Open` harus diverifikasi melalui struktur dan prototype komponen GEMS.

AI MUST NOT mengasumsikan bahwa property tersebut mengontrol dropdown, notification panel, atau menu lainnya tanpa bukti dari komponen.

### 2.3 Sidebar Property

**Property:** `Sidebar`

Available values:

- `Open`
- `Closed`

Property ini menentukan konfigurasi Navbar berdasarkan kondisi Sidebar.

**Rules:**

- MUST menggunakan `Sidebar=Open` ketika Sidebar berada dalam kondisi terbuka.
- MUST menggunakan `Sidebar=Closed` ketika Sidebar berada dalam kondisi tertutup.
- MUST menjaga kesesuaian Navbar dan Sidebar.
- MUST mengikuti layout resmi untuk setiap konfigurasi.
- MUST NOT membuat konfigurasi Sidebar baru.

### 2.4 Variant Selection Rules

AI MUST:

1. Mengidentifikasi kondisi Navbar.
2. Mengidentifikasi kondisi Sidebar.
3. Memilih kombinasi properties yang sesuai.
4. Menggunakan instance resmi.
5. Mempertahankan visual dan layout GEMS.

AI MUST NOT:

1. Menggabungkan struktur dari dua variant secara manual.
2. Membuat layout baru untuk kondisi Sidebar.
3. Mengubah ukuran Navbar tanpa acuan resmi.
4. Menggunakan variant yang tidak sesuai dengan kondisi aplikasi.

---

## 3. When to Use Navbar

### 3.1 Recommended Usage

Navbar SHOULD digunakan ketika:

1. Aplikasi menggunakan layout dengan navigasi bagian atas.
2. Pengguna membutuhkan akses ke navigasi atau tindakan global.
3. Halaman merupakan bagian dari aplikasi yang menggunakan Navbar sebagai struktur utama.
4. Aplikasi menggunakan Sidebar dan Navbar secara bersamaan.
5. Pengguna berpindah antarmodul dalam struktur aplikasi yang sama.
6. Halaman membutuhkan konsistensi navigasi dengan halaman lainnya.

### 3.2 Usage Matrix

| Page Context | Recommendation |
|---|---|
| Main Dashboard | Use Navbar jika merupakan bagian dari App Shell |
| Management List | Use Navbar |
| Detail Page | Use Navbar |
| Create Data Page | Use Navbar jika menggunakan layout aplikasi utama |
| Edit Data Page | Use Navbar jika menggunakan layout aplikasi utama |
| Report Page | Use Navbar |
| Settings Page | Use Navbar jika menggunakan layout aplikasi utama |
| Authentication Page | Follow dedicated authentication layout |
| Full-screen Modal | Do not create additional Navbar |
| Standalone Public Page | Follow approved page layout |

### 3.3 Mandatory Usage Conditions

AI MUST menggunakan Navbar ketika:

- Layout resmi aplikasi menggunakan Navbar.
- HSD/BRD atau approved design mengharuskan Navbar.
- Halaman berada dalam struktur App Shell yang menggunakan Navbar.
- Pattern halaman lain dalam modul yang sama menggunakan Navbar secara konsisten.

AI MUST NOT menghilangkan Navbar dari halaman yang menggunakan App Shell resmi tanpa persetujuan.

---

## 4. When NOT to Use Navbar

Navbar SHOULD NOT ditambahkan ketika:

1. Halaman menggunakan layout khusus tanpa Navbar.
2. Halaman Login menggunakan authentication layout tersendiri.
3. Halaman merupakan bagian dari Modal.
4. Komponen berada di dalam Card atau Table.
5. Konten merupakan bagian dari dialog atau overlay.
6. Navbar tidak diperlukan berdasarkan struktur navigasi aplikasi.

### Rules

AI MUST NOT:

1. Menambahkan Navbar pada setiap Frame.
2. Membuat Navbar kedua di dalam halaman.
3. Menggunakan Navbar sebagai Tabs.
4. Menggunakan Navbar sebagai Breadcrumbs.
5. Menggunakan Navbar sebagai Sidebar.
6. Menggunakan Navbar sebagai toolbar tabel.
7. Menggunakan Navbar hanya untuk dekorasi.

---

## 5. Navbar Component Anatomy

### 5.1 General Structure

Struktur internal Navbar MUST mengikuti instance resmi GEMS.

Elemen berikut perlu diperiksa sebelum implementasi:

| Element | Usage Rule |
|---|---|
| Navbar Container | MUST menggunakan container resmi |
| Navigation Elements | MUST mengikuti struktur resmi |
| Icons | MUST menggunakan ikon GEMS |
| Buttons | MUST menggunakan Button GEMS |
| Interactive Controls | MUST mengikuti komponen dan state resmi |
| Sidebar Integration | MUST mengikuti konfigurasi Sidebar |
| Responsive Layout | MUST mengikuti pattern GEMS |

Daftar tersebut merupakan checklist pemeriksaan, bukan klaim bahwa seluruh elemen selalu tersedia pada setiap variant.

### 5.2 Navbar Container

AI MUST:

- Menggunakan container resmi.
- Mempertahankan height dan width behavior sesuai GEMS.
- Menggunakan background dan border resmi.
- Mempertahankan padding dan spacing.
- Mengikuti alignment resmi.

AI MUST NOT:

- Membuat container baru.
- Mengubah height secara manual.
- Mengubah background custom.
- Mengubah radius atau shadow di luar GEMS.

### 5.3 Icons & Interactive Elements

AI MUST:

- Menggunakan ikon resmi.
- Menggunakan Button resmi.
- Menggunakan state resmi pada elemen interaktif.
- Mempertahankan ukuran dan posisi sesuai komponen.
- Mengikuti interaction behavior yang tersedia.

AI MUST NOT:

- Menggunakan ikon dari library lain.
- Membuat tombol custom.
- Mengubah icon size tanpa acuan.
- Membuat hover atau active styling baru.

---

## 6. Navbar States

### 6.1 Official Configuration States

Empat kombinasi berikut sudah terverifikasi dari metadata Figma.

| State | Configuration | Expected Usage |
|---|---|---|
| A | Open=true, Sidebar=Open | Navbar pada kondisi Open dengan Sidebar terbuka |
| B | Open=true, Sidebar=Closed | Navbar pada kondisi Open dengan Sidebar tertutup |
| C | Open=false, Sidebar=Open | Navbar pada kondisi non-Open dengan Sidebar terbuka |
| D | Open=false, Sidebar=Closed | Navbar pada kondisi non-Open dengan Sidebar tertutup |

### 6.2 State A — Open=true, Sidebar=Open

AI MUST:

1. Menggunakan konfigurasi resmi.
2. Mempertahankan tampilan Navbar pada kondisi `Open=true`.
3. Menggunakan layout untuk Sidebar terbuka.
4. Mempertahankan posisi dan alignment resmi.
5. Menjaga konsistensi dengan kondisi Sidebar.

AI MUST NOT:

- Menggunakan layout Sidebar tertutup.
- Membuat konfigurasi baru.
- Mengubah visual properties secara manual.

### 6.3 State B — Open=true, Sidebar=Closed

AI MUST:

1. Menggunakan konfigurasi resmi.
2. Mempertahankan tampilan `Open=true`.
3. Menggunakan layout untuk Sidebar tertutup.
4. Menjaga konsistensi dengan kondisi Sidebar.
5. Menggunakan ukuran dan spacing resmi.

AI MUST NOT:

- Mempertahankan layout Sidebar terbuka.
- Membuat penyesuaian posisi custom.
- Mengubah komponen secara manual.

### 6.4 State C — Open=false, Sidebar=Open

AI MUST:

1. Menggunakan konfigurasi resmi.
2. Mempertahankan tampilan `Open=false`.
3. Menggunakan layout Sidebar terbuka.
4. Mempertahankan struktur Navbar.
5. Menggunakan visual properties resmi.

AI MUST NOT:

- Menggunakan konfigurasi `Open=true`.
- Mengubah visual state secara manual.
- Menggunakan layout Sidebar tertutup.

### 6.5 State D — Open=false, Sidebar=Closed

AI MUST:

1. Menggunakan konfigurasi resmi.
2. Mempertahankan tampilan `Open=false`.
3. Menggunakan layout Sidebar tertutup.
4. Menjaga konsistensi struktur navigasi.
5. Mengikuti alignment dan spacing resmi.

AI MUST NOT:

- Membuat variant baru.
- Menggunakan layout Sidebar terbuka.
- Mengubah visual properties di luar GEMS.

---

## 7. Interactive Element States

Selain konfigurasi Navbar, elemen interaktif di dalamnya dapat memiliki state masing-masing.

Ketersediaan visual state berikut MUST diperiksa pada komponen pendukung resmi.

### 7.1 Interaction State Matrix

| State | Trigger | Expected Behavior |
|---|---|---|
| Default | Tidak ada interaksi | Menampilkan visual normal |
| Hover | Pointer diarahkan ke elemen | Menampilkan feedback resmi |
| Focused | Navigasi keyboard | Menampilkan focus indicator |
| Active / Selected | Elemen atau navigasi aktif | Menampilkan status aktif |
| Pressed | Pengguna mengaktifkan kontrol | Menampilkan feedback interaksi jika tersedia |
| Disabled | Kontrol tidak tersedia | Mencegah interaksi |
| Loading | Tindakan sedang diproses | Menggunakan loading state jika didukung |

### 7.2 Default State

- MUST menggunakan visual Default resmi.
- MUST mempertahankan typography dan warna GEMS.
- MUST NOT membuat styling custom.

### 7.3 Hover State

- MUST menggunakan Hover State resmi jika tersedia.
- MUST menampilkan feedback hanya pada elemen interaktif.
- MUST NOT mengubah warna secara manual.
- MUST NOT mengubah ukuran komponen.

### 7.4 Focused State

- MUST menggunakan focus indicator resmi.
- MUST mendukung keyboard navigation.
- MUST mempertahankan indikator fokus.
- MUST NOT menghilangkan focus outline tanpa pengganti resmi.

### 7.5 Active / Selected State

- MUST menunjukkan elemen aktif sesuai GEMS.
- MUST mengikuti route atau kondisi aplikasi.
- MUST NOT menampilkan beberapa navigasi aktif secara tidak konsisten.
- MUST NOT membuat active styling custom.

### 7.6 Disabled State

- MUST menggunakan visual Disabled resmi jika tersedia.
- MUST mencegah interaksi.
- MUST NOT menggunakan Disabled sebagai pengganti Active.
- MUST NOT membuat state baru.

### 7.7 Loading State

- MUST menggunakan Loading State resmi jika tersedia dan diperlukan.
- MUST mencegah tindakan berulang jika relevan.
- MUST NOT membuat loading indicator custom.
- MUST NOT menampilkan keberhasilan sebelum proses selesai.

---

## 8. Navbar & Sidebar Interaction

### 8.1 Sidebar Open

Ketika Sidebar berubah menjadi terbuka:

- MUST menggunakan konfigurasi `Sidebar=Open`.
- MUST memperbarui Navbar sesuai konfigurasi resmi.
- MUST menjaga konsistensi layout.
- MUST mempertahankan fungsi navigasi.
- MUST NOT membuat perubahan layout custom.

### 8.2 Sidebar Closed

Ketika Sidebar berubah menjadi tertutup:

- MUST menggunakan konfigurasi `Sidebar=Closed`.
- MUST memperbarui Navbar sesuai konfigurasi resmi.
- MUST menjaga alignment sesuai GEMS.
- MUST mempertahankan fungsi Navbar.
- MUST NOT membuat variant baru.

### 8.3 Navbar Open Property

Ketika kondisi yang dikendalikan property `Open` berubah:

- MUST menggunakan nilai `true` atau `false` sesuai kondisi.
- MUST mengikuti interaction behavior resmi.
- MUST mempertahankan hubungan dengan Sidebar.
- MUST NOT mengubah property Sidebar tanpa alasan yang valid.

### 8.4 State Synchronization

AI MUST memastikan:

1. Navbar dan Sidebar menggunakan state yang konsisten.
2. Perubahan Sidebar memperbarui konfigurasi Navbar.
3. Perubahan Navbar mengikuti component behavior resmi.
4. Perpindahan halaman tidak menghasilkan konfigurasi yang salah.
5. Layout tetap konsisten setelah perubahan state.

---

## 9. Navbar Layout Rules

### 9.1 Positioning

AI MUST:

- Menggunakan posisi sesuai App Shell resmi.
- Mempertahankan hubungan Navbar dengan Sidebar.
- Mempertahankan alignment sesuai GEMS.
- Mengikuti layout grid resmi jika tersedia.

AI MUST NOT:

- Mengubah posisi Navbar secara sembarangan.
- Membuat fixed atau sticky behavior tanpa acuan.
- Membuat layout overlap dengan Sidebar.
- Membuat offset manual yang tidak didukung GEMS.

### 9.2 Consistency Across Pages

AI MUST:

1. Menggunakan Navbar yang sama pada halaman dengan App Shell serupa.
2. Mempertahankan konfigurasi sesuai state.
3. Mengikuti navigasi dan role access.
4. Mempertahankan visual consistency.
5. Menggunakan komponen resmi untuk seluruh elemen pendukung.

---

## 10. Responsive Behavior

### 10.1 Desktop

AI MUST:

- Menggunakan Navbar resmi.
- Memilih konfigurasi sesuai Sidebar.
- Mengikuti ukuran dan layout GEMS.
- Mempertahankan interaksi.
- Memastikan konten tidak bertabrakan.

### 10.2 Tablet & Mobile

AI MUST:

- Memeriksa apakah GEMS menyediakan responsive Navbar.
- Menggunakan responsive pattern resmi jika tersedia.
- Mempertahankan navigation hierarchy.
- Menggunakan komponen resmi untuk kontrol navigasi.
- Meminta Human Approval jika responsive pattern tidak tersedia.

AI MUST NOT:

1. Menganggap konfigurasi Desktop otomatis berlaku pada Mobile.
2. Membuat hamburger menu custom.
3. Membuat mobile Navbar baru tanpa acuan.
4. Mengubah breakpoint secara manual tanpa spesifikasi.
5. Menghilangkan navigasi penting tanpa persetujuan.

---

## 11. Accessibility

AI MUST:

1. Menggunakan semantic navigation yang sesuai saat implementasi.
2. Memberikan accessible name pada kontrol interaktif.
3. Mendukung keyboard navigation.
4. Mempertahankan focus indicator.
5. Menandai elemen navigasi aktif dengan semantik yang sesuai.
6. Memastikan kontrol dapat dioperasikan tanpa mouse.
7. Menggunakan icon labels yang dapat dipahami.
8. Memastikan state interaktif tidak hanya dibedakan berdasarkan warna.
9. Mengikuti standar aksesibilitas yang ditetapkan proyek.

AI MUST NOT:

- Menggunakan ikon tanpa accessible label jika fungsinya tidak jelas.
- Menghilangkan keyboard support.
- Menghilangkan focus indicator.
- Menggunakan kontrol non-interaktif untuk tindakan navigasi.

---

## 12. AI Decision Logic

AI MUST mengikuti proses berikut.

### Step 1 — Identify Page Layout

Periksa HSD/BRD dan struktur App Shell.

Tentukan apakah halaman menggunakan Navbar.

### Step 2 — Retrieve Official Component

AI MUST mengakses komponen Navbar resmi GEMS.

### Step 3 — Inspect Component Properties

Periksa:

- `Open`
- `Sidebar`

### Step 4 — Determine Sidebar State

Pilih:

- `Sidebar=Open`
- `Sidebar=Closed`

### Step 5 — Determine Navbar Open State

Pilih:

- `Open=true`
- `Open=false`

AI MUST menentukan state berdasarkan definisi dan interaksi komponen resmi.

### Step 6 — Select Official Configuration

Pilih salah satu dari empat konfigurasi resmi.

AI MUST NOT membuat kombinasi baru.

### Step 7 — Configure Supported Content

Sesuaikan hanya konten dan properties yang didukung.

AI MUST menggunakan komponen pendukung resmi GEMS.

### Step 8 — Apply Interaction States

Pastikan elemen interaktif menggunakan state resmi yang tersedia.

### Step 9 — Validate Layout

Periksa:

- Navbar positioning.
- Sidebar alignment.
- Spacing.
- Typography.
- Icons.
- Buttons.
- Interaction behavior.

### Step 10 — Validate Against GEMS

AI MUST memastikan:

1. Instance resmi digunakan.
2. Konfigurasi `Open` sesuai.
3. Konfigurasi `Sidebar` sesuai.
4. Navbar dan Sidebar sinkron.
5. Typography sesuai.
6. Colors sesuai.
7. Spacing sesuai.
8. Icons sesuai.
9. Buttons sesuai.
10. Tidak ada custom visual.
11. Interaksi sesuai.
12. Layout sesuai App Shell.

### Step 11 — Request Human Approval

Jika kebutuhan tidak didukung komponen resmi, AI MUST meminta Human Approval sebelum membuat alternatif.

---

## 13. AI Restrictions

AI MUST NOT:

1. Membuat Navbar custom.
2. Menggunakan Navbar dari library lain.
3. Mengganti instance resmi dengan Frame custom.
4. Membuat variant baru.
5. Mengubah component properties di luar nilai resmi.
6. Mengubah ukuran Navbar secara manual.
7. Mengubah typography di luar GEMS.
8. Mengubah warna di luar GEMS.
9. Mengubah spacing di luar GEMS.
10. Mengubah struktur internal komponen.
11. Membuat ikon custom.
12. Membuat Button custom.
13. Membuat interaction state custom.
14. Menggunakan konfigurasi Sidebar yang salah.
15. Mengabaikan perubahan Sidebar.
16. Menggabungkan dua variant secara manual.
17. Membuat responsive Navbar tanpa acuan.
18. Membuat hamburger menu custom.
19. Menambahkan Navbar pada setiap Frame.
20. Membuat Navbar ganda.
21. Menggunakan Navbar sebagai Tabs.
22. Menggunakan Navbar sebagai Breadcrumbs.
23. Menggunakan Navbar sebagai Sidebar.
24. Mengubah struktur navigasi tanpa HSD/BRD.
25. Mengabaikan role access.
26. Menghilangkan keyboard accessibility.
27. Mengklaim desain sesuai GEMS tanpa verifikasi.

---

## 14. Official GEMS Design System Component

### 14.1 Component Reference

**Component Name:** Navbar  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=410-2009

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `410:2009`

### 14.2 Verified Configurations

| Open | Sidebar |
|---|---|
| true | Open |
| true | Closed |
| false | Open |
| false | Closed |

**Total:** 4 configurations.

### 14.3 Mandatory Component Usage

AI MUST:

1. Mengakses komponen Navbar resmi GEMS.
2. Menggunakan instance resmi.
3. Memilih konfigurasi yang tersedia.
4. Mempertahankan visual properties resmi.
5. Menggunakan Icon dan Button resmi.
6. Menjaga hubungan Navbar dan Sidebar.
7. Mengikuti interaction states yang didukung.
8. Mempertahankan koneksi library apabila didukung.
9. Memvalidasi implementasi terhadap sumber resmi.

### 14.4 Component Verification

Sebelum implementasi, AI MUST memeriksa:

- Component Name.
- Available Configurations.
- Component Properties.
- Navbar Structure.
- Sidebar Integration.
- Typography.
- Colors.
- Spacing.
- Icons.
- Buttons.
- Interaction States.
- Responsive Behavior.

Jika suatu property tidak dapat diverifikasi, AI MUST NOT mengarang spesifikasinya.

### 14.5 Final AI Instruction

**AI MUST retrieve and reuse the official GEMS Navbar component from the specified Figma source whenever the integration supports it.**

AI MUST select one of the four supported configurations, preserve the official component structure, and synchronize the Navbar configuration with the Sidebar state.

AI MUST use official GEMS components and tokens for all supported elements.

AI MUST NOT recreate Navbar manually, invent unsupported variants, or introduce custom visual and interaction patterns without Human Approval.

**GEMS Design System is the single source of truth for all Navbar visual specifications.**
