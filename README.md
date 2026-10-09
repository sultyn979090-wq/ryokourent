# Ryokourent - Rental Sepeda Motor Malang Raya & Kota Wisata Batu

Aplikasi dan sistem manajemen rental sepeda motor dengan pendekatan *zero-friction WhatsApp booking*, performa mobile-first, dan regulasi perlindungan data pribadi (UU PDP No. 27/2022).

---

## 🛵 Profil Bisnis
* **Brand:** Ryokourent
* **Kategori:** Rental Sepeda Motor & Adventure Fleet
* **Wilayah Layanan:** Malang Raya (Kota & Kabupaten Malang) dan Kota Wisata Batu
* **Dua Pool Resmi:**
  * **Pool 1 (Malang):** Jl. MT Haryono Gg. 21 No. 23, Dinoyo, Lowokwaru, Malang
  * **Pool 2 (Kota Batu):** Jl. Belakang Pompa Bensin, Jl. Diponegoro, Batu
* **Jam Operasional:** 07.00 – 23.00 WIB
* **Layanan Antar/Jemput:** Menyesuaikan situasi dan kondisi armada (sikon)

---

## 📂 Struktur Repositori

```text
/
├── README.md                           # Dokumentasi utama proyek & panduan ringkas
├── BLUEPRINT.md                        # Spesifikasi kebutuhan bisnis, arsitektur & wireframe
├── PROJECT_OVERVIEW.md                 # Ringkasan tujuan bisnis, target pengguna, MVP & batasan
├── ARCHITECTURE.md                     # Desain arsitektur web, dan alur data
├── DATA_MODEL.md                       # Skema CPT, taksonomi, meta fields, dan relasi data
├── TASKS.md                            # task terstruktur FASE 0 s/d Semua Selesai
├── AI_WORKFLOW.md                      # Pembagian peran AI, git flow, & commit standard
├── AI_RULES.md                         # Aturan pengembangan dan tata tertib coding
├── DECISIONS.md                        # Architectural Decision Records
├── TESTING.md                          # Matriks  skenario pengujian QA
├── CHANGELOG.md                        # Catatan riwayat perubahan rilis (SemVer)
├── SESSION_STATE.md                    # Sumber kebenaran tunggal status pengerjaan & task
└── docs/                               # 15 Panduan teknis, operasional, dan arsitektur
    ├── DEPLOYMENT_GUIDE.md             # Panduan deployment produksi
    ├── PRODUCTION_CHECKLIST.md         # Checklist pra-peluncuran dan uji asap go-live
    ├── OPERATOR_MANUAL.md              # SOP operasional staf operator (SLA, verifikasi e-KTP, Jalur Extreme)
    ├── ADMIN_GUIDE.md                  # Buku panduan administrator (RBAC, bulk pricing, backup)
    ├── INSTALLATION_HOSTING.md         # Panduan instalasi di cloud hosting / cPanel
    ├── GIT_WORKFLOW.md                 # Alur kerja Git, branch strategy, & Conventional Commits
    ├── CODING_STANDARDS.md             # Standar penulisan kode
    ├── HANDOVER.md                     # Protokol prompt jembatan handover antar AI

---
## ⚡ Fitur Utama
1. **Landing Page Mobile-First:** Kecepatan muat di bawah 1.5 detik dengan GeneratePress child theme.
2. **Katalog & Filter Armada:** Honda BeAT Series, Scoopy-Vario Series, dan Honda Trail CRF 150L.
3. **Aturan Keselamatan Trip Extrem/offroad:** Pembatasan tegas bahwa unit matik dilarang ke kaldera pasir Bromo; wajib Trail CRF 150L.
4. **Formulir Booking Interaktif:** Validasi nomor WhatsApp Indonesia, nomor darurat keluarga penjamin, dan kalkulator durasi sewa otomatis.
5. **Generator Pesan WhatsApp:** Menghasilkan draf pesanan resmi berformat rapi langsung ke WhatsApp admin.
6. **CPT & Status Booking:** CPT `motor` untuk armada dan CPT `penyewaan` dengan status `status_menunggu`, `status_dikonfirmasi`, `status_berjalan`, `status_selesai`, `status_dibatalkan`.
7. **Pencegahan Double Booking:** Algoritma pemeriksaan sisa kuota unit fisik terhadap pesanan aktif pada rentang tanggal sewa.
8. **Role-Based Access Control (RBAC):** Pemisahan hak akses Administrator (penuh) dan Operator (operasional harian, proteksi tarif).
9. **Penyesuaian Harga Massal (Bulk Pricing):** Kemudahan pengelola menaikkan atau menurunkan tarif armada saat peak/low season dengan fail-safe rollback.
10. **Validasi Plat Nomor Bebas Bentrok:** Alokasi plat kendaraan fisik divalidasi ketat terhadap jadwal pesanan lain.
