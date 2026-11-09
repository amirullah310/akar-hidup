# PRODUCT REQUIREMENTS DOCUMENT (PRD)
## AKARHIDUP — Every Root Has a Story

| Metadata | Keterangan |
|---|---|
| ID dokumen | AKH-PRD-001 |
| Versi | 1.0 — Draft implementasi kompetisi |
| Tanggal | 9 November 2026 |
| Status | Baseline produk; asumsi dan fitur lanjutan harus divalidasi |
| Kategori | INVOFEST 2026 — Web Design Competition, Mahasiswa |
| Subtema | Green Tech & Sustainable Environment (SDG 12 & 13; mangrove turut relevan dengan SDG 14/15 secara dampak tematik) |
| Slogan | Every Root Has a Story |
| Tahap | MVP prototipe interaktif berbasis data simulasi |
| Sumber | Guidebook Web Design INVOFEST 2026, halaman 3, 4, 9–14; laman resmi kompetisi (diakses 9 Nov 2026) |

> **PENTING:** AKARHIDUP pada versi lomba merupakan prototipe konsep dan **bukan** sistem monitoring mangrove operasional atau digital twin lapangan real-time. Semua data, nama zona, koordinat contoh, foto ilustratif, dan metrik di dataset demo HARUS diberi label **Data Simulasi / Ilustrasi** kecuali memiliki sumber dan izin pemakaian yang jelas.

---

## 1. Ringkasan eksekutif

**AKARHIDUP** adalah platform web untuk membantu publik, relawan, dan pengelola memahami perjalanan pemulihan mangrove setelah kegiatan penanaman. Nilai utamanya bukan menampilkan berapa banyak bibit pernah ditanam, melainkan menghubungkan **lokasi → observasi → perubahan dari waktu ke waktu → bukti → tindak lanjut**.

Produk menghadirkan peta zona mangrove interaktif, _growth journey_ berbasis tanggal pengamatan, perbandingan dokumentasi sebelum–sesudah, daftar laporan gangguan, dan antrean prioritas **pemantauan** yang transparan. Pengguna bisa membuka zona pada peta, memeriksa data dan validitasnya, membandingkan perkembangan antarperiode, dan menyampaikan laporan yang dapat ditinjau.

**Janji produk:** _See the change. Understand the evidence. Support the recovery._

**Batas penting:** indikator tanaman hidup hanyalah salah satu ukuran; keberhasilan pemulihan ekosistem harus mempertimbangkan konteks habitat, hidrologi, regenerasi alami, biodiversitas, dan validasi ahli. Skor antrean tindak lanjut bukan diagnosis ekologis.

## 2. Konteks lomba dan keputusan produk

- **Tema utama guidebook:** Smart Ecosystems: Digital Solutions for a Sustainable Future (hal. 3 dan 9).
- **Subtema dipilih:** Green Tech & Sustainable Environment (guidebook SDG 12 & 13, hal. 9).
- **Teknis wajib:** HTML, CSS, JavaScript; framework diperbolehkan, _full template_ dan CMS dilarang (hal. 9).
- **Penyisihan:** Desain 30%, Kreativitas/Inovasi 25%, Kemudahan/Responsivitas 20%, Orisinalitas 15%, Kesesuaian Tema 10% (hal. 13).
- **Final:** Presentasi 60%, Tanya Jawab 40%; durasi presentasi 5 menit, tanya jawab 10 menit (hal. 12 dan 14).
- **Berkas:** PDF deskripsi karya, tautan akses karya/source, video demo publik 3–10 menit dengan resolusi min. 720p, lembar orisinalitas (hal. 9–11).
- **Jadwal:** PDF guidebook hal. 4 menuliskan pengumpulan 7 Nov 2026; laman resmi per 9 Nov mencantumkan batas pengumpulan **11 Nov 2026**. Jadwal lain dan format unggah harus dikonfirmasi pada kanal resmi, karena guidebook memiliki inkonsistensi penamaan berkas demo (Web Design/UI/UX) dan tanggal pendaftaran.

**Dampak pada keputusan:** prioritaskan pengalaman interaktif berkualitas tinggi dan demonstrasi yang selesai; hindari memperluas MVP menjadi layanan penginderaan jauh, AI diagnostik, sensor IoT, atau GIS nasional.

