# Nomor 1

![CPU process](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/4bdcb750-d51a-449a-9357-55f6bd4354a0)



A. Mekanisme Eksekusi Program oleh CPU

Dalam mengeksekusi / menjalankan suatu program, CPU memiliki sebuah siklus atau cycle. Cycle ialah proses atau langkah langkah berulang yang dilaksanakan oleh CPU untuk menjalankan instruksi program.

Pada siklus CPU, terdapat tiga komponen atau langkah-langkah utama yaitu Fetch (Pengambilan), Decode (Proses pemecahan kode), dan Execute (Ekseskusi). Adapun penjelasan mengenai komponen-komponen utama tersebut adalah sebagai berikut : 

1. Fetch (Pengambilan)

   ![FETCH](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/4df0dab6-3a6a-46dc-9f21-6c3699344b96)


     - programme Counter mengambil adress 0
     - CPU pada instruction register memasukkan value dari adress 0 yaitu LOAD 6

   



Dalam siklus CPU, Fetch (Pengambilan) adalah langkah paling awal, di mana CPU mengambil instruksi dari memori. Proses ini melibatkan pengiriman alamat memori dari instruksi yang akan dieksekusi oleh CPU ke unit memori. Setelah itu, Unit memori mengambil instruksi tersebut dari lokasi memori yang sesuai lalu mengirimkan instruksi tersebut kembali ke CPU untuk diproses lebih lanjut dalam siklus eksekusi. Pada intinya, Fetch adalah proses pengambilan instruksi dari memori agar nantinya dapat dieksekusi oleh CPU.

2. Decode (Pemecahan Kode)
   ![decode](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/6a3da20b-d419-427c-98d0-5f84421920c3)

   - CPU memproses instruksi yang telah diterima dari langkah Fetch 


Langkah selanjutnya dalam siklus CPU ialah Decode (Pemecahan kode). Decode adalah langkah kedua di mana CPU mengurai instruksi yang telah diambil dari langkah Fetch sebelumnya hingga menjadi bentuk yang dapat dimengerti atau diinterpretasikan oleh CPU. Proses dekode ini melibatkan analisa kode instruksi guna menentukan operasi apa yang harus dilakukan oleh CPU. CPU kemudian menyiapkan sirkuit yang sesuai untuk melaksanakan instruksi yang telah diuraikan dari proses Decode. Dapat disimpulkan bahwa, Decode adalah proses pemecahan kode menjadi bentuk yang dapat dimengerti oleh CPU sehingga dapat diproses lebih lanjut dalam langkah selanjutnya.

3. Execute (Eksekusi)
   
   ![execute](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/e2b8bd99-b545-4ed9-b730-65b388c7680a)

   - CPU menjalankan instruksi sesuai dengan instruction register. Pada proses CPU diatas instruction register nya adalah LOAD 6, lalu pada accumulator CPU menampilkan value 1 sesuai dengan adress yg semula dimasukkan


Dalam siklus CPU, Execute (Eksekusi) adalah langkah ketiga yaitu ketika CPU menjalankan instruksi yang telah melalui proses Fetch dan Decode. Pada langkah ini, CPU melakukan operasi yang sesuai dengan instruksi yang telah dianalisis dari proses Decode sebelumnya. Operasi ini bisa berupa manipulasi data, pengolahan aritmetika, transfer data antar lokasi memori, dan lainnya berdasarkan pada instruksi yang dieksekusi. Setelah instruksi dieksekusi, maka CPU siap untuk mengulang langkah-langkah tadi dari awal, sehingga terbentuklah siklus. Siklus akan terus berlanjut hingga seluruh program berhasil dieksekusi oleh CPU

Kesimpulannya adalah siklus CPU merupakan proses kunci dalam jalannya program pada CPU. Pemahaman terhadap siklus amatlah penting dalam pengembangan software atau perangkat lunak, dan penyelesaian masalah.

B. Peran Bahasa Pemrograman, Compiler, dan Sistem Operasi dalam Siklus CPU

1. Bahasa Pemrograman
Bahasa pemrograman akan memberikan workframe, atau aturan untuk menulis instruksi yang akan dieksekusi oleh CPU. Bahasa pemrograman berfungsi untuk menyediakan syntax dan struktur untuk mengekspresikan algoritma ataupun logika dari program. Bahasa pemrograman akan memudahkan pengembang dalam menguraikan kebutuhan bisnis atau logika komputasi ke dalam serangkaian instruksi yang dapat dimengerti oleh komputer.

2. Compiler
Compiler memiliki tugas untuk menerjemahkan kode yang ditulis dalam bahasa pemrograman tingkat tinggi menjadi bahasa mesin sehingga nantinya dapat dimengerti oleh CPU. Compiler melakukan tugasnya dengan menjalankan proses transformasi dari kode sumber ke dalam binary yang nantinya dapat dieksekusi langsung oleh CPU. Dengan bantuan compiler, program yang ditulis dalam bahasa pemrograman manusia akan dapat dijalankan oleh CPU tanpa perlu memahami bahasa mesin secara langsung.

3. Sistem operasi / OS
OS bertindak sebagai media perantara antara hardware (termasuk CPU) dengan software aplikasi. Sistem operasi menyediakan lingkungan untuk jalannya pelaksanaan sehingga aplikasi dapat berinteraksi dengan hardware. Sistem operasi mengelola sumber daya seperti memori, dan proses-proses yang berjalan di sistem. Dalam konteks siklus CPU, sistem operasi berperan dalam mengelola eksekusi program, mengatur penggunaan CPU oleh berbagai proses, dan menyediakan layanan-layanan yang diperlukan guna menunjang jalannya program secara efisien.


# Nomor 3

