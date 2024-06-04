## 1. Berikan tiga contoh pemrograman di mana multithreading memberikan kinerja yang lebih baik daripada solusi dengan satu thread.
* Aplikasi Web Server:
a. Ketika mengimplementasikan web server, menggunakan multithreading memungkinkan server menangani banyak permintaan dari klien secara bersamaan.

b. Setiap permintaan dari klien dapat dijadwalkan ke thread yang berbeda, sehingga mengurangi waktu tunggu dan meningkatkan responsivitas server1.
* Pengolahan Data Paralel:
a. Misalkan kita memiliki tugas pengolahan data besar, seperti menghitung statistik dari set data yang besar.

b. Dengan menggunakan multithreading, kita dapat membagi tugas ini menjadi beberapa thread yang masing-masing menghitung bagian dari data.

c. Hasilnya, pengolahan data dapat dilakukan secara paralel, mengurangi waktu eksekusi secara signifikan2.
* Aplikasi Grafis dan Animasi:
a. Dalam aplikasi grafis atau animasi, seperti permainan video, multithreading memungkinkan pemrosesan gambar, fisika, dan interaksi pengguna berjalan secara bersamaan.

b. Thread terpisah dapat mengurus rendering grafis, menghitung fisika, dan menangani masukan pengguna tanpa menghambat satu sama lain.

c. Hasilnya, aplikasi menjadi lebih responsif dan lancar3.

## 2 Apa dua perbedaan antara user-level threads dan kernel-level threads? Dalam situasi apa salah satu jenis lebih baik daripada yang lain?

a. User-level threads tidak dikenal oleh kernel, sedangkan kernel mengetahui kernel threads.

b. Pada sistem yang menggunakan pemetaan M:1 atau M:N, user threads dijadwalkan oleh pustaka thread, sedangkan kernel menjadwalkan kernel threads.

c. Kernel threads tidak perlu terkait dengan proses, sedangkan setiap user thread terkait dengan proses. Kernel threads umumnya lebih mahal untuk dikelola daripada user threads karena harus direpresentasikan dengan struktur data kernel.

## 3 Jelaskan tindakan yang diambil oleh kernel untuk beralih konteks antara kernel-level threads.

Beralih konteks antara kernel threads biasanya melibatkan menyimpan nilai register CPU dari thread yang akan digantikan dan mengembalikan nilai register CPU dari thread baru yang akan dijadwalkan.

## 4. Sumber daya apa yang digunakan ketika sebuah thread dibuat? Bagaimana perbedaannya dengan sumber daya yang digunakan ketika sebuah proses dibuat?
Saat sebuah thread dibuat, sumber daya yang digunakan meliputi memori, stack, waktu CPU, dan sumber daya sinkronisasi. Perbedaannya dengan pembuatan proses adalah bahwa thread berbagi memori dan sumber daya dengan thread lain dalam proses yang sama, sementara proses memiliki alokasi memori dan sumber daya terpisah. Pembuatan thread memiliki overhead yang lebih rendah dan komunikasi antara thread biasanya lebih efisien daripada antar proses.

## 5. Anggaplah sistem operasi memetakan user-level threads ke kernel menggunakan model banyak-ke-banyak dan pemetaan dilakukan melalui LWPs. Selain itu, sistem memungkinkan pengembang untuk membuat real-time threads untuk digunakan dalam sistem real-time. Apakah perlu mengikat real-time thread ke LWP? Jelaskan.
Dalam sistem dengan pemetaan user-level threads ke kernel menggunakan LWPs, real-time threads biasanya tidak perlu diikat langsung ke LWP. Mereka memiliki mekanisme penjadwalan tersendiri di kernel untuk menangani prioritas waktu dan persyaratan waktu yang ketat. Oleh karena itu, tidak perlu mengikat real-time threads ke LWPs.
