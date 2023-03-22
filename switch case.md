# C PLUS PLUS 101 BY HIMATIKA

## Sejarah switch case pada dunia Pemprograman dan penerapan pada C++?

Switch case adalah konstruksi kontrol alur program dalam bahasa pemrograman yang memungkinkan untuk memilih satu dari beberapa blok kode untuk dieksekusi berdasarkan nilai suatu variabel. Konstruksi switch case pertama kali diperkenalkan dalam bahasa pemrograman Fortran pada tahun 1954, namun konstruksi tersebut lebih populer diimplementasikan dalam bahasa pemrograman C pada tahun 1970-an.

Dalam bahasa pemrograman C++, switch case digunakan untuk memilih salah satu dari beberapa blok kode untuk dieksekusi berdasarkan nilai suatu variabel. Konstruksi switch case ini memungkinkan programmer untuk menghindari penulisan kode yang berulang-ulang saat memeriksa nilai variabel yang sama berulang kali.

Berikut adalah contoh sederhana penggunaan switch case dalam bahasa pemrograman C++:

```c
#include <iostream>
using namespace std;

int main() {
   int num = 2;

   switch(num) {
      case 1:
         cout << "Angka adalah 1" << endl;
         break;
      case 2:
         cout << "Angka adalah 2" << endl;
         break;
      case 3:
         cout << "Angka adalah 3" << endl;
         break;
      default:
         cout << "Angka tidak ditemukan" << endl;
   }
   return 0;
}
```

Output dari program di atas akan menjadi:

```c
Angka adalah 2
```

Seperti yang terlihat pada contoh di atas, switch case digunakan untuk memilih salah satu blok kode untuk dieksekusi berdasarkan nilai variabel num. Jika num sama dengan 1, maka blok kode pada case 1 akan dieksekusi. Jika num sama dengan 2, maka blok kode pada case 2 akan dieksekusi. Jika num sama dengan 3, maka blok kode pada case 3 akan dieksekusi. Jika num tidak sama dengan semua kasus yang didefinisikan, maka blok kode pada default akan dieksekusi.

Switch case juga dapat digunakan untuk mengevaluasi variabel berupa karakter, bilangan riil, atau bahkan pointer. Namun, perlu diperhatikan bahwa setiap blok kode pada setiap kasus dalam switch case harus diakhiri dengan perintah break, sehingga program tidak akan mengeksekusi blok kode pada kasus selanjutnya secara otomatis.