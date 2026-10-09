# ARCHITECTURAL DECISION RECORDS (ADR): RYOKOURENT

Dokumen ini mencatat keputusan-keputusan arsitektural penting yang telah disepakati untuk proyek Ryokourent beserta latar belakang, konsekuensi, dan alasannya.

| Kode | Keputusan | Dampak | 
| :--- | :--- | :--- | 
| **D-01** | Pakai WordPress. Biaya hosting mengikuti. | T06b berubah dari 
| **D-02** | Operator punya akses penuh kecuali kelola akun staf dan hapus model unit. Edit data, termasuk harga, boleh. |	Konflik 1 selesai. Matriks RBAC: ubah harga dan bulk pricing ✅ untuk Operator, kelola akun ❌, hapus model ❌. |
| D-03 |	Pemilik cukup paham teknis. | 	Pilih alat yang bisa dikelola sendiri lewat dashboard WP. Panduan ditulis langkah demi langkah. |
| D-04 |	Volume 50–100 booking per bulan. |	Cukup untuk shared hosting biasa. Tidak perlu infrastruktur khusus. |
| D-05 |	Versi Inggris diperlukan, nanti multi-bahasa.	| Semua teks dibuat bisa diterjemahkan sejak awal. Plugin multi-bahasa dipilih di ADR. |
| D-06 |	Konsultan rute dihapus dari MVP. |	Hapus dari Overview (bagian 3) dan Blueprint (halaman 5 dan fitur terkait). Aturan Bromo tetap lewat peringatan dan FAQ. |
| D-07	| Anggaran hosting + domain maksimal Rp1.500.000/tahun. Belum punya domain.	| Hanya paket hosting WordPress tingkat pemula sampai menengah yang masuk. VPS tidak dipertimbangkan. Plugin dan tema berbayar belum termasuk (lihat pertanyaan di bawah).| 
| D-08	| Tunda semua plugin dan tema berbayar. Pakai yang gratis dulu, upgrade di tahap 2 setelah situs berjalan.	| Anggaran Rp1,5 juta/tahun hanya untuk hosting dan domain. Plugin multi-bahasa dipilih dari yang gratis.| 
| D-09	| Operator boleh edit harga dan tambah/edit paket harga.	| Pertegas D-02. Bulk pricing ✅ untuk Operator.| 
| D-10	| 07.00–23.00 adalah jam pelayanan admin dan kurir. Di luar jam itu, ambil/kembali bisa di Pool Dinoyo, atau lewat kurir, dengan syarat sudah ada konfirmasi dan kesepakatan dengan admin.	| Konflik 2 selesai, termasuk paket Sunrise Bromo. Form tidak lagi menolak jam di luar 07.00–23.00, tetapi menampilkan catatan “perlu kesepakatan admin”.| 
| D-11	| Perlengkapan: 2 helm tanpa menyebut jumlah jas hujan. Phone holder dan plastik HP tersedia jika persediaan masih ada.	| Konflik 7 selesai. Copy web dan pesan WA disesuaikan.| 
| D-12	| rented_motor_id diganti ID_motor (unit fisik): kode, plat nomor, model, tahun pembelian, nomor mesin, warna. Model hanya klasifikasi tampilan.| 	Konflik 8 selesai. Kode adalah penanda tetap. Plat bisa berubah (registrasi 5 tahunan).| 
| D-13	| Rumus ketersediaan: Total − Sedang Jalan − Dalam Servis − Booking. Menunggu tidak mengunci stok. Booking baru terhitung setelah di-approve.| 	Konflik 9 dan 10 selesai.| 
| D-14	| Alur status: pelanggan klik booking → Menunggu. Admin/Operator approve → Dikonfirmasi. Cancel = data dihapus. Menunggu otomatis dihapus setelah 48 jam.	| Konflik 11 sebagian selesai.| 

