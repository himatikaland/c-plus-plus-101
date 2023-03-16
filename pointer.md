# C PLUS PLUS 101 BY HIMATIKA

## Sejarah Pointer

Konsep pointer pertama kali muncul pada tahun 1960-an, ketika bahasa pemrograman komputer ALGOL 60 dikembangkan. Pada waktu itu, pointer digunakan untuk merepresentasikan alamat memori dan memberikan akses langsung ke data yang disimpan di dalamnya.

Kemudian, pada tahun 1970-an, ketika bahasa pemrograman C pertama kali dikembangkan, pointer menjadi salah satu fitur kunci dalam bahasa tersebut. Bahasa pemrograman C menyediakan dukungan yang kuat untuk pointer, dan penggunaannya sangat penting dalam pemrograman tingkat rendah, seperti pengembangan driver perangkat keras dan sistem operasi.

Pada saat itu, pointer direpresentasikan sebagai variabel yang menyimpan alamat memori, dan operator & digunakan untuk mengambil alamat variabel, sedangkan operator \* digunakan untuk mengambil nilai di alamat memori yang ditunjuk oleh pointer.

Pada tahun 1980-an, bahasa pemrograman C++ memperkenalkan konsep objek yang memungkinkan pointer digunakan dalam konteks yang lebih kompleks, seperti dalam pembuatan kelas dan struktur data yang lebih kompleks.

Pada saat ini, pointer masih menjadi fitur penting dalam bahasa pemrograman komputer modern, dan terus digunakan dalam pengembangan software dan aplikasi. Beberapa bahasa pemrograman modern, seperti Rust dan Go, juga memiliki dukungan yang kuat untuk pointer, meskipun dengan pendekatan dan sintaks yang berbeda dari bahasa pemrograman C dan C++.

## Apa itu Pointer pada C++?

Pointer pada C++ adalah variabel yang berisi alamat memori dari variabel lain, atau dari suatu lokasi memori. Pointer memungkinkan program untuk mengakses dan memanipulasi nilai variabel secara langsung melalui alamat memori, sehingga memungkinkan pemrogram untuk membuat program yang lebih efisien dan fleksibel.

Dalam C++, pointer direpresentasikan oleh tanda asterisk () yang ditempatkan sebelum nama variabel. Untuk mendapatkan alamat memori suatu variabel, operator & digunakan, sedangkan untuk mengakses nilai yang disimpan di alamat memori yang ditunjuk oleh pointer, operator dereferencing () digunakan.

Berikut adalah contoh sederhana untuk mendeklarasikan, mengisi nilai, dan mengakses nilai dari suatu pointer pada C++:

```C++
#include <iostream>
using namespace std;

int main() {
    int angka = 5;
    int* p = &angka;

    cout << "Alamat variabel angka: " << &angka << endl;
    cout << "Nilai variabel angka: " << angka << endl;
    cout << "Alamat dari pointer p: " << p << endl;
    cout << "Nilai yang ditunjuk oleh pointer p: " << *p << endl;

    *p = 10;

    cout << "Nilai variabel angka setelah diubah melalui pointer: " << angka << endl;

    return 0;
}
```

Output dari program tersebut adalah:

```yaml
Alamat variabel angka: 0x7ffeec7ba43c
Nilai variabel angka: 5
Alamat dari pointer p: 0x7ffeec7ba43c
Nilai yang ditunjuk oleh pointer p: 5
Nilai variabel angka setelah diubah melalui pointer: 10
```

Pada contoh di atas, variabel "angka" dideklarasikan dengan nilai awal 5. Kemudian, sebuah pointer "p" dideklarasikan dengan mengambil alamat memori dari variabel "angka". Kemudian, alamat memori dari variabel "angka", alamat dari pointer "p", nilai yang ditunjuk oleh pointer "p", dan nilai variabel "angka" setelah diubah melalui pointer, ditampilkan di layar menggunakan perintah cout.
