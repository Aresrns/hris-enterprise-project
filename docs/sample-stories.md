# Sample user stories

Two stories copied from the backlog as the team sees them. They're in Indonesian because that's the team's working language. Each one follows the same format: story, description, user journey, acceptance criteria.

*Dua story dari backlog, persis seperti yang dilihat tim.*

---

## US-PAY-02 · Buka slip gaji di HP dengan PIN

**User story**
Sebagai karyawan, saya ingin membuka slip gaji di HP dengan PIN atau sidik jari, supaya orang lain tidak bisa melihat gaji saya.

**Description**
Slip gaji terbit setelah periode payroll dipublikasi. Slip menampilkan rincian pendapatan, potongan BPJS, PPh 21, dan potongan lain. Akses dilindungi verifikasi ulang, dan PDF yang diunduh diberi kata sandi.

**User journey**
1. Karyawan menerima notifikasi "Slip gaji November sudah tersedia".
2. Karyawan membuka ESS › Slip Gaji dan memilih periode.
3. Aplikasi meminta PIN atau biometrik.
4. Karyawan melihat rincian slip dan bisa membandingkan dengan bulan lalu.
5. Karyawan mengunduh PDF yang terproteksi kata sandi bila perlu.

**Acceptance criteria**
1. **Diberikan** periode sudah Publish, **ketika** karyawan membuka slip, **maka** sistem meminta PIN atau biometrik sebelum menampilkan isinya.
2. **Diberikan** PIN salah 5 kali berturut-turut, **ketika** percobaan ke-5 gagal, **maka** akses slip terkunci 30 menit.
3. **Diberikan** karyawan mengunduh PDF, **ketika** file dibuka, **maka** diminta kata sandi sesuai format yang dijelaskan di aplikasi.
4. **Diberikan** periode masih Draft atau Review, **ketika** karyawan membuka menu slip, **maka** slip periode itu belum terlihat.
5. Rincian slip sama persis dengan hasil perhitungan payroll yang dikunci.

*Rujukan PRD: FR-PAY-09, FR-PAY-11.*

---

## US-EXT-02 · Karyawan resign melihat progres clearance dan estimasi hak akhir

**User story**
Sebagai karyawan yang resign, saya ingin melihat progres clearance dan perkiraan hak akhir yang akan saya terima, supaya saya tahu apa yang masih harus diselesaikan.

**Description**
Hak akhir dihitung dari gaji proporsional, sisa cuti yang dibayarkan, THR proporsional jika berlaku, pesangon/UPMK/UPH atau kompensasi PKWT sesuai Rule Pack, dikurangi kewajiban terbuka. Paklaring dibuat otomatis dan tidak boleh ditahan karena clearance yang belum selesai.

**User journey**
1. Karyawan membuka ESS › Proses Keluar.
2. Karyawan melihat daftar item clearance beserta status dan PIC.
3. Karyawan melihat estimasi hak akhir dengan rincian komponen.
4. Karyawan mengisi exit interview online.
5. Di hari terakhir, karyawan mengunduh paklaring yang sudah ditandatangani elektronik.

**Acceptance criteria**
1. **Diberikan** sisa cuti 5 hari, **ketika** estimasi dihitung, **maka** nilai penggantian cuti muncul sebagai komponen terpisah.
2. **Diberikan** ada kasbon Rp1.000.000 belum direalisasi, **ketika** estimasi dihitung, **maka** kasbon tampil sebagai pengurang dengan keterangan.
3. **Diberikan** clearance belum selesai, **ketika** tanggal efektif tiba, **maka** paklaring tetap terbit dan bisa diunduh.
4. **Diberikan** exit dengan alasan PHK, **ketika** HR memfinalkan status, **maka** sistem meminta unggahan berita acara bipartit terlebih dahulu.
5. Paklaring memuat masa kerja dan jabatan terakhir yang sesuai data riwayat jabatan.

*Rujukan PRD: FR-EXT-06 s.d. FR-EXT-09, FR-PAY-13.*
