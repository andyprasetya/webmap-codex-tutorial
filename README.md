# Webmap Development #CODEX
[CODEX: **COD**ing **EX**perience]

Tutorial membangun __*webmap*__ sederhana yang memuat dan menampilkan data [Overture Maps Foundation](https://overturemaps.org/), dengan menggunakan [Next.js](https://nextjs.org/), [TailwindCSS](https://tailwindcss.com/), [shadcn/ui](https://ui.shadcn.com/), dan [OpenLayers](https://openlayers.org/).

## *Create* Proyek Next.js
Untuk mengawali sebuah proyek Next.js, Anda dapat membuat sebuah direktori kosong di dalam *home directory*, dan masuk ke dalam direktori kosong tersebut.
```shell

mkdir project

cd project
```
Jalankan command berikut:
```shell

npx create-next-app@latest
```
![Image 01](./images/image_01.png)
Saat muncul akan dinamai apa proyeknya, tuliskan nama proyek Anda dan tekan `Enter`. Dalam contoh, proyek akan dinamai: `webmap-nextjs`.

Catatan: Nama proyek sebaiknya menggunakan `lowercase`, hindari spasi, dan lebih baik menggunakan `-` atau `_` jika butuh pemisahan kata.
![Image 02](./images/image_02.png)

Berikutnya akan muncul pilihan konfigurasi *default* proyek Next.js. Saat muncul pilihan seperti ini, dengan menggunakan *keyboard* pilih: `No, customize settings`:
![Image 03](./images/image_03.png)
Berikutnya akan muncul pilihan:

`TypeScript`:
![Image 04](./images/image_04.png)
Pilih: `Yes`.

`ESLint`
![Image 05](./images/image_05.png)
Pilih `ESLint`.

Berikutnya akan muncul pilihan:

`React Compiler`:
![Image 07](./images/image_07.png)
Pilih `No`.

`Tailwind CSS`
![Image 08](./images/image_08.png)
Pilih `Yes`.

Berikutnya akan muncul apakah seluruh kode Anda akan berada di dalam direktori `src/`:
![Image 09](./images/image_09.png)
Pilih `Yes`.

`App Router`
![Image 10](./images/image_10.png)
Pilih `Yes`.

`import alias`
![Image 11](./images/image_11.png)
Pilih `No` (berarti Anda akan menggunakan *default*, yaitu `@/*`).

Setelah Anda menekan `Enter` pada `Yes`, maka proses `create` akan berjalan:
![Image 12](./images/image_12.png)

Jika proses *create* sudah selesai, maka akan muncul:
![Image 13](./images/image_13.png)

Langkah selanjutnya adalah masuk ke direktori proyek yang sudah Anda buat. Nama direktori akan sesuai dengan nama proyek yang tadi di awal sudah Anda tulis. (Dalam contoh ini: `webmap-nextjs`)
```shell

cd webmap-nextjs
```

Penting: Untuk menghindari kompleksitas, lebih baik mengulang / me-*reset* proyek yang saat ini menggunakan `npm` sebagai basisnya, menjadi `yarn`. Langkah yang bisa Anda laksanakan:
Hapus direktori `node_modules` dan file `package-lock.json` dalam direktori proyek.
```shell

rm -rf node_modules

rm -rf package-lock.json
```

Selanjutnya, jalankan *command* `yarn` untuk membangun-ulang direktori `node_modules`:
```shell

yarn
```
Catatan: Dalam proses membangun-ulang direktori `node_modules` dengan menggunakan *Yarn*, `lock` file yang akan secara otomatis di-*generate* bukan `package-lock.json`, melainkan `yarn.lock`.

Untuk test, jalankan *command*:
```shell

yarn dev
```
dan buka URL: `http://localhost:3000` di *browser* Anda.
