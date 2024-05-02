# Boot Process dan Mengidentifikasi Laptop pada Aplikasi CPU-Z

## Boot Process

![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/image_asset/Diagram%20Tanpa%20Judul.jpg?raw=true)

Penjelasan:
- Processor start BIOS, proses pertama ketika menyalakan komputer terjadi di bios. BIOS (basic input output system) berfungsi untuk menjalankan POST dan membaca MBR
- POST (Power-on Self Test), untuk mengecek semua perangkat yang terhubung ke komputer seperti ram, cd, harddisk dan lainnya dan memastikan sistem dapat berjalan dengan baik dengan perangkat keras yang ada
- Setelah POST melakukan testing, selanjutnya BIOS membaca Master Boot Record (MBR). MBR disimpan di sektor pertama hard disk dan berisi boot loader
- Windows Boot Manager, memungkinkan user untuk memilih dari beberapa sistem operasi atau memilih kernel atau dapat membantu mendiagnosa memori pada windows. Windows Boot Manager memulai Windows Boot Loader
- Windows Boot Loader, adalah program kecil yang memuat kernel ke memori komputer yang ada di RAM. Di dalam sistem operasi windows ada 3 boot file yaitu NTDLR, NTDETECT.COM dan Boot.ini.
- Loading Windows Kernel, ntoskrnal.exe adalah file kernel di mesin windows dan path-nya adalah C:\Windows\system 32\ntoskrnal.exe. Kernel berperan sebagai lapisan antara software dan hardware. File library hal.dll (C;\Windows\system32\hal.dll) membantu kernel untuk berinteraksi dengan hardware. Kepanjangan HAL adalah Hardware Abstraction Layer dan file hal.dll ini adalah mesin spesifik. Sekarang driver hardware dimuat dari file C:\Windows\system32\config\system dan kernel dimuat ke memori primer
- Windows Executable, executable file atau file EXE adalah jenis file yang umum di perangkat berbasis Windows untuk menginstall atau menjalankan software/aplikasi
- Ketika kernel dimuat di memori primer, layanan untuk tiap proses dimulai dan masukan registry untuk layanan itu dapat ditemukan di HKEY_LOCAL_MACHINE - System - Current control set - Services. Winlogon.exe. C:\Windows\system32\winlogon.exe) adalah layanan terakhir pertama yang terjadi di proses. Winlogon.exe memulai log di prosedur mesin windows. Ini adalah call pertama file librari msgina.dll (C:\Windows\system32\msgina.dll). MSGINA kependekan dari Microsoft Graphics Identification and Authentication yang menyediakan log di windows. Sekarang msginal.dll melewatkan kendali ke LSA (Local Security Authority), yang memverifikasi username dan password dari file SAM. SAM (Security Accounts Manager) terdiri dari informasi tentang user yang dibuat di sistem operasi windows. Sekarang prosedur booting telah selesai dan kita telah mencapai desktop sistem operasi.

  
## Mengidentifikasi Laptop melalui aplikasi CPU-Z

### Spesifikasi CPU
![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/image_asset/Screenshot%20(38).png?raw=true)

#### _Section Processor_
- Name : Intel Core i3 4005U

  Menampilkan nama dari processor yang digunakan pada laptop atau komputer

- Code Name : Haswell ULT

  Menampilkan Code dari processor yang dipakai komputer atau laptop

- Max TDP : 15.0 W

  Menyatakan power consumption, Artinya laptop atau komputer ini membutuhkan daya 15.0 W saat bekerja

-   Package : Socket 1168 BGA

    Menampilkan bahwa jenis socket pada processor laptop ini adalah Socket 1168 BGA

- Technology :  22 nm

  Menampilkan Seberapa besar komponen yang digunakan

- Core Voltage : 0.670 V

  Menampilkan tegangan listrik yang digunakan

-  Specification : Intel Core i3-4005U CPU @ 1.70GHz

    Menampilkan Spesifikasi dari komputer atau laptop yang dipakai

- Family : 6

  Menampilkan generasi keberapa processor yang digunakan

- Ext Family : 6

  Menampilkan total family (keluarga) processor yang ada dalam komputer atau laptop

- Intruction : MMX, SSE, SSE2, SSE3, SSSE3, SSE4.1, SSE4.2, EM64T, VT-x, AES, AVX, AVX2, FMA3

  Menampilkan instruksi yang didukung dalam processor yang dipakai.

  MMX : berhubungan dengan Integrasi VGA (yang mangatur tentang visual berupa gambar, grafik, dll).
  SSE : jenis – jenis instruksi algoritma atau perhitungan yang dapat dipahami processor.
  EM64T : teknologi yang meningkatkan platform server dan stasiun kerja dengan keterlayakan alamat 64 bit dan instruksi terkait.
  VT-x :  dapat mengizinkan komputer untuk membuat mesin virtuaL