## 3. Problem statement

### 3.1 Masalah inti

Informasi restorasi sering ditampilkan sebagai keluaran kegiatan (jumlah bibit, agenda, foto kegiatan). Namun, audiens awam sulit memeriksa **perkembangan pasca-intervensi** dan menghubungkan hasil pemantauan dengan lokasi, waktu, bukti, dan tindakan berikutnya.

### 3.2 Job-to-be-done

> Ketika ingin mengetahui apakah suatu lokasi mangrove menunjukkan perkembangan dan membutuhkan perhatian, pengguna ingin melihat perubahan per periode bersama bukti yang bisa ditelusuri, agar dapat memahami kondisinya dan memutuskan partisipasi/tindakan berikutnya.

### 3.3 Hipotesis produk

Jika satu situs menyajikan perjalanan pemulihan per zona dalam narasi visual yang mudah dibaca, data bertanggal, penanda verifikasi, dan tindak lanjut, maka pengguna akan lebih mudah memahami kondisi yang dilaporkan dibanding hanya melihat angka agregat dan dokumentasi acara.

### 3.4 Asumsi yang BELUM tervalidasi

A1. Komunitas konservasi bersedia mengunggah observasi dan foto berkala.  
A2. Pengguna publik menganggap dokumentasi berdasarkan zona/interval lebih informatif daripada galeri foto.  
A3. Data zona berkoordinat dan status tindak lanjut dapat diperoleh secara konsisten dari mitra.  
A4. Pengelola menerima antrean prioritas yang dijelaskan secara transparan.  
A5. Data spasial yang dibagikan tidak membuka lokasi sensitif atau menimbulkan risiko lingkungan/privasi.

## 4. Visi, tujuan, dan batasan

### 4.1 Visi

Membuat proses pemulihan kawasan mangrove lebih mudah dipahami dan ditindaklanjuti melalui pengalaman web yang indah, inklusif, serta jujur terhadap kualitas datanya.

### 4.2 Tujuan MVP

1. Mendemonstrasikan alur eksplorasi kawasan dari hero hingga zona secara intuitif.
2. Menampilkan **minimal 1 lokasi demo dan 3 zona demo** dengan kondisi berbeda dan metadata sumber.
3. Menyediakan **minimal 3 periode observasi per zona**, beserta grafik, tanggal, dan indikator penjelasan.
4. Memungkinkan perbandingan dokumentasi sebelum–sesudah pada satu zona.
5. Menampilkan laporan gangguan dan hasil prioritas pekerjaan yang dapat diterangkan aturannya.
6. Menyediakan alur formulir laporan demonstrasi yang memvalidasi input dan menyimpan draft secara lokal.
7. Menjalankan pengalaman desktop dan ponsel dengan aksesibilitas dasar.
8. Mempunyai URL demo, source code terstruktur, PDF ringkasan, dan video presentasi.

### 4.3 Non-goals (bukan ruang lingkup MVP)

- Pemantauan real-time otomatis / perangkat sensor nyata.
- Prediksi keberhasilan ekologis atau estimasi emisi/karbon tanpa model tervalidasi.
- Mengukur jumlah pohon individual dari citra satelit resolusi rendah.
- Marketplace donasi, pembayaran, atau penggalangan dana.
- Manajemen multi-instansi dengan izin kompleks.
- Klaim sertifikasi atau audit dampak lingkungan.
- Pengganti observasi lapangan oleh tenaga kompeten.

## 5. Target pengguna

| Persona | Tujuan | Pain point | Tugas utama di MVP |
|---|---|---|---|
| Nadia — mahasiswa/pengunjung | Memahami perubahan kawasan | Grafik teknis sulit dibaca | Explore → zona → timeline → bukti |
| Fajar — relawan konservasi | Mengunggah kondisi yang ditemukan | Dokumentasi tercecer | Pilih zona → laporan → cek status |
| Maya — koordinator pengelola | Menentukan tindak lanjut | Laporan tidak terurut | Dashboard → prioritas → alasan → aksi |

**Persona ini adalah asumsi desain**, bukan hasil wawancara pengguna sungguhan.

## 6. Value proposition dan positioning

