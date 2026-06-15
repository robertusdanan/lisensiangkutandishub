# License Kill Switch

File JSON ini digunakan sebagai remote kill switch untuk aplikasi yang dikembangkan.

## Cara mematikan aplikasi

Edit `dishub-tulungagung.json`, ubah:
```json
"active": true  →  "active": false
```
Commit dan push. Dalam maksimal **1 jam**, aplikasi akan menampilkan halaman maintenance.

## Cara mengaktifkan kembali

Ubah kembali `"active": false` → `"active": true`, commit dan push.

## Catatan teknis
- App cek file ini maksimal 1x per jam (cache di PHP session)
- Jika GitHub Pages tidak bisa diakses (network error), app tetap berjalan (fail-open)
- File ini diakses via: `https://robertusdanan.github.io/license/dishub-tulungagung.json`
