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

  **Analisa:** 1> merupakan salah satu metode pembelokan pengganti standar output. Alternatifnya yaitu dengan menggunakan >

  2. Pembelokan standar input, yaitu input dibelokkan dari keyboard menjadi dari file
      ```
      $ cat 0< myfile.txt
      $ cat myfile.txt 
      ```

  **Analisa:** 0< merupakan salah satu metode pembelokan standar input, yaitu input dibelokkan dari keyboard menjadi dari file. Alternatifnya yaitu dengan menggunakan <

  3. Pembelokan standar error untuk disimpan di file
       ```
       $ mkdir mydir (Terdapat pesan error)
       $ mkdir mydir 2> myerror.txt
       $ cat myerror.txt
       ```

      Analisa: 2> merupakan metode pembelokan standar error untuk kemudian disimpan di file

  4. Notasi 2>&1 : pembelokan standar error (2>) adalah identik dengan file descriptor 1
     ```
     $ ls filebaru (Terdapat pesan error)
     $ ls filebaru 2> out.txt
     $ cat out.txt
     $ ls filebaru 2> out.txt 2>&
     $ cat out.txt
     ```

     Analisa: Notasi 2>&1 pembelokan standar error (2>) adalah identik dengan file descriptor 1

5. Notasi 1>&2 (atau >&2) : pembelokan standar output adalah sama dengan file descriptor 2 yaitu standar error
   ```
   $ echo “mencoba menulis file” 1> baru
   $ cat filebaru 2> baru 1>&
   $ cat baru
   ```

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

   Analisa:

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

  Analisa:

8. Notasi – (input keyboard) adalah representan input dari keyboard. Artinya menampilkan file 1, kemudian menampilkan input dari keyboard dan menampilkan file 2. Perhatikan bahwa notasi    “-“ berarti menyelipkan input dari keyboard
   ```
   $ cat myfile.txt – surat
   ```

   Analisa:

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

    Analisa:

2. Untuk membelokkan standart output ke file, digunakan operator ">"
   ```
   $ echo hello
   $ echo hello > output
   $ cat output
   ```

   Analisa:

3. Untuk menambahkan output ke file digunakan operator ">>"
   ```
   $ echo bye >> output
   $ cat output
   ```

   Analisa:

4. Untuk membelokkan standart input digunakan operator "<"
   ```
   $ cat < output
   ```

   Analisa:

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

    Analisa:

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

     Analisa:

# LATIHAN

1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru

   Analisa: 
2. Lihat daftar secara lengkap pada direktori /etc/passwd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya

   Analisa: 
3. Urutkan file baru dengan cara membelokkan standard input

   Analisa: 
4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut

   Analisa: 
5. Buatlah direktori latihan 2 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt

    Analisa: 
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


  Analisa: 
  
7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru

   Analisa: 
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

   Analisa:

# Kesimpulan
        

    