**Value proposition:** _Living restoration story_ — satu tempat untuk menelusuri lokasi, perkembangan, dasar pengamatan, serta langkah tindak lanjut.

**Positioning:** pengalaman komunikasi dan kolaborasi pemulihan di tingkat zona yang melengkapi platform geospasial atau pencatatan konservasi yang lebih teknis; **bukan klaim platform mangrove pertama**.

**Prinsip desain produk:**
1. Data harus mempunyai konteks (kapan, dari mana, bagaimana).
2. Setiap visual mempunyai tindakan atau pemahaman yang jelas.
3. Status pemantauan bukan klaim kesehatan ekosistem.
4. Visual kuat tanpa mengorbankan performa dan aksesibilitas.
5. Konten demo secara eksplisit ditandai sebagai simulasi.

## 7. Ruang lingkup fitur dan prioritas

| ID | Fitur | Prioritas | Release | Deskripsi |
|---|---|---|---|---|
| F01 | Homepage storytelling | P0 | MVP | Narasi editorial, CTA dan preview produk |
| F02 | Explore map | P0 | MVP | Zona/poligon interaktif, legenda, filter |
| F03 | Site & zone details | P0 | MVP | Profil, metadata, status, sumber data |
| F04 | Growth Journey | P0 | MVP | Pilih periode, perbarui grafik dan detail observasi |
| F05 | Before–after evidence | P0 | MVP | Slider dua foto yang tersedia dan bertanggal |
| F06 | Monitoring priority | P1 | MVP jika waktu cukup | Antrean tindak lanjut berbasis aturan transparan |
| F07 | Community report demo | P1 | MVP jika waktu cukup | Validasi, simpan lokal, label demo |
| F08 | Report status tracking | P1 | MVP jika waktu cukup | Draft/pending/verified/resolved dalam simulasi |
| F09 | Accessible mobile navigation | P0 | MVP | Menu, map list fallback, kontrol sentuh |
| F10 | Editorial story cards | P1 | MVP jika waktu cukup | Narasi berbasis sumber, tanpa data fiktif yang dipresentasikan sebagai fakta |
| F11 | Accounts & roles | P2 | Future | Autentikasi, izin relawan/pengelola |
| F12 | Shared database & uploads | P2 | Future | Sinkronisasi, verifikasi, audit trail |
| F13 | Sensor/remote sensing import | P3 | Research | Integrasi data lapangan/analisis satelit |
| F14 | 3D visual twin | P3 | Research | Visualisasi ruang tiga dimensi; jangan klaim live tanpa integrasi |

> P0 = wajib selesai; P1 = boleh dipangkas tanpa merusak cerita inti; P2/P3 = roadmap, tidak dipresentasikan sebagai sudah jadi.

## 8. Functional requirements (FR)

### FR-01 — Home & navigation

- FR-01.1: Homepage memiliki CTA utama **Explore the Forest** menuju `/explore`.
- FR-01.2: Header desktop memuat Home, Explore, Growth Journey, Action Center, About; menu mobile bisa dibuka/ditutup via keyboard.
- FR-01.3: Semua link menampilkan halaman yang benar atau state penjelasan; tidak ada tombol hiasan yang berpura-pura bekerja.
- FR-01.4: Scroll animation tidak menjadi prasyarat membaca konten.

### FR-02 — Explore kawasan

- FR-02.1: Peta menampilkan lokasi demo beserta tiga zona yang dapat dipilih.
- FR-02.2: Pengguna dapat memilih zona dengan mouse, touch, keyboard melalui **alternatif daftar**, dan marker/layer peta.
- FR-02.3: Filter minimal: status pemantauan (normal, perlu ditinjau, prioritas tindakan) dan periode terakhir.
- FR-02.4: Klik zona menampilkan kartu ringkas: nama, status, observasi terakhir, indikator tersedia, CTA detail.
- FR-02.5: Apabila tile peta gagal dimuat, daftar zona dan informasinya tetap dapat diakses.
- FR-02.6: Sumber dasar peta dan atribusi ditampilkan sesuai lisensi penyedia.

### FR-03 — Zone detail

