Berikut adalah spesifikasi teknis tingkat tinggi, **BAGIAN 1**.

---

## BAGIAN 1: BUSINESS LOGIC, CONVERSION BLUEPRINT & GLOBAL TECH STACK SPECIFICATION

### 1.1 EXECUTIVE BUSINESS OBJECTIVE & SPECIFIC CONVERSION MECHANICS

Tujuan utama dari arsitektur platform ini adalah menjadi mesin *lead generation* B2B yang menghasilkan permintaan penawaran harga (*Quotation Requests*) ber-SLA tinggi. Arsitektur *conversion rate optimization* (CRO) dibangun di atas tiga pilar metrik waktu absolut:

* 
**Aturan 5 Detik (Business Comprehension):** Saat halaman dimuat ($LCP < 2.5s$), eksekutif *procurement* harus langsung mengenali UD NIMARS sebagai entitas rantai pasok premium. Hal ini dieksekusi melalui *Hero Section* yang menggunakan tipografi *display* kokoh (Montserrat) dan visualisasi langsung dari infrastruktur *cold-chain* atau operasional gudang, menghindari ambiguitas vendor retail biasa.


* 
**Aturan 10 Detik (Product & Capability Discovery):** Navigasi berbasis taksonomi B2B (Sayuran Premium, Buah Tropis/Eksotis, Bumbu Esensial) dengan spesifikasi teknis yang langsung terlihat (seperti kalibrasi produk, *Brix index*, dan *Minimum Order Quantity* / MOQ). Pengguna tidak perlu menggali terlalu dalam untuk mengetahui kapasitas suplai harian atau mingguan.


* 
**Aturan 30 Detik (Frictionless Quotation):** Alur formulir RFQ (*Request for Quotation*) harus bersifat lengket (*sticky CTA*). Pengguna dapat melengkapi *field* kualifikasi B2B (Nama Perusahaan, Skala Volume, Frekuensi) dan mengirimkan data dengan enkripsi SSL dalam waktu kurang dari 30 detik.



**Struktur Alur Kualifikasi Lead (B2B Funnel Blueprint):**

1. 
**Awareness & Trust (Landing):** *Trust Bar* yang memvalidasi operasional (150+ Klien, SLA 98%, Distribusi 25 Ton/Minggu).


2. 
**Validation (Detailing):** Penjelasan transparan mengenai kapabilitas *Farm-to-Table*, jaminan retur (*Replacement Guarantee*), dan sistem kontrak *Term of Payment* (TOP).


3. 
**Conversion (Action):** Formulir RFQ yang mensimulasikan proteksi enkripsi untuk memberikan rasa aman pada integritas data korporat.



**Pemetaan Profil Audiens Eksekutif:**

| Profil Eksekutif | Titik Fokus Utama (Pain Points) | Solusi yang Ditampilkan di UI |
| --- | --- | --- |
| **Executive Chef (HORECA)** | Konsistensi kualitas, tingkat presisi kalibrasi (ukuran seragam), dan *defect rate* visual. | Lencana *100% Quality Audited*, garansi kesegaran, foto sortasi QC presisi tinggi.

 |
| **Procurement Manager** | Stabilitas HPP, perlindungan inflasi pasar, *Term of Payment* (TOP), dan legalitas pajak/PPN. | <br>*Highlight* pada *Fixed Pricing Agreement* dan SLA Pengiriman tepat waktu.

 |
| **Direktur Katering Institusional** | Skalabilitas volume masif (Tonase), kemampuan logistik *cold fleet*, kelengkapan sertifikasi (HACCP). | Visibilitas infrastruktur gudang, *Cold Storage*, dan lencana sertifikasi industri.

 |

---

### 1.2 GLOBAL DESIGN SYSTEM TOKENS & CONTENT AUDIT RULES

Sistem desain diwajibkan menggunakan pendekatan B2B yang bersih, percaya diri, dan humanis. Implementasi harus mematuhi token yang sangat spesifik untuk mencegah nuansa *template* atau proyek amatir.

A. Pemetaan Token Warna Global:

