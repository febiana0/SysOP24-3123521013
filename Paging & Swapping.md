## Swapping

Managing Memory / Swapping (tukar menukar) adalah antrian panjang dari proses yang disimpan dalam disk. Proses swapping menukarkan sebuah proses keluar dari memori untuk sementara waktu ke sebuah penyimpanan sementara dengan sebuah proses lain yang sedang membutuhkan sejumlah alokasi memori untuk dieksekusi.
Tempat penyimpanan sementara ini biasanya berupa sebuah fast disk dengan kapasitas yang dapat menampung semua salinan dari semua gambaran memori serta menyediakan akses langsung ke gambaran tersebut. Jika eksekusi proses yang dikeluarkan tadi akan dilanjutkan beberapa saat kemudian, maka ia akan dibawa kembali ke memori dari tempat penyimpanan sementara tadi.

contoh:

![image](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/6ae98f6e-547a-43b4-b724-cfc8d97036d8)


## Paging

Paging adalah suatu metode yang mengizinkan alamat logika proses untuk dipetakan ke alamat fisik memori yang tidak berurutan, yaitu sebagai solusi dari masalah fragmentasi ekstern. Metode dasar dari paging adalah dengan memecah memori fisik menjadi blok-blok yang berukuran tertentu (frame) dan memecah memori logika menjadi blok-blok yang berukuran sama (page).
Paging merupakan teknik menampilkan data dengan cara membaginya ke beberapa halaman. Teknik ini diberikan untuk mengurangi scrolling window apabila data yang disajikan terlalu banyak, sehingga akan menimbulkan kejemuan orang yang melihat dan juga akan menghasilkan page load time yang besar karena ukuran filenya besar (apabila data disajikan dalam satu halaman saja).

- Membagi memory dalam ukuran yang sama, dalam potongan kecil (disebut bingkai halaman)
- Membagi program (proses) dalam potongan kecil berukuran sama
- Mengalokasikan jumlah bingkai halaman yang diperlukan untuk sebuah proses
- Sistem Operasi mengelola daftar bingkai yang bebas (tidak digunakan)
- Sebuah proses tidak memerlukan bingkai halaman yang berdampingan
- Menggunakan tabel halaman untuk menjaga alur kerja
- Paging –> Mempersiapkan resource untuk proses yang akan dijalankan

contoh:

![image](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/19919deb-45d6-4aeb-a965-3d423f8fe610)  
![image](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/3676101d-83a5-4a59-aef4-de6a3bc651b5)


 
