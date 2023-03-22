# C PLUS PLUS 101 BY HIMATIKA

## Sejarah Function pada dunia Pemprograman dan penerapan pada C++?

Fungsi (function) merupakan suatu blok kode yang dapat dipanggil dari bagian lain dari program untuk melakukan tugas tertentu. Konsep fungsi sudah ada sejak awal pengembangan bahasa pemrograman, namun penggunaan yang lebih modern dan terstruktur diperkenalkan pada bahasa pemrograman Fortran pada tahun 1950-an.

Dalam bahasa pemrograman C++, fungsi digunakan untuk mengelompokkan sejumlah instruksi untuk memproses tugas tertentu. Fungsi memungkinkan programmer untuk memecah program menjadi bagian-bagian kecil yang dapat dipanggil dan dieksekusi secara terpisah, sehingga memudahkan dalam pembuatan, pengembangan, dan pemeliharaan program yang kompleks.

Berikut adalah contoh sederhana penggunaan fungsi dalam bahasa pemrograman C++:

```c
#include <iostream>
using namespace std;

int tambah(int x, int y) {
   int hasil = x + y;
   return hasil;
}

int main() {
   int a = 5, b = 3;
   int c = tambah(a, b);
   cout << "Hasil penjumlahan dari " << a << " dan " << b << " adalah " << c << endl;
   return 0;
}
```

Output dari program di atas akan menjadi:

```c
Hasil penjumlahan dari 5 dan 3 adalah 8
```

Seperti yang terlihat pada contoh di atas, fungsi tambah digunakan untuk menjumlahkan dua buah bilangan bulat, yaitu x dan y. Fungsi tersebut mengembalikan nilai hasil penjumlahan, yang kemudian disimpan ke dalam variabel c pada fungsi main.

Dalam bahasa pemrograman C++, fungsi juga dapat menerima argumen, mengembalikan nilai, dan memiliki sifat pemanggilan rekursif. Fungsi juga dapat didefinisikan dan dipanggil dari file yang berbeda untuk memungkinkan pengembangan program yang lebih terstruktur.

Fungsi merupakan konsep yang sangat penting dalam bahasa pemrograman C++ karena dapat membantu programmer dalam menulis program yang lebih efisien, mudah dipelihara, dan mudah diperluas.