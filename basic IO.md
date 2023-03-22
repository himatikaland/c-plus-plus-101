# C PLUS PLUS 101 BY HIMATIKA

## Sejarah Basic I/O

Basic I/O (Input/Output) atau masukan/keluaran dasar merupakan teknologi yang sudah ada sejak awal perkembangan komputer. Pada awalnya, komputer hanya digunakan untuk mengolah data dan tidak memiliki kemampuan untuk berinteraksi dengan lingkungan luar.

Namun, seiring perkembangan teknologi, komputer mulai dilengkapi dengan berbagai perangkat masukan dan keluaran. Perangkat masukan yang pertama kali digunakan adalah kartu punch, yaitu kartu berlubang yang dapat diisi dengan data oleh pengguna. Data tersebut kemudian dapat dimasukkan ke dalam komputer melalui mesin pembaca kartu.

Selain kartu punch, teknologi masukan lain yang dikembangkan adalah keyboard dan mouse. Keyboard digunakan untuk memasukkan data ke dalam komputer, sementara mouse digunakan untuk mengontrol pergerakan kursor pada layar monitor.

Sedangkan untuk teknologi keluaran, pada awalnya komputer hanya dapat menampilkan output dalam bentuk tulisan pada kertas melalui printer. Namun, dengan berkembangnya teknologi, komputer dapat menampilkan output dalam bentuk gambar dan suara melalui monitor dan speaker.

Pengembangan teknologi I/O terus berlanjut hingga saat ini, dengan adanya teknologi seperti touchscreen, scanner, webcam, dan perangkat lainnya yang dapat memudahkan interaksi antara pengguna dan komputer.

## Apa itu Basic I/O pada C++?

Dalam bahasa pemrograman C++, terdapat beberapa cara untuk melakukan input dan output data. Beberapa cara yang umum digunakan adalah sebagai berikut:

Input dan Output Console
Untuk melakukan input dan output data pada console atau layar komputer, kita dapat menggunakan perintah cin dan cout. Contohnya sebagai berikut:
```cpp
#include <iostream>
using namespace std;

int main() {
   int angka;
   cout << "Masukkan sebuah angka: ";
   cin >> angka;
   cout << "Angka yang Anda masukkan adalah: " << angka;
   return 0;
}
```

Pada contoh di atas, kita menggunakan perintah cout untuk menampilkan pesan pada layar dan cin untuk membaca input dari pengguna.

Input dan Output Berkas
Selain melakukan input dan output pada console, kita juga dapat melakukan input dan output pada berkas atau file. Untuk melakukan hal ini, kita dapat menggunakan fstream dan ifstream untuk membaca berkas dan ofstream untuk menulis berkas. Contohnya sebagai berikut:
```cpp
#include <fstream>
#include <iostream>
using namespace std;

int main() {
   string data;
   ofstream fileOutput("data.txt");
   cout << "Masukkan data yang ingin disimpan: ";
   getline(cin, data);
   fileOutput << data;
   fileOutput.close();
   ifstream fileInput("data.txt");
   getline(fileInput, data);
   cout << "Data yang disimpan dalam berkas: " << data;
   fileInput.close();
   return 0;
}
```

Pada contoh di atas, kita menggunakan perintah ofstream untuk membuat berkas dan menuliskan data ke dalamnya, dan perintah ifstream untuk membaca data dari berkas.