| Role / Intent | Hex Code | UI Component Mapping | Behavior / State |
| --- | --- | --- | --- |
| **Primary** | `#2D5A27` | Header utama, elemen *branding* inti, lencana sertifikasi, *background overlay*. | Default state untuk *trust elements*. |
| **Secondary** | `#3E7A35` | Gradasi aksen, *secondary buttons*, interaksi UI sekunder. | Hover state dari elemen Primary. |
| **Accent** | `#F2994A` | Garis bawah navigasi (*nav links*), ikon highlight, lencana spesifikasi produk. | Active state / Navigation indicators. |
| **CTA Action** | `#E67E22` | Tombol utama konversi (*Request Quote*), elemen yang memerlukan klik segera. | Default CTA state dengan *glow/shadow* ringan. |
| **Dark (Text)** | `#1D1D1F` | *Typography Heading*, garis teks utama, kontras tinggi. | Default untuk teks keterbacaan tinggi. |
| **Background** | `#F8FAF8` | Dasar kanvas halaman (MPA), *spacing* antar-seksi. | *Canvas base layout*. |
| **Border** | `#E5E7EB` | Garis pembatas *glass-card*, *input field form*. | Default structural borders. |
| **Success** | `#22C55E` | *Toast notification* formulir, status verifikasi. | Validasi form sukses. |

B. Aturan Ketat Tipografi:

* **Heading (Montserrat):** Digunakan murni untuk hierarki informasi kuat (H1-H4). Wajib menggunakan *Font-Weight* 700 (Bold), 800 (ExtraBold), atau 900 (Black). *Letter-spacing* ketat (`-0.02em` atau `tracking-tight`) untuk kesan modern dan *confident* korporat.


* **Body (Inter):** Digunakan murni untuk paragraf, deksripsi, label, dan data. Wajib menggunakan *Font-Weight* 400 (Regular), 500 (Medium), atau 600 (SemiBold). *Line-height* rileks (`1.6` hingga `1.8` / `leading-relaxed`) untuk meningkatkan keterbacaan (*thumb-friendly* dan *accessible*).



C. Kebijakan Audit Gambar (*Image Policy*):

* **Wajib (*Mandatory*):** Gambar beresolusi tinggi (WebP) yang memperlihatkan fasilitas nyata/representatif (*Cold Storage*, aktivitas bongkar muat logistik, inspeksi mikrobiologi/QC, hamparan hasil tani spesifik, *delivery vehicles*).
* **Dilarang Keras (*Strictly Banned*):** Penggunaan *generic stock-photos* (orang tersenyum tanpa konteks agrikultur, foto meja kantor dengan laptop generik, klise jabat tangan korporat yang usang, dan *mockup* teknologi abstrak). Semuanya harus bermuara pada kesan agrikultur modern (*Modern Agriculture*) dan rantai pasok otentik (*Authentic Supply Chain*).



---

### 1.3 CORE WEB VITALS & ARCHITECTURAL STACK BLUEPRINTS

Arsitektur aplikasi harus berbentuk *Multi Page Application* (MPA) tradisional namun terasa selancar SPA (*Single Page Application*) melalui optimasi teknis. Target krusial adalah PageSpeed Google melebihi 90, dengan metrik utama termuat dalam tenggat waktu $LCP < 2.5s$.

**1. Rendering & DOM Architecture:**

* HTML harus sepenuhnya *semantic* (menggunakan `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`) untuk memastikan skor aksesibilitas dan SEO maksimum.


* Menghindari struktur *div-soup* yang memberatkan *Main Thread*.

**2. Assets & Media Management:**

* **LCP Optimization:** Gambar pada *Hero Section* tidak boleh di-*lazy-load*. Gambar di bawah lipatan layar (*below-the-fold*) wajib menggunakan atribut `loading="lazy"`.
* Semua gambar dan aset grafis wajib dikonversi dan disajikan dalam format *next-gen* (WebP).
* Ikonografi dikelola menggunakan **Lucide Icons** secara dinamis, dimuat dari CDN tervalidasi atau di-bundle secara efisien.

3. Animation Library & TTI (Time to Interactive) Directive:

* *Lenis Smooth Scroll* dan *GSAP ScrollTrigger* diizinkan **HANYA** untuk transisi *fade-in*, *reveal on scroll* elemen kartu, atau *parallax* ringan.
* **CRITICAL DEPRECATION:** Berdasarkan dokumen PRD, elemen *Custom Cursor* (kursor berbasis JS/lerp) dan animasi *heavy sequence* (manipulasi DOM massal saat *scroll*) yang terdapat pada *draft* kode awal (`percobaan.html`, `kontak.html`) **WAJIB DIHAPUS**. Hal ini menyebabkan perlambatan *Time to Interactive* (TTI) yang tidak dapat ditolerir pada perangkat *mobile* rendah, serta mengurangi kesan profesional B2B. Animasi berlebih dan efek dekoratif usang tidak relevan dengan profil target manajer operasional.