#### _Section Clocks (Core #0)_

- Core Speed : 1695.95 MHz

  Mengetahui kecepatan satu core satuan dalam melakukan suatu perintah

- Multiplier : x 8.0 (8.0 – 17.0)
  
  Mengatur lebar jalur transfer yang tersedia. Pengkali. Apabila processor banyak melakukan proses pada computer, maka multiplier         meningkat. Sedangkan apabila processor sedikit melakukan proses pada computer, maka multiplier menurun dalam keadaan stabil.

- BUS speed : 99.76 MHz
  
  Menampilkan kecepatan transfer data dan instruksi atau kecepatan BUS. Jumlah alur yang mampu dilaksanakan oleh sebuah pemproses dalam   masa second. Satuan waktu ini diukur dalam unit juta arahan second yang disebut juga sebagai megahertz (MHz) atau juta kitaran second 

- Cache

  Cache memory adalah memory berukuran kecil berkecepatan tinggi yang berfungsi untuk menyimpan sementara instruksi dan/atau data   (informasi) yang diperlukan oleh prosesor
  - L1 : Trensfer data ke prosesor paling cepat karena letaknya paling dekat dengan prosesor
  - L2 : Transfer data ke proseror lebih lambat dari L1 karena posisinya lebih jauh dari prosesor
  - L3 : Transfer datanya paling lambat kerena jauh dari prosesor


### Spesifikasi Mainboard

![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/image_asset/Screenshot%20(39).png?raw=true)

#### _Section Motherboard_

- Manufacture : ASUStek Computer INC.

  Merupakan pembuat dari motherboard laptop ini

- Mode : X455LF

  Tipe dari motherboard pada komputer atau laptop

- Chipset : Intel
  
  Chipset yang digunakan adalah Intel, sedangkan Haswell-ULT merupakan tipe dari chipset yang digunakan. Secara fisik, chipset berupa sekumpulan IC kecil atau chips yang dirancang untuk   bekerjasama dan memiliki fungsi-fungsi tertentu

- Southbridge : Intel
  
#### _Section BIOS_
- Brand : American Megatrends Inc

  Merupakan merk BIOS yang digunakan

- Version : X455LF.205

  Menampilkan versi BIOS

- Date : 08/03/2015

  tanggal pembuatan BIOS Graphic Interface
  
#### _Section Graphic Interface_
- Bus : PCI-Express 

  Menampilkan versi Graphic (VGA)

  
### Spesifikasi Memory
![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/image_asset/Screenshot%20(40).png?raw=true)

#### _Section General_

- Type : DDR 3

  Menampilkan tipe memori apa yang digunakan pada laptop / komputer.

- Size : 4 Gbytes

  merupakan besaran memori yang terdapat pada kompter/ laptop

- Channel # : Dual

- Uncore frequency : 1397.2 Mhz


#### _Section Timings_
  
- DRAM Frequency : 798,1 MHZ

  frekuensi Memori DRAM adalah 798,4 MHZ
  
- FSB : DRAM = 1:6
- CL : 11,0 clocks
- tRCD : 11 clocks
- tRP : 11 clocks
- tRAS :28 clocks
- tRFC : 128 clocks
- CR : 1T

### Spesifikasi SPD
![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/image_asset/Screenshot%20(41).png?raw=true) 

#### _Section Memory Slot Selection_

Memory Slot yang digunakan pada laptop ini adalah slot ke-1 saja, karena laptop ini merupakan laptop yang menggunakan single channel dapat dilihat pada kolom (Rank).

- Modul Manuf. : TEAMGROUP.Inc 

  TEAMGROUP.Inc  merupakan pembuat dari modul laptop

- DRAM Manuf. : TEAMGROUP.Inc 

  TEAMGROUP.Inc  merupakan pembuat dari memori laptop

- Part Number : TEAMGROUP-SD3-1600

- Serial Number : 01047D37

  merupakan nomor seri dari memori DDR3 samsung tersebut


### Spesifikasi Graphics

![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/image_asset/Screenshot%20(42).png?raw=true) 

- Nama : NVIDIA GeForce 950M

  Merupakan nama dari kartu grafis (VGA) pada laptop

- Board Manf. : ASUSTeK Computer Inc. 

  merupakan pembuat dari VGA tersebut

- GFx Core : 927.9 MHz

  kecepatan clock pada core VGA 927.9 MHz

- Memory : 900.0 MHz

  kecepatan  memory 900.0 MHz
  
- Memory Size : 2 GBytes

  kapasitas dari memori VGA

- Type : DDr3

- Vendor : Micron
 
- Bus Width : 64 Widts


