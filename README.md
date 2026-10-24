# Raspberry Project

Berikut adalah dokumentasi dan konfigurasi beberapa proyek dengan perangkat Raspberry Pi 3B+ yang saya miliki. Saya menggunakan perangkat ini murni sebagai server hemat daya saja dan tidak mengakses pin GPIO. 

## Tujuan Project

* Akses SSH, sehingga perangkat dapat diakses secara lokal dan public juga
* Print Server, agar printer HP Smart Tank 520 yang hanya memiliki koneksi UBS bisa print via Wifi
* dan project lain yang akan ditambahkan berkala

## Memulai

* Baca dan ikuti langkah panduan secara berurutan pada folder Docs
* Untuk skrip dengan emotion # artinya hasil / output skrip perlu disimpan untuk digunakan pada langkah selanjutnya
* Jangan jalankan semua perintah / skrip sekaligus

## Struktur Repo

```
.
├── README.md
├── .gitignore
├── docs/
│   ├── 00-spesifikasi.md
│   ├── 01-roadmap.md
│   └── 02-backup-restore.md
└── .github/
    └── workflows/
        └── markdown-check.yml
```

## Catatan

* Berhubung Raspberry Pi 3B+ secara kemampuan hardware terbatas, maka OS yang digunakan non GUI / non DE sehingga perlu terbiasa dengan command linux, dimana saya adalah awam dan masih perlu belajar.
* Akan ada banyak perbaikan kedepan, dikarenakan perlu optimasi skrip menyesuaikan kemampuan hardware.
* Sistem Operasi pada Host yang digunakan adalah MacOS, jadi akan ada perbedaan minor jika menggunakan Windows ataupun Linux
