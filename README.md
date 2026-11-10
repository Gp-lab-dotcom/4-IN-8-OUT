# GP LAB DLMS - Web Kontrol 4 IN / 8 OUT

Kontrol dua unit GP LAB DLMS Mini (IN A-D, OUT 1-8) dari satu halaman web lewat Bluetooth BLE.

## Pasang di GitHub Pages
1. Buat repo baru di GitHub (mis. `gplab-4in8out`), upload semua isi folder ini ke root repo.
2. Buka **Settings > Pages**. Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)**, lalu Save.
3. Tunggu 1-2 menit. Alamat: `https://USERNAME.github.io/gplab-4in8out/`
4. Buka alamat itu di **Chrome Android** (atau Chrome/Edge desktop). Web Bluetooth butuh HTTPS, GitHub Pages sudah HTTPS. Safari/iPhone tidak mendukung Web Bluetooth (pakai browser Bluefy).

## Cara pakai
1. Beri nama Bluetooth berbeda di tiap alat (mis. `GP LAB DLMS 1` dan `GP LAB DLMS 2`) dan **samakan PIN**.
2. Tombol **Sambung UNIT 1** lalu Scan, pilih alat 1. Ulangi untuk **UNIT 2**.
3. Ketuk kolom meter (IN A-D, O1-O8) untuk edit kanal itu langsung.
4. P1-P5: PANGGIL / SIMPAN / NAMA preset di kedua unit sekaligus (ganti mode lewat tombol kiri).
5. SETUP BERSAMA: tema, standby, master, generator, kunci panel untuk kedua unit.

## Isi
- `index.html` halaman gabungan 4 in 8 out
- `unit.html` kontrol lengkap satu unit (dimuat dua kali; `?u=2` untuk unit 2)
- `ble-shim.js` placeholder
- `.nojekyll` agar GitHub Pages menyajikan file apa adanya

Baris tab (Utama, Crossover, PEQ, Comp/Lim, Gate, Delay, RTA) berlaku untuk kanal mana pun dari 12 kanal; tinggal ketuk kanal di meter. Salin kanal (di SETUP BERSAMA) bisa antar unit, input ke input atau output ke output.
