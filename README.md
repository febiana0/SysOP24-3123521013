# Perbedaan RISC dan CISC 

RISC singkatan dari Reduced Instruction Set Computer.Merupakan bagian dari arsitektur
mikroprosessor, berbentuk kecil dan berfungsi untuk negeset istruksi dalam komunikasi
diantara arsitektur yang lainnya

- Karakteristik:
  - Siklus machine ditentukan oleh waktu yang digunakan untuk mengambil dua buah
    operand dari register, melakukan operasi ALU, dan menyimpan hasil operasinya kedalam
    register, dengan demikian instruksi mesin RISC tidak boleh lebih kompleks dan harus dapat
    mengeksekusi secepat mikroinstruksi pada mesin-mesin CISC.
  - Operasi berbentuk dari register-ke register yang hanya terdiri dari operasi load dan
    store yang mengakses memori
  - Penggunaan format-format instruksi sederhana, panjang instruksinya tetapdan
    disesuaikan dengan panjang word. Fitur ini memiliki beberapa kelebihankarena dengan
    menggunakan field yang tetap pendekodean opcode danpengaksesan operand register dapat
    dilakukan secara bersama-sama

- Ciri - ciri:
  - Instruksi berukuran tunggal
  - Ukuran yang umum adalah 4 byte
  - Jumlah pengalamatan data sedikit, biasanya kurang dari 5 buah
  - Tidak terdapat pengalamatan tak langsung yang mengharuskan melakukan sebuah
    akses memori agar memperoleh alamat operand lainnya dalam memori
  - Tidak terdapat operasi yang menggabungkan operasi load/store dengan operasi
    aritmatika, seperti penambahan ke memori dan penambahan dari memori.
  - Tidak terdapat lebih dari satu operand beralamat memori per instruksi7. Tidak
    mendukung perataan sembarang bagi data untuk operasi load/ store
  - Jumlah maksimum pemakaian memori manajemen bagi suatu alamat data adalah
    sebuah instruksi .
  - Jumlah bit bagi integer register spesifier sama dengan 5 atau lebih, artinya sedikitnya
    32 buah register integer dapat direferensikan sekaligus secara eksplisit.
  - Jumlah bit floating point register spesifier sama dengan 4 atau lebih, artinya sedikitnya
  - register floating point dapat direferensikan sekaligus secara eksplisit

CISC adalah singkatan dari Complex Intruction Set Computer dimana prosesor tersebut
memiliki set instruksi yang kompleks dan lengkap

- Karakteristik:
  - Syarat informasi memberikan keuntungan di mana ukuran program-program yang
    dihasilkan akan menjadi relatif lebih kecil, dan penggunaan memory akan semakin
    berkurang
  - Dimaksudkan untuk meminimumkan jumlah perintah yang diperlukan untuk
    mengerjakan pekerjaan yang diberikan

- Ciri - ciri:
  - Instruksi berukuran tunggal
  - Ukuran yang umum adalah 4 byte
  - Jumlah mode pengalamatan data yang sedikit, biasanya kurang dari lima buah
  - Tidak terdapat pengalamatan tak langsung
  - Tidak terdapat operasi yang menggabungkan operasi load/store dengan operasi
    aritmetika (misalnya, penambahan dari memori, penambahan ke memori)

# Hubungan Arsitektur CPU dengan Arsitektur OS
CPU dan Arsitektur OS bekerja bersama-sama untuk menjalankan program-program dan mengelola sumber daya komputer secara efisien. CPU menjalankan instruksi-instruksi yang diberikan oleh OS, sementara OS mengatur dan mengelola cara di mana CPU digunakan oleh berbagai program dan proses

 - eksekusi instruksi:
    - CPU adalah otak komputer yang memiliki tugas untuk mengeksekusi instruksi-instruksi yang diberikan oleh sistem operasi. Sistem operasi menyediakan interface            antara aplikasi dan perangkat keras, yang memungkinkan CPU untuk menjalankan perintah-perintah yang diperlukan untuk menjalankan program-program

- Penjadwalan Proses:
    - CPU perlu mengeksekusi berbagai proses yang berjalan secara bersamaan di dalam sistem. Sistem operasi bertugas untuk melakukan penjadwalan proses , memastikan         bahwa setiap proses mendapatkan akses yang adil dan efisien terhadap CPU

# Fork
- untuk menjalankan fork diperlukan penginstallan g++ 

```sh$ su root

$ sudo apt update

$ sudo apt upgrade

$ sudo apt install g++
```



![ffork01](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/0d0f6992-1f6c-4a52-b86e-d0c901d95d0f)

### Fork 01


![fork03](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/a0ac3fc6-a6d0-49a5-b724-4e59846e0e86)


  1. memasukan $ nano fork01.cpp ke dalam compiler
  2. lalu menginputkan source code
  3. mengubah jenis file dari '.cpp' menjadi '.exe'
  4. menjalankan source code menggunakan $ ./fork01.exe

### Fork 02


![fork04](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/8c800c93-dee8-4e28-a202-c86b1bb8b2d6)

  1. memasukan $ nano fork02.cpp ke dalam compiler
  2. lalu menginputkan source code
  3. mengubah jenis file dari '.cpp' menjadi '.exe'
  4. menjalankan source code menggunakan $ ./fork02.exe

# Orphan

![orphan01](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/e060a02c-68ab-4156-8b47-fc7e432f7c5b)

  1. melakukan git clone ke https://github.com/ferryastika/operatingsystem
  2. masuk kedalam direktori operatingsystem
  3. memasukkan $ nano orphan.c
  4. mengubah jenis file dari 'orphan.c' menjadi 'orphan.exe'
  5. menjalankan source code menggunakan $ ./orphan.exe

# Zombie

![zombie01](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/c784498a-f5e5-414e-9e27-97e0514541d8)

  1. memasukkan $ nano zombie.c kedalam compiler
  2. mengubah jenis file dari 'zombie.c' menjadi 'zombie.exe'
  3. menjalankan source code menggunakan $ ./zombie.exe




  









