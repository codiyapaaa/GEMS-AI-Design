# GEMS Design System — Slide Bar Guidelines

## 1. Purpose

Slide Bar merupakan komponen navigasi utama yang digunakan untuk mengakses modul, fitur, dan subfitur dalam aplikasi GEMS.

Slide Bar membantu pengguna berpindah antarhalaman, memahami posisi navigasi aktif, dan mengakses fitur berdasarkan hak akses pengguna.

Komponen ini memiliki dua tema visual dan dua kondisi tampilan yang harus digunakan sesuai konfigurasi resmi GEMS Design System.

### 1.1 Core Principle

> AI MUST menggunakan instance GEMS Slide Bar resmi. Theme Primary merupakan default yang diprioritaskan. Theme Light hanya digunakan ketika terdapat kebutuhan atau acuan desain yang mendukung. AI MUST NOT membuat Slide Bar custom, mengubah struktur komponen, atau membuat variant baru tanpa persetujuan.

### 1.2 Mandatory Design System Compliance

AI MUST:

1. Menggunakan instance GEMS Slide Bar resmi.
2. Menggunakan Theme Primary sebagai default.
3. Menggunakan Theme Light hanya berdasarkan kebutuhan atau desain yang disetujui.
4. Menggunakan konfigurasi Expanded atau Collapsed yang tersedia.
5. Mempertahankan struktur, warna, typography, ikon, spacing, dan layout resmi.
6. Menggunakan komponen pendukung GEMS untuk seluruh elemen navigasi.
7. Mengikuti HSD/BRD dalam menentukan menu, submenu, dan hak akses.
8. Menggunakan nama menu sesuai terminologi aplikasi.
9. Memastikan navigasi aktif sesuai halaman pengguna.
10. Memastikan state Slide Bar konsisten dengan Navbar dan App Shell.

AI MUST NOT:

1. Membuat Slide Bar custom.
2. Menggunakan komponen navigasi dari library lain.
3. Mengganti instance resmi dengan Frame manual.
4. Mengubah warna merah atau putih secara manual.
5. Membuat tema tambahan.
6. Mengubah ukuran dan spacing tanpa acuan GEMS.
7. Membuat ikon atau menu item custom ketika komponen resmi tersedia.
8. Mengubah struktur navigasi tanpa dasar HSD/BRD.
9. Membuat variant atau interaction state baru tanpa Human Approval.

---

## 2. Official Slide Bar Variants

### 2.1 Verified Component Properties

Berdasarkan metadata komponen GEMS, tersedia dua properties utama.

| Property | Available Values |
|---|---|
| Theme | Primary, Light |
| State | Expanded, Collapsed |

### 2.2 Official Configurations

| Theme | State | Width |
|---|---|---|
| Primary | Expanded | 312 px |
| Primary | Collapsed | 72 px |
| Light | Expanded | 312 px |
| Light | Collapsed | 72 px |

Keempat konfigurasi tersebut merupakan komponen resmi GEMS.

Ukuran di atas berasal dari frame sumber. Implementasi responsif tetap harus mengikuti ketentuan GEMS.

### 2.3 Theme Priority

Urutan prioritas pemilihan tema:

1. Primary — Default.
2. Light — Conditional.

AI MUST menggunakan Primary kecuali terdapat alasan yang jelas untuk menggunakan Light.

---

## 3. Theme Usage Guidelines

### 3.1 Primary Theme

**Property:** `Theme=Primary`

Primary merupakan tema utama Slide Bar GEMS dan menjadi pilihan default.

Dalam penggunaan aplikasi yang kamu tetapkan, Primary adalah tampilan merah.

#### When to Use

- Dashboard utama.
- Halaman manajemen data.
- Halaman daftar.
- Halaman detail.
- Halaman pengajuan.
- Halaman laporan.
- Halaman pengaturan.
- Modul aplikasi yang tidak memiliki aturan tema khusus.

#### Rules

AI MUST:

1. Menggunakan Primary sebagai pilihan pertama.
2. Menggunakan warna dari komponen resmi.
3. Mempertahankan typography dan ikon resmi.
4. Menggunakan visual menu aktif sesuai GEMS.
5. Mempertahankan konsistensi antarhalaman.

