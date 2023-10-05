# **Object-Relational Mapping: Sequelize vs TypeORM vs Prisma**

**Pendahuluan:**
Dalam pengembangan aplikasi berbasis Node.js, memilih sebuah ORM yang tepat adalah salah satu keputusan penting yang akan mempengaruhi bagaimana kita berinteraksi dengan basis data dan menentukan struktur dari kode basis data kita. Sequelize, TypeORM, dan Prisma adalah tiga ORM yang populer dalam ekosistem Node.js, masing-masing menawarkan pendekatan yang berbeda dalam menangani interaksi basis data. 

Sequelize adalah ORM yang multi SQL dialect yang mendukung PostgreSQL, MySQL, MariaDB, SQLite, dan MSSQL dan memiliki fitur OOP yang solid, seperti Class dan Instance, yang memungkinkan kita untuk menulis kode yang modular dan reusable. 

TypeORM adalah ORM yang sangat fleksibel dan modular, menawarkan dukungan luas untuk berbagai database SQL dan NoSQL dan fokus pada dukungan TypeScript, memungkinkan pengembangan aplikasi dengan fitur ES6 modern dan pengecekan tipe statis.

Prisma, di sisi lain, adalah pendatang baru yang menawarkan pendekatan yang berbeda dari ORM tradisional, di mana ia bertindak sebagai layer query builder yang menghasilkan akses data yang aman dan efisien, dengan dukungan kuat untuk TypeScript dan flow-typing.

Mari kita bandingkan ketiga ORM ini berdasarkan beberapa kriteria untuk memahami kelebihan dan kekurangan masing-masing dan untuk membantu Anda memilih yang terbaik sesuai dengan kebutuhan proyek Anda.

## **1. Developer Experience dalam Membangun Sebuah Proyek Mini:**

Berdasarkan pengalaman beberapa pengembang saat membangun proyek mini menggunakan ketiga ORM ini, berikut adalah beberapa temuan kunci:

