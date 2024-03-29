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

# Nomor 4

## Melakukan clone https://github.com/ferryastika/flops-iops
  
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/d72d0504-8015-448f-94a4-d362d280b6e7)

## Build Binaries

```sh
$ make
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/76a1112a-8f4f-4c61-944e-0028d73597c3)

## Cleaning Old Build

```sh
$ make clean
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/7cfe9a53-109a-4070-9c3f-39c0b56c9797)

## Install Binaries 

```sh
$  make install
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/4dc689bc-68d0-4b00-83eb-63555254aefe)

## Uninstall Binaries 

```sh
$  make uninstall
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/2b447109-3596-4b6b-9a83-f970c3e0d79a)

## Usage

* **Percobaan 1**

```sh
  $ iops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/a9f61625-509a-4d65-8a62-753ce77e51ff)

```sh
  $ flops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/1b8a7888-9c5e-46b2-9562-76f903973d1a)

* **Percobaan 2**

```sh
  $ iops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/b745f3b6-89dc-4d7a-8f22-10ed1bc3dbad)


```sh
  $ flops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/6096124a-86d4-415c-8507-3767ec729b98)

* **Percobaan 3**
  
```sh
  $ iops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/66110b43-9755-4587-a24a-fb38c95e5c38)

```sh
  $ flops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/f00bdb95-fdaf-45d8-8102-25a25a3c96f1)

* **Percobaan 4**
  
```sh
  $ iops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/dd0371b5-0269-49fd-9bc7-9d2f4757816a)

```sh
  $ flops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/acff3547-8856-44ca-8c26-4950e18f3d3c)

* **Percobaan 5**
  
```sh
  $ iops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/8a5a9fea-36c3-4528-8ef9-5c167fe59b9f)

```sh
  $ flops64 $(nproc)
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/774c7996-47b0-4d8e-a670-7755149080c3)

# Analisa

Penjelasan tentang fungsionalitas dari perintah Debian :

* **make** : Perintah ini digunakan untuk mengkompilasi program dari sumber kode. Biasanya, Anda akan mengeksekusi **make** setelah melakukan perubahan pada kode sumber.
* **make clean** : Perintah ini menghapus file-file sementara dan output dari proses kompilasi. Namun, perintah ini hanya memengaruhi direktori sumber/kompilasi dan tidak menghapus perangkat lunak yang telah diinstal sebelumnya.
* **sudo make install** : Perintah ini menginstal perangkat lunak yang telah dikompilasi ke dalam sistem. Biasanya, perintah ini memerlukan hak akses administrator (dengan menggunakan sudo).
* **sudo make uninstall** : Jika tersedia, perintah ini akan menghapus perangkat lunak yang telah diinstal sebelumnya menggunakan sudo make install. Namun, tidak semua perangkat lunak menyediakan perintah ini. Jika tidak tersedia, Anda harus menghapusnya secara manual.
* **iosp64 $(nproc)** dan **flops64 $(nproc)** : Perintah ini mungkin spesifik untuk sistem atau perangkat lunak tertentu. Tanpa informasi lebih lanjut, saya tidak dapat memberikan penjelasan yang lebih rinci. Pastikan )
Anda merujuk pada dokumentasi atau panduan yang relevan untuk memahami perintah ini dengan lebih baik.

## PERBANDINGAN EKSEKUSI
https://docs.google.com/spreadsheets/d/1CVZH3rk8T0rY-0BirmPdzeeieXzrKRjIVq6fb6Yu5GQ/edit#gid=0

![WhatsApp Image 2024-03-18 at 09 04 09_09100271](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/f179b8b9-c8ef-40ee-8da1-a471fa096954)


**Analisa**

Dari plot perbandingan di atas, dapat dilihat bahwa Alyssa memiliki nilai rata-rata IOPS dan FLOPS yang lebih tinggi dibandingkan dengan Dyzka, Pelangi, dan Feby. Hal ini menunjukkan bahwa PC Alyssa cenderung memiliki performa yang lebih baik dalam menangani operasi input/output (IOPS) dan operasi floating point (FLOPS).

**Kesimpulan**

Kesimpulan yang bisa diambil adalah performa komputer dalam hal IOPS dan FLOPS sangat penting tergantung pada kebutuhan aplikasi atau tugas yang dijalankan. Semakin tinggi nilai IOPS dan FLOPS, semakin baik kemampuan komputer tersebut dalam menangani tugas-tugas yang memerlukan operasi input/output dan operasi floating point secara cepat dan efisien.

  # Nomor 4
```sh
  $ su -l
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/d76fa900-a4e4-497d-b841-30d4506e5bb5)

```sh
 $ apt install make
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/49368052-55e2-4672-a8be-c9b8704c579d)

```sh
 $ apt install git
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/c2f24f4f-25c9-4103-ab4f-999f4cdd819e)

```sh
$ apt install gcc
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/a62a023f-23bd-4bed-bf98-1f28fe1f1b31)

```sh
$ git clone https://github.com/ferryastika/flops-iops
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/d72d0504-8015-448f-94a4-d362d280b6e7)
```sh
$ cd flops-iops
```
![Uploading image.png…]()

