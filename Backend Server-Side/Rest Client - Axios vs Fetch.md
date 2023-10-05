# **Rest Client : Axios vs Fetch**

## **Pendahuluan:**
Dalam era pengembangan aplikasi web modern, metode pengambilan data dari server atau API menjadi salah satu komponen kritis dalam arsitektur aplikasi. Permintaan data dari sumber eksternal melalui HTTP adalah salah satu kegiatan yang sering dilakukan oleh aplikasi berbasis web, dan dalam JavaScript, Axios dan Fetch adalah dua pendekatan yang populer dalam menangani tugas tersebut. 

Axios adalah pustaka JavaScript populer yang digunakan untuk membuat permintaan HTTP. Ini menawarkan API yang konsisten di seluruh peramban dan Node.js, mendukung fitur seperti transformasi permintaan dan respons, pembatalan permintaan, serta penanganan kesalahan otomatis. Berkat desainnya yang berbasis Promise, Axios memudahkan penanganan respons dan kesalahan dengan metode `then()`, `catch()`, dan `finally()`. Selain itu, Axios memiliki kemampuan untuk mengintersep permintaan dan respons, yang memungkinkan pengembang untuk memodifikasi permintaan dan respons sebelum mereka ditangani atau dikirim.

Di sisi lain, Fetch adalah API bawaan dari sebagian besar browser modern yang memberikan cara yang lebih modern untuk mengambil sumber daya secara asinkron melalui jaringan. Dibandingkan dengan XMLHttpRequest, pendekatan lama untuk tugas ini, Fetch menawarkan sintaks yang lebih bersih dan ringkas dengan dukungan Promise yang inheren. Dengan Fetch, pengembang memiliki kontrol penuh atas permintaan, termasuk kemampuan untuk memodifikasi header, mode CORS, integritas sumber daya, dan lainnya. Sebagai bagian dari platform web, Fetch tidak memerlukan dependensi tambahan, tetapi untuk menggunakannya di lingkungan tertentu, seperti Node.js, Anda mungkin memerlukan polyfill atau implementasi alternatif.

Dalam hal popularitas, Axios sering menjadi pilihan pertama bagi banyak pengembang terutama karena kemudahannya dalam penanganan kesalahan dan fitur-fitur lanjutan yang ditawarkannya. Namun, dengan kehadiran Fetch sebagai standar dalam peramban modern, banyak pengembang merasa lebih nyaman menggunakan API bawaan yang tidak memerlukan tambahan dependensi.

Pemilihan antara Axios dan Fetch pada akhirnya akan bergantung pada kebutuhan spesifik proyek dan preferensi pribadi pengembang. Sementara Axios menawarkan set fitur yang kaya dan integrasi yang mulus dengan berbagai lingkungan, Fetch memberikan solusi ringan dengan kurva belajar yang lebih datar bagi mereka yang sudah familiar dengan Promises dan konsep asinkronitas dalam JavaScript.

Namun, kedua metode ini memiliki kelebihan dan kekurangan masing-masing. Untuk memberi Anda gambaran yang lebih jelas, mari kita jelajahi masing-masing lebih lanjut untuk memahami karakteristik, fitur, dan penerapannya dalam berbagai skenario pengembangan aplikasi.

#### Referensi:

