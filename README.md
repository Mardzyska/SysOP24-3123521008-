## Perbedaan RICS dan CISC

Perbedaan utama antara CISC (Complex Instruction Set Computing) dan RISC (Reduced Instruction Set Computing) terletak pada desain arsitektur CPU dan pendekatan mereka terhadap pemrosesan instruksi. Berikut adalah beberapa perbedaan kunci:

- **Unit Pemrograman**:
  - **RISC**: Menggunakan unit pemrograman terprogram, yang berarti instruksi lebih sederhana dan sering berbasis register.
  - **CISC**: Memiliki unit pemrograman mikro, yang memungkinkan untuk instruksi yang lebih kompleks dan sering kali langsung berinteraksi dengan memori.

- **Set Instruksi**:
  - **RISC**: Memiliki set instruksi yang lebih kecil dan optimasi berbasis perangkat lunak, yang mengarah pada waktu eksekusi yang lebih singkat untuk setiap instruksi.
  - **CISC**: Memiliki set instruksi yang lebih besar dan kompleks dengan optimasi berbasis perangkat keras, yang memungkinkan untuk operasi yang lebih kompleks dalam satu instruksi.

- **Mode Pengalamatan**:
  - **RISC**: Biasanya memiliki mode pengalamatan yang lebih terbatas dan menggunakan format instruksi tetap (seperti 32 bit).
  - **CISC**: Dapat memiliki rentang format instruksi yang lebih variabel (16-64 bit) dan mode pengalamatan yang lebih banyak³.

- **Performa**:
  - **RISC**: Dikenal dengan performa yang cepat karena waktu eksekusi yang konstan dan kompleksitas yang lebih rendah.
  - **CISC**: Meskipun mungkin lebih lambat per instruksi karena kompleksitasnya, ia dapat mengurangi jumlah total instruksi per program.
 
## Hubungan Arsitektur CPU dengan Arsitektur OS

Hubungan antara arsitektur CPU (Central Processing Unit) dan arsitektur sistem operasi (OS) adalah sangat penting karena keduanya harus bekerja secara harmonis untuk memastikan kinerja sistem komputer yang efisien. Berikut adalah beberapa aspek kunci dari hubungan ini:

- **Kompatibilitas**: Arsitektur CPU harus kompatibel dengan arsitektur OS agar dapat menjalankan instruksi dan program dengan benar. Misalnya, OS yang dirancang untuk arsitektur RISC mungkin tidak akan berjalan dengan baik pada CPU CISC, dan sebaliknya.

- **Manajemen Sumber Daya**: OS bertanggung jawab untuk manajemen sumber daya seperti CPU, memori, dan I/O. Arsitektur CPU menentukan bagaimana sumber daya ini diakses dan digunakan oleh OS.

- **Pemrosesan Instruksi**: Arsitektur CPU menentukan cara instruksi diproses, yang harus didukung oleh OS. Misalnya, CPU dengan pipelining atau paralelisme membutuhkan OS yang dapat memanfaatkan fitur-fitur tersebut untuk penjadwalan tugas dan pemrosesan yang efektif.

- **Optimisasi Kinerja**: OS sering dioptimalkan untuk arsitektur CPU tertentu untuk meningkatkan kinerja. Pengembang OS mungkin akan menggunakan fitur khusus dari CPU, seperti set instruksi khusus atau teknologi virtualisasi, untuk meningkatkan efisiensi.

- **Keamanan**: Fitur keamanan yang disediakan oleh CPU, seperti eksekusi yang terpisah dari data atau enkripsi memori, harus didukung dan dikelola oleh OS untuk memberikan lingkungan yang aman.

  ## FORK

  **Sebelum menjalankan fork terlebih dahalu kita menginstall g++ .
```sh
$ su root
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install g++
``` 
![Screenshot 2024-04-28 154736](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/583a20c4-e71c-4b94-a227-deee1e269b0f)
**Lalu kembali menjadi User
```sh
$login [username]
``` 
![Screenshot 2024-04-28 155109](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/d6ae671e-bd2d-457a-ba46-1135f2fd5acd)

![Screenshot 2024-04-28 164132](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/047b9aff-f574-480a-9a81-6a3b5a252252)
![Screenshot 2024-04-28 170800](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/acb8b68d-5937-430b-b701-d90a40d58ad8)


![Screenshot 2024-04-28 192116](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/01f7a65f-138f-42bd-8974-76f8a2425ea0)
![Screenshot 2024-04-28 192140](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/971466ce-4429-40cd-8874-42cb33b04135)

![Screenshot 2024-04-28 200027](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/56b7cbda-48dd-49a4-ac87-93cfb4e60552)


