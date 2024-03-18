# Nomor 1
A. Mekanisme Eksekusi Program oleh CPU

Dalam mengeksekusi / menjalankan suatu program, CPU memiliki sebuah siklus atau cycle. Cycle ialah proses atau langkah langkah berulang yang dilaksanakan oleh CPU untuk menjalankan instruksi program.

Pada siklus CPU, terdapat tiga komponen atau langkah-langkah utama yaitu Fetch (Pengambilan), Decode (Proses pemecahan kode), dan Execute (Ekseskusi). Adapun penjelasan mengenai komponen-komponen utama tersebut adalah sebagai berikut : 

1. Fetch (Pengambilan)

Dalam siklus CPU, Fetch (Pengambilan) adalah langkah paling awal, di mana CPU mengambil instruksi dari memori. Proses ini melibatkan pengiriman alamat memori dari instruksi yang akan dieksekusi oleh CPU ke unit memori. Setelah itu, Unit memori mengambil instruksi tersebut dari lokasi memori yang sesuai lalu mengirimkan instruksi tersebut kembali ke CPU untuk diproses lebih lanjut dalam siklus eksekusi. Pada intinya, Fetch adalah proses pengambilan instruksi dari memori agar nantinya dapat dieksekusi oleh CPU.

2. Decode (Pemecahan Kode)

Langkah selanjutnya dalam siklus CPU ialah Decode (Pemecahan kode). Decode adalah langkah kedua di mana CPU mengurai instruksi yang telah diambil dari langkah Fetch sebelumnya hingga menjadi bentuk yang dapat dimengerti atau diinterpretasikan oleh CPU. Proses dekode ini melibatkan analisa kode instruksi guna menentukan operasi apa yang harus dilakukan oleh CPU. CPU kemudian menyiapkan sirkuit yang sesuai untuk melaksanakan instruksi yang telah diuraikan dari proses Decode. Dapat disimpulkan bahwa, Decode adalah proses pemecahan kode menjadi bentuk yang dapat dimengerti oleh CPU sehingga dapat diproses lebih lanjut dalam langkah selanjutnya.

3. Execute (Eksekusi)

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
  $ iops44 $(nproc)
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