- [Axios. (n.d.). GitHub repository.](https://github.com/axios/axios)
- [Fetch API - Web APIs | MDN. (n.d.). MDN Web Docs.](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)


## **1. Pengalaman Pengembang dalam Membangun Sebuah Proyek Mini:**

### **Axios:**
- Axios adalah klien HTTP berbasis promise, cocok untuk digunakan di browser dan Node.js, menawarkan antarmuka yang sederhana dan mudah dikembangkan.
- Secara otomatis menolak promise pada respons error (kode status 4XX atau 5XX), yang sangat memudahkan penanganan error dibandingkan dengan Fetch.
- Axios membutuhkan kode boilerplate lebih sedikit untuk membuat permintaan HTTP dan menangani respons, yang dapat menghasilkan basis kode yang lebih langsung dan kurang verbose.
- Mendukung berbagai browser secara langsung, termasuk browser lama seperti IE11, yang bisa menjadi keuntungan besar dalam proyek yang membutuhkan kompatibilitas browser yang luas.
- Versi minified dari Axios cukup kecil (6.63KB), menunjukkan bahwa ini tidak akan berdampak negatif pada waktu pemuatan halaman saat digunakan di sisi klien.

### **Fetch:**
- Fetch adalah API tingkat lebih rendah untuk membuat permintaan HTTP dan membutuhkan lebih banyak kode boilerplate, terutama ketika menangani error. Misalnya, Fetch tidak secara otomatis menolak promise pada respons error, yang berarti pengembang perlu menangani kode status HTTP secara manual.
- Fetch tidak mengirim cookie lintas asal secara default, memerlukan konfigurasi tambahan jika cookie lintas asal diperlukan.
- Pengembang yang menggunakan Fetch mungkin akan menulis banyak abstraksi yang sudah ditangani oleh Axios, seperti penanganan error generik dan membaca tubuh respons.

#### **Referensi:**
- [Ship SaaS: Axios vs fetch - mana yang lebih cocok untuk Anda?](https://shipsaas.com/blog/axios-vs-fetch)
- [Blog LogRocket: Axios vs. fetch() : Mana yang terbaik untuk membuat permintaan HTTP?](https://blog.logrocket.com/axios-or-fetch-api/)

## **2. Komponen:**

| Kriteria      | Axios | Fetch |
|---------------|-------|-------|
| Maintenance   | 4     | 3     |
| Reputable     | 4     | 3     |
| Compatibility | 4     | 3     |
| Community     | 4     | 3     |
| Documentation | 4     | 3     |
| Licensing     | 4     | 4     |
| Extensible    | 4     | 3     |
| Size          | 4     | 3     |
| **Total Score**   | **32**  | **25**    |

#### Referensi:

- [GeeksforGeeks: Difference between Fetch and Axios.js for making http requests](https://www.geeksforgeeks.org/difference-between-fetch-and-axios-js-for-making-http-requests)
- [LogRocket Blog: Axios vs. fetch() : Which is best for making HTTP requests?](https://blog.logrocket.com/axios-or-fetch-api)
- [Pluralsight: JavaScript Guide: Axios vs. Fetch](https://www.pluralsight.com/guides/axios-vs-fetch)
- [Mastering JS: Axios vs Fetch: Which Should You Use?](https://masteringjs.io/tutorials/axios/vs-fetch)

## **3. Mengapa memilih salah satunya?**

Menghadapi pilihan antara menggunakan Axios atau Fetch sebagai klien REST dalam proyek Anda mungkin bisa menjadi keputusan penting yang akan mempengaruhi alur kerja pengembangan dan kinerja aplikasi. Berikut adalah beberapa pertimbangan yang mungkin membantu dalam membuat keputusan tersebut:

### **Mengapa memilih Axios?**
  - **Pro**:
    1. **Fitur Tambahan**: Axios memiliki beberapa fitur tambahan seperti transformasi JSON otomatis, pembatalan permintaan, timeout permintaan, dan interceptor yang dapat memudahkan dan mempercepat proses pengembangan【22†source】.
    2. **Dukungan Browser Luas**: Axios mendukung sebagian besar browser termasuk browser lama seperti IE11, yang bisa menjadi keuntungan besar dalam proyek yang membutuhkan kompatibilitas browser yang luas【24†source】.
    3. **Kurang Boilerplate**: Axios membutuhkan kode boilerplate lebih sedikit dibandingkan dengan Fetch, yang bisa menghemat waktu dan usaha pengembang【25†source】.
    4. **Dukungan Komunitas yang Kuat**: Komunitas yang aktif dan dokumentasi yang baik dapat membantu pengembang untuk memahami dan mengimplementasikan Axios dengan lebih efisien.
  - **Con**:
    1. **Ukuran Library**: Meskipun ukurannya kecil, Axios masih lebih besar dibandingkan dengan Fetch yang merupakan API bawaan browser.

### **Mengapa memilih Fetch?**
  - **Pro**:
    1. **Sederhana dan Asli**: Fetch adalah cara yang lebih sederhana dan asli untuk membuat permintaan HTTP dan mungkin lebih mudah dimengerti bagi pengembang yang baru dalam pengembangan web【22†source】.
    2. **API Bawaan Browser**: Sebagai API bawaan browser, Fetch tidak memerlukan pengguna untuk menginstal library tambahan.
    3. **Lebih Ringan**: Fetch mungkin lebih ringan dibandingkan dengan Axios karena memiliki fitur yang lebih sedikit.
  - **Con**:
    1. **Penanganan Error**: Fetch tidak menolak promise pada respons error, yang berarti pengembang perlu menangani kode status HTTP secara manual, yang bisa menjadi proses yang menjengkelkan【22†source】.
    2. **Dukungan Browser Terbatas**: Fetch tidak didukung secara luas di antara browser lama, dan mungkin memerlukan polyfill untuk dukungan browser lama【24†source】.

**Jika menggunakan Axios:**
| **Pros** | **Cons** |
|----------|----------|
| 1. Fitur Tambahan. | 1. Ukuran Library. |
| 2. Dukungan Browser Luas. | |
| 3. Kurang Boilerplate. | |
| 4. Dukungan Komunitas yang Kuat. | |

**Jika menggunakan Fetch:**
| **Pros** | **Cons** |
|----------|----------|
| 1. Sederhana dan Asli. | 1. Penanganan Error. |
| 2. API Bawaan Browser. | 2. Dukungan Browser Terbatas. |
| 3. Lebih Ringan. | |

#### Referensi:
- [GeeksforGeeks: Perbedaan antara Fetch dan Axios.js untuk membuat permintaan HTTP](https://www.geeksforgeeks.org/difference-between-fetch-and-axios-js-for-making-http-requests)
- [Pluralsight: Panduan JavaScript: Axios vs. Fetch](https://www.pluralsight.com/guides/axios-vs-fetch)
- [Mastering JS: Axios vs Fetch: Mana yang Harus Anda Gunakan?](https://masteringjs.io/tutorials/axios/vs-fetch)


## **4. Kapan Sebaiknya Menggunakan Rest Client Ini?**

Menggunakan rest client seperti Axios atau Fetch sangat bergantung pada kebutuhan proyek dan preferensi tim. Berikut adalah beberapa situasi dan pertimbangan utama saat memilih antara Axios dan Fetch:

### **Axios:**
1. **Fitur Lebih Lengkap**:
   - Axios menyediakan lebih banyak fitur out-of-the-box dibandingkan dengan Fetch API, seperti kemampuan untuk melakukan request yang dapat dibatalkan, transformasi data request dan response, serta pengaturan header default.
   - Dibandingkan dengan Fetch, Axios juga memiliki kemampuan untuk menangani timeout request, yang bisa sangat berguna dalam proyek dengan persyaratan waktu respon ketat.

2. **Simplicity dan Konsistensi**:
   - Axios menawarkan API yang sederhana dan konsisten untuk melakukan permintaan HTTP di berbagai platform, membuatnya menjadi pilihan yang baik untuk tim yang membutuhkan konsistensi antar platform.

3. **Transformasi Data Otomatis**:
   - Axios melakukan transformasi data JSON secara otomatis, yang bisa menghemat waktu dan upaya pengembang.

4. **Dukungan untuk Pembatalan Request**:
   - Fitur pembatalan request adalah salah satu keuntungan besar Axios dibandingkan dengan Fetch.

5. **Kustomisasi Header**:
   - Axios memungkinkan pengembang untuk menetapkan header default yang akan digunakan untuk setiap request, atau menetapkan header khusus untuk request tertentu.

6. **Kompatibilitas dengan Browser Lama**:
   - Jika proyek Anda perlu mendukung browser lama, Axios bisa menjadi pilihan yang lebih baik karena Fetch mungkin tidak didukung di browser lama seperti Internet Explorer.

### **Fetch:**
1. **Sederhana dan Minimalis**:
   - Jika prioritas utama Anda adalah kesederhanaan dan minimalisme, dan Anda tidak ingin memperkenalkan dependensi eksternal, Fetch adalah pilihan yang baik.

2. **Standar Browser**:
   - Sebagai API standar browser, Fetch tidak memerlukan pustaka eksternal atau dependensi lainnya, yang bisa mengurangi kompleksitas dan ukuran bundel proyek Anda.

3. **Proyek dengan Dependensi Minimum**:
   - Jika proyek Anda memiliki tujuan untuk meminimalkan dependensi eksternal, memilih Fetch bisa menjadi pilihan yang bijaksana.

4. **Pendekatan "Vanilla JavaScript"**:
   - Fetch mungkin lebih sesuai untuk pengembang yang lebih suka pendekatan JavaScript "vanilla" tanpa banyak abstraksi atau dependensi tambahan.

5. **Proyek dengan Tim yang Sudah Terbiasa dengan Fetch**:
   - Jika tim Anda sudah terbiasa dengan Fetch dan merasa nyaman menggunakannya, maka menggunakan Fetch bisa menjadi pilihan yang logis.

#### Referensi:

- [Mastering CRUD Operations with Axios: A Complete Guide](https://officiallysidsingh.hashnode.dev/mastering-crud-operations-with-axios)
- [Axios or fetch(): Which should you use?](https://blog.logrocket.com/axios-vs-fetch-best-http-requests/#:~:text=With%20Axios%2C%20the%20data%20response,run%20Axios%20without%20any%20issue)
- [Why Axios is Preferable to Fetch - JavaScript in Plain English](https://javascript.plainenglish.io/why-switch-to-axios-instead-of-fetch-d80c3fe2f156)
- [Axios vs Fetch - HTTP POST Request Comparison by Example](https://jasonwatmore.com/post/2021/10/03/axios-vs-fetch-http-post-request-comparison-by-example#:~:text=The%20one%20you%20choose%20really,Installing%20axios%20from%20npm)
- [Fetch vs. Axios: Choosing the Right](https://www.letsreact.org/fetch-vs-axios-choosing-the-right/#:~:text=When%20to%20Choose%20Fetch%20or,want%20to%20introduce%20external%20dependencies)
- [Why choose Axios over fetch? A simple and consistent API for HTTP](https://www.linkedin.com/posts/irfan-asgher-813bb3151_javascriptdeveloper-javascript-programming-activity-7109985347068903424-6XQh/)



## 5. Popularitas:

### **Axios**:

- **Bintang GitHub**: Axios memiliki lebih dari 77,000 bintang di GitHub, yang menunjukkan tingkat dukungan dan minat komunitas yang kuat.
- **Kontributor**: Ada lebih dari 270 kontributor untuk Axios, yang menunjukkan komunitas pengembang yang beragam dan aktif dalam memelihara dan meningkatkan perpustakaan.
- **Unduhan Mingguan di npm**: Axios diunduh lebih dari 7 juta kali setiap minggu di npm, yang menunjukkan penggunaannya yang luas di komunitas.
- **Penggunaan dalam Proyek**: Axios juga digunakan di banyak proyek dan organisasi karena set fitur dan kemudahan.

### **Fetch**:

- **Bintang GitHub**: Fetch API adalah standar yang diimplementasikan di seluruh browser dan tidak memiliki repositori GitHub khusus dengan bintang atau kontributor seperti Axios.
- **Kontributor**: Menjadi standar, Fetch dipelihara oleh komunitas pengembang web dan vendor browser, dan spesifikasinya ditangani oleh WHATWG.
- **Unduhan Mingguan di npm**: Mungkin ada polyfills atau perpustakaan tambahan untuk Fetch di npm, tetapi mereka tidak akan mewakili penggunaan sebenarnya dari Fetch karena sudah terintegrasi di browser modern.
- **Penggunaan dalam Proyek**: Fetch juga banyak digunakan, terutama di proyek yang lebih suka menggunakan API standar atau tidak memerlukan fitur tambahan yang disediakan oleh.

#### Referensi:

- [Axios GitHub](https://github.com/axios/axios) (Sumber: Axios GitHub)
- [npm trends: Axios vs Fetch](https://www.npmtrends.com/axios-vs-fetch) (Sumber: npm trends)
- [5 Ways to Make HTTP Requests in JavaScript](https://www.taniarascia.com) (Sumber: taniarascia.com)
- [Fetch vs. Axios.js for making HTTP requests](https://codeburst.io) (Sumber: codeburst.io)
- [JavaScript Fetch API and using Async/Await](https://www.javascripttutorial.net) (Sumber: javascripttutorial.net)


Berikut adalah pertimbangan performa untuk REST Client Axios dan Fetch:

### Axios:

- **Pengolahan Error yang Lebih Baik**:
  Axios memiliki kemampuan untuk menangani error dengan lebih baik dibandingkan dengan Fetch. Dalam Fetch, bahkan permintaan HTTP yang gagal (seperti status 404 atau 500) akan diselesaikan, dan harus diperiksa secara manual. Namun, Axios akan me-reject promise ketika terjadi kesalahan jaringan, atau jika respons tidak dalam kisaran 2xx, yang membuat penanganan error menjadi lebih mudah.

- **Fitur Tambahan**:
  Axios menawarkan fitur-fitur tambahan seperti interceptors, yang memungkinkan untuk menjalankan fungsi atau memodifikasi permintaan atau respons sebelum permintaan atau respons dijanjikan. Ini sangat berguna untuk tugas-tugas seperti logging, atau menambahkan header otomatis ke setiap permintaan.

- **Kemampuan untuk Membatalkan Permintaan**:
  Axios memiliki kemampuan untuk membatalkan permintaan yang sedang berlangsung, yang merupakan fitur yang tidak dimiliki Fetch.

- **Kemampuan untuk Memantau Kemajuan Permintaan**:
  Axios menawarkan kemampuan untuk memantau kemajuan permintaan, yang sangat berguna saat mengunggah file besar.

- **Transformasi Request dan Respons**:
  Axios memungkinkan Anda untuk mentransformasikan request dan respons sebelum mereka dijanjikan, atau bahkan setelah mereka dijanjikan. Ini dapat digunakan untuk serialisasi dan deserialisasi data otomatis.

- **Kompatibilitas Lintas-Browser dan Lintas-Lingkungan**:
  Axios dapat digunakan baik di browser dan Node.js, membuatnya menjadi pilihan yang baik untuk aplikasi isomorfik.

### Fetch:

- **Metode Bawaan Browser**:
  Fetch adalah API bawaan browser modern, yang berarti tidak memerlukan pustaka tambahan atau dependensi.

- **Sintaks yang Sederhana dan Mudah Dibaca**:
  Fetch menawarkan sintaks yang sederhana dan mudah dibaca, serta mengembalikan promises, yang membuat kode asinkron lebih mudah dibaca dan dirawat.

- **Tidak Memiliki Fitur Tambahan**:
  Berbeda dengan Axios, Fetch tidak memiliki fitur-fitur tambahan seperti interceptors atau kemampuan untuk membatalkan permintaan.

- **Penanganan Error yang Kurang Intuitif**:
  Seperti yang disebutkan sebelumnya, Fetch tidak akan me-reject promise pada respons error HTTP, yang berarti penanganan error harus dilakukan secara manual.

- **Tidak Ada Kemampuan untuk Memantau Kemajuan Permintaan**:
  Fetch tidak menawarkan kemampuan untuk memantau kemajuan permintaan, yang bisa menjadi kendala saat mengunggah file besar atau dalam skenario lain yang memerlukan pemantauan kemajuan.

Referensi:
- [LogRocket Blog](https://blog.logrocket.com/axios-or-fetch-api/) (source)

Tabel berikut memberikan ringkasan dari poin-poin di atas untuk pertimbangan performa antara Axios dan Fetch:

| **Aspek**                          | **Axios**                                 | **Fetch**                                |
|------------------------------------|-------------------------------------------|------------------------------------------|
| **Pengolahan Error**               | Lebih baik, otomatis me-reject pada error | Manual, tidak me-reject pada error HTTP |
| **Fitur Tambahan**                 | Ya, seperti interceptors                   | Tidak                                    |
| **Membatalkan Permintaan**         | Ya                                         | Tidak                                    |
| **Memantau Kemajuan Permintaan**   | Ya                                         | Tidak                                    |
| **Transformasi Request/Respons**   | Ya                                         | Tidak                                    |
| **Kompatibilitas Lintas-Lingkungan**| Ya, browser dan Node.js                    | Hanya browser                            |

Kesimpulan yang dapat diambil adalah bahwa Axios mungkin lebih cocok untuk skenario yang memerlukan penanganan error yang lebih baik, fitur tambahan seperti interceptors, atau kemampuan untuk membatalkan permintaan yang sedang berlangsung. Sementara Fetch mungkin lebih cocok untuk skenario yang lebih sederhana atau proyek yang ingin meminimalkan dependensi eksternal.
