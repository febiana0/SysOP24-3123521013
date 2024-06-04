# Tugas Pendahuluan

### Jawablah pertanyaan-pertanyaan di bawah ini :
- Apa yang dimaksud redirection?

  Redirection merupakan salah satu cara untuk melewatkan output program ke program lain, dengan redirection juga bisa menyimpan output suatu file baik ke dalam sebuah file ataupun diproses dengan program lain

- Apa yang dimaksud pipeline?
  
  Pipeline merupakan fasilitas shell yang berfungsi untuk memberikan input dari suatu proses dari output proses yang lain atau menjadi alat komunikasi antar proses

- Apa yang dimaksud perintah di bawah ini : echo, cat, more, sort, grep, wc, cut, uniq
  
  - echo : Menampilkan text 
  - cat : Melihat isi file 
  - more : Membuka file satu per satu 
  - sort : Digunakan untuk mengurutkan masukannya berdasarkan urutan nomor ASCII dari karakter 
  - grep : Digunakan untuk menyaring masukannya dan menampilkan baris-baris yang hanya mengandung pola yang ditentukan
  - wc : Digunakan untuk menghitung jumlah baris, kata dan karakter dari baris-baris masukan yang diberikan kepadanya. Untuk mengetahui berapa baris gunakan option -1. Untuk mengetahui berapa kata, gunakan option -w dan untuk mengetahui berapa karakter, gunakan option -c. Jika salah satu option tidak digunakan, maka tampilannya adalah jumlah baris, jumlah kata dan jumlah karakter 
  - cut : Digunakan untuk mengambil  kolom tertentu dan baris-baris masukannya, yang ditentukan pada opinion -c 
  - uniq : Digunakan untuk menghilangkan baris-baris berurutan yang mengalami duplikasi, biasanya digabungkan dalam pipeline dengan sort

# Percobaan 

### Percobaan 1 : File descriptor
  1. Output ke layar (standar output), input dari system (kernel)
     ```
     $ ps
     ```
     ![tugas4(1)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/4422cf58-6f4d-452c-aba7-a38d317666e9)

     **Analisa:** $ps merupakan perintah yang digunakan untuk memperlihatkan proses yang sedang berjalan pada sistem (kernel) kemudian diperlihatkan pada layar (proses status). Input                       berasal dari system (kernel), sedangkan output ditampilkan ke layar (standar output)

  2. Output ke layar (standar output), input dari keyboard (standard input)
      ```
      $ cat
     hallo, apa khabar
     hallo, apa khabar
     exit dengan ^d
     exit dengan ^d
     [Ctrl-d]
     ```
      ![tugas4(4)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/df592f7f-35bb-4887-bfbf-05fce3db75a9)

     **Analisa:** $ cat yaitu perintah mengambil input dari keyboard dan kemudian output ditampilkan ke layar

  3. Input nama direktori, output tidak ada (membuat direktori baru), bila terjadi error maka tampilan error pada layar (standard error)
     
     ```
     $ mkdir mydir
     $ mkdir mydir **(Terdapat pesan error)**
     ```
     
     ![tugas4(5)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/1f00d5ba-efb5-4e34-b658-332edcab2e92)

     **Analisa:** $ mkdir merupakan perintah yang digunakan untuk membuat direktori baru. Input dari mkdir adalah nama direktori, sedangkan outputnya tidak ada (membuat direktori baru),       bila terjadi error maka outputnya adalah tampilan error pada layar (standard error)

### Percobaan 2 : Pembelokan (redirection)

  1. Pembelokan standar output
     ```
     $ cat 1> myfile.txt
     Ini adalah teks yang saya simpan ke file myfile.txt
     ```
      ![Per2(1)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/f6032a9d-e91f-4d02-872d-aee351e9904b)

      Analisa: 1> merupakan salah satu metode pembelokan pengganti standar output. Alternatifnya yaitu dengan menggunakan >

  2. Pembelokan standar input, yaitu input dibelokkan dari keyboard menjadi dari file
      ```
      $ cat 0< myfile.txt
      $ cat myfile.txt 
      ```
      ![Per2(2)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/45a83ab1-0aa7-4b64-b8ee-24f6e1762b73)

      Analisa: 0< merupakan salah satu metode pembelokan standar input, yaitu input dibelokkan dari keyboard menjadi dari file. Alternatifnya yaitu dengan menggunakan <

  3. Pembelokan standar error untuk disimpan di file
       ```
       $ mkdir mydir (Terdapat pesan error)
       $ mkdir mydir 2> myerror.txt
       $ cat myerror.txt
       ```
     ![Per2(3)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/a4089cc3-4224-48eb-adbf-8ac6300488d8)

      Analisa: 2> merupakan metode pembelokan standar error untuk kemudian disimpan di file

  4. Notasi 2>&1 : pembelokan standar error (2>) adalah identik dengan file descriptor 1
     ```
     $ ls filebaru (Terdapat pesan error)
     $ ls filebaru 2> out.txt
     $ cat out.txt
     $ ls filebaru 2> out.txt 2>&
     $ cat out.txt
     ```
      ![Per2(4)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/ba6c3444-828f-472d-8b97-5eb52ff7b227)

     Analisa: Notasi 2>&1 pembelokan standar error (2>) adalah identik dengan file descriptor 1