AI MUST NOT:

1. Mengubah warna Primary menjadi warna merah custom.
2. Menggunakan Light hanya karena preferensi estetika.
3. Mengubah tema antarhalaman tanpa alasan.
4. Membuat variasi Primary baru.

### 3.2 Light Theme

**Property:** `Theme=Light`

Light merupakan tema alternatif resmi GEMS yang menggunakan tampilan terang atau putih.

#### When to Use

Light MAY digunakan ketika:

1. Desain aplikasi yang disetujui menggunakan Light.
2. Modul tertentu memiliki kebutuhan tema Light.
3. Existing application pattern menggunakan Light.
4. Product Owner atau Design Lead menetapkan penggunaan Light.
5. Kebutuhan visual khusus telah mendapatkan persetujuan.

#### Rules

AI MUST:

1. Menggunakan instance Light resmi.
2. Mempertahankan warna dan visual properties resmi.
3. Mengikuti struktur menu yang sama.
4. Menggunakan state Expanded atau Collapsed resmi.
5. Menjaga konsistensi tema dalam konteks aplikasi.

AI MUST NOT:

1. Menggunakan Light tanpa dasar.
2. Mengganti Primary dengan Light secara otomatis.
3. Membuat Light dengan mengganti background Primary menjadi putih.
4. Mengubah warna teks dan ikon secara manual.
5. Mencampur visual Primary dan Light dalam satu Slide Bar.

### 3.3 Theme Selection Matrix

| Condition | Theme |
|---|---|
| Aplikasi GEMS standar | Primary |
| Tidak ada ketentuan tema | Primary |
| Existing design menggunakan Primary | Primary |
| Existing design menggunakan Light | Light |
| HSD/BRD menetapkan Light | Light |
| Design Lead menyetujui Light | Light |
| Tema tidak dapat ditentukan | Primary, kecuali bertentangan dengan acuan |

**Important:** Theme merupakan visual configuration, bukan status aktif/tidak aktif dari menu.

---

## 4. When to Use Slide Bar

### 4.1 Recommended Usage

Slide Bar SHOULD digunakan pada aplikasi web yang memiliki navigasi utama berbasis modul.

Contohnya:

- Dashboard.
- Manajemen data.
- Pengelolaan operasional.
- Monitoring.
- Laporan.
- Pengaturan.
- Administrasi pengguna.
- Halaman detail dalam App Shell.

### 4.2 Usage Matrix

| Page Context | Recommendation |
|---|---|
| Dashboard | Use Slide Bar |
| Management List | Use Slide Bar |
| Detail Page | Use Slide Bar |
| Create Data Page | Use jika berada dalam App Shell |
| Edit Data Page | Use jika berada dalam App Shell |
| Reports | Use Slide Bar |
| Settings | Use Slide Bar |
| Login | Follow Authentication Layout |
| Standalone Public Page | Follow Approved Layout |
| Modal | Do not create another Slide Bar |

### 4.3 Mandatory Usage

AI MUST menggunakan Slide Bar ketika:

1. Halaman merupakan bagian dari App Shell yang menggunakan Slide Bar.
2. HSD/BRD mengharuskan navigasi berbasis Slide Bar.
3. Existing design menggunakan GEMS Slide Bar.
4. Halaman berada dalam modul dengan navigasi utama yang sama.

AI MUST NOT menghilangkan Slide Bar pada halaman yang seharusnya menggunakan App Shell resmi.

---

## 5. When NOT to Use Slide Bar

Slide Bar SHOULD NOT digunakan pada:

- Halaman Login dengan layout khusus.
- Halaman Reset Password dengan layout khusus.
- Modal atau Dialog.
- Card.
- Table.
- Dropdown.
- Landing Page publik tanpa App Shell.
- Halaman khusus yang secara eksplisit tidak menggunakan Slide Bar.

AI MUST NOT:

1. Menambahkan Slide Bar pada setiap Frame.
2. Membuat Slide Bar kedua di dalam konten.
3. Menggunakan Slide Bar sebagai Tabs.
4. Menggunakan Slide Bar sebagai Breadcrumbs.
5. Menggunakan Slide Bar sebagai Stepper.
6. Menggunakan Slide Bar untuk navigasi sementara dalam Modal.