- FR-03.1: Tiap zona memiliki identitas unik, nama, dan hubungan ke kawasan.
- FR-03.2: Profil memuat ukuran area jika tersedia, tanggal aktivitas, tujuan rehabilitasi, indikator, serta status keterkinian.
- FR-03.3: Tidak menampilkan label **sehat/gagal** secara otomatis hanya dari persentase bibit hidup.
- FR-03.4: Setiap grafik/metrik menampilkan tanggal observasi dan sumber.
- FR-03.5: Bila data indikator belum ada, tampilkan **Belum ada data**, bukan angka nol.

### FR-04 — Growth Journey

- FR-04.1: Pengguna memilih satu periode observasi yang valid (tanggal ISO).
- FR-04.2: Angka, deskripsi, grafik, dan dokumentasi bergerak sinkron terhadap periode yang dipilih.
- FR-04.3: Jumlah awal dan jumlah hidup selalu dikontekstualkan dengan metode pendataan/sampel.
- FR-04.4: Perbandingan indikator hanya dilakukan pada metode dan unit yang sebanding; bila tidak, munculkan catatan.
- FR-04.5: Pengguna dapat menavigasi timeline dengan keyboard, bukan hanya drag.

### FR-05 — Before–after

- FR-05.1: Slider menampilkan 2 bukti foto **dari zona/titik yang sesuai** (jika tersedia).
- FR-05.2: Label lokasi, tanggal, dan sumber foto terlihat.
- FR-05.3: Bila sudut pengambilan foto berbeda, tampilkan peringatan **foto tidak sepenuhnya sebanding**.
- FR-05.4: Komponen tidak boleh menyiratkan foto AI-generated sebagai bukti lapangan.

### FR-06 — Priority queue

- FR-06.1: Antrean tindakan dihitung dari **jadwal pemantauan** dan **laporan yang telah terverifikasi**; laporan belum diverifikasi menjadi antrean verifikasi, bukan fakta lapangan.
- FR-06.2: Prioritas memuat `priority_level`, `reason_codes`, `last_observation_at`, `next_action`.
- FR-06.3: Pengguna dapat membuka panel **Mengapa diprioritaskan?**.
- FR-06.4: Aturan dapat dijalankan ulang secara deterministik untuk dataset yang sama.
- FR-06.5: Label antrean adalah *prioritas pemantauan*, bukan prediksi tingkat kerusakan ekologis.

### FR-07 — Community report (demo)

- FR-07.1: Pengguna memilih zona, jenis temuan, tanggal, keterangan, dan optional gambar demo.
- FR-07.2: Validasi: zona dan jenis wajib; tanggal tidak boleh di masa depan; keterangan 20–1000 karakter; tipe berkas gambar dibatasi; ukuran file maksimal disesuaikan limit aplikasi.
- FR-07.3: Form memiliki success state **Laporan tersimpan di perangkat ini (mode demo)**.
- FR-07.4: Tidak ada klaim pengiriman ke pengelola jika hanya memakai localStorage.
- FR-07.5: Informasi sensitif (nomor telepon, lokasi presisi orang) tidak ditampilkan publik.

### FR-08 — Empty/error/loading

- FR-08.1: Semua halaman utama memiliki state loading dan error apabila relevan.
- FR-08.2: Data kosong menyertakan instruksi pemulihan atau konteks.
- FR-08.3: Error tile peta tidak merusak akses data zona.
- FR-08.4: Komponen tidak memunculkan _layout shift_ besar saat data/gambar dimuat.

## 9. User stories & acceptance criteria

### US-01 — Eksplorasi kawasan
**As a** pengunjung, **I want** memilih zona peta, **so that** saya dapat membuka informasi pemantauannya.
- GIVEN halaman Explore dimuat, WHEN pengguna memilih zona A, THEN detail ringkas zona A tampil dan dapat membuka halaman detail.
- GIVEN peta gagal dimuat, WHEN pengguna memakai daftar zona, THEN seluruh zona tetap bisa dibuka.

### US-02 — Membandingkan waktu
**As a** pengunjung, **I want** memilih periode, **so that** saya dapat menilai perubahan yang didokumentasikan.
- GIVEN zona memiliki tiga periode, WHEN saya pindah dari T0 ke T2, THEN judul waktu, grafik, foto, dan catatan ikut berubah tanpa reload.
- GIVEN indikator belum tersedia, THEN tampil pesan **Data belum tersedia**.