## BAGIAN 2: MULTI PAGE APPLICATION (MPA) ARCHITECTURE & PAGE-BY-PAGE BLUEPRINT

Bagian ini menguraikan arsitektur spesifik untuk masing-masing halaman dalam ekosistem *Multi Page Application* (MPA) UD NIMARS. Fokus utama adalah menyajikan aliran informasi hierarkis yang membimbing pengguna B2B menuju proses konversi formulir *Request Quote*.

### 2.1 HOME PAGE (INDEX) - THE CORPORATE GATEWAY

Tujuan *Home Page* adalah membentuk otoritas merek (*brand authority*) UD NIMARS dalam waktu kurang dari 5 detik dan memandu eksekutif ke spesifikasi atau katalog. Berdasarkan draf PRD, struktur elemen harus komprehensif, bukan sekadar etalase animasi.

**Struktur Elemen (Top to Bottom):**

1. **Global Navigation (Header):** Menu *sticky* melayang berbasis kapsul (*capsule header*) dengan latensi responsif. Menu terdiri dari: *Home*, *About*, *Products*, *Team*, *Contact*. Tombol WhatsApp (Aksi sekunder) dan *Request Quote* (CTA Utama - warna *CTA Orange*).
2. **Hero Section:** Visualisasi lebar layar (*full-width*) menggunakan WebP *high-res* dari operasional gudang pendingin (*cold-storage*) atau aktivitas bongkar muat produk segar nusantara yang otentik.
* **Headline:** Kuat, asertif, tanpa jargon berlebihan. Menggunakan Montserrat tebal.
* **Subheadline:** Janji kualitas, SLA, dan penekanan B2B.
* **Dual CTA:** Tombol "Eksplorasi Produk" dan "Request Quotation" berukuran besar (*Thumb Friendly*).


3. **Trust Bar (Data Validasi):** Terintegrasi tepat di bawah Hero. Menampilkan statistik operasional: "150+ Klien Bisnis", "Distribusi 25+ Ton Mingguan", "98% SLA On-Time Delivery", dan "10+ Tahun Pengalaman". Elemen ini krusial untuk manajemen risiko *procurement*.
4. **Value Proposition (Why Choose NIMARS):** Matriks informasi (grid) yang menjabarkan *Traceability*, *Fixed Pricing Agreement* untuk stabilitas HPP klien, dan garansi penggantian barang (*Replacement Guarantee*).
5. **Product Categories (Quick Entry):** Pratinjau 3 kategori inti (Sayuran Premium, Buah Tropis, Bumbu Esensial) dengan visual jernih dan tombol "Lihat Detail Katalog".
6. **Operational Capability (How We Work):** Diagram alur (visualisasi berurutan) yang menunjukkan *Sourcing* GAP (Good Agricultural Practices) -> *QC Intake* -> *Washing/Packing* bersuhu terkontrol -> Logistik *Cold Fleet*.
7. **Testimonials & Client Marquee:** Bukti sosial dengan format kutipan profesional dari klien eksisting (*Executive Chef*, *Procurement Manager*).
8. **Pre-Footer CTA:** Blok dorongan final menuju halaman *Request Quote*.
9. **Global Footer:** Area navigasi, tautan legal, info kontak, pendaftaran buletin (*newsletter/price list*), dan pilar *branding* B2B.

---

### 2.2 ABOUT PAGE - BRAND AUTHORITY & INFRASTRUCTURE

Halaman ini tidak hanya menampilkan "Siapa Kami", melainkan berfungsi sebagai portofolio infrastruktur berskala korporat, membangun rasa aman (kredibilitas) bagi eksekutif.

**Struktur Elemen:**

