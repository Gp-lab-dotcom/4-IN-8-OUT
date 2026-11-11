# GP LAB DLMS - Web Kontrol 4 IN / 8 OUT

Kontrol dua unit GP LAB DLMS Mini (IN A-D, OUT 1-8) dari satu halaman web lewat Bluetooth BLE.

## Pasang di GitHub Pages
1. Buat repo baru di GitHub (mis. `gplab-4in8out`), upload semua isi folder ini ke root repo.
2. Buka **Settings > Pages**. Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)**, lalu Save.
3. Tunggu 1-2 menit. Alamat: `https://USERNAME.github.io/gplab-4in8out/`
4. Buka alamat itu di **Chrome Android** (atau Chrome/Edge desktop). Web Bluetooth butuh HTTPS, GitHub Pages sudah HTTPS. Safari/iPhone tidak mendukung Web Bluetooth (pakai browser Bluefy).

## Cara pakai
1. Beri nama Bluetooth berbeda di tiap alat (mis. `GP LAB DLMS 1` dan `GP LAB DLMS 2`) dan **samakan PIN**.
2. Putar HP ke mode lanskap. **CONNECT** menyambung unit 1. **SAMBUNG U2** membuka halaman sambung unit 2 (tekan Scan) di layar yang sama, tanpa pindah halaman.
3. **MIXER**: 12 fader (IN A-D, OUT 1-8), ON/OFF, meter, CLIP. Garis oranye = unit 1, biru = unit 2.
4. **KANAL / SINYAL / SISTEM**: satu menu untuk semua. Barisan tombol kanal memuat 12 kanal; pilih kanal mana pun (unit 1 atau 2) dan halaman PEQ, Crossover, Comp/Lim, Gate, Delay, RTA ikut berpindah ke unit yang tepat.
5. **BERSAMA**: preset P1-P5 (panggil / simpan / nama), tema, standby, master, generator, kunci panel untuk kedua unit.

## Isi
- `index.html` aplikasi utama 4 in 8 out (unit 1 berjalan langsung di halaman ini)
- `unit.html` mesin unit 2, dimuat tersembunyi dan ditampilkan di area konten yang sama
- `ble-shim.js` placeholder, `.nojekyll`

Catatan: harus dibuka lewat HTTPS / GitHub Pages (satu alamat), karena unit 2 berbagi data dengan halaman utama.
