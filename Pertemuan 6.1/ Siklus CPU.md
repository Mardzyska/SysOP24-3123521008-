# Nomor 1
## Siklus CPU
Berikut adalah presentasi langkah demi langkah tentang siklus CPU (fetch, decode, execute) untuk mengeksekusi sebuah program, serta penjelasan mengenai peran bahasa pemrograman, compiler, dan sistem operasi:
![2](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/fd22ede4-dfe2-4e6d-8792-7b84b09fb44e)

Dari bahasa assembly bisa saja diartikan secara sederhana menjadi,
LOAD (ambil) instruksi dari memori 10 ke akumulator, lalu ADD (tambahkan)
dari memori 11 dengan apa yang ada di akumulator, dan STORE (simpan)
dari penjumlahan tadi yang ada diakumulator ke memori 12 
![1](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/d7347623-8330-4a93-803e-1f1ce54ab98b)
*  CPU itu terdapat Control Unit, Accumulator, dan ALU atau Arithmetic Logic Unit.
Selain 3 itu terdapat register lain seperti Program Counter (PC), Current Intruction Register
(CIR), Memory Address Register (MAR), dan Memory Data Register (MDR).

![3](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/8b989208-5ff0-4fc1-a8ac-b5013a28a740)
* Pertama Program Counter akan menyimpan insturksi selanjutnya yang akan
dieksekusi

![4](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/b4b11684-d029-42f6-aa9e-22edbe18df47)
* Selanjutnya alamat memori tadi harus disimpan didalam Memory Address Register,
setelah itu isi dari alamat memori tersebut akan dimuat di Memory Data Register,
Selanjutnya instruksi tadi harus disimpan di Current Instruction Register. 

![5](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/990a4e0b-01a7-4c49-ac97-d0bbe522dcfe)



![6](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/79fd69ec-b9c1-4dfb-94bf-e9ed48762f70)


![7](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/2b8626aa-1600-4164-8e44-83e1a460f149)



![8](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/24095a32-256a-462c-91e3-1e3a357574be)

* Setelah diambil ke dalam Current Instruction Register, Program Counter nya akan
bertambah 1.

![9](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/a208fec7-38a1-4d2d-85ba-2c30167c7e97)


![10](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/db40cf87-a013-46df-b259-cf02ec980128)


![11](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/ebe03bff-e127-4f2d-a6d8-643568d7e3b2)


![12](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/e782a168-0e1d-4c03-83f2-6312cf2f20ea)


![13](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/472e5759-4925-44c3-b339-f45491d94d3c)


![14](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/60d5f325-68f4-466f-b783-ef314b7c73ed)


![15](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/095e0a9b-76d9-4efa-9dff-ce8dfd5ab0a9)



![16](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/048e25dd-bcef-4a68-9996-e14bce5fb1bc)


![17](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/5116e61e-f85b-40d4-b596-65ededcf8c06)



![18](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/fe88972b-c725-40de-92cc-42f6af5e3bbc)


![19](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/eb8b023d-ba9e-4f1d-b550-e827d9b0bf2d)







1. Siklus CPU (Fetch, Decode, Execute)
   
**Fetch (Ambil)**
* CPU mengambil instruksi dari memori utama (RAM).
* Alamat memori instruksi disimpan dalam register program counter (PC).
* Instruksi diambil dari memori dan disalin ke dalam register instruksi di dalam CPU.

**Decode (Terjemahkan)**
* CPU menerjemahkan instruksi yang baru diambil ke dalam bentuk yang dapat dimengerti oleh unit eksekusi.
* Instruksi dipecah menjadi operasi yang lebih sederhana.

**Execute (Eksekusi)**
* CPU menjalankan operasi yang telah diterjemahkan.
* Operasi ini melibatkan manipulasi data, perhitungan, dan akses ke perangkat keras.

2. Peran Bahasa Pemrograman dan Compiler
   
**Bahasa Pemrograman**

* Bahasa pemrograman adalah alat yang digunakan oleh programmer untuk menulis kode sumber program.
Bahasa pemrograman memungkinkan programmer berkomunikasi dengan komputer melalui instruksi yang lebih mudah dipahami manusia.
Contoh bahasa pemrograman: Java, C++, Python, dan JavaScript.

**Compiler**

* Compiler adalah perangkat lunak yang mengubah kode sumber program dalam bahasa pemrograman menjadi kode objek atau bahasa mesin yang dapat dijalankan oleh komputer.
Compiler menerjemahkan kode program menjadi bentuk yang lebih efisien untuk dieksekusi.
Contoh compiler: GCC (untuk C/C++), javac (untuk Java), dan Kotlin compiler.

3. Peran Sistem Operasi (Operating System)

Sistem operasi mengelola sumber daya perangkat keras dan menyediakan layanan ke pengguna.

**Fungsi sistem operasi:**
* Mengelola memori, proses, dan perangkat keras.
* Menyediakan antarmuka untuk pengguna dan aplikasi.
* Mengoptimalkan kinerja komputer.
* Menyediakan layanan seperti file system, jaringan, dan keamanan.