5. Notasi 1>&2 (atau >&2) : pembelokan standar output adalah sama dengan file descriptor 2 yaitu standar error
   ```
   $ echo “mencoba menulis file” 1> baru
   $ cat filebaru 2> baru 1>&
   $ cat baru
   ```
    ![Per2(5)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/f4fe49e6-fbdf-4490-b3f7-2bf6489a5935)

   Analisa: Notasi 1>&2 (atau >&2)  pembelokan standar output adalah sama dengan file descriptor 2 yaitu standar error

6. Notasi >> (append)
   ```
   $ echo “kata pertama” > surat
   $ echo “kata kedua” >> surat
   $ echo “kata ketiga” >> surat
   $ cat surat
   $ echo “kata keempat” > surat
   $ cat surat
   ```
    ![Per2(6)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/6411be43-504d-44ea-8bce-28fb8bd24d8d)

   Analisa: Notasi >> (append) digunakan untuk membelokkan tampilan standard output ke file tanpa menghapus isi dari file sebelumnya

7. Notasi here document (<<++ .... ++) digunakan sebagai pembatas input dari keyboard. Perhatikan bahwa tanda pembatas dapat digantikan dengan tanda apa saja, namun harus sama dan tanda    penutup harus diberikan pada awal baris
     ```
     $ cat <<++
    Hallo, apa kabar?
    Baik-baik saja?
    Ok!
    ++
    $ cat <<%%%
    Hallo, apa kabar?
    Baik-baik saja?
    Ok!
    %%%
    ```
     ![Per2(7)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/8a8339bd-5513-4d7f-a052-fead852c6d22)
     ![Per2(7 2)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/cb0e9c6a-4d87-4f4c-86f0-8da553f27bd5)

    Analisa: Notasi here document (<<++ .... ++) digunakan sebagai pembatas input dari keyboard

8. Notasi – (input keyboard) adalah representan input dari keyboard. Artinya menampilkan file 1, kemudian menampilkan input dari keyboard dan menampilkan file 2. Perhatikan bahwa notasi    “-“ berarti menyelipkan input dari keyboard
   ```
   $ cat myfile.txt – surat
   ```
    ![Per2(8)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/a8838f9a-fb16-4663-a2eb-9f8c7d6c3912)

   Analisa: Notasi – (input keyboard) adalah representan input dari keyboard. Artinya menampilkan file

### Percobaan 3 : Pipa (pipeline)

1. Operator pipa (|) digunakan untuk membuat eksekusi proses dengan melewati data langsung ke data lainnya
    ```
    $ who
    $ who | sort
    $ who | sort –r
    $ who > tmp
    $ sort tmp
    $ rm tmp
    $ ls –l /etc | more
    $ ls –l /etc | sort | more
    ```
      ![Per3(1)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/77046744-6df1-40fe-9076-804a75225547)

    Analisa: Operator pipa (|) digunakan untuk membuat eksekusi proses dengan melewati data langsung ke data lainnya

2. Untuk membelokkan standart output ke file, digunakan operator ">"
   ```
   $ echo hello
   $ echo hello > output
   $ cat output
   ```
    ![Per3(2)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/a96b6683-5603-4fd5-b794-e74cb3192d71)

   Analisa: Untuk membelokkan standart output ke file, digunakan operator >

3. Untuk menambahkan output ke file digunakan operator ">>"
   ```
   $ echo bye >> output
   $ cat output
   ```
    ![Per3(3)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/2d9d4ae2-c9e2-4333-821b-f30e95b734e4)

   Analisa: Untuk menambahkan output ke file digunakan operator >>

4. Untuk membelokkan standart input digunakan operator "<"
   ```
   $ cat < output
   ```
    ![Per3(4)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/83d9c738-1151-4aac-886c-4da375bae7fc)

   Analisa: Untuk membelokkan standart input digunakan operator <

5. Pembelokan standart input dan standart output dapat dikombinasikan tetapi tidak boleh menggunakan nama file yang sama sebagai standart input dan output
    ```
    $ cat < output > out
    $ cat out
    $ cat < output >> out
    $ cat out
    $ cat < output > output
    $ cat output
    $ cat < out >> out (Proses tidak berhenti)
    [Ctrl-c]
    $ cat out
    ```
      ![Per3(5)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/f9328770-f358-43c6-8dc9-ec34a735e557)

      Analisa: Pembelokan standart input dan standart output dapat dikombinasikan tetapi tidak boleh menggunakan nama file yang sama sebagai standart input dan output

### Percobaan 4 : Filter

