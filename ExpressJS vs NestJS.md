**Server-Side: NestJS vs Express.js**

**Pendahuluan:**
NestJS dan Express.js adalah dua kerangka kerja yang populer untuk membangun aplikasi server-side dengan Node.js. Sementara Express.js lebih lama dan lebih sederhana, NestJS adalah kerangka kerja yang lebih modern dengan fitur tambahan, terutama dukungan TypeScript. Mari kita bandingkan kedua kerangka kerja ini berdasarkan beberapa kriteria.

**1. Developer Experience dalam Membangun Sebuah Proyek Mini:**

Berdasarkan pengalaman beberapa pengembang saat mencoba membangun proyek mini menggunakan kedua kerangka kerja ini, berikut beberapa temuan kunci:

- **NestJS:**
  - **Struktur dan Organisasi:** NestJS menawarkan pendekatan modular yang memudahkan pemisahan logika bisnis, menjadikannya lebih terstruktur dan mudah dikelola. Ini sangat membantu saat proyek mulai tumbuh.
  - **Dukungan TypeScript:** Dengan dukungan bawaan untuk TypeScript, NestJS memudahkan pengembang untuk mendapatkan manfaat dari fitur-fitur seperti static typing, interfaces, dan generics. Ini membantu dalam deteksi kesalahan lebih awal dan peningkatan kualitas kode.
  - **Abstraksi Tinggi:** Dengan dekorator, injeksi ketergantungan, dan lainnya, NestJS mengurangi boilerplate yang diperlukan, meningkatkan produktivitas pengembang.
  - **Ekosistem yang Terintegrasi:** NestJS hadir dengan integrasi bawaan untuk banyak pustaka populer, seperti TypeORM, GraphQL, dan lainnya. Ini menghilangkan kebutuhan untuk patchwork solusi dan memastikan kerja sama yang mulus antara komponen yang berbeda.

- **Express.js:**
  - **Fleksibilitas:** Salah satu kekuatan utama Express.js adalah fleksibilitasnya. Meskipun ini berarti lebih banyak kebebasan, ini juga bisa menjadi pedang bermata dua. Pengembang harus membuat keputusan arsitektur yang penting dan mendefinisikan struktur aplikasi mereka sendiri.
  - **Kurva Pembelajaran Rendah:** Bagi mereka yang baru memulai dengan Node.js, Express.js mungkin lebih mudah dipelajari karena sifatnya yang minimalis.
  - **Kekurangan Fitur Bawaan:** Meskipun ini memungkinkan integrasi dengan berbagai pustaka, ini juga berarti pengembang harus menghabiskan waktu lebih banyak untuk memilih solusi terbaik untuk setiap masalah dan menyesuaikannya dengan kebutuhan mereka.
  - **Performa:** Dikarenakan sifatnya yang ringan dan minimalis, aplikasi yang dibuat dengan Express.js cenderung cepat, tetapi ini juga tergantung pada banyak faktor lainnya seperti pustaka yang digunakan dan kualitas kode.


**2. Komponen:**

| Kriteria          | NestJS   | Express.js |
|-------------------|----------|------------|
| Maintenance       | 4        | 3          |
| Reputable         | 4        | 3          |
| Compatibility     | 4        | 4          |
| Community         | 4        | 4          |
| Documentation     | 4        | 4          |
| Licensing         | 4        | 4          |
| Extensible        | 4        | 4          |
| Size              | 4        | 3          |
| **Total Score**       | **32**       | **29**       |

 **Penjelasan Skoring:**

- **Maintenance:** NestJS sering mendapatkan pembaruan, sedangkan Express.js, meskipun masih aktif, memiliki frekuensi pembaruan yang sedikit lebih rendah.
  
- **Reputable:** Kedua kerangka kerja tersebut dikembangkan oleh pengembang yang dikenal dan memiliki reputasi yang baik dalam komunitas.
  
- **Compatibility:** Kedua kerangka kerja ini sangat kompatibel dengan berbagai teknologi dan arsitektur lainnya.
  
- **Community:** Express.js dan NestJS memiliki komunitas global yang besar.
  
- **Documentation:** Kedua kerangka kerja ini memiliki dokumentasi web yang lengkap.
  
- **Licensing:** Keduanya adalah open source.
  
- **Extensible:** NestJS, dengan struktur modular dan integrasi TypeScript, memberikan sedikit keunggulan dalam hal ekstensibilitas.
  
- **Size:** Kedua framework ini memiliki ukuran pustaka yang kecil dan ringan.


**3. Mengapa memilih salah satunya?**

- **Mengapa memilih NestJS?**
  - **Pro**: NestJS menawarkan dukungan bawaan untuk TypeScript, pengaturan awal yang konsisten, dan pendekatan modular terhadap pengembangan aplikasi.
  - **Con**: Kurva belajar mungkin sedikit lebih curam bagi mereka yang belum familiar dengan TypeScript atau konsep OOP.
  
- **Mengapa memilih Express.js?**
  - **Pro**: Express.js adalah framework yang sudah lama ada, stabil, dan memiliki komunitas yang besar. Penggunaannya juga lebih sederhana.
  - **Con**: Pengembang mungkin perlu menghabiskan lebih banyak waktu untuk setup dan konfigurasi tambahan, terutama jika menginginkan fitur yang tidak disertakan secara default.

 



**Jika menggunakan Express.js:**
| **Pros** | **Cons** |
|----------|----------|
| 1. Sederhana dan mudah digunakan, ideal untuk pemula. | 1. Tanpa struktur bawaan, pengembang harus mendefinisikan strukturnya sendiri. |
| 2. Fleksibel dengan pilihan middleware dan pustaka tambahan. | 2. Kurangnya fitur bawaan mungkin memerlukan lebih banyak konfigurasi dan integrasi pustaka tambahan. |
| 3. Komunitas yang besar dan aktif, dengan banyak sumber daya pembelajaran. | 3. Dukungan TypeScript memerlukan konfigurasi tambahan. |
| 4. Ringan dan cepat. | 4. Bisa jadi kurang sesuai untuk aplikasi skala besar tanpa struktur yang tepat. |
| 5. Didokumentasikan dengan baik. | 5. Memerlukan setup dan konfigurasi tambahan untuk arsitektur berbasis microservices. |

**Jika menggunakan NestJS:**
| **Pros** | **Cons** |
|----------|----------|
| 1. Struktur modular yang meningkatkan organisasi dan scalability. | 1. Memerlukan kurva pembelajaran untuk beberapa konsep. |
| 2. Dukungan penuh untuk TypeScript out-of-the-box. | 2. Beberapa overhead tambahan untuk fitur-fitur canggih. |
| 3. Paradigma OOP, FP, dan FRP memberi fleksibilitas dalam coding. | 3. Bisa membuat developer tergantung pada ekosistem NestJS. |
| 4. Ekosistem yang kaya dengan paket yang terintegrasi dengan baik. |  |
| 5. Pendekatan berorientasi kelas untuk middleware dan fitur lainnya. |  |
| 6. Dukungan bawaan untuk arsitektur berbasis microservices. |  |
| 7. Dekorator meningkatkan keterbacaan dan fungsionalitas. |  |
| 8. Integrasi bawaan dengan banyak pustaka populer. |  |
| 9. Didukung oleh komunitas yang aktif dan dokumentasi yang kaya. |  |


**4. Kesimpulan:**

- Jika Anda mencari kerangka kerja yang lebih terstruktur, dengan fitur bawaan untuk aplikasi skala besar atau enterprise, **NestJS** lebih sesuai.


