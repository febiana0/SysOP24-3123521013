# Concurrent & Serial

![image](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/1850b4fb-6d96-44d2-abb8-d262725dc35a)

### Concurrent

- Definisi: Eksekusi konkuren berarti beberapa tugas atau proses dijalankan secara bersamaan dalam periode waktu yang sama. Ini tidak berarti bahwa tugas-tugas tersebut berjalan pada saat yang persis sama (secara paralel), tetapi mereka dijalankan dalam potongan waktu yang tumpang tindih.
- Implementasi:
  
  - Multithreading: Beberapa thread dalam satu proses berjalan secara bersamaan.
  - Multiprocessing: Beberapa proses dijalankan secara bersamaan pada CPU yang sama atau berbeda.
  - Asynchronous Programming: Tugas-tugas dapat berjalan secara overlapped menggunakan async/await, tanpa harus menunggu satu tugas selesai sebelum memulai yang lain.
- Contoh:
  - Web server yang menangani beberapa permintaan klien secara bersamaan.
  - Aplikasi GUI yang merespon input pengguna sambil menjalankan tugas latar belakang.

### Serial
- Definisi: Eksekusi serial berarti tugas atau proses dijalankan satu per satu, satu tugas harus selesai sebelum tugas berikutnya dimulai.
- Implementasi:
  - Tugas-tugas dikerjakan dalam urutan tertentu tanpa ada tumpang tindih waktu eksekusi.
- Contoh:
  - Program yang membaca file, memproses datanya, dan kemudian menulis hasilnya ke file lain, dilakukan satu langkah demi satu langkah.

### Perbandingan Utama
- Waktu Eksekusi: Eksekusi konkuren seringkali lebih efisien dalam hal waktu karena beberapa tugas dapat berjalan bersamaan, sementara eksekusi serial bisa lebih lambat karena harus menunggu setiap tugas selesai sebelum melanjutkan ke tugas berikutnya.
- Kompleksitas: Pengelolaan eksekusi konkuren biasanya lebih kompleks karena melibatkan sinkronisasi dan penanganan masalah seperti race conditions dan deadlocks. Eksekusi serial lebih sederhana dan mudah di-debug karena alirannya yang linier.
- Kinerja: Dalam sistem dengan banyak CPU atau core, eksekusi konkuren dapat memberikan peningkatan kinerja yang signifikan, sementara eksekusi serial tidak dapat memanfaatkan keuntungan dari multi-core CPU.

# Concurrent & Parallel

![image](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/85cd7591-3418-42e6-81b7-2c27e07402a0)

### Concurrent
- Definisi: Eksekusi konkuren berarti beberapa tugas atau proses dijalankan pada waktu yang sama dalam konteks yang sama, dengan masing-masing tugas mungkin tidak berjalan pada saat yang persis sama, tetapi saling bergantian atau tumpang tindih dalam periode waktu yang sama.
- Cara Kerja:
  - Multithreading: Beberapa thread dalam satu proses berbagi waktu CPU dan dapat saling bergantian menjalankan tugas.
  - Asynchronous Programming: Tugas-tugas yang berjalan secara overlapped menggunakan mekanisme seperti async/await tanpa harus menunggu satu tugas selesai sebelum memulai yang lain.
  - Tujuan: Meningkatkan efisiensi dengan menjalankan beberapa tugas secara bersamaan, membuat sistem tetap responsif, terutama pada operasi I/O yang menunggu.

- Contoh:
  - Server web yang menangani beberapa permintaan klien secara bersamaan dengan mengalokasikan waktu CPU ke masing-masing permintaan secara bergantian.
  - Aplikasi desktop yang tetap merespons input pengguna sambil menjalankan operasi latar belakang seperti mengunduh data.

### Parallel
- Definisi: Eksekusi paralel berarti beberapa tugas atau proses benar-benar berjalan pada saat yang sama pada perangkat keras yang terpisah, seperti multiple core atau multiple CPU.
- Cara Kerja:
  - Multiprocessing: Menjalankan beberapa proses secara bersamaan pada core CPU yang berbeda atau bahkan pada CPU yang berbeda.
  - Parallel Algorithms: Algoritma yang dirancang untuk membagi tugas menjadi sub-tugas yang dapat dijalankan secara simultan pada perangkat keras terpisah.
  - Tujuan: Mempercepat eksekusi tugas dengan mendistribusikan pekerjaan ke beberapa unit pemrosesan yang dapat bekerja secara bersamaan.
    
- Contoh:
  - Pemrosesan gambar yang membagi gambar menjadi beberapa bagian dan memproses bagian-bagian tersebut secara bersamaan pada core yang berbeda.
  - Algoritma komputasi ilmiah yang memecah tugas besar menjadi beberapa tugas kecil yang dijalankan secara simultan pada superkomputer.
 
### Perbandingan Utama
- Hardware: Konkuren dapat terjadi pada satu core CPU dengan penjadwalan yang tepat, sedangkan paralel memerlukan multiple core atau CPU untuk menjalankan tugas secara simultan.
- Tujuan dan Penggunaan: Konkuren bertujuan untuk meningkatkan efisiensi dan responsivitas dalam penanganan tugas yang saling bergantian, sementara paralel bertujuan untuk mempercepat eksekusi dengan menjalankan tugas secara simultan pada perangkat keras terpisah.
- Kompleksitas: Pengelolaan konkuren melibatkan penjadwalan tugas dan sinkronisasi di tingkat software, sedangkan pengelolaan paralel lebih banyak berfokus pada pembagian dan distribusi tugas ke perangkat keras yang berbeda serta sinkronisasi hasilnya.
