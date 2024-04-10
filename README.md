# RAYCORP INDONESIA INTERNAL OPERATIONAL MANAGEMENT APPLICATION

## PENDAHULUAN
### 1.	LATAR BELAKANG
RayCorp Indonesia yang terletak di Jalan Bima No. 14 merupakan sebuah perusahaan di bidang retail, yang memiliki beberapa unit bisnis seperti Guppy Indonesia, Kopi Miring Group, dan GudangBerry Group. Sistem manajemen operasional internal perusahaan RayCorp masih dilakukan secara manual, sehingga Rayon Wibowo selaku CEO RayCorp Indonesia memiliki keinginan untuk mengotomatisasi dan mengintegrasikan semua sistem tersebut. Kami selaku pihak yang ditunjuk oleh RayCorp Indonesia untuk membangun sistem yang terdiri dari sistem absen, pengingat joblist, manajemen stok, dan pencatatan transaksi. Sistem ini akan dibangun berbasis mobile untuk mempermudah karyawan-karyawan dalam melakukan pekerjaannya sehingga lebih fleksibel(bisa dilakukan dimana saja dan kapan saja), meningkatkan efisiensi operasional, mengurangi resiko kesalahan, serta menciptakan lingkungan kerja yang lebih responsif dan adaptif terhadap dinamika bisnis yang cepat berubah. 
Oleh karena itu, pada laporan ini berisi penjelasan tentang cara pengembangan dari perancangan sistem yang akan dibangun untuk RayCorp Indonesia dengan  memberikan gambaran yang komprehensif tentang proses perancangan perangkat lunak sesuai kebutuhan perusahaan RayCorp Indonesia. Rancangan ini mencakup diagram-diagram yang menggambarkan bagaimana aplikasi ini akan beroperasi di masa mendatang. Laporan ini juga bertindak sebagai bahan evaluasi bagi CEO RayCorp untuk menentukan sejauh mana kesesuaian antara rancangan yang diusulkan dengan keinginan mereka. Dengan demikian, laporan ini diharapkan dapat membantu memastikan bahwa pembangunan sistem berjalan dengan lebih baik dan terencana dengan berbagai fitur yang jelas dan sesuai dengan kebutuhan perusahaan.

### 2.	TUJUAN
Tujuan pembuatan dokumen SRS ini yaitu : 
1.	Mengembangkan rancangan solusi perangkat lunak yang efektif dan efisien untuk mengotomatisasi dan mengintegrasikan sistem manajemen operasional internal perusahaan.
2.	Merancang sistem berbasis mobile agar karyawan dapat melakukan tugas mereka secara fleksibel, dimana saja dan kapan saja dengan tujuan meningkatkan efisiensi operasional.
3.	Menyajikan rancangan sistem secara komprehensif dengan menggunakan diagram-diagram untuk menjelaskan bagaimana aplikasi akan beroperasi di masa mendatang.
4.	Menyediakan laporan sebagai bahan evaluasi bagi CEO RayCorp Indonesia agar dapat menilai kesesuaian rancangan dengan keinginan dan kebutuhan perusahaan.
5.	Memberikan panduan yang jelas dan terstruktur untuk memastikan bahwa pembangunan sistem berjalan dengan baik dan terencana, dengan fokus pada fitur-fitur yang sesuai dengan kebutuhan perusahaan.

### 3.	AUDIENS YANG DITUJU DAN PEMBACA YANG DISARANKAN
Dokumen ini ditujukan untuk pihak RayCorp Indonesia terutama Pak Ray selaku Owner dan tim pengembang aplikasi. Dimana Owner RayCorp dapat melihat gambaran umum dari sistem yang akan dibuat dan hasil akhir yang ingin dicapai. Sehingga, owner dapat melakukan evaluasi agar sistem yang dibangun bisa sesuai dengan keinginan dan kebutuhan RayCorp. Lalu dokumen ini juga ditujukan ke pihak pengembang aplikasi, baik itu tim UI/UX, Programmer, Database Administrator dan lainnya, agar memahami sistem yang ingin dibuat. Sehingga bisa menjadi patokan pihak pengembang dalam mengembangkan sistem, agar mengurangi kesalahan dalam pengembangannya. Lalu dokumen ini juga disarankan untuk dibaca oleh end user sistem ini, yaitu karyawan RayCorp Indonesia. Sehingga mereka dapat mengerti bagaimana alur dari sistem yang akan mereka gunakan untuk bekerja nantinya.

