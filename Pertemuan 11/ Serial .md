## SERIAL  (Sequential)

![WhatsApp Image 2024-05-14 at 09 01 08_59e26df8](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/6bb6e034-3646-4de1-9d8e-11e8c7325cd0)
 * Serial mengacu pada eksekusi tugas atau instruksi secara berurutan, satu demi satu.
Dalam komputasi, ini berarti bahwa tugas dieksekusi satu per satu, tanpa ada pemrosesan paralel.

**Contoh** 

Ketika kita menjalankan program yang memiliki langkah-langkah berurutan, seperti membaca data, menghitung, dan menampilkan hasil.

## Konkurensi (Concurrency), Paralel (Parallelism) & Konkurensi Paralel (Parallel Concurrency)

![WhatsApp Image 2024-05-14 at 09 03 30_23a217d5](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/7fdda55c-d29c-445f-8ea2-c94ba2cafb2d)
* **Konkurensi** berkaitan dengan cara menghadapi banyak pekerjaan sekaligus.
Dalam komputasi, konkurensi memungkinkan banyak tugas berjalan bersamaan, meskipun tidak selalu secara paralel.

**Contoh**

Browsing web sambil mendengarkan musik di Spotify, di mana CPU membagi waktu untuk mengeksekusi tugas-tugas yang berbeda secara bersamaan.

* **Paralel** adalah eksekusi banyak tugas secara bersamaan.
Dalam komputasi, ini terjadi ketika beberapa tugas dieksekusi secara simultan, seperti pada prosesor multi-core.

**Contoh** 

 Menghitung operasi matematika pada beberapa thread secara bersamaan.

* **Konkurensi Paralel**Ini adalah kombinasi dari konkurensi dan paralelisme.
Dalam komputasi, tugas-tugas dikerjakan secara bersamaan (paralel) dalam lingkup konkurensi, baik antar aplikasi maupun dalam satu aplikasi.

**Contoh**

Memutar musik di Spotify sambil melakukan pencarian playlist lain atau mencari lagu baru.

## Masalah Penulis-Pembaca (Reader-Writer Problem)
adalah salah satu masalah yang sering muncul dalam sistem operasi dan pemrograman paralel. Mari kita bahas keduanya:

1. **Masalah Penulis-Pembaca (Reader-Writer Problem):**
    - Dalam situasi ini, kita memiliki sebuah berkas yang dibagi di antara banyak orang. Jika salah satu orang mencoba mengedit berkas tersebut, tidak ada orang lain yang boleh membaca atau menulis pada saat yang bersamaan, karena perubahan tidak akan terlihat oleh orang lain.
    - Namun, jika ada orang yang sedang membaca berkas tersebut, orang lain masih dapat membacanya secara bersamaan.
    - Dalam sistem operasi, situasi ini disebut sebagai masalah penulis-pembaca.
    - Parameter masalah:
        - Ada satu set data yang dibagi di antara beberapa proses.
        - Hanya satu penulis yang dapat menulis pada satu waktu.
        - Jika ada proses yang sedang menulis, tidak ada proses lain yang dapat membacanya.
        - Jika ada setidaknya satu pembaca yang sedang membaca, tidak ada proses lain yang dapat menulis.
        - Pembaca tidak dapat menulis, hanya membaca.
    - Solusi ketika pembaca memiliki prioritas lebih tinggi daripada penulis:
        - Terdapat empat jenis kasus yang dapat terjadi:
            1. Penulis menulis, penulis menulis (Tidak diperbolehkan)
            2. Penulis menulis, pembaca membaca (Tidak diperbolehkan)
            3. Pembaca membaca, penulis menulis (Tidak diperbolehkan)
            4. Pembaca membaca, pembaca membaca (Diperbolehkan)
        - Tiga variabel digunakan: `mutex`, `wrt`, dan `readcnt` untuk mengimplementasikan solusi:
            - `mutex`: Memastikan eksklusi gegabah ketika `readcnt` diperbarui (ketika pembaca masuk atau keluar dari bagian kritis).
            - `wrt`: Digunakan oleh pembaca dan penulis.
            - `readcnt`: Menyimpan jumlah proses yang sedang membaca di bagian kritis (awalnya 0).
        - Proses penulis:
            - Penulis meminta akses ke bagian kritis.
            - Jika diperbolehkan (yaitu `wait(wrt)` memberikan nilai benar), penulis masuk dan menulis.
            - Jika tidak diperbolehkan, penulis menunggu.
            - Proses pembaca:
            - Pembaca meminta akses ke bagian kritis.
            - Jika diperbolehkan:
            - Jumlah pembaca dalam bagian kritis bertambah.
            - Jika pembaca pertama yang masuk, kunci `wrt` untuk mencegah penulis masuk.
            - Setelah membaca, pembaca keluar dari bagian kritis.
            - Jika tidak ada pembaca lagi, sinyalkan `wrt` agar penulis dapat masuk.
            - Jika tidak diperbolehkan, pembaca menunggu.
            - Referensi lebih lanjut: .

2. **Masalah Dining Philosophers (Masalah Filosof Pemakan):**
    - Masalah ini melibatkan lima filosof yang duduk di sekitar meja bundar dan memikirkan kehidupan mereka.
    - Di antara setiap dua filosof ada garpu.
    - Filosof hanya dapat makan jika memegang dua garpu sekaligus (kiri dan kanan).
    - Tantangan adalah menghindari deadlock ketika semua filosof mencoba mengambil garpu secara bersamaan.
    - Solusi melibatkan penggunaan semafor dan koordinasi yang cermat.
    - Referensi lebih lanjut: ².



