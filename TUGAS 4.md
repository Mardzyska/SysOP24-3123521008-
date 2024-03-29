# TUGAS PENDAHULUAN
## Jawablah pertanyaan-pertanyaan di bawah ini :

1. Apa yang dimaksud redirection?
* Pembelokan dilakukan untuk standard input, output dan error, yaitu untuk mengalihkan file descriptor dari 0, 1 
dan 2. Simbol untuk pembelokan adalah : 

0< atau < pengganti standard inp ut 
1> 
2> atau > pengganti standard output 
   
2. Apa yang dimaksud pipeline?
 * Mekanisme pipa digunakan sebagai alat komunikasi antar proses. 

Input => Proses1 => Output => Input => Proses2 => Output Proses 1 menghasilkan output yang selanjutnya 
digunakan sebagai input oleh Proses . Hubungan output input ini dinamakan pipa, yang menghubngkan 
Proses 1 dengan Proses2 dan dinyatakan dengan symbol “|”. 

 
Proses1 | Proses2 

3 . Apa yang dimaksud perintah di bawah ini : echo, cat, more, sort, grep, wc, cut, uniq

echo, cat, more, sort, grep, wc, cut, uniq  
• Perintah grep 

Digunakan untuk menyaring masukannya da n menampilkan baris-baris yang hanya mengandung pola yang 
ditentukan. Pola ini disebut regular expression.

• Perintah wc 

Digunakan untuk menghitung jumlah baris, kata dan karakter dari baris-baris masukan yang diberikan 
kepadanya. Untuk mengetahui berapa baris gunakan option – l, untuk mengetahui berapa kata, gunakan 
option –w dan untuk mengetahui berapa karakter, gunakan option –c. Jika salah satu option tidak digunakan, 
maka tampilannya adalah jumlah baris, jumlah kata dan jumlah karakter. 

• Perintah sort 

Digunakan untuk mengurutkan masukannya berdasarkan urutan nomor ASCII dari karakter. 

• Perintah cut 

Digunakan untuk mengambil kolom tertentu dari baris-baris masukannya, yang ditentukan pada option –c. 

• Perintah uniq 

Digunakan untuk menghilangkan baris-baris berurutan yang mengalami duplikasi, biasanya digabungkan 
dalam pipeline dengan sort. 

# PERCOBAAN
1. Login sebagai user.
2. Bukalah Console Terminal dan lakukan percobaan-percobaan di bawah ini. Perhatikan hasil setiap percobaan.
3. Selesaikan soal-soal latihan.

## Percobaan 1 : File descriptor

1. Output ke layar (standar output), input dari system (kernel)

```sh
$ ps
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/fb8df44c-f0e9-4067-ab4b-a93b125abf90)

* $ ps yaitu perintah yang digunakan untuk memperlihatkan proses yang sedang berjalan pada
sistem (kernel) kemudian diperlihatkan pada layar (proses status). Input berasal dari system
(kernel), sedangkan output ditampilkan ke layar (standar output)

2. Output ke layar (standar output), input dari keyboard (standard input)
   
 ```sh
 $ cat
 hallo, apa khabar
 hallo, apa khabar
 exit dengan ^d
 exit dengan ^d
 [Ctrl-d]
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/e4d306d9-f2ba-4073-a6f1-63196fe30195)

* . $ cat yaitu perintah mengambil input dari keyboard dan kemudian output ditampilkan ke
layar.

3. Input nama direktori, output tidak ada (membuat direktori baru), bila terjadi error maka tampilan error pada layar (standard error)
 ```sh
$ mkdir mydir
$ mkdir mydir **(Terdapat pesan error)**
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/285c3619-f50b-4e7d-9df9-6e8389eb721b)
* . $ mkdir merupakan perintah yang digunakan untuk membuat direktori baru. Input dari mkdir
adalah nama direktori, sedangkan outputnya tidak ada (membuat direktori baru), bila terjadi
error maka outputnya adalah tampilan error pada layar (standard error)

## Percobaan 2 : Pembelokan (redirection)
1. Pembelokan standar output

```sh
 $ cat 1> myfile.txt
 Ini adalah teks yang saya simpan ke file myfile.txt
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/0cccaa16-29ab-4df2-8e19-cd8d75b4ecb4)

*  1> merupakan salah satu metode pembelokan pengganti standar output. Alternatifnya yaitu
dengan menggunakan >

