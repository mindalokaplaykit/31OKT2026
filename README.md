# The Growth Challenge — Mission Control v1

Website informasi peserta dan countdown Amazing Race UGM (31 Oktober 2026).

## File
- `index.html` — seluruh website, CSS, dan JavaScript. Tanpa ketergantungan eksternal, database, atau login.

## Publikasi via GitHub Pages
1. Buat repository baru, misalnya `growth-challenge-mission-control`, dengan akses **Public**.
2. Unggah file `index.html` ini ke direktori utama repository, bukan ke folder tambahan.
3. Di repository, buka **Settings → Pages**.
4. Pada **Build and deployment**, pilih **Deploy from a branch**, **main**, dan **/(root)**. Simpan.
5. Setelah terbit, alamat umumnya `https://USERNAME.github.io/growth-challenge-mission-control/`.
6. Uji tautan di HP, lalu jadikan URL akhir sebagai QR Code pembuka kegiatan.

## Mengubah deadline
Buka `index.html` dengan editor teks dan temukan:

```js
const MISSION_DEADLINE_WIB = '2026-10-31T10:15:00+07:00';
```

Ubah tanggal dan jam di **satu baris** tersebut menggunakan format `YYYY-MM-DDTHH:MM:SS+07:00` (WIB). Countdown dan teks deadline pada hero, layar waktu habis, serta aturan ke-07 akan berubah otomatis. Tanggal kegiatan di header/footer adalah identitas acara, bukan deadline; ubah teks itu secara manual hanya jika tanggal acara juga berubah. Script menghitung sisa waktu dari jam perangkat ke timestamp absolut UTC+7.

## Aturan terkunci (v1)
- 8 challenge: 4 Corner @30 poin, 4 Core @50 poin.
- Lulus = minimal 2 Bingo **dan** 3 Core selesai.
- Garis Bingo sah: atas, bawah, kiri, kanan; tidak ada diagonal dan kotak tengah tidak berlaku.
- Stamp utama di depan passport; bonus di belakang; bonus stamp +10 poin dan bukan bagian dari Bingo.
- Lulus mendapat +1.000 poin di samping poin challenge dan bonus. Tidak lulus = 0 poin.
- Waktu habis: hentikan semua challenge dan segera kembali ke titik kumpul.

## Catatan teknis
- Website dapat dibuka langsung sebagai berkas HTML setelah diunduh.
- Tidak memerlukan koneksi internet setelah halaman terbuka, karena tidak memuat aset eksternal.
- GitHub Pages diperlukan untuk akses publik pertama melalui QR Code.
- Timer menggunakan jam perangkat; jika jam pengguna meleset, ikuti arahan resmi panitia. Halaman aturan tetap dapat dibuka setelah waktu habis.
- Tidak menyimpan atau menghitung pencapaian tim. Semua stamp dicatat di passport fisik dan diverifikasi fasilitator.
- Empat tombol contoh Bingo adalah **ilustrasi garis sah**, bukan pemantau progres dan bukan petunjuk strategi.
