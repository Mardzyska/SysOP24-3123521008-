# Pengertiang Paging
Paging adalah metode manajemen memori yang digunakan oleh sistem operasi. Dalam skema manajemen memori paging, data disimpan dan dikelola dalam blok yang konsisten identik yang disebut sebagai "halaman"

Paging biasanya terlihat dalam daftar hasil pencarian, galeri gambar, atau daftar posting blog yang dibagi menjadi beberapa halaman. Ini membantu mengelola konten yang besar sehingga pengguna tidak perlu menggulir terlalu jauh atau menunggu waktu pemuatan yang lama.

Teknik paginasi juga digunakan dalam database, di mana hasil query yang besar dibagi menjadi bagian-bagian kecil (halaman) untuk mempermudah manajemen data. Hal ini membantu mengoptimalkan kinerja dan memungkinkan pengguna untuk menavigasi hasil dengan lebih efisien.

# Pengertian Swapping
Swapping adalah teknik dalam sistem operasi di mana data yang tidak lagi diperlukan atau jarang digunakan dipindahkan dari memori utama (RAM) ke ruang swap di media penyimpanan sekunder, seperti hard disk atau SSD. Tujuan utama swapping adalah membebaskan ruang di memori utama agar dapat digunakan untuk menyimpan data yang lebih penting atau aktif.

* Pemindahan Sementara: Swapping memindahkan proses secara sementara dari memori utama ke disk. Ketika proses tersebut perlu dieksekusi, sistem operasi akan mengembalikannya ke memori utama.
* Waktu Transfer: Waktu yang dibutuhkan untuk mentransfer proses antara memori utama dan disk tergantung pada kecepatan transfer data. Misalnya, jika proses memiliki ukuran 5 MB dan kecepatan transfer disk adalah 20 MB per detik, maka waktu swap adalah sekitar 252 milidetik (ms)
* Prioritas: Dalam beberapa kasus, swapping dapat berdasarkan prioritas. Proses dengan prioritas lebih tinggi akan diberikan akses ke memori utama, sementara proses dengan prioritas lebih rendah akan dipindahkan ke disk hingga diperlukan kembali.
* Manajemen Memori: Swapping adalah salah satu teknik dalam manajemen memori yang memastikan alokasi memori yang efisien dan optimal. 
