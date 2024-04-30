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

  * Sebelum menjalankan fork terlebih dahalu kita menginstall g++ .
```sh
$ su root
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install g++
``` 
![Screenshot 2024-04-28 154736](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/583a20c4-e71c-4b94-a227-deee1e269b0f)
* Lalu kembali menjadi User
```sh
$ login [username]
``` 
![Screenshot 2024-04-28 155109](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/d6ae671e-bd2d-457a-ba46-1135f2fd5acd)
**Fork 1**
* Masukan ke compiler
```sh
$ nano fork01.cpp
```
* Lalu MengInputkan Source code
```sh
using namespace std;

#include <iostream>
#include <sys/types.h>
#include <unistd.h>


/* getpid() adalah system call yg dideklarasikan pada unistd.h.
Menghasilkan suatu nilai dengan type pid_t.
pid_t adalah type khusus untuk process id yg ekuivalen dg int
*/
int main(void) {
	pid_t mypid;
	uid_t myuid;
	for (int i = 0; i < 3; i++) {
		mypid = getpid();
		cout << "I am process " << mypid << endl;
		cout << "My parent process ID is " << getppid() << endl;
		cout << "The owner of this process has uid " << getuid()
	<< endl;
/* sleep adalah system call atau fungsi library
yang menghentikan proses ini dalam detik
*/
	sleep(3);
	}
return 0;
}
```
* Lalu file 'ccp' menjadi 'exe' 
```sh
$ g++ fork01.cpp -o fork01.exe
```
* Menjalankan Source codenya
```sh
$ ./fork01.exe
``` 
![Screenshot 2024-04-28 164132](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/047b9aff-f574-480a-9a81-6a3b5a252252)
**Fork 2**

* Masukan ke compiler
```sh
$ nano fork02.cpp
```
* Lalu MengInputkan Source code
```sh
#include <iostream>
#include <sys/types.h>
#include <unistd.h>
using namespace std;


/* getpid() dan fork() adalah system call yg dideklarasikan
pada unistd.h.
Menghasilkan suatu nilai dengan type pid_t.
pid_t adalah type khusus untuk process id yg ekuivalen dg int
*/
int main(void) {
	pid_t childpid;
	int x = 5;
	childpid = fork();

	while (1) {
		cout << "This is process ID" << getpid() << endl;
		cout << "In this process the value of x becomes " << x << endl;	
		sleep(2);
		x++;
	}
	return 0;
}
```
* Lalu file 'ccp' menjadi 'exe'
```sh
$ g++ fork02.cpp -o fork02.exe
```
* Menjalankan Source codenya
```sh
$ ./fork02.exe
``` 
![Screenshot 2024-04-28 170800](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/acb8b68d-5937-430b-b701-d90a40d58ad8)

**Orphan**
* Masukan Ke compiler
```sh
$ nano orphan.c
```
* Lalu MengInputkan Source code
```sh
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>

int main()
{
	// fork() Create a child process

	int pid = fork();
	if (pid > 0)
	{
		//getpid() returns process id
		// while getppid() will return parent process id
		printf("Parent process\n");
		printf("ID : %d\n\n",getpid());
	}
	else if (pid == 0)
	{
		printf("Child process\n");
		// getpid() will return process id of child process
		printf("ID: %d\n",getpid());
		// getppid() will return parent process id of child process
		printf("Parent -ID: %d\n\n",getppid());

		sleep(10);

		// At this time parent process has finished.
		// So if u will check parent process id 
		// it will show different process id
		printf("\nChild process \n");
		printf("ID: %d\n",getpid());
		printf("Parent -ID: %d\n",getppid());
	}
	else
	{
		printf("Failed to create child process");
	}
	
	return 0;
}

/* https://www.includehelp.com/c-programs/orphan-process.aspx */
```
* Lalu file 'c' menjadi 'exe'
```sh
$ g++ orphon.c -o orphan.exe
```
* Menjalankan Source codenya
```sh
$ ./orphan.exe
``` 

![Screenshot 2024-04-28 192116](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/01f7a65f-138f-42bd-8974-76f8a2425ea0)

**Zombie**
* Masukan Ke compiler
```sh
$ nano zombie.c
```
* Lalu MengInputkan Source code
```sh
#include <stdlib.h>
#include <sys/types.h>
#include <unistd.h>
int main ()
{
  pid_t child_pid;

   /* Create child*/
  child_pid = fork ();
  if (child_pid > 0) {

    /* Parent process */
    sleep (60);
  }
  else {

    /*Child process. Exit immediately. */
    exit (0);
  }
  return 0;
}

/*ps -e -o pid,ppid,stat,cmd */
```
* Lalu file 'c' menjadi 'exe'
```sh
$ g++ zombie.c -o zombie.exe
```
* Menjalankan Source codenya
```sh
$ ./zombie.exe
``` 
![Screenshot 2024-04-28 200027](https://github.com/Mardzyska/SysOP24-3123521008-/assets/139208195/56b7cbda-48dd-49a4-ac87-93cfb4e60552)
## Producer-Consumer problem


Produsen mencoba memasukkan data ke slot kosong buffer. Seorang konsumen mencoba untuk menghapus data dari slot diisi dalam buffer. Seperti yang mungkin sudah Anda duga sekarang, kedua proses tersebut tidak akan menghasilkan output yang diharapkan jika dijalankan secara bersamaan.

Perlu ada cara untuk membuat produsen dan konsumen bekerja secara independen.