1. **Corporate Story & Milestones:** Narasi *Farm-to-Table* yang disempurnakan. Garis waktu (*timeline*) evolusi dari perusahaan lokal menuju skala agrikultur modern (*milestones* penting seperti tahun ekspansi HORECA dan integrasi logistik *Cold Chain*).
2. **Vision & Mission:** Penjabaran standar emas logistik kesegaran.
3. **Operational Coverage & Area:** Visualisasi geografis jangkauan operasional logistik, dengan fokus pada Jabodetabek dan fleksibilitas *Enterprise* (melalui mitra 3PL yang tersertifikasi *cold-chain*).
4. **Certifications & Compliance (Trust Anchors):** Presentasi lencana sertifikasi industri seperti HACCP, ISO 22000, 100% Quality Audited, dan standar Keamanan Pangan lainnya.
5. **Warehouse & Logistics Gallery (Image Rule Compliant):** Grid *masonry* foto-foto beresolusi tinggi (*real-world*) dari proses operasional: penyortiran QC manual, *cold storage*, serta logistik menggunakan armada khusus berpendingin. Tidak ada stok foto kantor generik.
6. **Corporate Values:** Etos kerja profesional B2B.
7. **Leadership Message:** Pesan eksekutif singkat yang memberikan nuansa kemitraan dan dedikasi.

---

### 2.3 PRODUCTS PAGE - CATALOGUE & SPECIFICATION DIRECTORY

Didesain bukan sebagai halaman belanja (seperti *e-commerce* B2C), melainkan sebagai direktori spesifikasi katalog yang membantu *Executive Chef* atau manajer pengadaan memahami standar mutu UD NIMARS.

**Struktur Elemen:**

1. **Catalogue Entry Header:** Mempromosikan kualitas komoditas terkurasi.
2. **Categorized Directory:**
* **Sayuran Premium:** Penjelasan visual (selada hidroponik, sayuran daun hijau, umbi-umbian) disertai data kalibrasi (misal: 3-4 pcs per Kg) dan MOQ.
* **Buah Tropis & Eksotis:** Penjelasan visual (melon grade A, mangga standar ekspor, alpukat mentega) disertai parameter kematangan (*Brix/Firmness index*) dan MOQ.
* **Imported Produce / Custom Supply:** Produk spesifik untuk kebutuhan *niche* perhotelan berbintang (*garnish*, *herbs* premium).


3. **Quality Assurance Protocol:** Penjelasan ulang tentang pembersihan mikrobiologis (higienitas food-grade) dan jaminan 0% *visual defect* sebelum pemuatan.
4. **Product FAQ:** Pertanyaan umum spesifik mengenai produk, MOQ per *item*, pengemasan (opsi karung, krat, atau *bulk box*), dan stabilitas ketersediaan komoditas saat fluktuasi cuaca.

---

### 2.4 TEAM PAGE - THE OPERATIONAL BACKBONE

Tujuan halaman *Team* adalah menyajikan wajah profesional (humanis namun korporat) dari para pakar penggerak di lapangan (*Sourcing*, Logistik, QC, Sales), meyakinkan klien bahwa mereka bermitra dengan ahli sejati.

**Struktur Elemen:**

1. **Organizational Hero:** Pengantar singkat yang menegaskan bahwa *Supply Chain* bergantung pada kolaborasi tim yang solid.
2. **Core Leadership & Experts:** Grid representasi tim dengan gaya korporat. (Contoh profil dari draf: *Head of Sourcing*, *QA Manager*, *Supply Chain Director*, *Sales Manager*). Profil harus ringkas dengan deskripsi fungsional.
3. **Team Culture & Operations Activity:** Visual dokumentasi pelatihan agronomi pascapanen, koordinasi logistik di *loading dock*, atau aktivitas di fasilitas penyimpanan. Hal ini menunjukkan dinamika tim profesional.
4. **Departmental Strengths:** Menguraikan peran spesifik divisi (Misal: ketelitian tim penyortiran/QC, dedikasi tim logistik/Cold Fleet).
5. **CTA Kemitraan:** Transisi langsung dari kepercayaan tim menuju ajakan berdiskusi atau presentasi penawaran B2B.

---

### 2.5 CONTACT & REQUEST QUOTE PAGE - THE LEAD FUNNEL

Ini adalah terminal akhir konversi (Target 30 Detik Eksekusi). Arsitekturnya harus memisahkan interaksi umum (Contact) dari formulir permintaan pengadaan bernilai tinggi (Request Quote).

**Struktur Elemen (Contact Layer):**

1. **Information Hub:** Penempatan jelas untuk lokasi *Head Office* dan alamat fasilitas Gudang Agrikultur (*Cold Storage*).
2. **Communication Channels:** Menampilkan jalur khusus (*Direct Line/WhatsApp Business* B2B), alamat email korporat (misal: *partnership@udnimars.com*), dan waktu operasional layanan klien.

