# C PLUS PLUS 101 BY HIMATIKA

## Apa itu C++?

Halo! C++ adalah sebuah bahasa pemrograman yang digunakan untuk membuat program komputer. Dalam bahasa ini, kita menulis kode yang memberi tahu komputer apa yang harus dilakukan.

Contohnya, bayangkan jika kamu ingin membuat program yang menghitung luas segitiga. Kamu bisa menulis kode C++ yang memberi tahu komputer cara menghitung luas segitiga, dan kemudian programmu bisa menampilkan hasilnya.

Contohnya seperti ini:

```C++
#include <iostream>
using namespace std;

int main() {
   float alas, tinggi, luas;
   cout << "Masukkan alas segitiga: ";
   cin >> alas;
   cout << "Masukkan tinggi segitiga: ";
   cin >> tinggi;
   luas = (alas * tinggi) / 2;
   cout << "Luas segitiga adalah: " << luas << endl;
   return 0;
}
```

Jadi, C++ adalah sebuah bahasa pemrograman yang digunakan untuk membuat program komputer, dan kita menulis kode C++ untuk memberi tahu komputer apa yang harus dilakukan. Semoga penjelasan ini dapat membantumu memahami C++ dengan lebih mudah!

## Apa yang akan kamu pelajari?

- [C PLUS PLUS 101 BY HIMATIKA](#c-plus-plus-101-by-himatika)
  - [Apa itu C++?](#apa-itu-c)
  - [Apa yang akan kamu pelajari?](#apa-yang-akan-kamu-pelajari)
  - [sejarah C++](#sejarah-c)
  - [cara menginstal C++](#cara-menginstal-c)
    - [common error dalam penginstalan](#common-error-dalam-penginstalan)
  - [cara menggunakan C++](#cara-menggunakan-c)

## sejarah C++

C++ adalah bahasa pemrograman yang dikembangkan oleh seorang ahli komputer bernama Bjarne Stroustrup pada tahun 1980-an. Dia ingin membuat bahasa pemrograman yang lebih kuat dan fleksibel daripada bahasa pemrograman lain yang ada pada saat itu.

Bjarne Stroustrup terinspirasi oleh bahasa pemrograman C, yang digunakan oleh banyak ahli komputer pada saat itu. Ia menambahkan fitur-fitur baru ke dalam bahasa C sehingga menjadi bahasa pemrograman yang lebih kuat dan fleksibel, dan kemudian ia menyebutnya "C++".

C++ terus berkembang dan menjadi salah satu bahasa pemrograman paling populer di dunia. Bahasa pemrograman ini digunakan oleh banyak perusahaan dan ahli komputer untuk membuat program komputer yang kompleks dan berukuran besar, seperti game, aplikasi desktop, dan sistem operasi.

Jadi, C++ adalah bahasa pemrograman yang dikembangkan oleh Bjarne Stroustrup pada tahun 1980-an. Ia menambahkan fitur-fitur baru ke dalam bahasa C sehingga menjadi bahasa pemrograman yang lebih kuat dan fleksibel, dan kemudian ia menyebutnya "C++". C++ terus berkembang dan menjadi salah satu bahasa pemrograman paling populer di dunia.

## cara menginstal C++

kalian bisa menginstal C++ di windows dengan cara berikut:
untuk mac dan linux tidak perlu saya jelaskan karena sudah ada di sistemnya.

1. install dari berikut [link](https://www.msys2.org/)
2. kalian install hingga selesai
3. ketika install selesai buka terminal `MSYS2 MSYS` dan ketikkan `pacman -Syu` untuk update packagenya
4. lalu pencet y untuk agree dan tunggu sampai selesai
5. sekarang ketik `pacman -Su` (kemungkinan kalian akan menulis `pacman -Sy` terlebih dahulu)
6. lalu pencet y untuk agree dan tunggu sampai selesai
7. sekarang kita install G++ dan G++ compiler dengan memilih terminal `MSYS2 MinGW win64` lalu masukan line berikut `pacman -S mingw-w64-x86_64-gcc` dan jika sistem kalian 32bit pilih x86 dan masukan line berikut `pacman -S mingw-w64-i686-gcc`

### common error dalam penginstalan

1. cek apakah kalian sudah menginstall `MSYS2` atau belum
2. cek environment variable kalian, apakah sudah sesuai dengan yang diinginkan atau belum
3. jika masih belum bisa, coba install ulang `MSYS2` dan ikuti langkah-langkahnya dengan teliti
4. jika masih terdapat error, silahkan tanya di discord

## cara menggunakan C++

kalian bisa menggunakan compiler online seperti berikut:

- [online gdb](https://www.onlinegdb.com/online_c++_compiler)
- [replit](https://replit.com/)
- [programiz](https://www.programiz.com/cpp-programming/online-compiler/)

dan jika kalian ingin menggunakan offline, kalian bisa menggunakan berikut

- [vscode](https://code.visualstudio.com/)
- [dev-c](https://sourceforge.net/projects/orwelldevcpp/)
- [jetbrains](https://www.jetbrains.com/clion/) tapi khusus ini, kalian harus apply terlebih dahulu untuk github student agar bisa mendapatkan lisensi gratis
