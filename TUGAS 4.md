# TUGAS PENDAHULUAN
## Jawablah pertanyaan-pertanyaan di bawah ini :

1. Apa yang dimaksud redirection?
2. Apa yang dimaksud pipeline?
3. Apa yang dimaksud perintah di bawah ini : echo, cat, more, sort, grep, wc, cut, uniq

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

3. Input nama direktori, output tidak ada (membuat direktori baru), bila terjadi error maka tampilan error pada layar (standard error)
 ```sh
$ mkdir mydir
$ mkdir mydir **(Terdapat pesan error)**
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/285c3619-f50b-4e7d-9df9-6e8389eb721b)

## Percobaan 2 : Pembelokan (redirection)
1. Pembelokan standar output

```sh
 $ cat 1> myfile.txt
 Ini adalah teks yang saya simpan ke file myfile.txt
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/0cccaa16-29ab-4df2-8e19-cd8d75b4ecb4)

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

4. Notasi 2>&1 : pembelokan standar error (2>) adalah identik dengan file descriptor 1.
 ```sh
 $ ls filebaru (Terdapat pesan error)
 $ ls filebaru 2> out.txt
 $ cat out.txt
 $ ls filebaru 2> out.txt 2>&
 $ cat out.txt
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/e0e1dd28-e876-441d-8796-f8190963151e)

5. Notasi 1>&2 (atau >&2) : pembelokan standar output adalah sama dengan file descriptor 2 yaitu standar error

 ```sh
$ echo “mencoba menulis file” 1> baru
$ cat filebaru 2> baru 1>&
$ cat baru
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/c6647be1-4b96-4dfc-807c-28ad6dd713fe)

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

8. Notasi – (input keyboard) adalah representan input dari keyboard. Artinya menampilkan file 1, kemudian menampilkan input dari keyboard dan menampilkan file 2. Perhatikan bahwa notasi “-“ berarti menyelipkan input dari keyboard

 ```sh
$ cat myfile.txt – surat
```
![image](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/90e5853e-2189-40bb-8c80-a5557f1ac8de)

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


## LATIHAN :

1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru.
2. Lihat daftar secara lengkap pada direktori /etc/passwd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
3. Urutkan file baru dengan cara membelokkan standard input.
4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.
5. Buatlah direktori latihan 2 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.
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

7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.
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
# LAPORAN RESMI
1. Analisa hasil percobaan 1 sampai dengan 4, untuk setiap perintah jelaskan tampilannya.
2. Kerjakan latihan diatas dan analisa hasilnya
3. Berikan kesimpulan dari praktikum ini.