**Struktur Elemen (Request Quote Layer - B2B Form):**

1. **Form Security Badge:** Memberikan indikasi verbal/visual mengenai enkripsi SSL dan privasi perlindungan data *procurement* (*Data Protection Policy*), hal ini krusial untuk B2B.
2. **Frictionless Fields (Minimal Input, Maximum Data):**
* Nama Lengkap (Representatif).
* Nama Perusahaan.
* Email Korporat.
* Nomor WhatsApp / Kontak Langsung.
* Pilihan *Dropdown* Kategori Industri (Hotel & Resort, Jaringan Restoran, Retail Supermarket, Katering Institusional).
* Area Teks Terbuka: Spesifikasi Komoditas (Kalibrasi, jenis kemasan) & Volume Pengadaan Rutin (Tonase).


3. **CTA Submission:** Tombol CTA berukuran penuh ("Kirim Request Quotation" / "Prepare Quotation").
4. **Submission Feedback (Validation State):** Sistem validasi form lokal menggunakan indikator status (*Success toast*) untuk memastikan pengguna memahami umpan balik dari sistem.

## BAGIAN 3: MODULAR COMPONENT ARCHITECTURE & INTERACTIVE LOGIC

Bagian ini mendefinisikan standar rekayasa (*engineering standards*) untuk komponen UI/UX yang digunakan ulang (*reusable components*) di seluruh aplikasi. Spesifikasi ini dirancang untuk memastikan sistem otomasi (*code generator*) membangun elemen antarmuka yang bebas ambiguitas, *accessible*, dan memiliki manajemen *state* yang deterministik.

### 3.1 GLOBAL NAVIGATION & STATE MANAGEMENT

Komponen navigasi merupakan tulang punggung *user experience* dan *conversion funnel*. Desain navigasi menggunakan pola *Floating Capsule Header* yang responsif terhadap *scroll event*.

**A. Floating Capsule Header Specifications:**

* **Default State:** Lebar 95% (maksimal 1400px), berada 24px dari *top viewport*, dengan *background* `rgba(255, 255, 255, 0.98)` atau ekuivalen *glassmorphism* menggunakan `backdrop-filter: blur(10px)`.


* **Scrolled State:** Diaktifkan melalui *event listener* saat `window.scrollY > 80`. Header berpindah ke jarak 16px dari atas, dan *box-shadow* menguat menjadi `0 15px 40px rgba(45, 90, 39, 0.12)` untuk pemisahan visual yang tegas dari konten.


* **Logo Container:** Terpusat (*absolute center* pada desktop) menggunakan format SVG murni (tanpa teks) untuk optimasi LCP (*Largest Contentful Paint*) dan skalabilitas vektor tanpa pecah.


* **Navigation Links (Desktop):** Menggunakan *hover indicator* berupa garis bawah dinamis (warna *Accent Orange* `#F2994A`) yang tumbuh dari tengah ke luar (`width: 0%` ke `100%`).



**B. Off-Canvas Mobile Menu:**

* Dipicu (*triggered*) melalui tombol hamburger menggunakan Lucide Icons.


* **Behavior:** Menggunakan *fixed inset-0* dengan latar belakang layar penuh (`bg-brand-dark/95` dengan `backdrop-blur`). Saat menu terbuka, fungsi *smooth scroll* (Lenis) wajib dihentikan (`lenis.stop()`) untuk mencegah *background scrolling*, dan diaktifkan kembali saat ditutup.



---

### 3.2 FORM PROCESSING & CONVERSION MECHANICS

Formulir *Request Quotation* merupakan titik terminasi dari seluruh konversi bisnis. Oleh karena itu, interaksi pengguna harus direspons dengan sistem validasi yang tidak memberikan celah kebingungan.

A. Input Fields Architecture:

* **Floating Labels:** Semua *input* teks dan area teks harus mengimplementasikan teknik *floating label* murni menggunakan utilitas CSS (`:focus` dan `:not(:placeholder-shown)` *pseudo-classes*). Hal ini mengurangi penumpukan DOM dan menjaga kebersihan antarmuka.
* **Icon Integration:** Mengharuskan penggunaan *inline-SVG* atau *icon library* (Lucide) di dalam *wrapper input* untuk mempertegas konteks *field* (misal: ikon gedung untuk Nama Perusahaan).



