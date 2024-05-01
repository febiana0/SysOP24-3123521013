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
