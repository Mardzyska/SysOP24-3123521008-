
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