**B. Form State Handling & Validation Protocol:**
Sistem wajib mengelola empat *state* absolut saat pengguna berinteraksi dengan form RFQ:

1. **Default/Typing State:** Batas *input* berwarna `Border #E5E7EB` dengan latar abu-abu terang. Saat fokus, *border* berubah menjadi `Primary Green #2D5A27` dengan efek cincin (*focus ring*).
2. **Error State (Client-Side Validation):** Validasi *real-time* wajib memblokir pengiriman (*submission*). Jika kolom kosong atau format email salah, *border input* berubah menjadi merah (`#EF4444`) dan memunculkan pesan *error inline* spesifik tanpa perlu *reload* halaman. Peringatan ini harus segera terhapus (*clearError*) saat pengguna mulai mengetik kembali.


3. **Processing State:** Saat tombol "Kirim" ditekan, fungsi *submit* (misal: `handleFormSubmit(e)`) dipicu. Tombol CTA diubah ke status `disabled = true`, transparansi turun (`opacity: 0.8`), dan teks tombol berubah menjadi indikator *loading* (misalnya: "Memproses Enkripsi...") disertai rotasi SVG *spinner*.


4. **Success State (Toast Notification):** Pasca-simulasi jaringan (atau respons API faktual), formulir akan mereset nilai input (`e.target.reset()`). Pesan keberhasilan tidak ditampilkan dengan *alert browser* bawaan, melainkan memunculkan komponen *Toast Notification* yang melayang masuk dari bawah atau pojok kanan (`translateY(0)` dari `translateY(150px)`), berwarna hijau (`Success #22C55E`), dan otomatis menghilang (*auto-dismiss*) setelah 5 detik.



---

### 3.3 THEME LOGIC (DARK MODE) & INTERNATIONALIZATION (i18n)

Sebagai perusahaan rantai pasok B2B modern, adaptabilitas platform terhadap preferensi pengguna tingkat tinggi dieksekusi secara struktural, bukan sekadar pelapis visual.

A. Dark Mode Global Switcher:

* **Arsitektur CSS Variables:** Menggunakan fitur bawaan `darkMode: 'class'` dari konfigurasi Tailwind CSS. Hal ini mengizinkan penulisan kelas berawalan `dark:` pada setiap komponen (contoh: `bg-white dark:bg-slate-900`).


* **Toggle Behavior:** Tombol sakelar terintegrasi di *Header* bagian kiri. Modifikasi *state* dilakukan dengan menambah atau menghapus kelas `.dark` pada elemen `<body>`. Perubahan ikon sakelar antara Matahari (*Light*) dan Bulan (*Dark*) dieksekusi dengan manipulasi kelas pembantu utilitas `.hidden`.

B. i18n (Internationalization) Data Mapping:

* **DOM Structure:** Teks yang berpotensi diterjemahkan (ID/EN) tidak boleh di-*hardcode* sebagai properti mutlak tanpa pengait. Setiap simpul teks (*text node*) harus memiliki atribut pengenal `data-i18n="[kunci-translasi]"`.
* **Switching Logic:** Saat tombol Bahasa ditekan, fungsi JavaScript akan melakukan iterasi massal terhadap semua elemen DOM yang memiliki atribut `data-i18n` dan menukar isi properti `innerHTML` berdasarkan kamus objek JSON atau objek JS (*Localization Dictionary*) tanpa melakukan *page reload*.

---

### 3.4 STRICT ANIMATION & INTERACTIVITY DIRECTIVES

Untuk melindungi *Core Web Vitals* dan persepsi otoritas korporat, aturan interaksi ditetapkan dengan sangat ketat (mengacu pada pedoman pelarangan animasi berlebih di draf dokumen).

**A. Komponen Interaksi yang Diwajibkan:**

* **Native Reveal (Intersection Observer):** Elemen halaman yang berada di bawah lipatan (*below-the-fold*) harus memuat menggunakan metode *fade-up* (`opacity: 0` menuju `opacity: 1`, `translateY(40px)` menuju `translateY(0)`) yang digerakkan secara efisien oleh API bawaan *Intersection Observer*, meminimalkan latensi manipulasi DOM berulang pada *scroll event*. Komponen harus menetapkan `will-change: opacity, transform` di CSS.