2. Pembelokan standar input, yaitu input dibelokkan dari keyboard menjadi dari file
 ```sh
 $ cat 0< myfile.txt
 $ cat myfile.txt
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/ec32005f-dd2b-4c7e-80fe-ba8c8197a172)

3. Pembelokan standar error untuk disimpan di file
 ```sh
 $ mkdir mydir (Terdapat pesan error)
 $ mkdir mydir 2> myerror.txt
 $ cat myerror.txt
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/3ce5491c-126b-4313-8e42-a7b63f2895a3)

*  0< merupakan salah satu metode pembelokan standar input, yaitu input dibelokkan dari
keyboard menjadi dari file. Alternatifnya yaitu dengan menggunakan <

4. Notasi 2>&1 : pembelokan standar error (2>) adalah identik dengan file descriptor 1.
 ```sh
 $ ls filebaru (Terdapat pesan error)
 $ ls filebaru 2> out.txt
 $ cat out.txt
 $ ls filebaru 2> out.txt 2>&
 $ cat out.txt
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/e0e1dd28-e876-441d-8796-f8190963151e)
*  Dalam percobaan ini, output standar error (stderr) dari perintah `mkdir mydir` dialihkan ke file 
`myerror.txt` dengan menggunakan `2> myerror.txt`. 
  
5. Notasi 1>&2 (atau >&2) : pembelokan standar output adalah sama dengan file descriptor 2 yaitu standar error

 ```sh
$ echo “mencoba menulis file” 1> baru
$ cat filebaru 2> baru 1>&
$ cat baru
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/c6647be1-4b96-4dfc-807c-28ad6dd713fe)
* Notasi `>>` digunakan untuk menambahkan konten ke akhir file tanpa menghapus konten 
sebelumnya. Dalam contoh yang diberikan, perintah `echo "kata pertama" > surat` menulis kata 
pertama ke dalam file `surat`. Kemudian, perintah-perintah `echo` berikutnya menggunakan `>>` untuk menambahkan kata-kata kedua dan ketiga ke file yang sama. Namun, ada kesalahan ketika perintah 
`echo "kata keempat" > surat` digunakan. Karena menggunakan `>`, ini akan menghapus konten file 
`surat` dan menulis ulang dengan hanya kata keempat. 
6. Notasi >> (append)
 ```sh
$ echo “kata pertama” > surat
$ echo “kata kedua” >> surat
$ echo “kata ketiga” >> surat
$ cat surat
$ echo “kata keempat” > surat
$ cat surat
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/f0ee67b2-0bce-4e22-8534-2cd98866c4dd)
* Notasi >> (append) digunakan untuk membelokkan tampilan standard output ke file tanpa
menghapus isi dari file sebelumnya.

7. Notasi here document (<<++ .... ++) digunakan sebagai pembatas input dari keyboard. Perhatikan bahwa tanda pembatas dapat digantikan dengan tanda apa saja, namun harus sama dan tanda penutup harus diberikan pada awal baris

 ```sh
$ cat <<++
Hallo, apa kabar?
Baik-baik saja?
Ok!
++
$ cat <<%%%
Hallo, apa kabar?
Baik-baik saja?
Ok!
%%%
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/a26a763f-8f7a-42fc-932e-ee72f7201449)
*Notasi here document (`<<++`) digunakan untuk memberikan input teks yang lebih panjang secara 
interaktif. Dalam contoh yang diberikan, teks yang dimasukkan di antara `++` dianggap sebagai input 
sampai menemukan tanda `++` lagi. Ini adalah cara yang berguna untuk memberikan input yang lebih 
panjang atau lebih kompleks kepada perintah shell tanpa harus menuliskannya langsung di command 
line.

8. Notasi – (input keyboard) adalah representan input dari keyboard. Artinya menampilkan file 1, kemudian menampilkan input dari keyboard dan menampilkan file 2. Perhatikan bahwa notasi “-“ berarti menyelipkan input dari keyboard

 ```sh
$ cat myfile.txt – surat
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/90e5853e-2189-40bb-8c80-a5557f1ac8de)
* Notasi `-` dalam perintah `cat` seperti `cat myfile.txt - surat` memungkinkan penggunaan input dari 
keyboard di antara file-file yang ditampilkan oleh `cat`. Dalam contoh ini, `cat` akan menampilkan isi 
`myfile.txt`, kemudian meminta input dari keyboard, dan setelahnya menampilkan isi file `surat`. Ini 
adalah cara yang berguna untuk menggabungkan output dari file dengan input yang dimasukkan 
melalui keyboard dalam satu tampilan.

## Percobaan 3 : Pipa (pipeline)

1. Operator pipa (|) digunakan untuk membuat eksekusi proses dengan melewati data langsung ke data lainnya.

 ```sh
