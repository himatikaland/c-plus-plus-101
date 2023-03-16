# C PLUS PLUS 101 BY HIMATIKA

## Sejarah String

Konsep String pertama kali ditemukan pada tahun 1960-an ketika bahasa pemrograman komputer FORTRAN pertama kali dikembangkan. Pada waktu itu, string digunakan untuk merepresentasikan teks dalam bahasa pemrograman.

Kemudian, pada tahun 1970-an, ketika bahasa pemrograman C pertama kali dikembangkan, string juga menjadi fitur yang sangat penting dalam bahasa tersebut. Pada waktu itu, string direpresentasikan sebagai array karakter dan diakhiri dengan karakter null (nul atau '\0'). Bahasa pemrograman C juga menyediakan sejumlah fungsi bawaan untuk memanipulasi string, seperti strcpy() dan strcat().

Pada tahun 1980-an, bahasa pemrograman C++ memperkenalkan konsep objek yang memungkinkan string digunakan dalam konteks yang lebih kompleks, seperti dalam pembuatan kelas dan struktur data yang lebih kompleks. C++ juga menyediakan tipe data string yang lebih baik, dengan dukungan untuk operasi string yang lebih lengkap.

Pada saat ini, string tetap menjadi salah satu fitur kunci dalam bahasa pemrograman komputer modern, dan terus berkembang dengan dukungan yang lebih baik untuk operasi string dan karakter. Banyak bahasa pemrograman modern, seperti Python dan JavaScript, juga memiliki dukungan yang kuat untuk string dan menawarkan banyak fitur dan fungsi untuk memanipulasi string dengan mudah.

## Apa itu String pada C++?

String pada C++ adalah tipe data yang digunakan untuk merepresentasikan teks atau karakter dalam sebuah program. String pada C++ sebenarnya adalah kumpulan karakter atau array karakter yang diletakkan dalam satu variabel.

Dalam bahasa C++, string didefinisikan dengan tipe data string yang didefinisikan di dalam library string. Anda harus menyertakan library ini di dalam program Anda jika ingin menggunakan tipe data string. Sebagai contoh, untuk menggunakan tipe data string, Anda bisa menuliskan kode seperti ini di awal program:

```C++
#include <string>
using namespace std;
```

Setelah library string dimuat, Anda dapat membuat variabel string dengan cara yang sama seperti variabel biasa. Sebagai contoh, kode berikut akan membuat variabel string bernama nama dan mengisinya dengan teks "John Doe":

```C++
string nama = "John Doe";
```

Anda dapat melakukan banyak operasi pada variabel string, seperti menambahkan teks atau karakter, mengubah atau menghapus karakter, mencari posisi karakter tertentu, dan sebagainya. Beberapa contoh operasi pada string adalah sebagai berikut:

```C++
string s1 = "Hello";
string s2 = "World";
string s3 = s1 + " " + s2; // menggabungkan dua string
int len = s3.length(); // mengambil panjang string
char c = s3[0]; // mengambil karakter pertama pada string
s3[0] = 'h'; // mengubah karakter pertama pada string
```

Dalam contoh di atas, kita menggabungkan dua string s1 dan s2 menjadi satu string s3 menggunakan operator +. Kemudian, kita mengambil panjang string dengan menggunakan fungsi length(), mengambil karakter pertama dengan menggunakan operator [], dan mengubah karakter pertama menjadi huruf kecil. Ada banyak fungsi dan operator lain yang tersedia untuk operasi pada string pada C++.