- **Sequelize:**
  - **Dialect Support:** Sequelize mendukung banyak dialect SQL seperti PostgreSQL, MySQL, dan lainnya, memberi fleksibilitas kepada pengembang untuk memilih database.
  - **Object-Relational Mapping:** Dengan fitur ORM, Sequelize memungkinkan interaksi dengan database menggunakan objek dan model yang mudah dipahami dan diimplementasikan.
  - **Associations:** Sequelize menyediakan fitur associations yang mempermudah dalam mendefinisikan relasi antar tabel di database.
  - **Migrations and Seeders:** Dukungan untuk migrasi dan seeder memudahkan pengelolaan schema database dan pengisian data awal.
  - **Reference:** [Sequelize Documentation](https://sequelize.org/master/)

- **TypeORM:**
  - **TypeScript Support:** TypeORM dibangun dengan fokus pada dukungan TypeScript, memungkinkan pengembangan dengan pengecekan tipe statis dan fitur ES6 modern.
  - **Wide Range Database Support:** Dukungan untuk berbagai database SQL dan NoSQL memudahkan pengembang yang bekerja dengan berbagai jenis database.
  - **Active Record and Data Mapper:** TypeORM mendukung pola Active Record dan Data Mapper, memberi fleksibilitas dalam mendefinisikan struktur kode basis data.
  - **Decorators:** Syntax decorator yang digunakan oleh TypeORM membuat kode lebih bersih dan mudah dibaca.
  - **Reference:** [TypeORM Documentation](https://typeorm.io/#/)

- **Prisma:**
  - **Intuitive Query Builder:** Prisma menyediakan query builder yang intuitif dan mudah digunakan, menghasilkan akses data yang efisien dan aman.
  - **Strong TypeScript Support:** Dengan dukungan kuat untuk TypeScript, Prisma memastikan bahwa kode yang dikembangkan adalah tipe-aman dan mudah dikelola.
  - **Auto-Generated Types:** Prisma secara otomatis menghasilkan tipe dari skema database, mempermudah pengembangan dengan autocompletion dan type checking.
  - **Migrations:** Sistem migrasi Prisma yang kuat mempermudah perubahan dan pengelolaan skema database.
  - **Reference:** [Prisma Documentation](https://www.prisma.io/docs/)

## **2. Komponen:**

| Kriteria      | Sequelize | TypeORM | Prisma |
|---------------|-----------|---------|--------|
| Maintenance   | 4         | 4       | 4      |
| Reputable     | 4         | 4       | 4      |
| Compatibility | 4         | 4       | 4      |
| Community     | 4         | 4       | 4      |
| Documentation | 4         | 4       | 4      |
| Licensing     | 4         | 4       | 4      |
| Extensible    | 3         | 4       | 3      |
| Size          | 3         | 3       | 3      |
| **Total Score**   | **30**      | **31**    | **30**    |


## **3. Mengapa memilih salah satunya?**

- **Mengapa memilih Sequelize?**
  - **Pro**:
    1. Sequelize mendukung berbagai DBMS seperti MySQL, PostgreSQL, SQLite, dan MSSQL.
    2. Dengan Sequelize, Anda bisa menggunakan JavaScript murni dan Objek JavaScript.
    3. Komunitas yang aktif dan dukungan yang baik.
    4. Dokumentasi yang sangat lengkap dan jelas.
  - **Con**:
    1. Untuk pengguna yang tidak familiar dengan SQL, Sequelize mungkin tampak rumit.
    2. Terkadang, menghasilkan query yang tidak efisien.
    
- **Mengapa memilih TypeORM?**
  - **Pro**:
    1. TypeORM sangat cocok untuk proyek TypeScript.
    2. Mendukung berbagai tipe database seperti SQL, MongoDB, dan lain-lain.
    3. Mudah diintegrasikan dengan framework lain seperti NestJS.
    4. Dekorator dan sintaks yang ramah pengguna.
  - **Con**:
    1. Pengembangan fitur lebih lambat dibanding ORM lainnya.
    2. Dokumentasi bisa lebih lengkap dan lebih jelas di beberapa bagian.
    
- **Mengapa memilih Prisma?**
  - **Pro**:
    1. Prisma menyediakan akses ke database yang aman, mudah, dan kuat.
    2. Schema yang kuat dan tipe data yang aman.
    3. Auto-completion yang baik dan pengalaman pengembangan yang menyenangkan.
    4. Performa tinggi dan optimasi tingkat tinggi.
  - **Con**:
    1. Tidak sepenuhnya cocok untuk semua jenis proyek.
    2. Beberapa fitur masih dalam pengembangan dan belum stabil.

**Jika menggunakan Sequelize:**
| **Pros** | **Cons** |
|----------|----------|
| 1. Mendukung berbagai DBMS. | 1. Kurva belajar bagi yang tidak familiar dengan SQL. |
| 2. Sintaks yang familiar bagi pengguna JavaScript. | 2. Bisa menghasilkan query yang kurang efisien. |
| 3. Komunitas aktif dan dukungan yang baik. | 3. Mungkin overkill untuk proyek-proyek kecil. |
| 4. Dokumentasi lengkap. | 4. Butuh waktu untuk menguasai fitur-fitur lanjutan. |

**Jika menggunakan TypeORM:**
| **Pros** | **Cons** |
|----------|----------|
| 1. Cocok untuk TypeScript. | 1. Pengembangan fitur bisa lebih lambat. |
| 2. Dukungan untuk berbagai tipe database. | 2. Beberapa bagian dokumentasi kurang jelas. |
| 3. Integrasi baik dengan framework lain. | 3. Butuh waktu untuk menguasai. |
| 4. Sintaks ramah pengguna. | 4. Mungkin ada bug atau isu yang belum teratasi. |

**Jika menggunakan Prisma:**
| **Pros** | **Cons** |
|----------|----------|
| 1. Akses database yang aman dan mudah. | 1. Tidak cocok untuk semua jenis proyek. |
| 2. Schema yang kuat dan tipe data yang aman. | 2. Beberapa fitur masih dalam pengembangan. |
| 3. Pengalaman pengembangan yang menyenangkan. | 3. Kurva belajar untuk fitur-fitur lanjutan. |
| 4. Performa tinggi. | 4. Mungkin ada batasan penggunaan dalam kasus tertentu. |

**Referensi:**
- [Sequelize Documentation](https://sequelize.org/master/)
- [TypeORM Documentation](https://typeorm.io/#/)
- [Prisma Documentation](https://www.prisma.io/docs/)

## 4. Kapan Sebaiknya Menggunakan ORM Ini?

- **Kapan Sequelize Cocok Dipakai?**
  1. **Relational Database**: Sequelize adalah pilihan yang baik untuk mereka yang menggunakan basis data relasional seperti MySQL, MariaDB, PostgreSQL, dan lain-lain.
  2. **Modeling Data Dinamis**: Jika Anda ingin mengimplementasikan schema dinamis dan relasi yang kompleks antar tabel, Sequelize menyediakan metode dan fungsi bawaan yang lengkap.
  3. **Transaksi**: Dukungan untuk transaksi membuat Sequelize cocok untuk aplikasi yang memerlukan operasi basis data yang aman dan dapat di-rollback.
  4. **Custom Queries**: Jika Anda perlu menulis query SQL kustom tetapi masih ingin memanfaatkan fitur ORM, Sequelize memungkinkan ini.

- **Kapan TypeORM Cocok Dipakai?**
  1. **Projek TypeScript**: TypeORM adalah solusi ORM yang baik untuk proyek yang menggunakan TypeScript, meskipun juga mendukung JavaScript.
  2. **Decorators dan OOP**: Jika Anda menginginkan syntax yang rapi dengan decorator dan pendekatan berorientasi objek, TypeORM adalah pilihan yang tepat.
  3. **Support untuk Berbagai Database**: TypeORM mendukung berbagai tipe basis data, baik SQL maupun NoSQL, memberikan fleksibilitas dalam memilih database.
  4. **Migrasi dan CLI**: Fitur migrasi dan CLI yang kuat mempermudah proses pengembangan dan penyesuaian schema database.

- **Kapan Prisma Cocok Dipakai?**
  1. **Type-Safety dan Auto-completion**: Prisma adalah pilihan tepat jika Anda mencari fitur type-safety dan auto-completion yang baik, terutama dalam proyek TypeScript.
  2. **Database Agnostik**: Prisma mendukung berbagai jenis database SQL dan NoSQL, membuatnya menjadi solusi yang fleksibel.
  3. **Performa dan Optimalisasi Query**: Jika performa adalah prioritas, Prisma memungkinkan pengoptimalan query yang baik dan memiliki kemampuan untuk menghasilkan SQL yang efisien.
  4. **Schema Declarative**: Dengan Prisma, Anda mendefinisikan schema Anda dalam sebuah file konfigurasi, membuatnya menjadi mudah dibaca dan dirawat.


## 5. Popularitas:

- **Sequelize** telah memperoleh banyak perhatian dari komunitas pengembang dengan 28,400 bintang dan 1,063 kontributor. Dalam 12 bulan terakhir, popularitasnya tampak meningkat sekitar 10%. Sebagai perbandingan, **TypeORM**, walaupun sudah populer, memiliki 32,100 bintang dengan 994 kontributor. Popularitas TypeORM dalam setahun terakhir menunjukkan pertumbuhan sekitar 20%. Di sisi lain, **Prisma**, meskipun relatif baru, telah dengan cepat mendapatkan traksi dengan 34,000 bintang dan 220 Kontributor. Yang menarik, Prisma menunjukkan peningkatan popularitas paling pesat dalam 12 bulan terakhir, dengan pertumbuhan sekitar 120%.

## 6. Pertimbangan Performa untuk Tiga ORM:

Performa dari Sequelize, TypeORM, dan Prisma dapat berbeda tergantung pada bagaimana setiap ORM digunakan dan dikonfigurasi, serta kebutuhan spesifik dari proyek Anda. Berikut adalah gambaran umum pertimbangan performa untuk masing-masing ORM:

- **Sequelize:**
  - **Dukungan Bahasa:** Mendukung TypeScript dan JavaScript, menjadikannya opsi yang baik untuk proyek berbasis JavaScript.
  - **Query Builder:** Sequelize menggunakan query builder, memungkinkan pembangunan query kompleks menggunakan JavaScript atau TypeScript. Ini bisa lebih sesuai untuk query yang lebih kompleks.
  - **Pendefinisian Hubungan:** Mendefinisikan hubungan dengan metode konvensional, yaitu constraint foreign key ditentukan dalam migrasi atau definisi model.
  - **Dukungan Database:** Menawarkan dukungan yang lebih luas untuk database, seperti MySQL, PostgreSQL, SQLite, dan Microsoft SQL Server.

- **TypeORM:**
  - **Dukungan Bahasa:** Lebih cocok untuk proyek berbasis TypeScript.
  - **Repository Pattern:** Menggunakan pattern repository, memudahkan operasi CRUD dasar dengan metode seperti find, findOne, save, update, dan delete. Ini bisa lebih user-friendly untuk operasi CRUD sederhana.
  - **Pendefinisian Hubungan:** Mendefinisikan hubungan dengan dekorator dalam desain model Anda, pendekatan yang lebih kontemporer.
  - **Performa:** Menunjukkan performa yang unggul dalam skenario stress saat membuat catatan baru, dan memiliki fleksibilitas serta dukungan untuk query SQL mentah.

- **Prisma:**
  - **Optimasi Query:** Optimasi query, batching, dan update real-time Prisma berkontribusi pada efisiensi performa keseluruhan.
  - **Performa Pembacaan:** Memulai dengan cepat dalam query bacaan, tetapi mengalami penurunan performa seiring dengan penambahan catatan ke dalam database.
  - **Dukungan Database:** Mendukung berbagai database seperti MySQL, PostgreSQL, MariaDB, SQLite, Oracle, Microsoft SQL Server, dan MongoDB.

## **7. Kesimpulan:**

- Jika proyek Anda membutuhkan dukungan untuk berbagai bahasa pemrograman seperti JavaScript dan TypeScript, **Sequelize** mungkin menjadi pilihan yang baik, terutama karena mendukung beragam database dan menggunakan pendekatan konvensional dalam mendefinisikan hubungan antartabel.
  
- Untuk pengembangan yang lebih condong pada TypeScript dan menyukai pendekatan dekoratif dalam mendefinisikan relasi antar tabel, **TypeORM** bisa menjadi opsi yang sesuai. Ini juga menjadi pilihan yang baik untuk operasi CRUD yang lebih sederhana dan memungkinkan penggunaan raw SQL untuk kebutuhan yang lebih kompleks.

- **Prisma** mendukung optimasi query, batching, dan real-time updates yang membuatnya efisien dalam hal performa. Jika aplikasi Anda memiliki pola query yang kompleks dan membutuhkan pembaruan data secara real-time, Prisma dapat menjadi pilihan yang optimal.
  
- Dalam hal performa, TypeORM dan Prisma memiliki karakteristik yang hampir sama dalam beberapa skenario. Namun, Prisma cenderung sedikit lebih cepat dalam beberapa kasus dan menjadi lebih lambat seiring dengan penambahan record dalam database, sehingga TypeORM dapat menjadi lebih cepat untuk aplikasi dengan data yang sangat besar.

- Untuk skenario penulisan di bawah tekanan (stress scenario), TypeORM memiliki performa yang superior, namun informasi ini mungkin sudah usang karena Prisma terus melakukan update dan optimasi.
  
- Dalam kasus penggunaan spesifik dan kebutuhan database tertentu, pilihan ORM akan sangat bergantung pada kebutuhan proyek dan preferensi tim pengembangan.

- Secara keseluruhan, pilihan ORM harus mempertimbangkan kebutuhan proyek, kepreferensian bahasa pemrograman, jenis database yang digunakan, dan bagaimana hubungan antar tabel didefinisikan dan dikelola. Melakukan benchmarking dan pengujian dalam konteks proyek tertentu juga sangat direkomendasikan untuk menentukan karakteristik performa yang paling sesuai dengan kebutuhan aplikasi.



### Referensi:

- [Sequelize Documentation](https://sequelize.org/master/)
- [TypeORM Documentation](https://typeorm.io/#/)
- [Prisma Documentation](https://www.prisma.io/docs/)
- [Prisma vs. TypeORM – Which is Right For You?](https://spin.atomicobject.com/2023/08/22/prisma-vs-typeorm/)
- [Battle of the Node.js ORMs: Sequelize vs TypeORM](https://dev.to/victor1890/battle-of-the-nodejs-orms-sequelize-vs-typeorm-35ng)
- [Npm Trends: Prisma vs Sequelize vs Typeorm usage](https://npmtrends.com/prisma-vs-sequelize-vs-typeorm)