## Melakukan clone https://github.com/ferryastika/flops-iops
  
  ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/VirtualBox_Debian12%20Desktop%20FEBI_17_03_2024_10_40_31.png?raw=true)

## Build Binaries

```sh
$ make
```
![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/VirtualBox_Debian12%20Desktop%20FEBI_17_03_2024_10_42_50.png?raw=true)

## Cleaning Old Build

```sh
$ make clean
```
![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/makeclean.png?raw=true)

## Install Binaries 

```sh
$ sudo make install
```
![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/install.png?raw=true)

## Uninstall Binaries 

```sh
$ sudo make uninstall
```
![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/uninstall.png?raw=true)

## Usage

```sh
  $ iops64 $(nproc)
```

### $ iops64 $(nproc) 1
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/iops64(1).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2874645384 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - IOPS = 2874645384 menunjukkan jumlah operasi input/output (I/O) per detik (IOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.874645384 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaiops (Giga input/output operations per second)
   - maximum single core cpu throughput: 2.874645384 Gigaiops enunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaiops

### $ iops64 $(nproc) 2
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/iops64(2).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2899442572 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - IOPS = 2899442572 menunjukkan jumlah operasi input/output (I/O) per detik (IOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.899442572 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaiops (Giga input/output operations per second)
   - maximum single core cpu throughput: 2.899442572 Gigaiops enunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaiops
   

### $ iops64 $(nproc) 3
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/iops64(3).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2879324656 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - IOPS = 2879324656 menunjukkan jumlah operasi input/output (I/O) per detik (IOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.879325 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaiops (Giga input/output operations per second)
   - maximum single core cpu throughput: 2.879325 Gigaiops enunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaiops

### $ iops64 $(nproc) 4
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/iops64(4).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2847016588 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - IOPS = 2847016588 menunjukkan jumlah operasi input/output (I/O) per detik (IOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.847017 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaiops (Giga input/output operations per second)
   - maximum single core cpu throughput: 2.847017 Gigaiops enunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaiops

### $ iops64 $(nproc) 5
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/iops64(5).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2893818928 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - IOPS = 2893818928 menunjukkan jumlah operasi input/output (I/O) per detik (IOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.8938189 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaiops (Giga input/output operations per second)
   - maximum single core cpu throughput: 2.8938189 Gigaiops enunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaiops


## Usage

```sh
  $ flops64 $(nproc)
```

### $ flops64 $(nproc) 1
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/flops64(1).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2701029188 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - FLOPS = 2701029188 menunjukkan jumlah operasi floating-point per detik (FLOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.701029 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaflops (Giga floating-point operations per second)
   - maximum single core cpu throughput: 2.701029 Gigaflops menunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaflops

### $ flops64 $(nproc) 2
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/flops64(2).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2722983120 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - FLOPS = 2722983120 menunjukkan jumlah operasi floating-point per detik (FLOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.722983 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaflops (Giga floating-point operations per second)
   - maximum single core cpu throughput: 2.722983 Gigaflops menunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaflops

### $ flops64 $(nproc) 3
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/flops64(3).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2723450600 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - FLOPS = 2723450600 menunjukkan jumlah operasi floating-point per detik (FLOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.723451 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaflops (Giga floating-point operations per second)
   - maximum single core cpu throughput: 2.723451 Gigaflops menunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaflops

### $ flops64 $(nproc) 4
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/flops64(4).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2684977490 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - FLOPS = 2684977490 menunjukkan jumlah operasi floating-point per detik (FLOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.684977 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaflops (Giga floating-point operations per second)
   - maximum single core cpu throughput: 2.684977 Gigaflops menunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaflops

### $ flops64 $(nproc) 5
   ![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Tugas%203/flops64(5).png?raw=true)
   
   hasil: 
   - 1 | Tr 1: 2538892798 merupakan nomor iterasi atau transaksi, diikuti oleh identifikasi unik atau penanda waktu yang terkait dengan pengujian
   - FLOPS = 2538892798 menunjukkan jumlah operasi floating-point per detik (FLOPS) yang dicapai selama pengujian
   - Maximum CPU throughput: 2.538893 Gigaiops menunjukkan throughput maksimum CPU yang dicapai selama pengujian, diukur dalam Gigaflops (Giga floating-point operations per second)
   - maximum single core cpu throughput: 2.538893 Gigaflops menunjukkan throughput maksimum yang diperoleh pada satu core CPU, juga diukur dalam Gigaflops

### Plot Perbandingan Antar Teman
![Screenshot (67)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/e16e70ca-2213-413d-ad36-03d60dfcb863)

  **Analisa:** Dari plot perbandingan di atas, dapat dilihat bahwa Alyssa memiliki nilai rata-rata IOPS dan FLOPS yang lebih tinggi dibandingkan dengan Dyzka, Pelangi, dan Feby. Hal ini   menunjukkan bahwa PC Alyssa cenderung memiliki performa yang lebih baik dalam menangani operasi input/output (IOPS) dan operasi floating point (FLOPS).

  **Kesimpulan:** performa komputer dalam hal IOPS dan FLOPS sangat penting tergantung pada kebutuhan aplikasi atau tugas yang dijalankan. Semakin tinggi nilai IOPS dan FLOPS, semakin     baik kemampuan komputer tersebut dalam menangani tugas-tugas yang memerlukan operasi input/output dan operasi floating point secara cepat dan efisien.


# Nomor 4

```sh
  apt install make
```
![apt (2)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/a11e09f8-2e3c-4948-a30b-12803a772a87)

```sh
  apt install gcc
```
![apt (3)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/0639500c-2c37-4578-a6a5-1c8b143d8b9e)

```sh
  apt install git
```
![apt (4)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/cdd0409f-d59e-45f5-ab64-d193e3e471e1)





