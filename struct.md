# C PLUS PLUS 101 BY HIMATIKA

## Struct

Kita sering menghadapi situasi di mana kita perlu menyimpan sekelompok data, baik itu jenis data yang serupa atau tidak serupa. Kita telah melihat Array di C++ yang digunakan untuk menyimpan set data dari jenis data yang serupa pada lokasi memori yang berdekatan.

Berbeda dengan Array, Struktur di C++ adalah jenis data yang ditentukan oleh pengguna yang digunakan untuk menyimpan kelompok item dari jenis data yang tidak serupa.

## apa itu Struct

Struktur adalah jenis data yang ditentukan oleh pengguna dalam C/C++. Struktur membuat jenis data yang dapat digunakan untuk mengelompokkan item dengan jenis yang mungkin berbeda menjadi satu jenis data.

## Cara membuat Struct

kata kunci 'struct' berguna untuk membuat structure. Sintaks umum untuk membuat struktur adalah sebagai berikut:

```cpp
struct structureName{
    member1;
    member2;
    member3;
    .
    .
    .
    memberN;
};
```

struct didalam C++ dapat berisi dua jenis anggota:

1. Data Member: Anggota-anggota ini adalah variabel C++ biasa. Kita dapat membuat struktur dengan variabel-variabel dari jenis data yang berbeda-beda dalam C++.
2. Member Functions: Anggota-anggota ini adalah fungsi C++ biasa. Selain variabel, kita juga dapat menyertakan fungsi-fungsi di dalam deklarasi struktur.

### Contoh

```cpp
// Data Members
int roll;
int age;
int marks;

// Member Functions
void printDetails()
{
    cout<<"Roll = "<<roll<<"\n";
    cout<<"Age = "<<age<<"\n";
    cout<<"Marks = "<<marks;
}
```

struct diatas terdapat 3 buah integer yang digunakan untuk menyimpan data dari mahasiswa (angka roll, angka umur dan angka nilai) dan juga terdapat fungsi untuk menampilkan data tersebut.

## cara mendaklarasi struct

A structure variable can either be declared with structure declaration or as a separate declaration like basic types.

variable struct bisa di deklarasi dengan 2 cara: deklarasi struct atau memisa deklarasi struct seperti tipe data dasar.

### Contoh

Pernyataan variabel dengan deklarasi struktur.
Variabel p1 dideklarasikan dengan 'Point'.

```cpp
struct Point
{
   int x, y;
} p1;
```

Pernyataan variabel seperti tipe data dasar.
Variabel p1 dideklarasikan seperti variabel biasa.

```cpp
struct Point
{
   int x, y;
};

int main()
{
   struct Point p1;
}
```

### cara menginisisasi member struct

Anggota struktur tidak dapat diinisialisasi dengan deklarasi. Sebagai contoh, program C berikut gagal dalam kompilasi. Namun, dianggap benar dalam C++11 dan versi yang lebih baru.

```cpp
struct Point
{
   int x = 0;  // COMPILER ERROR:  tidak bisa menginisialisasi member disini
   int y = 0;  // COMPILER ERROR:  tidak bisa menginisialisasi member disini
};
```

Alasan untuk kesalahan di atas adalah sederhana, ketika suatu jenis data dideklarasikan, tidak ada memori yang dialokasikan untuknya. Memori dialokasikan hanya ketika variabel dibuat.

**Anggota struktur dapat diinisialisasi dengan deklarasi di C++. Sebagai contoh, program C++ berikut berhasil dieksekusi tanpa melemparkan kesalahan apapun.**

```cpp
// didalam C++ kita bisa menginisialisasi variabel dengan deklarasi di struct.
#include <iostream>
using namespace std;

struct Point {
    int x = 0; // ini disebut default argument dan tidak akan menimbulkan error
    int y = 1;
};

int main()
{
    struct Point p1;

    // akses member dari point p1
    // tidak ada nilai yang di inisialisasi maka nilai default akan di gunakan. yaitu x=0 dan y=1;
    cout << "x = " << p1.x << ", y = " << p1.y<<endl;

    // menginisialisasi nilai y = 20;
    p1.y = 20;
    cout << "x = " << p1.x << ", y = " << p1.y;
    return 0;
```

output:
x=0, y=1
x=0, y=20

struct member bisa di inisialisasi dengan menggunakan curly braces ‘{}’. Sebagai contoh, berikut adalah inisialisasi yang valid.

```cpp
struct Point {
    int x, y;
};

int main()
{
    // inisialisasi yang valid. member x mendapatkan nilai 0 dan y mendapatkan nilai 1. Urutan deklarasi diikuti.
    struct Point p1 = { 0, 1 };
}
```

### cara mengakses struct element

Structure members diakses dengan operator titik (.) seperti variabel biasa.

```cpp
#include <iostream>
using namespace std;

struct Point {
    int x, y;
};

int main()
{
    struct Point p1 = { 0, 1 };

    // mengakses member dari point p1
    p1.x = 20;
    cout << "x = " << p1.x << ", y = " << p1.y;

    return 0;
}
```

output:
x = 20, y = 1

### apa itu array struct?

seperti tipe data dasar lainnya, kita bisa membuat array dari struct.

```cpp

#include <iostream>
using namespace std;

struct Point {
    int x, y;
};

int main()
{
    // membuat array dari struct
    struct Point arr[10];

    // mengakses member dari array
    arr[0].x = 10;
    arr[0].y = 20;

    cout << arr[0].x << " " << arr[0].y;
    return 0;
}
```

output:
10 20

### apa itu struct pointer?

seperti tipe data dasar lainnya, kita bisa membuat pointer dari struct. jika kita membuat pointer dari struct, kita bisa mengakses member dari struct dengan menggunakan operator arrow (->) bukan dengan menggunakan operator titik (.)

```cpp
#include <iostream>
using namespace std;

struct Point {
    int x, y;
};

int main()
{
    struct Point p1 = { 1, 2 };

    // p2 adalah pointer ke struct p1
    struct Point* p2 = &p1;

    // mengakses member dari struct p1 dengan menggunakan pointer p2/pointer struct
    cout << p2->x << " " << p2->y;
    return 0;
}
```

output:
1 2
