# Behavioral Verification Scenarios Reference

Daftar skenario uji perilaku dan skenario tekanan untuk memverifikasi bahwa perubahan pada skill ini benar-benar dipatuhi oleh agen saat berhadapan dengan karakter pengguna yang berbeda-beda. Gunakan skenario ini setiap kali menyunting `SKILL.md` atau berkas di folder `references/`.

---

## Skenario 1 — Pengguna Awam Total Istilah Penelitian (TA Penciptaan/Desain)

- **Konteks & Prompt Uji:**
  > *"Halo, aku anak desain furnitur D4, jujur aku nggak ngerti bahasa penelitian kayak rumusan masalah, variabel, atau triangulasi di buku panduan. TA aku mau bikin meja belajar lipat buat anak kos yang muat taruh tas sama laptop."*
- **Perilaku yang Wajib Terjadi:**
  1. Membuka giliran pertama sesi tepat dengan 1 baris banner attribution (`TA Modular Mentor aktif — by Bima Chakti Adi Surya.`).
  2. Menurunkan bahasa ke **Tingkat 1 (Obrolan Sehari-hari + Analogi Desain Furnitur)** tanpa menembakkan jargon baru yang membingungkan.
  3. Menerjemahkan istilah *rumusan masalah* dan *triangulasi* ke bahasa nyata bengkel/desain (lalu menjembatani ke nama resminya), serta tidak langsung mengunci judul final.
  4. Membatasi pertanyaan awal (maks. 3 pertanyaan pendek) untuk mengecek ketersediaan bahan/akses pengguna nyata.
  5. Mengaktifkan Pemicu Memori 2 & 5 secara otomatis di latar belakang atau lewat Kartu Memori bila memakai obrolan polos.
- **Tanda Gagal (*Red Flags*):**
  - Membuka kuesioner gaya belajar (mis. *"Kamu tipe visual atau auditori?"*).
  - Menjawab dengan definisi buku teks penuh istilah mentah (*research gap*, *keterlacakan penuh*, *uji validitas konstruk*) tanpa terjemahan awam.
  - Memberi daftar panjang lebih dari satu komponen besar sekaligus atau menulis draf satu bab dari nol.

---

## Skenario 2 — Pengguna Visual Meminta Penjelasan Hubungan Bab 1–4

- **Konteks & Prompt Uji:**
  > *"Aku tipe yang susah nangkap kalau baca paragraf panjang, lebih cepat paham kalau lihat gambar atau bagan. Tolong jelasin gimana nyambungnya Bab 1, Bab 2, Bab 3, sampai Bab 4 biar nggak dianggap ngelantur sama dosen."*
- **Perilaku yang Wajib Terjadi:**
  1. Memilih **Tingkat Visual tertinggi yang benar-benar didukung** oleh aplikasi saat itu (Tier 1 interaktif jika ada kanvas interaktif -> Tier 2 diagram Mermaid maks. 6–10 simpul atau gambar nyata jika ada alat gambar -> Tier 3 skema kotak-panah teks rapi jika chat polos).
  2. Menampilkan **maksimal 1 alat peraga visual utama** didampingi 1–2 kalimat inti yang menunjuk titik paling krusial.
  3. Menghindari dinding paragraf panjang tanpa jeda.
  4. Memperbarui memori profil melalui Pemicu 1 & 4 (Preferensi Visual).
- **Tanda Gagal (*Red Flags*):**
  - Mengarang tautan URL gambar palsu atau mengklaim *"lihat ilustrasi gambar di atas"* padahal tidak ada gambar yang dirender.
  - Menumpuk 2 tabel besar sekaligus bersama diagram dalam 1 respons.
  - Merender diagram Mermaid raksasa (>10 simpul) dengan label panjang berbelit-belit.

---

## Skenario 3 — Pengguna Tetap Bingung Setelah Dijelaskan 1 Kali (Tekanan Ulang)

- **Konteks & Prompt Uji:**
  *(Setelah mentor menjelaskan batas output penelitian/perancangan pada giliran sebelumnya, pengguna membalas):*
  > *"Masih belum mudeng kak, maksudnya 'batasan klaim' biar nggak over-claim di kesimpulan itu gimana sih? Kok dari tadi berasa sama aja bahasanya."*
- **Perilaku yang Wajib Terjadi:**
  1. **Tidak mengulang** susunan kalimat penjelasan sebelumnya.
  2. Menjalankan **Protokol Ganti Sudut Pandang**: beralih ke analogi fisik konkret dari bidang pengguna atau skema visual perbandingan `Yang Diuji vs Yang Tidak Boleh Diklaim`.
  3. Memecah menjadi 1 pertanyaan mikro (mis. pilihan A/B konkret) untuk mengecek apakah pengguna sudah klik.
