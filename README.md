Boot Process
![Uploading WhatsApp Image 2024-03-03 at 20.03.58_3672de1b.jpg…]()


Boot adalah proses awal pada saat menyalakan komputer dimana sistem komputer akan membaca seluruh hardware dan software guna memastikan bahwa komputer siap dinyalakan.

POST (Power On Self Test): adalah prosesTahapan yang paling awal adalah menyalakan komputer dengan menekan tombol ON pada CPU yang mana akan menyuplai listrik ke komponen-komponen utama komputer.

Bootloader :Yaitu tahap mencari sistem operasi pada hard drive dan mulai memuat sistem operasi yang ditemukan, seperti Linux, macOS, atau Windows.

Sistem Operasi : Pada langkah ini, sistem operasi dimuat ke dalam memori utama. Kemudian sistem operasi mulai bekerja dan mengeksekusi semua file dan instruksi awal.

Dekstop : Pada tahap ini yang merupakan tampilan grafis utama dari sistem operasi. Pengguna dapat menjalankan program, membuka file, dan mengelola komputer dari desktop.

Jenis-jeni Booting 

1. Warm Booting
Warm booting adalah proses memulai ulang komputer tanpa mematikan daya secara fisik, atau biasa disebut dengan restart. 
Saat melakukan warm booting, komputer akan me-reset ulang dirinya sendiri dan memulai kembali proses booting tanpa mematikan daya. 
Warm booting biasanya dilakukan untuk tujuan tertentu, seperti memperbaiki masalah dan mengatur ulang pengaturan.

2. Cold Booting
Cold booting adalah proses umum yang dilakukan ketika menghidupkan komputer awalnya dalam mati. 
Saat melakukan cold booting, arus listrik mengalir ke komponen yang sebelumnya tidak memiliki daya. 
Tujuannya adalah untuk menghidupkan komponen dan mengaktifkan kembali komputer yang sebelumnya mati.

3. Soft Booting
Soft booting adalah proses yang terjadi ketika komputer dan komponennya dalam keadaan hidup atau sudah mendapatkan aliran listrik. Lalu, apa perbedaannya dengan warm booting?
Soft booting adalah proses yang terjadi secara otomatis oleh sistem komputer. Jadi, booting ini tidak dilakukan karena adanya masalah. 
Soft booting umumnya hanya saat ada perubahan pada BIOS atau pengaturan keamanan. 

4. Hard Booting
Jika jenis-jenis booting sebelumnya dilakukan secara sukarela tanpa paksaan, hal berbeda berlaku untuk hard booting. 
Hard booting adalah proses yang dilakukan secara paksa dengan menekan tombol reset pada CPU (Central Processing Unit), atau casing komputer. 
Hal ini biasanya dilakukan ketika terjadi masalah yang mengakibatkan komputer tidak dapat beroperasi dengan normal.

5. Rebooting
Rebooting adalah proses memulai ulang sistem operasi komputer tanpa mematikan daya. Proses ini dilakukan ketika sistem tidak merespons, terjadi perubahan pada sistem operasi setelah pembaruan dilakukan, atau saat instalasi driver perangkat keras dilakukan. 
Tujuan dari rebooting adalah untuk memperbaiki masalah yang terjadi atau menerapkan pengaturan dengan benar. 
Permintaan untuk melakukan rebooting biasanya muncul setelah adanya perubahan yang dilakukan pada sistem komputer, seperti instalasi aplikasi atau driver. 
Melakukan rebooting umumnya merupakan langkah yang diperlukan jika diminta.


Mengidentifikasi Laptop


![Screenshot (386)](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/47160b2c-583b-4766-970c-6db95ab8748f)

CPU: Tab ini menunjukkan informasi tentang prosesor, seperti nama, kode nama, kecepatan clock, jumlah inti, dan teknologi yang digunakan.

Processor menunjukan :

Nama atau jenis dari processor yaitu " Intel Celeron N4100 "

Code Name yaitu menunjukan "Gemini Lake " 

Package pada gambar menunjukan jenis paket yang digunakan prosesor "Socket 1090 FCBGA" 

Technology menunjukan proses manufaktur yang digunakan "14 nm" lalu setelah itu

Specification menunjukan nama lengkap dan nomor model"Intel® Celeron® N4120 CPU @1. 10Hz" '

Family menunjukan jenis keluarga yaitu "6"

Ext. Family "6" 

Model "A"

Ext. Model 

Stepping "8"

revision "R0"

Instructions "NMX, SSE, SSE2, SSE3, SSSE3, SSE41, SSE4,2, EM64T, VT-x, AES, SHA"
Max TDP "6.0 W" dan Code VID yaitu "0.880 V"

Clocks (core #0) menunjukan :

Core Speed menunjukan kecepatan "1690.56 MHz"

Multplier x 17.0
Bus Speed 99.44MHz
L1 Data: Menunjukkan ukuran cache L1 data, dalam hal ini "4x 24 KBytes + 6-way".
L1 Inst.: Menunjukkan ukuran cache L1 instruksi, dalam hal ini "4 x 32 KBytes + 8-way".
Level 2: Menunjukkan ukuran cache L2, dalam hal ini "4MBytes".
Level 3: menunjukan kosong


![Screenshot (387)](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/29753310-c90d-471c-ae85-39e5bfbd06d2)
Informasi Motherboard :

Manufacture yaitu "HP"

Model Motheboardnya adalah "864D/58.20"

Bus specs yaitu "PCI-Express 2.0 (5.0 GT/s)"

Chipset "Intel/gemini lake host bridge (Rev. 06)"

Southbridge "Intel/gemini lake LPC bridge (Rev. 06)"

Informasi BIOS :

Brand : AMI

Version : F.30

Date : 07/04/2023


![Screenshot (388)](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/4b2d1286-1621-475e-a4bc-318d9e7013d0)

Informasi Memory :

General Type yaitu DDR4

Size : 4GB

Informasi Timings :

FSB:DRAM: Menunjukkan rasio antara FSB dan DRAM clock speed, dalam hal ini 1:12.

![Screenshot (389)](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/fda9f503-5f94-4895-8537-b67d123ad2cb)

Informasi SPD :

Di kolom Memory Selection tersebut, jumlah kolom menu yang ada mengikuti jumlah slot RAMnya. Misalnya terdapat 4 menu, artinya ada 4 slot RAM. Dan seterusnya.

![Screenshot (390)](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/148df31e-78a9-4624-b5cc-c1ee07f6bd69)

Informasi Graphich :

GPU menunjukan informasi nama, Board manuf, Code name, Technology, Revision.

![Screenshot (391)](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/30fd342e-4c81-4d8f-bd9e-ace3187a9e49)

Informasi Bench :

Pada gambar diatas menunjukan dari Versi Bachmark dan informasi processor