### 4.	RUANG LINGKUP DAN BATASAN MASALAH
Berikut merupakan ruang lingkup dan batasan dalam pengembangan sistem ini, sehingga sistem tetap dapat terkontrol pengembangannya, yaitu : 
1.	Sistem yang dikembangkan hanya ditujukan untuk pihak RayCorp Indonesia, dengan karyawan sebagai penggunanya. 
2.	Sistem yang dikembangkan hanya berbasis mobile.
3.	Sistem dibuat untuk Role yang sudah ditentukan, yaitu Owner/CEO, Admin, Kasir, Finance dan Marketing. Owner/CEO akan bertindak sebagai Superuser atau Administrator dari akun Role lainnya. 
4.	Sistem dibuat dengan fitur untuk mengakses dashboard, menginput presensi, menginput joblist, membuat akun karyawan, menginput stok ikan, mencatat penjualan dan fitur otomatis untuk reminder.

### 5.	DEFINISI DAN SINGKATAN
| NO | ISTILAH           | DEFINISI                                                                                                                                                                                                                             |
|----|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  | SRS               | Software Requirements Specification adalah sebuah penjelasan tentang cara pengembangan dari sebuah software.                                                                                                                        |
| 2  | Class Diagram     | Diagram Kelas adalah salah satu jenis diagram struktur pada UML yang menggambarkan dengan jelas struktur serta deskripsi class, atribut, metode, dan hubungan dari setiap objek.                                                     |
| 3  | Use Case          | Use Case adalah deskripsi dari urutan aksi-aksi yang ditampilkan sistem yang menghasilkan suatu hasil yang terukur bagi suatu actor.                                                                                                   |
| 4  | Activity Diagram  | Activity Diagram adalah diagram yang bersifat dinamis dan digunakan untuk memperlihatkan aliran dari suatu aktifitas ke aktifitas lainnya dalam suatu sistem.                                                                            |
| 5  | Sequence Diagram  | Sequence Diagram adalah diagram yang bersifat dinamis dengan interaksi yang menekankan pada pengiriman pesan (message) dalam suatu waktu tertentu.                                                                                      |

### 6.	REFERENSI
•	Diktat Rekayasa Perangkat Lunak oleh Dr. Adi Nugroho, ST., MMSI

•	https://www.dicoding.com/blog/memahami-class-diagram-lebih-baik/

•	https://badr.co.id/id/panduan-menyusun-dokumen-software-requirement-specification-srs/


### 7.	NAMA SOFTWARE
Sistem Manajemen Operasional Internal RayCorp Indonesia atau RayCorp Operational Management System disingkat RCOPS.
 
## GAMBARAN UMUM
### 1.	URAIAN SINGKAT
RCOPS yang akan dibuat berbasis mobile, merupakan aplikasi internal untuk karyawan RayCorp Indonesia. Dimana aplikasi ini terdiri dari beberapa jenis Role yang akan memiliki fungsi dan tampilan berbeda. Kelima Role tersebut ialah CEO, Admin, Kasir, Finance dan Marketing. Untuk CEO akan menjadi Superuser atau Administrator untuk akun Role lainnya. Dimana tiap pembuatan akun Role baru dan penghapusan akun, hanya bisa dilakukan oleh CEO. Serta CEO dapat memasukkan Joblist berdasarkan Role masing-masing dan Dashboard yang dapat membantu CEO untuk melihat ringkasan informasi seperti stok. Untuk keempat Role lainnya memiliki kesamaan untuk bisa melihat Dashboard dan melakukan presensi. Tetapi ada tambahan fungsi lainnya seperti manajemen stok untuk Role Admin dan Role Kasir juga memiliki fungsi untuk bisa mencatat penjualan atau transaksi yang diterima dari Whatsapp ke dalam sistem. Untuk Role Kasir dan Admin akan saling terintegrasi, sehingga tiap Kasir mencatat penjualan, maka stok barang siap jual akan mengalami pengurangan jumlah. Sehingga Admin tidak perlu melakukan pengurangan jumlah stok secara manual lagi. Lalu sistem ini juga memiliki fitur otomatis untuk mengingatkan Joblist apa saja yang belum diselesaikan untuk Role Admin, Kasir, Finance dan Marketing. 

