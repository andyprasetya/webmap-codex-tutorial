# Webmap Development #CODEX
[CODEX: **COD**ing **EX**perience]

Tutorial membangun __*webmap*__ sederhana yang memuat dan menampilkan data [Overture Maps Foundation](https://overturemaps.org/), dengan menggunakan [Next.js](https://nextjs.org/), [TailwindCSS](https://tailwindcss.com/), [shadcn/ui](https://ui.shadcn.com/), dan [OpenLayers](https://openlayers.org/).

### Integrasi [OpenLayers](https://openlayers.org/)
Dalam membangun sebuah *webmap*, Anda akan membutuhkan *web-mapping library* yang berupa paling-tidak 1 atau kumpulan dari beberapa file JavaScript, dan file ini harus dimasukkan / diintegrasikan dengan proyek Anda. Hingga saat ini (tahun 2025), sudah terdapat cukup banyak *web-mapping library* yang bisa kita dapatkan di Internet secara bebas seperti contohnya [Leaflet.js](https://leafletjs.com), [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript/overview), [OpenLayers](https://openlayers.org/), [ArcGIS Maps SDK for JavaScript](https://developers.arcgis.com/javascript/latest/), [HERE Maps API](https://www.here.com/developer/javascript-api), [MapBox GL JS](https://docs.mapbox.com/mapbox-gl-js/guides/), dan lain sebagainya.

*Web-mapping library* tersebut sebelumnya pasti memiliki kelebihan dan kekurangannya masing-masing, mulai dari *availability* dan metode akuisisinya (*proprietary* atau *opensource*, atau bahkan berbayar), fitur, *library handling*, hingga *learning curve*-nya.

Pada proyek ini Anda akan menggunakan [OpenLayers](https://openlayers/org/).

Untuk menambahkan OpenLayers ke dalam proyek Anda, pada *command shell* eksekusi *command* (asumsi: proyek sedang tidak dijalankan, atau jika sedang berjalan, Anda bisa menghentikannya dulu sementara dengan menekan `Ctrl + C`.)
```shell

yarn add ol
```

Catatan: Alasan teknis mengapa menggunakan OpenLayers dapat Anda baca [di sini](https://www.google.com/search?q=why+i+use+openlayers) (red.: subjektif)

### Selanjutnya: [Instalasi __NVM__, __Node.js__, dan __Yarn__](https://github.com/andyprasetya/webmap-codex-tutorial/tree/feat/00-nvm-node-yarn)
