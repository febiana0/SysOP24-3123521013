

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
