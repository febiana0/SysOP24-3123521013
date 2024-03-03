# Boot Process dan Mengidentifikasi CPU pada Laptop

## Boot Process

![alt text](https://github.com/febiana0/SysOP24-3123521013/blob/main/Diagram%20Tanpa%20Judul.jpg?raw=true)

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

