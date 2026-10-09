# HANDOVER: PROMPT JEMBATAN ANTAR-AI

> **Fungsi tunggal:** menyediakan prompt siap salin agar AI yang berbeda (untuk optimasi peran) bisa melanjutkan proyek tanpa kehilangan konteks.
> **Bukan** tempat status. Status sesi, cabang Git, riwayat task, dan hasil pengujian hanya ada di `SESSION_STATE.md`. Spesifikasi task hanya ada di `TASKS.md`.

**Tugas AI setiap selesai task:** ganti hanya blok `TARGET PEKERJAAN` pada prompt di bawah (task berikutnya, peran AI, catatan khusus). Jangan mengubah bagian lain.

---

## PROMPT SIAP SALIN

```markdown
# HANDOVER (dari Claude, 9 Okt 2026)
Konteks: Rencana situs rental motor Ryokourent (Malang/Batu), dikerjakan dengan beberapa AI
  gratis dan disimpan di GitHub. Stack WordPress, hosting+domain maks Rp1,5 jt/tahun.
  Hanya perencanaan, belum ada kode.
File yang berubah: DECISIONS (D-01..D-14), SESSION_STATE, OPEN_QUESTIONS
Terverifikasi: harga hosting/domain hanya dari sumber sekunder — cek ulang di situs resmi.
Asumsi: jas hujan tetap disebut tanpa angka; Operator tidak boleh hapus model unit.
Prompt lanjutan:
  "Baca SESSION_STATE.md dan DECISIONS.md. Lanjut T04: tanyakan konflik 3, 4, 5, 6, 12
   satu per satu dan catat jawabannya sebagai D-15 dst. Jangan menulis kode."
```