### 2.	KARAKTERISTIK PENGGUNA
Karakter yang disyaratkan dari pengguna RCOPS yaitu pengguna yang familiar denga aplikasi berbasis mobile.

### 3.	PENGGUNA
Berikut adalah kelima jenis pengguna RCOPS atau yang akan disebut dengan Role, yaitu : 

1.	CEO (Adminstrator) 
2.	Kasir
3.	Admin
4.	Finance
5.	Marketing

### 4.	PENGGOLONGAN KARAKTERISTIK PENGGUNA 

| Kategori Pengguna | Tugas                                    | Hak Akses ke Aplikasi                | Kemampuan yang harus dimiliki                             |
|-------------------|------------------------------------------|--------------------------------------|-----------------------------------------------------------|
| CEO               | Manajemen Akun Karyawan                  | Tambah dan Hapus Data Akun           | Memahami cara pembuatan akun dan proses penginputan data  |
|                   | Menginput Joblist                        | Tambah Data Joblist                  | Memahami cara menambahkan data                            |
| Admin, Kasir,     | Melakukan Presensi                       | Tambah Presensi kehadiran            | Memahami cara menambahkan data presensi                   |
| Finance dan       |                                          | (Check-In) dan kepulangan (Check-out)|                                                           |
| Marketing         |                                          |                                      |                                                           |
| Admin             | Manajemen Stok Barang                    | Tambah, Edit dan Hapus Data Stok     | Memahami cara manajemen Data Stok                         |
| Kasir             | Mencatat Penjualan yang diterima dari    | Tambah Data Penjualan                | Memahami cara memasukkan Data Penjualan                   |
|                   | Whatsapp                                 |                                      |                                                           |


### FITUR SOFTWARE
| NO  | FITUR                  | URAIAN                                                                                                                                                                                                                                                             |
|-----|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UMUM|                        |                                                                                                                                                                                                                                                                    |
| 1   | Login                  | Semua Role harus melakukan Login terlebih dahulu untuk masuk ke dalam sistem. Username dan Password untuk Role CEO akan diberikan oleh pengembang, sedangkan Role lainnya akan dibuat oleh CEO.                                                               |
| 2   | Mengakses Dashboard   | Setelah berhasil Login, setiap Role akan masuk ke Dashboard masing-masing yang disesuaikan dengan kebutuhan mereka.                                                                                                                                               |
| 3   | Menginput Presensi    | Fitur ini diperuntukkan bagi Role Admin, Kasir, Finance & Marketing untuk melakukan Presensi Hadir (Check-In) dan Pulang (Check-Out), serta memilih Ijin saat Presensi Hadir dan menyelesaikan Joblist.                                                          |
| 4   | Reminder               | Fitur otomatis untuk mengingatkan Role Admin, Kasir, Finance, dan Marketing tentang Joblist yang belum terselesaikan dan sudah terpending lama.                                                                                                                |
| CEO |                        |                                                                                                                                                                                                                                                                    |
| 1   | Manajemen Akun Karyawan| CEO dapat menambah dan menghapus Akun Karyawan serta membuat Username dan Password Karyawan.                                                                                                                                                                     |
| 2   | Menginput Joblist      | CEO dapat menambah Joblist untuk karyawan.                                                                                                                                                                                                                        |
| ADMIN|                        |                                                                                                                                                                                                                                                                    |
| 1   | Manajemen Stok         | Admin dapat menambah, mengedit, dan menghapus Stok, serta mengelola Stok berdasarkan label.                                                                                                                                                                       |
| KASIR|                        |                                                                                                                                                                                                                                                                    |
| 1   | Mencatat Penjualan     | Kasir mencatat penjualan yang diterima melalui Whatsapp ke dalam sistem untuk mempermudah perekapan penjualan dan pengurangan Stok.                                                                                                                                 |


