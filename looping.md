# C PLUS PLUS 101 BY HIMATIKA

## Sejarah Looping

Looping atau perulangan merupakan konsep dasar dalam pemrograman yang memungkinkan untuk mengeksekusi serangkaian perintah secara berulang-ulang sampai suatu kondisi tertentu terpenuhi atau hingga batas perulangan tertentu tercapai. Konsep ini telah ditemukan sejak awal perkembangan pemrograman.

Salah satu bahasa pemrograman yang pertama kali mengimplementasikan konsep looping adalah Fortran, yaitu bahasa pemrograman yang dikembangkan pada tahun 1950-an. Pada saat itu, looping hanya dapat dilakukan dengan menggunakan perintah GOTO yang diarahkan ke label tertentu. Pada perkembangan selanjutnya, bahasa pemrograman lain seperti BASIC, C, dan Pascal juga mengadopsi konsep looping dari Fortran.

Pada tahun 1960-an, bahasa pemrograman Algol 60 memperkenalkan perintah perulangan do-while dan for, yang menjadi dasar dari konsep looping pada bahasa pemrograman modern saat ini. Kemudian, pada tahun 1970-an, bahasa pemrograman C mengimplementasikan perulangan while, do-while, dan for yang hingga kini masih banyak digunakan dalam pemrograman.

Dalam perkembangan selanjutnya, bahasa pemrograman seperti Java, Python, dan Ruby juga mengadopsi konsep looping dari bahasa pemrograman sebelumnya dan menambahkan fitur-fitur baru seperti perulangan foreach dan iterator. Konsep looping juga diterapkan dalam paradigma pemrograman fungsional seperti pada bahasa pemrograman Haskell dan Scala.

Dengan berkembangnya teknologi dan kebutuhan pemrograman yang semakin kompleks, konsep looping terus berkembang dan diterapkan pada berbagai jenis bahasa pemrograman dan aplikasi.

## Apa itu Looping pada C++?

Looping pada C++ adalah cara untuk melakukan pengulangan terhadap suatu kode program secara berulang-ulang sesuai dengan kondisi yang telah ditentukan. Terdapat dua jenis looping pada C++, yaitu:

For Loop
For Loop digunakan untuk melakukan pengulangan sebanyak jumlah tertentu yang sudah ditentukan sebelumnya.
Contoh penggunaan For Loop pada C++:
```cpp
for (int i = 0; i < 10; i++) {
    cout << i << endl;
}
```
Penjelasan: Loop akan berjalan dari 0 hingga 9, karena batas atasnya adalah 10 dan menggunakan operator < artinya loop berjalan selama nilai i kurang dari 10. Setiap kali loop berjalan, nilai i akan bertambah 1.

While Loop
While Loop digunakan untuk melakukan pengulangan selama kondisi yang ditentukan masih terpenuhi.
Contoh penggunaan While Loop pada C++:

```cpp
int i = 0;
while (i < 10) {
    cout << i << endl;
    i++;
}
```
Penjelasan: Loop akan berjalan selama nilai i kurang dari 10. Setiap kali loop berjalan, nilai i akan bertambah 1. Perbedaan dengan For Loop adalah kita harus menginisialisasi nilai i terlebih dahulu sebelum menggunakan While Loop.