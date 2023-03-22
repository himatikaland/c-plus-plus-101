# C PLUS PLUS 101 BY HIMATIKA

## Sejarah Condition pada dunia Pemprograman?

Dalam dunia pemrograman, istilah "condition" (kondisi) mengacu pada ekspresi boolean yang dievaluasi sebagai true atau false, yang digunakan untuk memilih jalur eksekusi yang berbeda dalam program. Konsep condition telah ada sejak lama dalam dunia pemrograman, terutama sejak pengembangan bahasa pemrograman tingkat tinggi.

Salah satu bahasa pemrograman pertama yang memperkenalkan konsep condition adalah FORTRAN (Formula Translation) yang dikembangkan oleh IBM pada tahun 1954. Bahasa pemrograman tersebut memperkenalkan pernyataan IF yang digunakan untuk menguji suatu kondisi dan menjalankan blok kode tertentu jika kondisi tersebut benar.

Pada tahun 1960-an, bahasa pemrograman ALGOL (Algorithmic Language) muncul dengan menambahkan struktur kontrol FLOR (Flowchart Oriented Language) yang mendukung pemrosesan kondisi dan pengambilan keputusan. Pada saat yang sama, bahasa pemrograman COBOL (Common Business Oriented Language) muncul dengan kemampuan untuk memproses kondisi dan logika bisnis.

Pada tahun 1970-an, bahasa pemrograman seperti Pascal, C, dan BASIC memperkenalkan konsep conditional statement seperti if-then-else dan switch-case statement. Bahasa pemrograman C menjadi populer karena kemampuannya yang kuat dalam mengelola kondisi dan pengambilan keputusan.

Seiring perkembangan teknologi dan bahasa pemrograman baru yang muncul, konsep condition semakin berkembang dan semakin kompleks. Saat ini, bahasa pemrograman modern seperti Java, Python, dan JavaScript telah mengembangkan banyak fitur baru dalam pemrosesan kondisi, seperti operator ternary, operator logika, dan conditional expression yang lebih fleksibel dan kuat.

## Condition pada Pemprograman C++?

Dalam bahasa pemrograman C++, kondisi (condition) dapat diterapkan dengan menggunakan statement if-else dan switch-case.

Statement if-else
Statement if-else digunakan untuk memilih satu dari dua blok kode yang akan dieksekusi, tergantung pada apakah kondisi yang ditentukan benar atau salah.

Contoh:

```c
int x = 10;
if (x < 20) {
   cout << "Nilai x kurang dari 20" << endl;
} else {
   cout << "Nilai x lebih besar atau sama dengan 20" << endl;
}
```c
Penjelasan: Jika nilai variabel x kurang dari 20, maka blok kode pada if akan dijalankan. Jika tidak, maka blok kode pada else akan dijalankan.

Statement switch-case
Statement switch-case juga digunakan untuk memilih satu dari beberapa blok kode yang akan dieksekusi, tergantung pada nilai suatu variabel.

Contoh:

```c
char grade = 'B';
switch (grade) {
   case 'A':
      cout << "Excellent!" << endl;
      break;
   case 'B':
   case 'C':
      cout << "Good job!" << endl;
      break;
   case 'D':
      cout << "You passed!" << endl;
      break;
   case 'F':
      cout << "Better try again" << endl;
      break;
   default:
      cout << "Invalid grade" << endl;
}
```
Penjelasan: Variabel grade akan dievaluasi terhadap setiap kasus pada switch-case. Jika nilai grade sama dengan A, maka blok kode pada case A akan dijalankan. Jika nilai grade sama dengan B atau C, maka blok kode pada case B dan C akan dijalankan. Jika nilai grade sama dengan D, maka blok kode pada case D akan dijalankan. Jika nilai grade sama dengan F, maka blok kode pada case F akan dijalankan. Jika nilai grade tidak sesuai dengan semua kasus di atas, maka blok kode pada default akan dijalankan.

Perlu diingat bahwa dalam statement switch-case, setiap kasus harus diakhiri dengan break, agar tidak menjalankan blok kode pada kasus selanjutnya secara otomatis. Selain itu, statement default adalah opsional dan hanya akan dijalankan jika variabel tidak cocok dengan semua kasus yang didefinisikan.