$ who
$ who | sort
$ who | sort –r
$ who > tmp
$ sort tmp
$ rm tmp
$ ls –l /etc | more
$ ls –l /etc | sort | moret – surat
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/3e6cb044-a830-42cf-a7d8-dc1aaea76753)
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/cf826ad6-d5ba-4c14-b7b8-096cdb0e42c2)

* Perintah `who`: Perintah ini digunakan untuk menampilkan informasi tentang pengguna yang saat 
ini login ke sistem. Outputnya berisi daftar pengguna yang sedang aktif. 
* Pipa (`|`) ke `sort`: Dengan menggunakan pipa (`|`), output dari perintah `who` dialirkan langsung 
sebagai input ke perintah `sort`. Dengan demikian, daftar pengguna yang aktif akan diurutkan secara 
alfabetis oleh perintah `sort`, dan hasilnya akan ditampilkan di layar. 
* Pipa (`|`) ke `sort -r`: Sama seperti sebelumnya, namun dengan opsi `-r` yang diberikan kepada 
perintah `sort`, hasilnya akan diurutkan secara terbalik (dari Z ke A). Ini mengakibatkan daftar 
pengguna yang aktif diurutkan secara alfabetis secara terbalik, dan hasilnya akan ditampilkan di layar. 
* Redirect output (`>`) ke file `tmp`: Dalam langkah ini, output dari perintah `who` dialihkan 
(redirected) ke dalam file `tmp`. Sehingga, daftar pengguna yang aktif disimpan dalam file `tmp`. 
* Perintah `sort` pada file `tmp`: Setelah daftar pengguna disimpan dalam file `tmp`, perintah `sort` 
digunakan untuk mengurutkan daftar pengguna tersebut. Hal ini dilakukan dengan membaca isi file 
`tmp` dan mengurutkannya, kemudian hasilnya ditampilkan di layar. 
 * Perintah `rm` untuk menghapus file `tmp`: Setelah selesai digunakan, file `tmp` dihapus dari sistem 
menggunakan perintah `rm`. Hal ini dilakukan untuk membersihkan sisa-sisa file sementara yang tidak 
dibutuhkan lagi.

Dengan menggunakan kombinasi perintah, pipa, dan redirect output, pengguna dapat melakukan 
berbagai manipulasi data dengan cara yang efisien dan fleksibel dalam lingkungan shell. Dalam contoh 
ini, perintah-perintah tersebut digunakan untuk mengelola dan memanipulasi informasi tentang 
pengguna yang aktif di sistem.

2. Untuk membelokkan standart output ke file, digunakan operator ">"

```sh
$ echo hello
$ echo hello > output
$ cat output
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/14b5d4d4-c215-46c1-9169-ad156fee9d2f)

3.  Untuk menambahkan output ke file digunakan operator ">>"
  ```sh
$ echo bye >> output
$ cat output
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/6b4c8e54-681f-463a-a497-d26e78cc49cf)

4. Untuk membelokkan standart input digunakan operator "<"
  ```sh
$ cat < output
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/287278ef-76f1-4099-ba00-d726fd5b1681)

5. Pembelokan standart input dan standart output dapat dikombinasikan tetapi tidak boleh menggunakan nama file yang sama sebagai standart input dan output.
  ```sh
$ cat < output > out
$ cat out
$ cat < output >> out
$ cat out
$ cat < output > output
$ cat output
$ cat < out >> out (Proses tidak berhenti)
[Ctrl-c]
$ cat out
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/a2236521-4b63-48bc-95f5-8b774e034d62)


## Percobaan 4 : Filter

