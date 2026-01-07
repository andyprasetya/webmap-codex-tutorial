# Webmap Development #CODEX
[CODEX: **COD**ing **EX**perience]

Tutorial membangun __*webmap*__ sederhana yang memuat dan menampilkan data [Overture Maps Foundation](https://overturemaps.org/), dengan menggunakan [Next.js](https://nextjs.org/), [TailwindCSS](https://tailwindcss.com/), [shadcn/ui](https://ui.shadcn.com/), dan [OpenLayers](https://openlayers.org/).

### Pengantar
__*Webmap*__ (peta digital interaktif berbasis web), dari sudut-pandang pemanfaatannya, adalah sebuah solusi alternatif tepat-guna untuk pemecahan masalah di seputar bagaimana cara penyampaian dan visualisasi [data geospasial](https://en.wikipedia.org/wiki/Geographic_data_and_information).

Sedikit menyinggung tentang data geospasial, *webmap* tentu saja memiliki kemampuan untuk menampilkan data geospasial bertipe [raster](https://datacarpentry.github.io/organization-geospatial/01-intro-raster-data.html) maupun [vektor](https://datacarpentry.github.io/organization-geospatial/02-intro-vector-data.html), yang selama ini sudah umum diolah menggunakan *software* GIS berbasis desktop seperti [QGIS](https://qgis.org/), [GRASS](https://grass.osgeo.org/), [SAGA](https://saga-gis.sourceforge.io/en/index.html), [ArcGIS](https://www.esri.com/en-us/arcgis/geospatial-platform/overview), [ERDAS IMAGINE](https://hexagon.com/products/erdas-imagine), [CARTO](https://carto.com/), dan lain sebagainya.

Dari sudut-pandang pengguna-akhir (*end-user*) *webmap*, yang menjadi perbedaan antara *webmap* dan *software* GIS adalah:
- __Aspek kemudahan akses__: sekali *webmap* kita jadi dan di-*publish* ke Internet, maka *webmap* tersebut akan dengan mudah diakses oleh semua orang dengan hanya menggunakan *browser* Internet seperti Mozilla Firefox, Google Chrome atau Microsoft Edge, yang *notabene* sudah umum terpasang di desktop, laptop, atau smartphone.
- __Aspek interaktivitas__: bergantung pada kreativitas pengembangnya, sebuah *webmap* dapat memiliki fitur-fitur interaktif bagi pengguna-akhir (*end-user*)-nya.

### Asumsi dan Peralatan
Untuk memulai membangun *webmap* sederhana ini, Anda diasumsikan:
- Menggunakan OS Linux, terutama Ubuntu Linux Desktop versi 24.04 LTS. Tidak tertutup kemungkinan untuk penggunaan OS lain seperti Windows atau MacOS. Yang terpenting adalah Anda bisa menggunakan text editor dan [Node.js](https://nodejs.org/en).
- Memiliki pemahaman umum tentang aktivitas pemrograman komputer.
- Memiliki pemahaman tentang lokasi geografis secara umum.

### Selanjutnya: Instalasi __NVM__, __Node.js__, dan __Yarn__