### US-03 — Melihat kualitas bukti
**As a** pengunjung, **I want** melihat sumber foto/observasi, **so that** saya tahu apakah informasi merupakan simulasi atau data terverifikasi.
- GIVEN observasi demo, THEN label **Data Simulasi** terlihat di detail dan saat grafik diunduh/ditampilkan.

### US-04 — Mengerti prioritas
**As a** koordinator, **I want** membaca alasan antrean, **so that** saya tahu tindakan yang disarankan.
- GIVEN laporan belum diverifikasi, THEN aplikasi tidak otomatis menandainya sebagai kerusakan nyata.
- GIVEN aturan dan data sama, THEN hasil penentuan prioritas konsisten.

### US-05 — Melaporkan kondisi
**As a** relawan, **I want** membuat laporan, **so that** sebuah temuan tercatat untuk demonstrasi.
- GIVEN form valid, WHEN submit, THEN laporan muncul di daftar lokal dan ada penjelasan bahwa data tidak dikirim ke server.
- GIVEN field wajib kosong, WHEN submit, THEN error dekat field dan fokus diarahkan dengan benar.

### US-06 — Akses mobile
**As a** pengguna ponsel, **I want** mengakses peta/list dan timeline, **so that** fitur inti tetap dapat dipakai dengan satu tangan.
- GIVEN lebar layar 360 px, THEN tidak ada horizontal overflow dan CTA utama dapat dipakai.

## 10. Model interaksi dan alur pengguna

**Primary flow:** Home → Explore → pilih kawasan → pilih zona → Zone Detail → Growth Journey → evidence → Action Center.

**Secondary flow:** Home/Explore → pilih zona → Report Issue → input & validasi → simpan lokal → lihat daftar laporan.

**Priority flow:** Action Center → filter antrean → pilih zona → baca alasan → tandai tindak lanjut simulasi.

**State map:** `initial → loading → success | empty | error`; laporan: `draft → pending_review → verified | rejected → in_progress → resolved` (MVP demo hanya subset; tidak boleh menampilkan status verifikasi palsu dari pengguna publik).

## 11. Konten dan data minimum

- 1 lokasi demo, 3 zona demo A/B/C; **nama fiktif tanpa mengklaim lokasi nyata**.
- 3 observasi bertanggal per zona (T0, T1, T2), dengan struktur dan metode konsisten.
- 2 foto per zona bila tersedia untuk perbandingan; jika aset belum ada, gunakan placeholder berlabel ilustrasi.
- 3 contoh laporan (masing-masing status berbeda dan tetap berlabel demo).
- 3 alasan antrean pekerjaan yang dapat dijelaskan.
- 1 halaman "How we interpret data" yang singkat tentang observasi, verifikasi, dan keterbatasan.

**Konvensi:** tidak menghitung `survival_rate` jika denominator tidak ada/berbeda metode; `null` bukan `0`; urutan observasi ascending by date; tampilkan satuan `cm`, `ha`, dan tanggal dengan label eksplisit.

## 12. Non-functional requirements (NFR)

| ID | Area | Kriteria target MVP |
|---|---|---|
| NFR-01 | Responsive | Layout 360, 390, 768, 1024, 1440 px tanpa overflow utama |
| NFR-02 | Accessibility | Keyboard nav, focus visible, alt text, label form, kontras mendekati WCAG 2.2 AA |
| NFR-03 | Motion | Hormati prefers-reduced-motion, gerakan non-essential bisa dikurangi |
| NFR-04 | Performance | Target Lighthouse Performance ≥ 85 dan Accessibility ≥ 90 pada halaman inti sebagai target, bukan jaminan |
| NFR-05 | Security | Sanitasi input, tidak menggunakan unsafe innerHTML untuk laporan, CSP/dependency review bila deploy |
| NFR-06 | Privacy | Tidak memublikasikan identitas pelapor atau metadata EXIF sensitif |
| NFR-07 | Reliability | Build production sukses, reload nested route tidak 404, fallback map tersedia |
| NFR-08 | Transparency | Label simulasi konsisten di semua halaman dan demo |
| NFR-09 | Maintainability | TypeScript strict, modul terpisah, lint, unit test aturan prioritas |
| NFR-10 | Attribution | Lisensi peta, foto dan sumber data ditampilkan sesuai ketentuan |