* **Micro-interactions Haptic/Elastic:** Tombol CTA atau *Card* portofolio harus menggunakan transisi transform halus saat di-*hover* (`scale: 1.05` untuk *card*, `scale: 1.01` untuk desain *tilt*) dan efek penekanan (`scale: 0.95` pada state `:active`).


* **Marquee / Infinite Scroll Horizontal:** Diizinkan hanya untuk kompilasi logo klien (Portofolio/Trust Bar) yang diselesaikan sepenuhnya menggunakan animasi kunci CSS murni (`@keyframes marqueeScroll`) tanpa manipulasi rekursif JavaScript.



**B. Komponen Interaksi yang DIHAPUSKAN (Deprecation Protocol):**

* Berdasarkan profil B2B kelas atas, integrasi elemen `custom-cursor` (titik kursor yang melacak pergerakan tetikus via JS berpotensi *delay/lag*) yang terdapat pada *stack* sebelumnya **DIHAPUS SECARA TOTAL**.


* *Heavy GSAP Parallax Sequences*, efek bayangan kursor *magnetic* yang mendistorsi elemen saat *hover*, serta manipulasi model 3D kompleks dihentikan operasinya demi mencapai Time to Interactive (TTI) instan.



## BAGIAN 4: DATA SCHEMA, ACCESSIBILITY (A11Y), SEO & DEPLOYMENT PROTOCOL

Bagian terakhir ini mendefinisikan skema data untuk integrasi *backend*, standar aksesibilitas, optimasi mesin pencari (SEO) tingkat korporat, serta protokol *deployment* untuk memastikan seluruh target metrik performa UD NIMARS tercapai tanpa regresi.

### 4.1 RFQ DATA SCHEMA & SECURITY PAYLOAD BLUEPRINT

Formulir *Request for Quotation* (RFQ) pada halaman Kontak dan pop-up modal tidak boleh dikirimkan sebagai form HTML tradisional (`application/x-www-form-urlencoded`). Untuk memastikan keamanan dan integrasi langsung dengan sistem CRM atau ERP *procurement*, data harus diserialisasi menjadi JSON *payload* yang terstruktur.

**Struktur JSON Payload (B2B Inquiry Schema):**
Mengacu pada arsitektur form eksisting, sistem *front-end* wajib merangkai objek data berikut sebelum dienkripsi dan ditransmisikan melalui protokol HTTPS/SSL:

```json
{
  "inquiry_id": "REQ-UUID-TIMESTAMP",
  "timestamp": "ISO-8601-FORMAT",
  "client_data": {
    "full_name": "string (Required, max 100 chars)",
    "company_name": "string (Required, max 150 chars)",
    "corporate_email": "string (Required, Valid Email Format)",
    "whatsapp_number": "string (Required, Numeric, Valid E.164 Format)"
  },
  "procurement_details": {
    "industry_category": "enum [hotel, resto, retail, other] (Required)",
    "supply_frequency": "enum [harian, mingguan, insidental] (Required for specific endpoints)",
    "commodity_specification": "text (Required, sanitised string, max 1000 chars)"
  },
  "consent": {
    "data_protection_agreed": "boolean (Must be true)"
  },
  "metadata": {
    "source_language": "enum [id, en]",
    "utm_source": "string (Optional for marketing attribution)"
  }
}

```

**Aturan Penanganan (*Handling Rules*):**

* **Sanitisasi Klien:** Sebelum data diubah menjadi JSON, semua *field input* wajib disanitisasi dari potensi injeksi skrip (XSS) pada fungsi `handleFormSubmit`.


* **Graceful Degradation:** Jika API gagal merespons, komponen *Toast Notification* yang sebelumnya diatur untuk status *Success* harus secara dinamis menampilkan pesan "Terjadi kesalahan koneksi" dengan warna *Error* merah (`#EF4444`), bukan membiarkan pengguna terjebak pada status *loading*.



---

### 4.2 SEO, ACCESSIBILITY (A11Y) & SEMANTIC ARCHITECTURE

Sebagai platform B2B yang menargetkan pencarian organik oleh eksekutif pengadaan, arsitektur *Multi Page Application* (MPA) harus dieksekusi dengan kepatuhan SEO teknis dan aksesibilitas (WCAG 2.1 AA) tingkat tertinggi.

**1. Meta Data & Head Architecture:**

* Setiap dokumen HTML wajib memiliki tag `<meta name="description" content="...">` yang unik dan deskriptif.