---

## 6. Slide Bar Anatomy

### 6.1 Component Structure

AI MUST mempertahankan struktur internal sesuai instance resmi GEMS.

Bagian yang perlu diperiksa:

| Element | Purpose |
|---|---|
| Slide Bar Container | Membungkus navigasi utama |
| Branding Area | Menampilkan identitas aplikasi jika tersedia |
| Navigation Item | Menampilkan menu |
| Navigation Icon | Identifikasi menu |
| Navigation Label | Nama menu |
| Submenu | Menampilkan hierarki fitur jika didukung |
| Expand/Collapse Control | Mengubah state Slide Bar |
| Active Indicator | Menunjukkan navigasi aktif |
| Supporting Elements | Elemen tambahan sesuai komponen resmi |

Daftar ini merupakan checklist struktur yang harus diverifikasi pada instance, bukan klaim bahwa seluruh elemen selalu tersedia.

### 6.2 Container Rules

AI MUST:

- Menggunakan container resmi.
- Mengikuti warna Theme.
- Menggunakan ukuran resmi.
- Mempertahankan alignment.
- Mempertahankan padding dan spacing.
- Mengikuti responsive behavior GEMS.

AI MUST NOT:

- Membuat container custom.
- Mengubah radius atau shadow secara manual.
- Mengubah background di luar Theme.
- Membuat ukuran baru tanpa persetujuan.

### 6.3 Navigation Item Rules

AI MUST:

- Menggunakan item navigasi resmi.
- Menggunakan ikon GEMS.
- Menggunakan label yang sesuai.
- Mengikuti hierarchy menu.
- Menggunakan state resmi.
- Menjaga konsistensi visual.

AI MUST NOT:

- Membuat item menggunakan Text dan Rectangle manual.
- Menggunakan ikon dari library lain.
- Mengubah ukuran ikon tanpa acuan.
- Membuat active indicator custom.

---

## 7. Slide Bar States

### 7.1 Official Layout States

GEMS menyediakan dua state utama:

- Expanded.
- Collapsed.

Keduanya tersedia pada Theme Primary dan Light.

### 7.2 Expanded State

**Property:** `State=Expanded`

Expanded merupakan kondisi ketika Slide Bar menggunakan tampilan lebar.

**Verified Source Width:** 312 px.

#### When to Use

- Pengguna membutuhkan navigasi dengan label yang terlihat.
- Aplikasi baru dibuka dengan konfigurasi Expanded.
- Pengguna memilih memperluas Slide Bar.
- Hierarki menu membutuhkan ruang lebih luas.
- Existing application menggunakan Expanded.

#### Rules

AI MUST:

1. Menggunakan variant Expanded resmi.
2. Mempertahankan struktur dan alignment.
3. Menggunakan label sesuai komponen.
4. Mempertahankan state menu aktif.
5. Menggunakan Theme yang sedang berlaku.

AI MUST NOT:

1. Membuat Expanded dengan memperbesar Collapsed secara manual.
2. Mengubah lebar di luar konfigurasi resmi.
3. Mengubah ukuran ikon atau label.
4. Mengganti Theme saat Expand tanpa alasan.

### 7.3 Collapsed State

**Property:** `State=Collapsed`

Collapsed merupakan kondisi ketika Slide Bar menggunakan tampilan ringkas.

**Verified Source Width:** 72 px.

#### When to Use

- Pengguna memilih memperkecil Slide Bar.
- Aplikasi membutuhkan area konten lebih luas.
- Existing application menggunakan Collapsed.
- Layout yang disetujui menetapkan tampilan ringkas.

#### Rules

AI MUST:

1. Menggunakan variant Collapsed resmi.
2. Mempertahankan ikon dan elemen sesuai komponen.
3. Mengikuti visual item aktif resmi.
4. Mempertahankan Theme yang dipilih.
5. Memastikan navigasi tetap dapat digunakan.

AI MUST NOT:

1. Membuat Collapsed dengan menyembunyikan teks secara manual.
2. Mengubah ukuran container sendiri.
3. Menghapus ikon navigasi.
4. Membuat tooltip atau flyout custom tanpa acuan.
5. Mengubah Theme ketika Collapse tanpa kebutuhan.

### 7.4 Expanded/Collapsed Transition

Ketika pengguna mengubah state:

1. Sistem mengidentifikasi state saat ini.
2. Sistem memilih variant tujuan.
3. Theme tetap dipertahankan.
4. Navigasi aktif tetap dipertahankan.
5. Area konten menyesuaikan layout resmi.
6. Fokus pengguna tetap terjaga.

AI MUST NOT mereset menu aktif hanya karena Slide Bar berubah ukuran.

---

## 8. Navigation Item States

State item navigasi berbeda dari state Expanded/Collapsed.

### 8.1 State Matrix

| State | Trigger | Expected Behavior |
|---|---|---|
| Default | Item tidak aktif | Menggunakan visual normal |
| Hover | Pointer diarahkan | Feedback visual resmi |
| Focused | Keyboard focus | Focus indicator resmi |
| Active / Selected | Halaman sedang aktif | Menunjukkan lokasi pengguna |
| Expanded Submenu | Parent memiliki submenu terbuka | Menampilkan submenu jika didukung |
| Collapsed Submenu | Submenu ditutup | Menyembunyikan submenu |
| Disabled | Aksi tidak tersedia jika didukung | Tidak menjalankan navigasi |

State visual item harus diverifikasi pada komponen navigasi GEMS yang digunakan.

### 8.2 Default State

- MUST menggunakan visual Default resmi.
- MUST mengikuti Theme.
- MUST mempertahankan typography dan ikon.
- MUST NOT membuat styling custom.

### 8.3 Hover State

- MUST menggunakan Hover resmi jika tersedia.
- MUST memberikan feedback pada item interaktif.
- MUST NOT membuat warna hover custom.
- MUST NOT mengubah ukuran item.

### 8.4 Focused State

- MUST menggunakan focus indicator resmi.
- MUST mendukung keyboard navigation.
- MUST mempertahankan indikator fokus.
- MUST NOT menghilangkan focus styling.

### 8.5 Active / Selected State

- MUST menunjukkan menu sesuai route aktif.
- MUST menggunakan active indicator resmi.
- MUST mempertahankan active state ketika Slide Bar di-collapse.
- MUST memperbarui active state ketika pengguna berpindah halaman.
- MUST NOT menampilkan dua item aktif yang saling bertentangan.

### 8.6 Submenu Expanded

Jika komponen mendukung submenu:

- MUST menggunakan struktur submenu resmi.
- MUST mempertahankan hierarchy.
- MUST mengikuti visual Expanded submenu resmi.
- MUST menampilkan submenu sesuai interaksi.
- MUST NOT membuat dropdown custom.

### 8.7 Submenu Collapsed

Jika submenu ditutup:

- MUST mengikuti behavior resmi.
- MUST mempertahankan navigasi aktif.
- MUST NOT menghapus struktur submenu.
- MUST NOT mereset halaman aktif.

### 8.8 Disabled State

Jika didukung:

- MUST menggunakan visual Disabled resmi.
- MUST mencegah interaksi.
- MUST NOT menggunakan Disabled sebagai pengganti role-based visibility.
- MUST NOT membuat state baru.

---

## 9. Input Data & Menu Configuration

Bagian ini mengatur bagaimana AI memasukkan data menu ke dalam Slide Bar.

### 9.1 Data Source Priority

AI MUST menggunakan urutan sumber berikut:

1. Approved HSD/BRD.
2. Approved Information Architecture.
3. Approved Navigation Structure.
4. Existing Application Design.
5. User-provided Menu Requirements.

AI MUST NOT membuat menu berdasarkan asumsi tanpa dasar.

### 9.2 Required Menu Data

Sebelum menyusun Slide Bar, AI MUST mengidentifikasi:

| Data | Description |
|---|---|
| Menu Name | Nama menu utama |
| Menu Icon | Ikon resmi GEMS |
| Parent Menu | Menu induk jika tersedia |
| Submenu Name | Nama submenu |
| Navigation Route | Tujuan navigasi |
| Active Route | Halaman yang sedang aktif |
| Role Access | Hak akses pengguna |
| Menu Order | Urutan menu |
| Visibility | Kondisi tampil/sembunyi |

### 9.3 Menu Naming Rules

AI MUST:

1. Menggunakan nama menu dari HSD/BRD.
2. Mempertahankan terminologi bisnis.
3. Menggunakan label singkat dan jelas.
4. Menjaga konsistensi penamaan.
5. Menggunakan nama yang sama pada navigasi dan halaman terkait.

AI MUST NOT:

1. Mengubah nama menu tanpa persetujuan.
2. Menggunakan istilah berbeda untuk fitur yang sama.
3. Membuat singkatan yang tidak dikenal.
4. Menambahkan menu yang tidak diminta.

### 9.4 Menu Hierarchy Rules

AI MUST:

1. Mengikuti parent-child hierarchy.
2. Menempatkan submenu di bawah parent yang sesuai.
3. Mengikuti urutan menu yang disetujui.
4. Menggunakan struktur submenu resmi.
5. Mempertahankan hierarchy ketika state berubah.

AI MUST NOT:

1. Memindahkan submenu ke parent lain tanpa dasar.
2. Membuat level navigasi baru tanpa persetujuan.
3. Menggabungkan menu yang berbeda.
4. Memecah menu menjadi beberapa item tanpa kebutuhan.

### 9.5 Icon Mapping Rules

AI MUST:

1. Menggunakan ikon resmi GEMS.
2. Memilih ikon sesuai konteks fitur.
3. Mempertahankan ukuran dan styling resmi.
4. Menggunakan ikon yang konsisten untuk fitur yang sama.

AI MUST NOT:

1. Menggunakan ikon eksternal.
2. Menggambar ikon baru.
3. Mengubah stroke atau fill secara manual.
4. Menggunakan ikon berbeda untuk menu yang sama tanpa alasan.

### 9.6 Navigation Route Rules

AI MUST:

1. Menghubungkan menu dengan route yang valid.
2. Menampilkan active state berdasarkan route.
3. Mempertahankan hubungan parent-child.
4. Mengikuti aturan navigasi aplikasi.
5. Memastikan menu tidak mengarah ke halaman yang salah.

AI MUST NOT:

1. Menggunakan route dummy pada hasil final.
2. Membuat route yang tidak tersedia.
3. Menghubungkan beberapa menu berbeda ke route yang salah.
4. Menggunakan menu hanya sebagai dekorasi jika seharusnya interaktif.

---

## 10. Dynamic Menu & Role Access

### 10.1 Role-Based Navigation

Slide Bar dapat menampilkan menu berbeda berdasarkan hak akses pengguna jika aplikasi mendukungnya.

AI MUST:

1. Membaca Role Access Matrix.
2. Menampilkan menu sesuai izin pengguna.
3. Mengikuti aturan visibility.
4. Mempertahankan urutan menu yang relevan.
5. Menggunakan komponen Slide Bar yang sama.

AI MUST NOT:

1. Membuat Slide Bar custom untuk setiap role.
2. Menampilkan menu yang tidak memiliki izin akses.
3. Menganggap menyembunyikan menu sebagai pengganti authorization.
4. Mengubah hak akses berdasarkan preferensi visual.

### 10.2 Dynamic Menu Data

Jika menu berasal dari data sistem:

- MUST mengikuti struktur data yang tersedia.
- MUST memvalidasi route dan parent-child relationship.
- MUST menggunakan komponen resmi.
- MUST mempertahankan visual consistency.
- MUST menangani perubahan menu tanpa mengubah Design System.

### 10.3 Empty Menu Configuration

Jika data navigasi belum tersedia:

- MUST NOT membuat menu fiktif.
- MUST NOT menambahkan dummy navigation pada hasil final.
- MUST meminta klarifikasi atau menggunakan struktur yang sudah disetujui.
- MUST mempertahankan komponen resmi.

---

## 11. Slide Bar & Navbar Integration