1. Pipa juga digunakan untuk mengkombinasikan utilitas sistem untuk membentuk fungsi yang lebih kompleks
  ```sh
 $ w –h | grep <user>
 $ grep <user> /etc/passwd
 $ ls /etc | wc
 $ ls /etc | wc –l
 $ cat > kelas1.txt
 Badu
 Zulkifli
 Yulizir
 Yudi
 Ade
 [Ctrl-d]
 $ cat > kelas2.txt
 Budi
 Gama
 Asep
 Muchlis
 [Ctrl-d]
 $ cat kelas1.txt kelas2.txt | sort
 $ cat kelas1.txt kelas2.txt > kelas.txt
 $ cat kelas.txt | sort | uniq
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/323fa990-b550-42f6-8741-c7a56c6486b7)
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/fa816c84-f1e6-46fe-b157-060b4cee44d1)
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/68a01524-4f34-4fd1-aff4-9acde927a032)
* Pipa juga digunakan untuk mengkombinasikan utilitas sistem untuk membentuk fungsi yang
lebih kompleks

## LATIHAN :

1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru.
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/f3b4fab4-7911-4bdf-bc82-ad6a5c1ea155)
* Untuk melihat daftar direktori aktif, gunakan perintah $ ls, sedangkan untuk
membelokkan tampilan standard output ke file baru, gunakan ‘>’

2. Lihat daftar secara lengkap pada direktori /etc/passwd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
 ![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/d32838bc-e235-4faf-9c91-050e84935720)
 *  Untuk melihat daftar lengkap dari direktori /etc/passwd, gunakan perntah $ ls, sedangkan
untuk membelokkan tampilan standard output ke file baru tanpa menghapus file baru
sebelumnya, gunakan ‘>>’

3. Urutkan file baru dengan cara membelokkan standard input.
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/bd7ed2d6-58af-4e13-bf79-1fd58cd38699)
* Untuk mengurutkan file, gunakan perintah $ sort, sedangkan untuk membelokkan
standard input, gunakan ‘<

4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/2ce9dd3a-cd1e-4d62-a0c8-ebe265ecde6f)
* Untuk mengurutkan file, gunakan perintah $ sort, sedangkan untuk membelokkan
standard input, gunakan ‘<’, sedangkan untuk membelokkan standard output ke file,
gunakan ‘>’. Pembelokan standart input dan standart output dapat dikombinasikan
asalkan tidak boleh menggunakan nama file yang sama sebagai standart input dan output

5. Buatlah direktori latihan 2 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/955a85c1-b4c7-4db7-9a7f-3d6def81bf83)
* Gunakan perintah $ mkdir untuk membuat direktori baru. Saat membuat direktori yang
sama sebanyak dua kali, akan muncul pesan error. Pesan error itu kemudian dibelokkan
ke file dengan menggunakan ‘2>

6. Urutkan kalimat berikut :
  ```sh
Jakarta
Bandung
Surabaya
Padang
Palembang
Lampung
```
Dengan menggunakan notasi here document (<@@@ ...@@@) . HINT
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/787e2932-bcd3-4373-9645-a60849cfcf40)
*  Pertama, buat notasi here document yang akan dibelokkan ke sebuah file kemudian isi
document tersebut. Setelah diisi dan diakhiri, isi dokumen akan tersimpan ke file yang
dibelokkan. File tersebut kemudian diurutkan menggunakan perintah $ sort.

7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/15cf5d65-f1c4-4b47-89b8-4b688da3c42d)
*  Untuk mendapatkan jumlah baris, kata, dan karakter (secara berurutan) dari sebuah file,
gunakan perintah wc yang dipipakan dengan perintah cat. Hasilnya kemudian bisa
ditambahkan ke file menggunakan ‘>>’

8. Gunakan perintah di bawah ini dan perhatikan hasilnya.
  ```sh
 $ cat > hello.txt
 dog cat
 cat duck
 dog chicken
 chicken duck
 chicken cat
 dog duck
 [Ctrl-d]
 $ cat hello.txt | sort | uniq
 $ cat hello.txt | grep “dog” | grep –v “cat”
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/414d9104-7bb9-45cb-8477-b904fb16e6d2)
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/a2f21199-1fe7-4121-b979-06d1c85a9f36)
* Uniq digunakan untuk menghilangkan baris-baris berurutan yang mengalami duplikasi,
Grep digunakan untuk menyaring masukannya dan menampilkan baris-baris yang hanya
mengandung pola yang ditentukan. Pola ini disebut regular expression. Salah satu regular
expression dari grep adalah -v (invert0match), yang akan menampilkan baris yang
TIDAK mengandung pola yang ditentukan.

## KESIMPULAN
Dengan menggunakan perintah-perintah ini, dapat melakukan berbagai tugas, seperti melihat daftar file, membuat direktori, mengurutkan dan memanipulasi teks, serta mengelola output dan error dengan cara yang diinginkan. Semua langkah-langkah tersebut merupakan bagian dari proses pengelolaan file.

# LAPORAN RESMI
1. Analisa hasil percobaan 1 sampai dengan 4, untuk setiap perintah jelaskan tampilannya.
2. Kerjakan latihan diatas dan analisa hasilnya
3. Berikan kesimpulan dari praktikum ini.
