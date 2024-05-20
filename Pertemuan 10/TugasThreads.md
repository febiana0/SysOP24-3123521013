# Threads (Alur kontrol)

### Latihan

**4.1 Berikan tiga contoh pemrograman di mana multithreading menyediakan Performa yang lebih baik daripada solusi thread tunggal**

Jawab:

a. Server Web yang melayani setiap permintaan dalam thread terpisah.

b. Aplikasi paralel seperti perkalian matriks di mana Bagian matriks yang berbeda dapat dikerjakan secara paralel

c. Program GUI interaktif seperti debugger tempat thread berada digunakan untuk memantau input pengguna, thread lain mewakili yang sedang berjalan
aplikasi, dan monitor performa thread ketiga 

**4.2 Apa dua perbedaan antara thread tingkat pengguna dan tingkat kernel thread? Dalam keadaan apa satu jenis lebih baik dari yang lain?**

Jawab:

a. Thread tingkat pengguna tidak diketahui oleh kernel, sedangkan kernel mengetahui utas kernel.

b. Pada sistem yang menggunakan pemetaan M:1 atau M:N, thread pengguna adalah dijadwalkan oleh pustaka thread dan kernel menjadwalkan kernel thread

c. Kernel thread tidak perlu dikaitkan dengan proses sedangkan setiapThread pengguna termasuk dalam suatu proses. Kernel thread umumnya
lebih mahal untuk perawatannya daripada user sebagaimana mestinya diwakili dengan struktur data kernel.

**4.3 Menjelaskan tindakan yang diambil oleh kernel untuk context-switch antara thread kernellevel**

Jawab:

Peralihan konteks antar thread kernel biasanya memerlukan penyimpanan nilai register CPU dari thread yang sedang dialihkan dan memulihkan register CPU dari thread baru yang sedang dijadwalkan.


**4.4 Sumber daya apa yang digunakan saat thread dibuat? Bagaimana mereka berbeda dari yang digunakan saat proses dibuat?**

Jawab:

Karena thread lebih kecil dari proses, pembuatan thread biasanya menggunakan lebih sedikit sumber daya daripada pembuatan proses. Membuat proses membutuhkan mengalokasikan blok kontrol proses (PCB), struktur data yang agak besar. PCB mencakup peta memori, daftar file yang terbuka, dan lingkungan
Variabel. Mengalokasikan dan mengelola peta memori biasanya adalah aktivitas yang paling memakan waktu. Membuat thread pengguna atau kernel melibatkan mengalokasikan struktur data kecil untuk menampung set register, tumpukan, dan prioritas.

**4.5 Asumsikan bahwa sistem operasi memetakan thread tingkat pengguna ke kernel menggunakan model banyak-ke-banyak dan pemetaan dilakukan melalui LWP. Selain itu, sistem ini memungkinkan pengembang untuk membuat real-time
thread untuk digunakan dalam sistem real-time. Apakah perlu untuk mengikat real-time thread ke LWP? Jelaskan.**

Jawab:

Ya! Waktu sangat penting dalam aplikasi real-time. Jika sebuah thread ditandai sebagai real-time tetapi tidak terikat ke LWP (Lightweight Process), thread tersebut mungkin harus menunggu untuk terhubung ke LWP sebelum berjalan. Pertimbangkan situasi di mana sebuah thread real-time sedang berjalan (terikat ke LWP) dan kemudian mengalami blok (misalnya, harus melakukan I/O, telah dipreempti oleh thread real-time dengan prioritas lebih tinggi, menunggu kunci eksklusi bersama, dll.). 
Ketika thread real-time terblokir, LWP yang sebelumnya terikat ke thread tersebut telah dialokasikan ke thread lain. Ketika thread real-time dijadwalkan untuk berjalan kembali, ia harus menunggu terlebih dahulu untuk terhubung ke LWP. Dengan mengikat LWP ke thread real-time, Anda memastikan bahwa thread tersebut dapat berjalan dengan penundaan minimal setelah dijadwalkan