## 13. Metrik keberhasilan

**Metrik validasi prototipe (target internal, belum hasil uji):**
- ≥ 80% dari ≥ 5 penguji dapat menemukan zona prioritas dan menjelaskan alasannya tanpa bantuan.
- ≥ 80% dari ≥ 5 penguji dapat berpindah dua periode dan mengidentifikasi observasi terakhir.
- Semua tugas P0 berfungsi dalam demo langsung dan layar mobile.
- 0 tombol mati pada alur penilaian; 0 klaim data lapangan tanpa sumber/label.
- Lighthouse dan QA target sesuai NFR; semua temuan kritis diperbaiki sebelum submit.

**North-star masa depan (bukan metrik lomba):** proporsi zona aktif dengan observasi terverifikasi tepat waktu dan tindakan yang dapat ditelusuri. Jangan membuat klaim dampak ekologis hanya dari analytics website.

## 14. Dependensi dan risiko

| Risiko | Dampak | Mitigasi |
|---|---|---|
| Waktu sangat pendek | Fitur P1 tidak selesai | Freeze scope P0, satu demo utama |
| Peta provider gagal | Explore tidak berfungsi | Data list fallback + cached/demo snapshot bila diperlukan |
| Klaim digital twin berlebihan | Kredibilitas turun | Sebut representasi digital historis/prototipe digital twin |
| Foto tidak sebanding | Interpretasi salah | Timestamp, titik, dan disclaimer |
| Prioritas disalahartikan | Kesimpulan keliru | Label prioritas operasional, alasan terbuka |
| Aturan submission kontradiktif | Berkas ditolak | Cek template dan kanal panitia terakhir |
| Sumber aset/lisensi tidak jelas | Risiko orisinalitas | Aset milik tim / berlisensi, catat atribusi |

## 15. Definisi selesai (Definition of Done)

Sebuah fitur selesai jika: dapat dijalankan pada build produksi; semua state penting dapat diamati; data demo diberi label; keyboard dan mobile diuji; tidak ada error console kritis; code di-review; screenshot dan video dapat menunjukkan hasilnya; acceptance criteria lulus.

**Release MVP selesai jika:** semua fitur P0 lulus, URL aktif, source siap, PDF dan video tersedia, lembar orisinalitas siap, semua tautan sesuai instruksi panitia.

## 16. Keputusan terbuka

1. Apakah nama final tetap **AKARHIDUP** dan slogan berbahasa Inggris?
2. Apakah peta demo akan menggunakan lokasi fiktif atau lokasi nyata berizin?
3. Dari tiga zona demo, indikator apa yang bisa ditampilkan secara konsisten?
4. Apakah submission memerlukan upload cloud dan repo **publik** atau cukup akses yang dapat dibuka panitia?
5. Apakah fitur laporan disimpan lokal atau ditambah Supabase bila waktu tersedia?
6. Siapa pemegang review akhir konten, desain, dan berkas lomba?

## 17. Sumber, batas pengetahuan, dan pelacakan

**Sumber persyaratan kompetisi:** `Guidebook lomba Web Design Design.pdf` (hal. 3–4, 9–14) dan laman resmi https://www.invofest-harkatnegeri.com/competition/web-design (diakses 9 November 2026). Jika berbeda, gunakan pengumuman panitia terakhir dan simpan bukti komunikasi.

**Landasan bidang:** Global Mangrove Alliance, Best Practice Guidelines for Mangrove Restoration, https://www.mangrovealliance.org/id/best-practice-guidelines-for-mangrove-restoration — pedoman menekankan restorasi ekologis, konteks lokal, dan pemantauan/adaptive management. Ini mendukung penentuan fokus produk, **bukan validasi** semua desain, indikator, maupun algoritme AKARHIDUP.

**Sumber teknis:** MapLibre https://maplibre.org/maplibre-gl-js/docs/; pilihan library lain merupakan rekomendasi desain/rekayasa, bukan persyaratan guidebook.

---

**Catatan versioning:** dokumen lain dalam paket ini (`02` sampai `07`) menjabarkan detail implementasi PRD ini. Ketika scope berubah, naikkan nomor versi dan catat perubahan agar tim tidak mengembangkan spesifikasi yang berbeda.