### 5.	KETERGANTUNGAN SOFTWARE
Sistem yang dibangun ini sangat bergantung dengan koneksi internet. Sehingga, jika koneksi internet bermasalah, tentu akan menghambat proses berjalannya sistem. Selain itu sistem ini akan terbatas hanya bisa berjalan jika terkoneksi dengan WiFi dari RayCorp itu sendiri, untuk mencegah penyalahgunaan diluar jam kerja. Software yang berbasis mobile ini, tentu akan mempermudah fleksibilitas penggunanya, karena bisa digunakan di mana saja dan kapan saja. Maka dari itu karyawan diwajibkan untuk memiliki perangkat mobile. 

### 6.	SPESIFIKASI PENDUKUNG SOFTWARE
Berikut merupakan spesifikasi minimun untuk bisa menjalankan RCOPS di perangkat mobile, yaitu : 
•	Sistem Operasi : Android 10 atau Sistem Operasi yang setingkat (Seperti MIUI, One UI, Color OS dan lainnya) 

•	RAM : 4 GB 

•	ROM : 5 GB 

•	Koneksi Internet : Harus Stabil 


### 7.	BATASAN DESAIN DAN IMPLEMENTASI
Untuk masalah yang menjadi batasan bagi pihak pengembang, baik dari segi desain dan implementasi yaitu pemberian Label dalam fitur Manajemen Stok, cukup menjadi masalah yang lumayan susah untuk diselesaikan. Karena adanya label yang digunakan pada suatu Stok. Sebagai contoh, barang1 berjumlah 500 di gudang, tetapi 500 barang tersebut tidak semua dalam kondisi sama. Kondisi pada barang tersebut dinyatakan dengan Label, maka dari itu nantinya akan ada pembagian dari 500 barang1 menjadi 100 barang dengan label1 lalu 100 barang lagi dengan label2 dan seterusnya. Sehingga ini akan cukup menjadi persoalan untuk penyimpanannya ke dalam Database. Lalu untuk akses aplikasi hanya bisa melalui koneksi yang sudah disediakan pihak RayCorp, untuk meminimalisir penyalahgunaan sistem ini diluar jam kerja. Maka dari itu pihak pengembang harus bekerja sama dengan pihak penyedia layanan atau provider internet yang akan digunakan RayCorp nantinya. Sehingga untuk bagian ini, tentu akan memakan waktu yang cukup lama untuk pengimplementasiannya, karena perlunya koordinasi dua belah pihak.

### 8.	DOKUMENTASI PENGGUNA
Berikut merupakan daftar dokumentasi yang akan diberikan ketika sistem sudah selesai dibangun, yaitu : 
1.	Dokumen SRS
2.	Mockup Rancangan Sistem (Menggunakan Figma)

#### Link Figma: https://bit.ly/lsgfigmasraycorp
 
## ANALISIS KEBUTUHAN

### 1.	IDENTIFIKASI AKTOR
| NO  | AKTOR     | DESKRIPSI AKTOR                                                                                                                                  |
|-----|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | CEO       | Aktor menggunakan sistem ini untuk membuat/menghapus akun karyawan, membuat joblist untuk karyawan, dan melihat dashboard.                       |
| 2   | Admin     | Aktor menggunakan sistem ini untuk melakukan manajemen stok, menginput presensi, serta melihat dashboard dan joblist.                            |
| 3   | Kasir     | Aktor menggunakan sistem ini untuk mencatat penjualan, menginput presensi, serta melihat dashboard dan joblist.                                  |
| 4   | Finance   | Aktor menggunakan sistem ini untuk menginput presensi, serta melihat dashboard dan joblist.                                                      |
| 5   | Marketing | Aktor menggunakan sistem ini untuk menginput presensi, serta melihat dashboard dan joblist.                                                      |


