# C PLUS PLUS 101 BY HIMATIKA

## Struct

Kita sering menghadapi situasi di mana kita perlu menyimpan sekelompok data, baik itu jenis data yang serupa atau tidak serupa. Kita telah melihat Array di C++ yang digunakan untuk menyimpan set data dari jenis data yang serupa pada lokasi memori yang berdekatan.

Berbeda dengan Array, struc di C++ adalah jenis data yang ditentukan oleh pengguna yang digunakan untuk menyimpan kelompok item dari jenis data yang tidak serupa.

### apa itu Struct

struc adalah jenis data yang ditentukan oleh pengguna dalam C/C++. struc membuat jenis data yang dapat digunakan untuk mengelompokkan item dengan jenis yang mungkin berbeda menjadi satu jenis data.

### Cara membuat Struct

kata kunci 'struct' berguna untuk membuat structure. Sintaks umum untuk membuat struc adalah sebagai berikut:

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

1. Data Member: Anggota-anggota ini adalah variabel C++ biasa. Kita dapat membuat struc dengan variabel-variabel dari jenis data yang berbeda-beda dalam C++.
2. Member Functions: Anggota-anggota ini adalah fungsi C++ biasa. Selain variabel, kita juga dapat menyertakan fungsi-fungsi di dalam deklarasi struc.

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

### cara mendaklarasi struct

A structure variable can either be declared with structure declaration or as a separate declaration like basic types.

variable struct bisa di deklarasi dengan 2 cara: deklarasi struct atau memisa deklarasi struct seperti tipe data dasar.

### Contoh

Pernyataan variabel dengan deklarasi struc.
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

Anggota struc tidak dapat diinisialisasi dengan deklarasi. Sebagai contoh, program C berikut gagal dalam kompilasi. Namun, dianggap benar dalam C++11 dan versi yang lebih baru.

```cpp
struct Point
{
   int x = 0;  // COMPILER ERROR:  tidak bisa menginisialisasi member disini
   int y = 0;  // COMPILER ERROR:  tidak bisa menginisialisasi member disini
};
```

Alasan untuk kesalahan di atas adalah sederhana, ketika suatu jenis data dideklarasikan, tidak ada memori yang dialokasikan untuknya. Memori dialokasikan hanya ketika variabel dibuat.

**Anggota struc dapat diinisialisasi dengan deklarasi di C++. Sebagai contoh, program C++ berikut berhasil dieksekusi tanpa melemparkan kesalahan apapun.**

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

## perbedaan struct dan class

Dalam C++, struc bekerja sama dengan class, kecuali hanya ada dua perbedaan kecil. Yang paling penting adalah penyembunyian detail implementasi. Secara default, struc tidak akan menyembunyikan detail implementasinya dari siapa pun yang menggunakannya dalam kode, sedangkan class secara default menyembunyikan semua detail implementasinya dan oleh karena itu secara default mencegah programmer mengaksesnya. Tabel berikut merangkum semua perbedaan mendasar.

| struct                                                                                 | class                                                                                    |
| -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| 1. anggota dari suatu class adalah private secara default/otomatis.                    | 1. anggota dari suatu struktur adalah public secara default/otomatis.                    |
| 2. isi dari suatu class adalah object.                                                 | 2. isi dari suatu struktur adalah ‘variabel struktur’.                                   |
| 3. anggota class atau struktur dari suatu class adalah private secara default/otomatis | 3. anggota class atau struktur dari suatu struktur adalah public secara default/otomatis |
| 4. dideklarasikan dengan keyword ‘class’                                               | 4. dideklarasikan dengan keyword ‘struct’                                                |
| 5. biasanya digunakan untuk abstraksi data dan inheritance/pewarisan lebih lanjut      | 5. biasanya digunakan untuk mengelompokkan data                                          |
| 6. bisa terdapat nilai NULL dalam class                                                | 6. tidak bisa terdapat nilai NULL                                                        |

bentuk class dan struct

```cpp
// struct
    struct structure_name{
          type structure_member1;
          type structure_member2;
    };
```

bentuk class

```cpp
    struct structure_name{
          type structure_member1;
          type structure_member2;
    };
```

beberapa contoh penggunaan struct dan class

1. member dari class private secara default, sedangkan member dari struct public secara default.

program 1:

```cpp
// program C++ untuk menunjukkan bahwa member dari class adalah private secara default
#include <iostream>

using namespace std;

class Test {
    // x is private
    int x;
};

int main()
{
    Test t;
    // compiler error karena x adalah private
    t.x = 20;

    return t.x;
}
```

Time Complexity: O(1)
Auxiliary Space: O(1)

Output:

./cf03c8d1-d4a3-43ea-a058-fe5b5303167b.cpp: In function 'int main()':
./cf03c8d1-d4a3-43ea-a058-fe5b5303167b.cpp:10:9: error: 'int Test::x' is private
int x;
^
./cf03c8d1-d4a3-43ea-a058-fe5b5303167b.cpp:18:7: error: within this context
t.x = 20;
^
./cf03c8d1-d4a3-43ea-a058-fe5b5303167b.cpp:10:9: error: 'int Test::x' is private
int x;
^
./cf03c8d1-d4a3-43ea-a058-fe5b5303167b.cpp:20:14: error: within this context
return t.x;
^

Program 2:

```cpp
// C++ program untuk menunjukkan bahwa member dari struktur adalah public secara default
#include <iostream>

using namespace std;

struct Test {
	// x adalah public
	int x;
};

int main()
{
	Test t;
	t.x = 20;

	// berjalan lancar karena x public
	cout << t.x;
}
```

output:
20

Time Complexity: O(1)
Auxiliary Space: O(1)

2. sebuah class dideklarasikan menggunakan kata kunci class, dan sebuah struktur dideklarasikan menggunakan kata kunci struct.

program 1:

```cpp
class ClassName {
private:
    member1;
    member2;

public:
    member3;
    .
    .
    memberN;
};
```

program 2:

```cpp
struct StructureName {
    member1;
    member2;
    .
    .
    .
    memberN;
};
```

3. sebuah class memiliki penurunun/inheritance, sedangkan sebuah struktur tidak memiliki penurunun/inheritance.

program 1:

```cpp
// C++ program untuk menunjukkan Inheritance dengan class.
#include <iostream>

using namespace std;

// Base class
class Parent {
public:
    int x;
};

// penurunan/inheritance dari class Parent
class Child : public Parent {
public:
    int y;
};

int main()
{
    Child obj1;

    // sebuah objek dari class Child memiliki semua data member dan fungsi member dari class Parent.
    obj1.y = 7;
    obj1.x = 91;
    cout << obj1.y << endl;
    cout << obj1.x << endl;

    return 0;
}
```

Output:
7
91

Time Complexity: O(1)
Auxiliary Space: O(1)

program 2:

```cpp

// C++ Program to demonstrate Inheritance with structures.
#include <iostream>

using namespace std;

struct Base {
public:
    int x;
};

// is equivalent to
// struct Derived : public Base {}
struct Derived : Base {
public:
    int y;
};

int main()
{
    Derived d;

    // Works fine because inheritance
    // is public.
    d.x = 20;
    cout << d.x;
    cin.get();
    return 0;
}
```

Output:
20

Time Complexity: O(1)
Auxiliary Space: O(1)