### 11.1 State Synchronization

AI MUST memastikan:

- Slide Bar Expanded sesuai konfigurasi Navbar yang mendukung Sidebar terbuka.
- Slide Bar Collapsed sesuai konfigurasi Navbar yang mendukung Sidebar tertutup.
- Theme Slide Bar tetap konsisten.
- Layout konten mengikuti perubahan state.
- Tidak ada overlap antara Slide Bar dan Navbar.

### 11.2 State Mapping

| Slide Bar State | Navbar Sidebar Property |
|---|---|
| Expanded | Open |
| Collapsed | Closed |

Mapping ini merupakan aturan integrasi yang direkomendasikan berdasarkan hubungan state, dan harus divalidasi pada App Shell yang digunakan.

### 11.3 Layout Consistency

AI MUST:

1. Menggunakan Navbar resmi GEMS.
2. Menggunakan Slide Bar resmi GEMS.
3. Menjaga kesesuaian state.
4. Mempertahankan layout resmi.
5. Menghindari offset manual.

---

## 12. Responsive Behavior

### 12.1 Desktop

AI MUST:

- Menggunakan variant resmi.
- Mengikuti layout App Shell.
- Mempertahankan Theme.
- Mempertahankan state navigasi.
- Mengikuti ukuran komponen.

### 12.2 Tablet & Mobile

AI MUST:

1. Memeriksa responsive pattern GEMS.
2. Menggunakan komponen resmi jika tersedia.
3. Mempertahankan hierarchy navigasi.
4. Memastikan kontrol tetap dapat digunakan.
5. Meminta Human Approval jika pattern tidak tersedia.

AI MUST NOT:

1. Menganggap Collapsed otomatis merupakan mobile navigation.
2. Membuat drawer mobile custom.
3. Membuat hamburger menu custom.
4. Mengubah breakpoint tanpa acuan.
5. Menghilangkan menu penting secara sembarangan.

---

## 13. Accessibility

AI MUST:

1. Mendukung keyboard navigation.
2. Menggunakan focus indicator resmi.
3. Memberikan accessible label pada menu berbasis ikon.
4. Menandai route aktif dengan semantik yang sesuai.
5. Menjaga keterbacaan dan kontras sesuai standar proyek.
6. Menggunakan kontrol yang dapat dioperasikan tanpa mouse.
7. Memastikan submenu dapat digunakan dengan keyboard jika tersedia.
8. Menjaga aksesibilitas pada Expanded dan Collapsed.

AI MUST NOT:

- Mengandalkan ikon tanpa accessible name.
- Menghilangkan focus indicator.
- Menggunakan warna saja untuk menyampaikan active state.
- Menghilangkan navigasi keyboard.

---

## 14. AI Decision Logic

AI MUST mengikuti proses berikut.

### Step 1 — Identify Application Layout

Periksa HSD/BRD dan App Shell.

Tentukan apakah halaman menggunakan GEMS Slide Bar.

### Step 2 — Retrieve Official Component

AI MUST mengakses komponen GEMS Slide Bar resmi.

### Step 3 — Determine Theme

Default:

`Theme=Primary`

Gunakan:

`Theme=Light`

hanya ketika terdapat acuan atau persetujuan.

### Step 4 — Determine Layout State

Pilih:

- `State=Expanded`
- `State=Collapsed`

Berdasarkan kondisi aplikasi dan interaksi pengguna.

### Step 5 — Retrieve Menu Data

Baca:

- Menu Name.
- Menu Hierarchy.
- Menu Order.
- Route.
- Role Access.
- Active Page.

### Step 6 — Configure Navigation

AI MUST mengisi menu menggunakan struktur resmi.

AI MUST NOT membuat komponen menu custom.

### Step 7 — Apply Active State

Tentukan menu aktif berdasarkan route saat ini.

### Step 8 — Configure Submenu

Jika diperlukan dan didukung, gunakan submenu resmi.

### Step 9 — Synchronize Navbar

Pastikan state Slide Bar sesuai dengan Navbar.

### Step 10 — Validate Design System

Periksa:

1. Instance resmi.
2. Theme benar.
3. State benar.
4. Width sesuai variant.
5. Colors sesuai.
6. Typography sesuai.
7. Icons sesuai.
8. Spacing sesuai.
9. Menu hierarchy benar.
10. Active state benar.
11. Role access benar.
12. Tidak ada komponen custom.

### Step 11 — Request Human Approval

Jika komponen tidak mendukung kebutuhan, AI MUST meminta Human Approval sebelum membuat alternatif.

---

## 15. AI Restrictions

AI MUST NOT:

1. Membuat Slide Bar custom.
2. Menggunakan library lain.
3. Mengganti instance dengan Frame manual.
4. Membuat Theme baru.
5. Mengubah Primary menjadi warna custom.
6. Mengubah Light menjadi warna custom.
7. Menggunakan Light tanpa alasan.
8. Mengubah ukuran Expanded atau Collapsed secara manual.
9. Membuat state baru.
10. Mengubah typography di luar GEMS.
11. Mengubah spacing di luar GEMS.
12. Membuat ikon custom.
13. Membuat menu item custom.
14. Membuat submenu custom.
15. Membuat hover atau active styling custom.
16. Menambahkan menu tanpa HSD/BRD.
17. Mengubah urutan menu tanpa dasar.
18. Mengubah parent-child hierarchy.
19. Mengabaikan role access.
20. Menggunakan route yang salah.
21. Menggunakan data dummy pada hasil final.
22. Membuat Slide Bar berbeda untuk setiap role.
23. Menghilangkan menu aktif ketika Collapse.
24. Mengubah Theme saat Expand/Collapse tanpa alasan.
25. Membuat mobile navigation custom tanpa acuan.
26. Mengabaikan hubungan Navbar dan Slide Bar.
27. Mengklaim implementasi sesuai GEMS tanpa verifikasi.

---

## 16. Official GEMS Design System Component

### 16.1 Component Reference

**Component Name:** GEMS Slide Bar  
**Design System:** GEMS Design System

**Figma Component URL:**  
https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2714-24723

**Figma File Key:** `vaAJgd6yZ7l9TrIuF04671`  
**Component Node ID:** `2714:24723`

### 16.2 Verified Component Configurations

| Theme | State | Source Width |
|---|---|---|
| Primary | Expanded | 312 px |
| Primary | Collapsed | 72 px |
| Light | Expanded | 312 px |
| Light | Collapsed | 72 px |

### 16.3 Mandatory Component Usage

AI MUST:

1. Mengakses GEMS Slide Bar resmi.
2. Menggunakan instance resmi.
3. Menggunakan Primary sebagai default.
4. Menggunakan Light hanya jika dibutuhkan.
5. Memilih Expanded atau Collapsed.
6. Mempertahankan visual properties.
7. Menggunakan menu item dan ikon resmi.
8. Mengikuti HSD/BRD.
9. Mengikuti Role Access Matrix.
10. Memvalidasi hasil terhadap GEMS.

### 16.4 Verification Requirements

Sebelum implementasi, AI MUST memeriksa:

- Component Name.
- Available Variants.
- Theme Properties.
- State Properties.
- Width.
- Menu Item Structure.
- Icon Mapping.
- Typography.
- Colors.
- Spacing.
- Active State.
- Submenu Behavior.
- Navbar Integration.
- Responsive Behavior.

Jika suatu property tidak dapat diverifikasi, AI MUST NOT mengarang spesifikasinya.

### 16.5 Final AI Instruction

**AI MUST retrieve and reuse the official GEMS Slide Bar component from the specified Figma source whenever the integration supports it.**

AI MUST prioritize `Theme=Primary`, use `Theme=Light` only when supported by approved requirements, and select either `State=Expanded` or `State=Collapsed`.

AI MUST populate the Slide Bar using approved navigation data, maintain the correct hierarchy, preserve active states, respect role-based access, and synchronize the component with the application Navbar.

AI MUST use official GEMS components, icons, typography, colors, and interaction patterns.

AI MUST NOT recreate the Slide Bar manually, invent unsupported variants, or introduce custom visual properties without Human Approval.

**GEMS Design System is the single source of truth for all Slide Bar visual specifications.**
