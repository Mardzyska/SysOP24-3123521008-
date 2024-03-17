# Nomor 1
## Siklus CPU
Berikut adalah presentasi langkah demi langkah tentang siklus CPU (fetch, decode, execute) untuk mengeksekusi sebuah program, serta penjelasan mengenai peran bahasa pemrograman, compiler, dan sistem operasi:

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

Fungsi sistem operasi:
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