* Penambahan atribut `class="antialiased scroll-smooth"` pada tag `<html>` untuk *rendering* tipografi yang lebih tajam dan navigasi dasar yang halus.


* Integrasi tag `<meta name="robots" content="index, follow">` pada seluruh halaman publik untuk memastikan proses *crawling* optimal.



2. Standar Aksesibilitas (a11y):

* **Atribut ARIA:** Semua tombol yang menggunakan ikon tanpa teks (seperti tombol *Hamburger Menu* atau *Close Modal*) wajib dilengkapi dengan atribut `aria-label="Toggle Menu"` atau `aria-label="Close"`.


* **Kontras Warna:** Kombinasi *Primary Green* (`#2D5A27`) dengan teks putih, dan *Accent Orange* (`#F2994A`) di atas kanvas gelap/terang telah lulus rasio kontras standar. Sistem otomatisasi wajib mematuhi pemetaan token ini.


* **Focus Management:** Elemen form dan *dropdown* telah dikonfigurasi dengan cincin fokus (`box-shadow: 0 0 0 4px rgba...`) untuk memberikan umpan balik visual yang jelas bagi pengguna yang menavigasi menggunakan *keyboard*.



---

### 4.3 PERFORMANCE BUDGET & PRODUCTION DEPLOYMENT PROTOCOL

Untuk memenuhi mandat performa (PageSpeed > 90, LCP < 2.5s), setiap baris kode yang digenerasi oleh sistem (seperti Antigravity) wajib melewati *performance budget* berikut sebelum dikerahkan ke tahap *Production*.

**A. Optimasi Aset & Library:**

* **Tailwind CSS Compilation:** Seluruh kelas utilitas Tailwind harus di-*purge* atau dikompilasi menggunakan JIT (*Just-In-Time*) *compiler* untuk menghasilkan file CSS statis yang sangat ringan. Penggunaan `<script src="[https://cdn.tailwindcss.com](https://cdn.tailwindcss.com)"></script>` **HANYA** diperbolehkan di lingkungan *Development*.


* **Eksekusi Skrip Eksternal:** Pemuatan pustaka eksternal seperti GSAP, ScrollTrigger, Lucide Icons, dan Lenis wajib diposisikan di akhir dokumen (sebelum `</body>`) atau menggunakan atribut `defer` agar tidak memblokir *Main Thread* saat DOM melakukan *parsing*.



**B. Resolusi Kinerja Visual:**

* **CLS (Cumulative Layout Shift):** Ditetapkan pada batas **< 0.1**. Gambar yang dirender, khususnya pada komponen *Card* di halaman *Products* dan *Team*, harus memiliki reservasi rasio aspek (misal: `aspect-[4/5]` atau tinggi/lebar absolut) untuk mencegah pergeseran *layout* secara tiba-tiba saat file WebP dimuat.


* **Preloading Critical Assets:** *Web font* Montserrat dan Inter harus dipanggil dengan instruksi `<link rel="preconnect">` ke Google Fonts untuk memangkas *Time to First Byte* (TTFB) dan menghindari FOIT (*Flash of Invisible Text*).



**C. Final Deployment Checklist:**

1. **Hapus Dead Code:** Singkirkan semua sisa eksperimen animasi interaktif (*custom cursor*, *blob tracking*) dan modifikasi *marquee* berlebih yang melanggar direktif efisiensi.


2. **Minifikasi:** Lakukan minifikasi pada HTML, CSS, dan file skrip lokal.
3. **Link Integrity:** Pastikan semua tautan pintas di area *Footer* (Tentang Kami, Produk, Tim Kami, Kontak Kami) mengarah ke URL `.html` yang tepat secara relatif.



---

### KESIMPULAN PRD

Dokumen *Product Requirement Document* V2 ini kini menjadi spesifikasi *blueprint* absolut yang utuh (Bagian 1 hingga Bagian 4). Dengan eliminasi anomali teknis (seperti animasi kursor berat) dan penerapan pola desain *Enterprise B2B*, UD NIMARS akan diproyeksikan tidak hanya sebagai platform informasi, melainkan infrastruktur *lead generation* yang sangat dioptimalkan, memancarkan integritas kualitas yang konsisten sejalan dengan komoditas yang mereka suplai. Sistem *generator* dapat segera memulai kompilasi basis kode berdasarkan mandat ini.