### 2.	USE CASE DIAGRAM

![image](https://github.com/MeiLing19/RAYCORP-INDONESIA-INTERNAL-OPERATIONAL-MANAGEMENT-APPLICATION/assets/94893138/73955ba6-35c3-40c7-98d1-439f7ccae5c0)


Berikut merupakan deskripsi dari Use Case Diagram diatas :

| NO  | USE CASE                            | DESKRIPSI USE CASE                                                                                                                        |
|-----|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Membuat Akun Karyawan               | CEO sebagai administrator memiliki kemampuan untuk membuat akun karyawan baru dalam sistem dengan menetapkan izin akses sesuai rolenya.   |
| 2   | Menginput Joblist                   | CEO dapat menginput atau menetapkan joblist kepada setiap karyawan melalui dashboard.                                                     |
| 3   | Mengakses masing-masing Dashboard   | Setiap user akan masuk menggunakan akun khusus dan diarahkan ke dashboard masing-masing sesuai rolenya.                                   |
| 4   | Menginput Presensi                  | Marketing, Admin, Kasir, dan Finance dapat menginput presensi harian melalui masing-masing dashboard.                                     |
| 5   | Menginput Stok Ikan dengan Labeling | Admin dapat menginput stok ikan ke dalam sistem dengan memberikan label khusus untuk mempermudah manajemen stok.                          |
| 6   | Mencatat Penjualan                  | Kasir dapat mencatat penjualan harian melalui dashboard termasuk detail produk dan jumlahnya.                                             |
| 7   | Extend Reminder                     | Ketika para karyawan berhasil login, maka akan ada fitur reminder joblist pada masing-masing dashboard sesuai role.                       |


### 3.	ACTIVITY DIAGRAM
Setiap activity diagram dirancang untuk mencerminkan langkah-langkah yang terlibat dalam setiap tugas yang berkaitan dengan manajemen operasional internal perusahaan RayCorp Indonesia. Dan diagram ini menggambarkan secara lebih jelas dan rinci bagaimana proses tiap Use Case berjalan. 

![image](https://github.com/MeiLing19/RAYCORP-INDONESIA-INTERNAL-OPERATIONAL-MANAGEMENT-APPLICATION/assets/94893138/606ee8cf-2901-46f8-822c-d74139aa31f7)

 
### 4.	CLASS DIAGRAM
 
Kelas ‘Karyawan’ berfungsi sebagai entitas utama atau container utama yang akan berelasi dengan kelas-kelas lainnya.  Selain itu, kelas 'Karyawan' berfungsi sebagai kelas induk (parent class) yang memiliki beberapa kelas anak (child classes), seperti kelas 'Finance', 'Admin', 'CEO', 'Kasir', dan 'Marketing'. Ini mencerminkan struktur hierarki yang jelas dan memungkinkan pengorganisasian peran dengan lebih sistematis.
Pada class diagram ini menggunakan enumeration yang digunakan sebagai Role pada kelas ‘Karyawan’, sebagai Label pada kelas ‘Stok’, sebagai Status dan Jenis Presensi pada kelas ‘Presensi’. Enumeration membuat konstanta hak akses supaya dapat digunakan dikelas yang lain tanpa perlu di definisikan ulang pada tiap kelas yang ingin menggunakan hak akses.
Kelas Boundary ‘Whatsapp Integration’ merupakan kelas yang menghubungkan antara dunia luar dengan sistem aplikasi ini. Dalam konteks ini, kelas ini bertanggung jawab untuk mengintegrasikan orderan yang diterima melalui WhatsApp ke dalam fitur transaksi di dalam sistem aplikasi manajemen operasional internal RayCorp Indonesia. Ini menunjukkan adanya antarmuka yang efisien antara sistem internal dan input eksternal.
Kelas Entity ‘Stok’ dan ‘Transaksi’ merupakan kelas yang berhubungan dengan database. Kedua kelas ini berfungsi sebagai entitas yang terhubung dengan basis data, menyediakan wadah untuk informasi terkait stok dan transaksi. Dengan keterkaitan langsung ini, sistem dapat efisien mengelola informasi terkini terkait stok dan sejarah transaksi dengan akurat.

![image](https://github.com/MeiLing19/RAYCORP-INDONESIA-INTERNAL-OPERATIONAL-MANAGEMENT-APPLICATION/assets/94893138/8fc8ef65-ca4c-4f64-a9ae-f3a74ba99d66)


### 5.	SEQUENCE DIAGRAM
Diagram ini menggambarkan bagaimana tiap objek dalam sistem saling berinteraksi dalam satu waktu. Dimana interaksi ini dijelaskan secara berurut sesuai dengan Activity Diagram. Serta menampilkan apa saja reaksi dari setiap input maupun output yang ada di dalam sistem.

![image](https://github.com/MeiLing19/RAYCORP-INDONESIA-INTERNAL-OPERATIONAL-MANAGEMENT-APPLICATION/assets/94893138/2f179f03-c140-480a-8cf5-c2b7421bc58d)

 
 
  
## FUNCTIONAL REQUIREMENT
Berikut merupakan Functional Requirement atau Kebutuhan Fungsional dari RCOPS, yaitu :

| No  | Kebutuhan Fungsional              | Penjelasan                                                                                                                                                          |
|-----|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Login ke akun                     | Setiap pengguna harus dapat login ke akun masing-masing sesuai peran (role) mereka.                                                                                 |
| 2   | Mengakses masing-masing dashboard | Setiap pengguna harus dapat mengakses dashboard yang sesuai dengan peran (role) mereka.                                                                             |
| 3   | Melakukan presensi                | Pengguna selain CEO harus dapat melakukan presensi ketika login.                                                                                                    |
| 4   | Melihat joblist                   | Kasir, admin, finance, dan marketing harus dapat melihat joblist mereka masing-masing sesuai dengan peran (role) mereka.                                            |
| 5   | Manajemen akun pengguna           | CEO harus dapat membuat, mengedit, melihat, dan menghapus akun pengguna, serta memberikan hak akses sesuai dengan peran (role) pengguna tersebut.                   |
| 6   | Manajemen joblist                 | CEO harus dapat menambah dan menghapus joblist untuk setiap pengguna.                                                                                               |
| 7   | Menginput penjualan               | Kasir harus dapat memasukkan data penjualan dan membatalkan inputan data tersebut.                                                                                  |
| 8   | Manajemen stok                    | Admin harus dapat menambah, melihat, mengedit, dan menghapus stok barang.                                                                                           |
| 9   | Memberikan reminder               | Sistem harus memberikan reminder secara otomatis kepada admin, kasir, finance, dan marketing jika ada joblist yang belum diselesaikan dalam tenggat waktu tertentu. |


 
## NON FUNCTIONAL REQUIREMENT
Berikut merupakan Non Functional Requirement atau Kebutuhan Non Fungsional dari RCOPS, yaitu : 
| No  | Kebutuhan Non Fungsional  | Penjelasan                                                                                                                |
|-----|---------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 1   | Antarmuka pengguna        | Antarmuka pengguna harus berbasis mobile, ramah pengguna, dan mematuhi prinsip dasar desain UI/UX.                        |
| 2   | Kinerja sistem            | Sistem harus mampu memproses minimal 50 pencatatan penjualan dalam satu waktu.                                            |
| 3   | Keamanan aplikasi         | Aplikasi hanya dapat diakses ketika tersambung dengan jaringan lokal yang disediakan oleh pihak RayCorp Indonesia.        |
| 4   | Koneksi internet          | Koneksi internet yang disediakan oleh pihak RayCorp harus cukup cepat untuk mendukung banyak pengguna dalam satu waktu.   |
| 5   | Layanan IT                | RayCorp harus mendirikan divisi baru, yaitu IT, untuk merawat aplikasi dan menangani troubleshooting selama jam kerja.    |


 