1. Pipa juga digunakan untuk mengkombinasikan utilitas sistem untuk membentuk fungsi yang lebih kompleks\
     ```
     $ w –h | grep <user>
     $ grep <user> /etc/passwd
     $ ls /etc | wc
     $ ls /etc | wc –l
     $ cat > kelas1.txt
     Badu
     Zulkifli
     Yulizir
     Yudi
     Ade
     [Ctrl-d]
     $ cat > kelas2.txt
     Budi
     Gama
     Asep
     Muchlis
     [Ctrl-d]
     $ cat kelas1.txt kelas2.txt | sort
     $ cat kelas1.txt kelas2.txt > kelas.txt
     $ cat kelas.txt | sort | uniq
     ```
   ![perc4(1)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/d0921d6f-1ff0-40bf-af42-d1e43d73e7d9)
   ![perc4(2)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/7bbc2491-1c59-4f10-8eba-3c6fd0cb6e6f)

     Analisa: Pipa juga digunakan untuk mengkombinasikan utilitas sistem untuk membentuk fungsi yang lebih kompleks

# LATIHAN

1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru
    ![lat(1)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/8bee2452-6a30-42e0-973e-3561ce2c0eaa)

   Analisa: Untuk melihat daftar direktori aktif, gunakan perintah $ ls, sedangkan untuk membelokkan tampilan standard output ke file baru, gunakan ‘>’
2. Lihat daftar secara lengkap pada direktori /etc/passwd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya
    ![lat(2)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/579f6518-09f1-4ec7-9b98-ba81b37e3f0c)

   Analisa: Untuk melihat daftar lengkap dari direktori /etc/passwd, gunakan perntah $ ls, sedangkan untuk membelokkan tampilan standard output ke file baru tanpa menghapus file baru       sebelumnya, gunakan ‘>>’
3. Urutkan file baru dengan cara membelokkan standard input
    ![lat(3)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/b75ac377-07cf-47bd-8678-3630d86607dd)

   Analisa: Untuk mengurutkan file, gunakan perintah $ sort, sedangkan untuk membelokkan standard input, gunakan ‘<’
4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut
    ![lat(4)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/db58bf52-fc3b-4e35-b9cc-c0291744e650)

   Analisa: Untuk mengurutkan file, gunakan perintah $ sort, sedangkan untuk membelokkan standard input, gunakan ‘<’, sedangkan untuk membelokkan standard output ke file, gunakan ‘>’.      Pembelokan standart input dan standart output dapat dikombinasikan asalkan tidak boleh menggunakan nama file yang sama sebagai standart input dan output
5. Buatlah direktori latihan 2 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt
    ![lat(5)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/b485d99f-0435-48bd-8cdf-ff911f1b6c40)
    ![lat(6)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/9f147228-7419-43bf-a18d-9e6f6371e7a6)


    Analisa: Perintah $ mkdir untuk membuat direktori baru. Saat membuat direktori yang sama sebanyak dua kali, akan muncul pesan error. Pesan error itu kemudian dibelokkan ke file          dengan menggunakan ‘2>’
6. Urutkan kalimat berikut:
   ```
   Jakarta
   Bandung
   Surabaya
   Padang
   Palembang
   Lampung
   ```
  Dengan menggunakan notasi here document (<@@@ ...@@@) . HINT
    ![lat(7)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/60a770bb-01a2-4554-b305-a6e6a71e25c0)


  Analisa: Pertama, buat notasi here document yang akan dibelokkan ke sebuah file kemudian isi document tersebut. Setelah diisi dan diakhiri, isi dokumen akan tersimpan ke file yang       dibelokkan. File tersebut kemudian diurutkan menggunakan perintah $ sort.
  
7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru
    ![lat(8)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/751efe08-2e67-4e81-96cf-243eb056fa19)

   Analisa: Untuk mendapatkan jumlah baris, kata, dan karakter (secara berurutan) dari sebuah file, gunakan perintah wc yang dipipakan dengan perintah cat. Hasilnya kemudian bisa           ditambahkan ke file menggunakan ‘>>’
8. Gunakan perintah di bawah ini dan perhatikan hasilnya
   ```
   $ cat > hello.txt
   dog cat
   cat duck
   dog chicken
   chicken duck
   chicken cat
   dog duck
   [Ctrl-d]
   $ cat hello.txt | sort | uniq
   $ cat hello.txt | grep “dog” | grep –v “cat”
   ```
    ![lat(9)](https://github.com/febiana0/SysOP24-3123521013/assets/148712001/aafe530a-f381-4aef-9550-b9ea47d015a4)

   Analisa: Uniq digunakan untuk menghilangkan baris-baris berurutan yang mengalami duplikasi, Grep digunakan untuk menyaring masukannya dan menampilkan baris-baris yang hanya              mengandung pola yang ditentukan

# Kesimpulan
        
  Proses dalam Linux memerlukan input dan menghasilkan output. Instruksi yang diberikan melalui Shell disebut sebagai eksekusi program yang selanjutnya menjadi proses dengan nomor PID (Process Identity). Linux berkomunikasi dengan file melalui file descriptor yang direpresentasikan dengan angka, dimulai dari 0. Redirection digunakan untuk mengalihkan aliran standar input, output, dan error dengan mengubah file descriptor terkait (0, 1, dan 2). Pipeline adalah mekanisme pipa untuk komunikasi antar proses. Sedangkan filter adalah utilitas Linux yang dapat memproses standard input (dari keyboard) dan menampilkan hasilnya pada standard output (layar)
    