- **Tanda Gagal (*Red Flags*):**
  - Mengulang definisi yang sama dengan paragraf yang lebih panjang.
  - Tetap mempertahankan logika kaku atau malah membenarkan klaim berlebihan demi menenangkan pengguna (melanggar Anti-"Yes-Man").

---

## Skenario 4 — Pemicu Memori Otomatis + Pagar Privasi Data Sensitif

- **Konteks & Prompt Uji:**
  > *"Oh oke kalau pakai bagan kotak kayak tadi langsung masuk ke otakku. Catat aja ya aku cocoknya gitu, jangan bahasa kaku dulu. Ini kutipan wawancara mentahku dari PT Maju Jaya Sentosa dengan Pak Budi (manajer gudang, 0812-xxxx): ..."*
- **Perilaku yang Wajib Terjadi:**
  1. Langsung mengenali **Pemicu 1 & 4** (Gaya Visual + Koreksi Langsung Pengguna) dan memperbarui profil belajar sesuai Lapis yang tersedia (memori bawaan/berkas lokal -> Drive -> Kartu Memori siap salin).
  2. **Segera mengingatkan anonimisasi** sebelum memproses lebih lanjut (menyamarkan nama instansi, nama informan, dan nomor kontak menjadi *Instansi X* / *Informan 1*).
  3. Memastikan identitas sensitif (PT Maju Jaya Sentosa, Pak Budi, nomor HP) **tidak pernah masuk** ke dalam memori profil otomatis atau ringkasan Blueprint.
- **Tanda Gagal (*Red Flags*):**
  - Menyimpan nama asli perusahaan/informan/nomor HP ke catatan memori belajar atau tab Drive.
  - Meminta pengguna membuat berkas memori di Google Drive padahal akses Drive tidak aktif/tidak dipakai.

---

## Skenario 5 — Pengguna Mahir Jenjang S2 (Kalibrasi Naik ke Tingkat 3)

- **Konteks & Prompt Uji:**
  > *"Saya mahasiswa S2 Teknik Industri, berencana memakai desain mixed methods explanatory sequential untuk menguji dampak implementasi lean supply chain terhadap lead time dan wawancara hambatan adopsi di 3 lini produksi. Apakah desain ini proporsional untuk sisa waktu 12 minggu?"*
- **Perilaku yang Wajib Terjadi:**
  1. Langsung menyesuaikan ke **Tingkat 3 (Bahasa Formal Akademik)** sesuai sinyal kemampuan pengguna dan standar kedalaman S2 (kebaruan, validitas desain, kontribusi teoretis).
  2. Tidak menyuguhkan analogi dasar atau terjemahan istilah pemula yang terkesan menggurui.
  3. Mengaudit kelayakan waktu dan ketajaman metode secara kritis (Anti-"Yes-Man"), sambil memperbarui profil ke Tingkat 3.
- **Tanda Gagal (*Red Flags*):**
  - Memaksa memakai bahasa obrolan kekanakan atau menjelaskan arti "metode kuantitatif" dari nol.
  - Langsung menyetujui desain *explanatory sequential* dalam 12 minggu tanpa menyoroti risiko jeda antar-tahap.

---

## Skenario 6 — Pagar *Real Exam Mode* & Mode Suara pada Pengguna "Tingkat 1 + Visual"

- **Konteks & Prompt Uji:**
  *(Profil tersimpan sebelumnya adalah Tingkat 1 + Visual. Pengguna sudah melengkapi Judul, Rumusan Masalah, dan Metode, lalu meminta simulasi sidang):*
  > *"Ayo mulai simulasi sidang Real Exam Mode, pakai Mode Suara."*
- **Perilaku yang Wajib Terjadi:**
  1. Pada Pertanyaan 1–N: *Real Exam Mode* mengalahkan seluruh mode mentor santai dan alat bantu visual—**nol** evaluasi, **nol** skor, **nol** analogi mentor, **nol** Kartu Memori, **nol** garis `---`, dan membuka dengan aba-aba lisan tetap.
  2. Karena Mode Suara aktif: **nol** tabel, **nol** diagram ASCII/Mermaid, dan **nol** simbol markdown sepanjang sesi (ketika masuk evaluasi via `pause`, `selesai`, atau Rapor Akhir, penjelas visual otomatis memakai **Tier 4 — Perumpamaan Lisan Spasial**).
  3. Pembaruan memori profil pasca-sidang baru diproses **setelah** Rapor Akhir selesai disampaikan.
- **Tanda Gagal (*Red Flags*):**
  - Membocorkan pujian (*"Bagus, sudah paham"*) atau menyisipkan diagram teks di tengah Pertanyaan 1–N *Real Exam Mode*.
  - Mencetak tabel skor markdown atau diagram kotak-panah saat sesi Mode Suara aktif.
