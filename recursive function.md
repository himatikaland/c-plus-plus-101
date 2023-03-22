# C PLUS PLUS 101 BY HIMATIKA

## Recursive function pada C++?

Fungsi rekursif (recursive function) adalah fungsi yang memanggil dirinya sendiri secara berulang untuk menyelesaikan tugas yang lebih kompleks. Fungsi rekursif biasanya digunakan untuk menyelesaikan masalah yang dapat dipecahkan dalam bentuk masalah yang lebih kecil yang serupa.

Dalam bahasa pemrograman C++, fungsi rekursif dapat ditulis seperti fungsi biasa dengan pengecualian bahwa dalam blok fungsi, fungsi itu sendiri dipanggil untuk menyelesaikan masalah yang lebih kecil. Fungsi rekursif harus memiliki kondisi dasar atau kondisi terminasi (base case) yang akan menghentikan rekursi dan mengembalikan nilai.

Berikut adalah contoh sederhana fungsi rekursif untuk menghitung faktorial dalam bahasa pemrograman C++:

```c
#include <iostream>
using namespace std;

int faktorial(int n) {
   if (n == 1) { // kondisi terminasi
      return 1;
   } else {
      return n * faktorial(n-1); // panggil diri sendiri dengan argumen yang lebih kecil
   }
}

int main() {
   int n = 5;
   int hasil = faktorial(n);
   cout << "Faktorial dari " << n << " adalah " << hasil << endl;
   return 0;
}
```

Output dari program di atas akan menjadi:

```c
Faktorial dari 5 adalah 120
```

Pada contoh di atas, fungsi faktorial dipanggil dengan argumen 5. Fungsi tersebut mengecek apakah argumen sama dengan 1 (kondisi terminasi), jika iya, maka fungsi akan mengembalikan nilai 1. Jika tidak, maka fungsi akan memanggil dirinya sendiri dengan argumen yang lebih kecil (n-1) dan mengalikan dengan nilai n. Proses ini akan terus berulang sampai kondisi terminasi terpenuhi.

Fungsi rekursif dapat sangat berguna dalam menyelesaikan masalah yang kompleks dengan cara yang elegan dan mudah dipahami. Namun, karena fungsi rekursif memanggil dirinya sendiri secara berulang, dapat terjadi masalah kecepatan dan penggunaan memori yang berlebihan jika tidak diimplementasikan dengan benar. Oleh karena itu, penggunaan fungsi rekursif harus dipertimbangkan dengan matang dan hati-hati.