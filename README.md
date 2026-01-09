# SvgPathEditor
Edit atau buat path SVG di browser:
https://mcikadu-dev.github.io/svg-path-editor/
Atau versi asli (Bahasa Inggris) disini:
https://yqnn.github.io/svg-path-editor/
[![Image of Yaktocat](./doc/screenshot.png)](https://mcikadu-dev.github.io/svg-path-editor/)

## Cara menggunakan

### Dasar
- Tempel atau edit path mentah (raw path) pada kolom **path**
- Klik **+** untuk menambahkan perintah baru ke dalam path, pilih tipe perintah, lalu klik pada titik tujuan
- Pindahkan titik dengan cara seret dan letakkan (drag dan drop)
- Klik pada sebuah titik, lalu klik tombol **•••** untuk menyisipkan perintah tepat setelah titik yang dipilih, hapus, atau ubah tipe

### Panel perintah
- Klik tipe perintah untuk beralih antara koordinat relatif dan absolut
- Tipe perintah relatif berwarna **oranye**, absolut berwarna **ungu**
- Klik **•••** lalu **Hapus** untuk menghapus perintah
- Klik **•••** lalu **Sisipkan setelah** untuk menyisipkan perintah baru tepat setelah perintah yang dipilih
- Klik **•••** lalu **Ubah ke** untuk mengubah perintah yang dipilih ke tipe lain
- Klik **•••** lalu **Mulai path dari sini** untuk mengatur ulang path sehingga perintah yang dipilih menjadi yang pertama
- Klik **•••** lalu **Mulai subpath dari sini** untuk mengatur ulang path sehingga perintah yang dipilih menjadi yang pertama dalam subpath
- Klik **•••** lalu **Balikkan subpath** untuk membalik urutan perintah dalam subpath dari perintah yang dipilih

### ViewBox
- Gunakan roda mouse, atau klik **Perbesar** dan **Perkecil** untuk memperbesar/memperkecil tampilan
- Gunakan seret & letakkan (drag & drop) untuk memindahkan viewBox
- Klik **Sesuaikan ke Layar** untuk mengatur viewBox secara otomatis sesuai dengan path saat ini
- ViewBox juga dapat diatur secara manual melalui kolom **x**, **y**, **lebar**, dan **tinggi**

### Operasi path
- Ubah skala seluruh path dengan tombol **Skala**
- Geser seluruh path dengan tombol **Geser**
- Rotasi seluruh path dengan tombol **Rotasi**
- Bulatkan semua koordinat dari path saat ini dengan tombol **Bulatkan**
- Ubah semua perintah menjadi koordinat relatif atau absolut dengan tombol **Ubah ke relatif** atau **Ubah ke absolut**
- Balik urutan perintah dengan tombol *Balikkan*
- Minimalkan panjang path dengan tombol *Optimalkan*

### Pintasan (Shortcut)
- Tekan **m**, **l**, **v**, **h**, **c**, **s**, **q**, **t**, **a**, atau **z** untuk menyisipkan perintah setelah perintah yang dipilih
- Tekan **shift** + **m**, **l**, **v**, **h**, **c**, **s**, **q**, **t**, **a**, atau **z** untuk mengubah perintah yang dipilih ke tipe baru
- Tekan **esc** untuk membatalkan pembuatan perintah, atau membatalkan operasi seret (drag) yang sedang berlangsung
- Tekan **delete** atau **backspace** untuk menghapus perintah yang dipilih
- Tekan **ctrl** + **z** atau **cmd** + **z** untuk urung (undo)
- Tekan **ctrl** + **shift** + **z** atau **cmd** + **shift** + **z** untuk ulang (redo)
- Tekan **ctrl** saat melakukan letakkan (drag) untuk mengabaikan batasan `kaitkan ke kisi`

## Library

Library yang digunakan oleh aplikasi ini tersedia sebagai paket mandiri: [`svg-path-editor-lib`](https://www.npmjs.com/package/svg-path-editor-lib).

## Menjalankan di Lokal

### Dengan Node.js

##### Persyaratan
- [Node.js](https://nodejs.org/) v18.13 atau lebih tinggi.

##### Dependensi
Jalankan `npm install` untuk mengunduh semua dependensi proyek.

##### Server pengembang
Jalankan `npm start` untuk menjalankan server pengembang.
Buka `http://localhost:4200/`.
Aplikasi akan otomatis dimuat ulang jika Anda mengubah file sumber.

##### Build
Jalankan `npm run build` untuk membangun proyek.
Hasil build akan disimpan di direktori `dist/`.

##### Menjalankan Unit Test
Jalankan `npm test` untuk mengeksekusi unit test menggunakan [Karma](https://karma-runner.github.io).

## Ucapan terima kasih khusus
Terima kasih banyak kepada para sponsor kami 🙇 !

[@riovir](https://github.com/riovir), [@miniBill](https://github.com/miniBill), [@GitHub](https://github.com/GitHub), [@alexandernst](https://github.com/alexandernst), [@Filimoa](https://github.com/Filimoa), [@agrogers](https://github.com/agrogers), [@MilesTails01](https://github.com/MilesTails01), [@robetus](https://github.com/robetus), [@adcar](https://github.com/adcar), [@getsentry](https://github.com/getsentry), [@simplicitywebdesign](https://github.com/simplicitywebdesign) 😎, [@PassPilot](https://github.com/PassPilot), [@zeroin](https://github.com/zeroin), [@jholmes-dev](https://github.com/jholmes-dev), [@sh-csg](https://github.com/sh-csg), [@MarcoRudin](https://github.com/MarcoRudin), [@Oddpod](https://github.com/Oddpod), [@roboflow](https://github.com/roboflow), [@lasaldan](https://github.com/lasaldan), [@stevekerrick](https://github.com/stevekerrick), [@toth-istvan-zoltan](https://github.com/toth-istvan-zoltan), [@PBI-DataVizzle](https://github.com/PBI-DataVizzle), [@gucr](https://github.com/gucr), [@Guiorgy](https://github.com/Guiorgy), [@LeaVerou](https://github.com/LeaVerou)
