# C PLUS PLUS 101 BY HIMATIKA

## class

object oriented programming - Seperti namanya, menggunakan objek dalam pemrograman. object oriented programming bertujuan untuk menerapkan entitas dunia nyata seperti warisan, penyembunyian, polimorfisme, dan sebagainya dalam pemrograman. Tujuan utama dari OOP adalah mengikat bersama data dan fungsi yang beroperasi pada data tersebut sehingga bagian lain dari kode tidak dapat mengakses data ini kecuali fungsi itu sendiri.

ada beberapa konsep dasar yang berfungsi sebagai blok pembangun OOPs yaitu:

1. Class
2. Objects
3. Encapsulation
4. Abstraction
5. Polymorphism
6. Inheritance
7. Dynamic Binding
8. Message Passing

## apa itu class

Blok bangunan C++ yang mengarah ke object oriented programming adalah class. class adalah jenis data yang ditentukan oleh pengguna, yang memiliki anggota data dan anggota fungsi sendiri, yang dapat diakses dan digunakan dengan membuat instance dari class tersebut. class seperti sebuah blueprint untuk sebuah objek. Sebagai contoh: Pertimbangkan class Mobil. Mungkin ada banyak mobil dengan nama dan merek yang berbeda-beda, tetapi semuanya akan memiliki beberapa properti umum seperti keempat roda, batas kecepatan, jarak tempuh bahan bakar, dan sebagainya. Jadi, di sini, Mobil adalah class, dan roda, batas kecepatan, dan jarak tempuh bahan bakar adalah propertinya.

- Kelas adalah jenis data yang ditentukan oleh pengguna yang memiliki anggota data dan anggota fungsi.

- Anggota data adalah variabel data dan anggota fungsi adalah fungsi yang digunakan untuk memanipulasi variabel-variabel tersebut. Bersama-sama, anggota data dan anggota fungsi ini mendefinisikan properti dan perilaku objek dalam suatu kelas.

- Dalam contoh kelas Mobil di atas, anggota data akan menjadi batas kecepatan, jarak tempuh bahan bakar, dan sebagainya, dan anggota fungsi dapat mengaplikasikan rem, meningkatkan kecepatan, dan sebagainya.

kita bisa sebut class didalam c++ adalah blueprint yang merepresentasikan sebuah kelompok objek yang berbagi beberapa properti dan perilaku umum.

## Object

sebuah object diidentifikasi oleh sebuah state dan behavior. state adalah nilai-nilai yang disimpan dalam field (variabel-variabel) dari object tersebut. behavior adalah kemampuan dari object untuk melakukan sesuatu, biasanya berupa fungsi-fungsi yang dapat dipanggil oleh object tersebut.

```cpp
// program C++ untuk menunjukkan sintaks/kerja dari objek sebagai bagian dari pemrograman berorientasi objek
#include <iostream>
using namespace std;

class person {
    char name[20];
    int id;

public:
    void getdetails() {}
};

int main()
{

    person p1; // p1 is a object
    return 0;
}
```

Objek mengambil ruang di memori dan memiliki alamat terkait seperti record dalam pascal atau struktur atau union. Ketika program dijalankan, objek berinteraksi dengan mengirim pesan satu sama lain.
Setiap objek berisi data dan kode untuk memanipulasi data. Objek dapat berinteraksi tanpa harus mengetahui detail dari data atau kode satu sama lain, cukup untuk mengetahui jenis pesan yang diterima dan jenis respons yang dikembalikan oleh objek.

## beberapa contoh penggunaan class

## Encapsulation

Dalam istilah normal, Encapsulation didefinisikan sebagai membungkus data dan informasi dalam satu unit tunggal. Dalam Pemrograman Berorientasi Objek, Encapsulation didefinisikan sebagai mengikat bersama data dan fungsi yang memanipulasinya. Pertimbangkan contoh kehidupan nyata dari encapsulation, di sebuah perusahaan, ada bagian-bagian yang berbeda seperti bagian akuntansi, bagian keuangan, bagian penjualan, dan lain-lain. Bagian keuangan menangani semua transaksi keuangan dan menyimpan catatan semua data terkait keuangan. Demikian pula, bagian penjualan menangani semua aktivitas penjualan dan menyimpan catatan semua penjualan. Sekarang mungkin muncul situasi ketika karena beberapa alasan, seorang pejabat dari bagian keuangan memerlukan semua data tentang penjualan dalam bulan tertentu. Dalam hal ini, dia tidak diizinkan untuk secara langsung mengakses data dari bagian penjualan. Dia harus terlebih dahulu menghubungi petugas lain di bagian penjualan dan kemudian memintanya untuk memberikan data tertentu. Ini adalah apa yang disebut encapsulation. Di sini, data dari bagian penjualan dan karyawan yang dapat memanipulasinya dibungkus di bawah satu nama "bagian penjualan".

contoh:

```cpp
#include <iostream>
#include <string>

using namespace std;

class Person {
private:
    string name; //variabel name di-encapsulate dengan modifier access private
    int age; //variabel age di-encapsulate dengan modifier access private
public:
    Person(string name, int age) { //constructor
        this->name = name;
        this->age = age;
    }
    void setName(string name) { //setter untuk variabel name
        this->name = name;
    }
    string getName() { //getter untuk variabel name
        return name;
    }
    void setAge(int age) { //setter untuk variabel age
        this->age = age;
    }
    int getAge() { //getter untuk variabel age
        return age;
    }
};

int main() {
    Person person("John Doe", 30); //instansiasi objek person dengan parameter constructor

    cout << "Name: " << person.getName() << endl; //mengakses variabel name dengan getter
    cout << "Age: " << person.getAge() << endl; //mengakses variabel age dengan getter

    person.setName("Jane Doe"); //mengubah variabel name dengan setter
    person.setAge(32); //mengubah variabel age dengan setter

    cout << "Name: " << person.getName() << endl; //mengakses variabel name dengan getter
    cout << "Age: " << person.getAge() << endl; //mengakses variabel age dengan getter

    return 0;
}
```

Pada kodingan di atas, class Person memiliki 2 private member variables yaitu name dan age. Selain itu, class Person juga memiliki 4 public member functions yaitu constructor, setName(), getName(), setAge(), dan getAge(). Pada main() function, pertama-tama dibuat object dari class Person dengan nama "John Doe" dan umur 30. Kemudian, dilakukan print untuk nama dan umur dari object tersebut menggunakan getName() dan getAge(). Setelah itu, nilai dari name dan age pada object tersebut diubah menggunakan setName() dan setAge() dan dilakukan print ulang untuk memastikan perubahan nilai berhasil dilakukan.

## Abstraction

Data abstraction adalah salah satu fitur paling penting dan penting dalam pemrograman berorientasi objek di C ++. Abstraksi berarti menampilkan hanya informasi penting dan menyembunyikan detailnya. Abstraksi data mengacu pada memberikan informasi penting tentang data kepada dunia luar, menyembunyikan detail latar belakang atau implementasi. Pertimbangkan contoh kehidupan nyata seorang pria yang mengemudikan mobil. Pria itu hanya tahu bahwa menekan pedal gas akan meningkatkan kecepatan mobil atau menerapkan rem akan menghentikan mobil, tetapi dia tidak tahu bagaimana ketika menekan pedal gas kecepatan benar-benar meningkat, dia tidak tahu tentang mekanisme internal mobil atau implementasi gas, rem, dll. dalam mobil. Inilah yang disebut abstraksi.

berikut contoh abstraksi menggunakan class:

```cpp
#include<iostream>
using namespace std;

class Shape { //mendefinisikan kelas Shape
   public:
      virtual void area() = 0; //mendefinisikan fungsi virtual yang tidak memiliki implementasi
};

class Square : public Shape { //mendefinisikan kelas turunan Square yang mewarisi kelas Shape
   public:
      int side; //variabel untuk sisi persegi
      Square(int a = 0) { //constructor dengan nilai default
         side = a;
      }
      void area() { //mendefinisikan fungsi area dengan implementasi
         cout << "Luas persegi: " << (side * side) << endl;
      }
};

int main() {
   Square s(5); //membuat objek Square dengan sisi = 5
   s.area(); //memanggil fungsi area pada objek Square
   return 0;
}
```

Baris 3: Mendefinisikan kelas Shape.
Baris 4: Fungsi area() dideklarasikan sebagai fungsi virtual murni dan tidak memiliki implementasi.
Baris 6: Mendefinisikan kelas Square yang mewarisi kelas Shape.
Baris 8: Variabel side dideklarasikan untuk menyimpan nilai sisi persegi.
Baris 9-12: Constructor untuk kelas Square dengan nilai default sisi = 0.
Baris 14-17: Mendefinisikan fungsi area() untuk menghitung luas persegi dengan mengalikan sisi dengan sisi.
Baris 19-21: Fungsi main() membuat objek Square dengan sisi = 5 dan memanggil fungsi area() pada objek tersebut.
Baris 23: Program diakhiri dengan mengembalikan nilai 0.

berikut ini contoh abstraksi tanpa menggunakan class:

shape.h

```cpp
#ifndef SHAPE_H
#define SHAPE_H

class Shape {
public:
    // pure virtual function untuk menghitung luas shape
    virtual double getArea() = 0;
    // pure virtual function untuk menghitung keliling shape
    virtual double getPerimeter() = 0;
};

#endif // SHAPE_H
```

circle.h

```cpp
#ifndef CIRCLE_H
#define CIRCLE_H

#include "Shape.h"

class Circle : public Shape {
private:
    double radius;
public:
    Circle(double radius) {
        this->radius = radius;
    }
    double getArea() {
        return 3.14 * radius * radius;
    }
    double getPerimeter() {
        return 2 * 3.14 * radius;
    }
};

#endif // CIRCLE_H
```

square.h

```cpp
#ifndef SQUARE_H
#define SQUARE_H

#include "Shape.h"

class Square : public Shape {
private:
    double side;
public:
    Square(double side) {
        this->side = side;
    }
    double getArea() {
        return side * side;
    }
    double getPerimeter() {
        return 4 * side;
    }
};

#endif // SQUARE_H
```

main.cpp

```cpp
#include <iostream>
#include "Circle.h"
#include "Square.h"

using namespace std;

int main() {
    // membuat objek Circle dan Square
    Circle c(5);
    Square s(5);

    // memanggil fungsi getArea dan getPerimeter pada objek
    cout << "Circle Area: " << c.getArea() << endl;
    cout << "Circle Perimeter: " << c.getPerimeter() << endl;
    cout << "Square Area: " << s.getArea() << endl;
    cout << "Square Perimeter: " << s.getPerimeter() << endl;

    return 0;
}
```

Penjelasan tiap line dalam kodingan:

#ifndef SHAPE_H
Mencegah file Shape.h di-include lebih dari satu kali.

#define SHAPE_H
Mendefinisikan konstanta SHAPE_H.

class Shape
Deklarasi kelas Shape.

public:
Menunjukkan bahwa semua member berikutnya bersifat publik.

virtual double getArea() = 0;
Deklarasi fungsi virtual murni untuk menghitung luas shape.

virtual double getPerimeter() = 0;
Deklarasi fungsi virtual murni untuk menghitung keliling shape.

#endif // SHAPE_H
Menutup blok kondisi praprosesor.

#ifndef CIRCLE_H
Mencegah file Circle.h di-include lebih dari satu kali.

#define CIRCLE_H
Mendefinisikan konstanta CIRCLE_H.

#include "Shape.h"
Include file Shape.h.

class Circle : public Shape
Deklarasi kelas Circle yang merupakan turunan dari kelas Shape.

double radius;
Mendeklarasikan variabel radius.

Circle(double radius)
Membuat konstruktor kelas Circle yang menerima parameter radius.

this->radius = radius;
Mengisi nilai radius dengan nilai parameter radius.

double getArea()
Implementasi fungsi getArea untuk kelas Circle dan Square.

double getPerimeter()
Implementasi fungsi getPerimeter untuk kelas Circle dan Square.

## Polymorphism

Kata "polymorphism" berarti memiliki banyak bentuk. Dalam kata-kata sederhana, kita dapat mendefinisikan polymorphism sebagai kemampuan sebuah pesan untuk ditampilkan dalam lebih dari satu bentuk. Seorang individu pada saat yang sama dapat memiliki karakteristik yang berbeda. Seorang pria pada saat yang sama adalah seorang ayah, suami, dan pegawai. Jadi, orang yang sama memiliki perilaku yang berbeda dalam situasi yang berbeda. Ini disebut polymorphism. Suatu operasi dapat menunjukkan perilaku yang berbeda dalam contoh-contoh yang berbeda. Perilaku tergantung pada jenis data yang digunakan dalam operasi tersebut. C++ mendukung operator overloading dan function overloading.

bentuk Operator Overloading:

```cpp
#include <iostream>
using namespace std;

class Complex {
   private:
      int real, imag;
   public:
      Complex(int r = 0, int i =0) {real = r; imag = i;}

      // Fungsi operator overloading '+'
      Complex operator + (Complex const &obj) {
         Complex res;
         res.real = real + obj.real;
         res.imag = imag + obj.imag;
         return res;
      }

      void print() { cout << real << " + i" << imag << endl; }
};

int main() {
   Complex c1(10, 5), c2(2, 4);
   Complex c3 = c1 + c2; // Memanggil fungsi operator overloading '+'
   c3.print();
   return 0;
}
```

Penjelasan:

Dalam contoh di atas, kita membuat sebuah class Complex yang berisi 2 variabel integer real dan imag.
Kemudian, kita membuat fungsi operator+ yang merupakan operator overloading untuk operator '+'.
Fungsi tersebut memungkinkan objek Complex untuk dijumlahkan menggunakan operator '+'.
Kemudian, kita membuat objek c1 dan c2 dengan nilai-nilai real dan imag yang berbeda.
Setelah itu, kita menjumlahkan kedua objek tersebut menggunakan operator '+' dan hasilnya disimpan di dalam objek c3.
Terakhir, kita memanggil fungsi print untuk menampilkan hasil penjumlahan dari kedua objek tersebut yang ditampung dalam objek c3.
Dalam contoh ini, polymorphism ditunjukkan oleh operator overloading '+' yang mampu melakukan operasi penjumlahan pada objek Complex dengan dua cara, yaitu dengan operator '+' biasa dan dengan operator overloading '+' yang telah kita buat.

bentuk Function Overloading:

```cpp
#include <iostream>
#include <string>

using namespace std;

class Math {
public:
    // Function Overloading dengan 2 parameter bertipe integer
    int add(int x, int y) {
        return x + y;
    }

    // Function Overloading dengan 3 parameter bertipe integer
    int add(int x, int y, int z) {
        return x + y + z;
    }
};

int main() {
    Math math;

    // Memanggil function add dengan 2 parameter
    cout << "Hasil penjumlahan 10 dan 20: " << math.add(10, 20) << endl;

    // Memanggil function add dengan 3 parameter
    cout << "Hasil penjumlahan 10, 20, dan 30: " << math.add(10, 20, 30) << endl;

    return 0;
}
```

Penjelasan:

Baris 4-11: Mendefinisikan sebuah class Math.
Baris 13-18: Mendefinisikan sebuah function add dengan 2 parameter bertipe integer.
Baris 20-25: Mendefinisikan sebuah function add dengan 3 parameter bertipe integer.
Baris 27-37: Implementasi program utama.
Baris 29: Membuat objek math dari class Math.
Baris 32: Memanggil function add dengan 2 parameter dan menampilkan hasilnya.
Baris 35: Memanggil function add dengan 3 parameter dan menampilkan hasilnya.

Dalam contoh di atas, terdapat 2 function add yang berbeda, yaitu dengan 2 parameter dan 3 parameter. Karena kedua function tersebut memiliki nama yang sama namun berbeda jumlah parameter, maka hal ini disebut dengan function overloading. Dengan menggunakan function overloading, kita dapat membuat function dengan nama yang sama namun berbeda jenis atau jumlah parameter, sehingga memudahkan dalam penggunaannya.

## Inheritance

Kemampuan dari sebuah kelas untuk mendapatkan properti dan karakteristik dari kelas lain disebut dengan Inheritance. Inheritance merupakan salah satu fitur yang paling penting dari pemrograman berorientasi objek.

contoh subclass:

```cpp
#include <iostream>
using namespace std;

// Base class
class Shape {
   public:
      void setWidth(int w) {
         width = w;
      }
      void setHeight(int h) {
         height = h;
      }
   protected:
      int width;
      int height;
};

// Derived class
class Rectangle: public Shape {
   public:
      int getArea() {
         return (width * height);
      }
};

int main() {
   Rectangle Rect;

   Rect.setWidth(5);
   Rect.setHeight(7);

   // Print the area of the object.
   cout << "Total area: " << Rect.getArea() << endl;

   return 0;
}
```

Penjelasan:

Pada baris ke-5 hingga 14, terdapat base class bernama Shape yang memiliki dua method yaitu setWidth() dan setHeight(). Method tersebut digunakan untuk mengatur nilai dari width dan height.
Pada baris ke-17 hingga 23, terdapat derived class bernama Rectangle yang merupakan subclass dari Shape. Rectangle memiliki satu method yaitu getArea() yang akan mengembalikan hasil perkalian width dan height dari objek.
Pada baris ke-26 hingga 33, di dalam fungsi main() terdapat objek Rect dari kelas Rectangle yang kemudian mengatur nilai dari width dan height menggunakan method setWidth() dan setHeight(). Kemudian, hasil perkalian width dan height dari objek Rect dicetak ke layar menggunakan method getArea() pada baris ke-30.
Inheritance digunakan pada kelas Rectangle dengan menuliskan nama base class yang ingin diwarisi dengan menggunakan operator ':' setelah nama kelas Rectangle.

Dalam contoh di atas, kelas Rectangle mewarisi variabel width dan height dari kelas Shape. Oleh karena itu, kelas Rectangle dapat menggunakan variabel width dan height dari kelas Shape. Dengan menggunakan inheritance, kita dapat membuat kode yang lebih efisien dan dapat menghindari pengulangan kode yang tidak perlu.

contoh Super Class

```cpp
#include <iostream>
using namespace std;

// superclass
class Shape {
   public:
      void setWidth(int w) {
         width = w;
      }
      void setHeight(int h) {
         height = h;
      }
   protected:
      int width;
      int height;
};

// subclass
class Rectangle: public Shape {
   public:
      int getArea() {
         return (width * height);
      }
};

int main() {
   Rectangle Rect;

   Rect.setWidth(5);
   Rect.setHeight(7);

   // Print the area of the object.
   cout << "Total area: " << Rect.getArea() << endl;

   return 0;
}
```

Penjelasan:

Pada baris 6-13, kita mendefinisikan superclass Shape dengan dua atribut width dan height serta dua method setWidth() dan setHeight().
Pada baris 16-20, kita mendefinisikan subclass Rectangle yang merupakan turunan dari superclass Shape. Subclass ini memiliki method getArea() yang mengembalikan hasil perkalian antara atribut width dan height.
Pada main() function (baris 23-30), kita membuat objek Rect dari subclass Rectangle. Lalu kita memanggil method setWidth() dan setHeight() dari superclass untuk mengatur nilai width dan height pada objek tersebut. Setelah itu, kita memanggil method getArea() dari subclass untuk menghitung dan mencetak luas dari objek Rect.

contoh reusability:

```cpp
#include <iostream>
using namespace std;

// superclass
class Shape {
protected:
    int width;
    int height;
public:
    Shape(int a = 0, int b = 0) {
        width = a;
        height = b;
    }
    virtual int area() {
        cout << "Parent class area :" << endl;
        return 0;
    }
};

// subclass yang mewarisi class Shape
class Rectangle: public Shape {
public:
    Rectangle(int a = 0, int b = 0):Shape(a, b) { }
    int area() {
        cout << "Rectangle class area :" << endl;
        return (width * height);
    }
};

// subclass yang mewarisi class Shape
class Triangle: public Shape {
public:
    Triangle(int a = 0, int b = 0):Shape(a, b) { }
    int area() {
        cout << "Triangle class area :" << endl;
        return (width * height / 2);
    }
};

// main function
int main() {
    Shape *shape;
    Rectangle rec(10,7);
    Triangle  tri(10,5);

    // memanggil area dari objek Rectangle
    shape = &rec;
    shape->area();

    // memanggil area dari objek Triangle
    shape = &tri;
    shape->area();

    return 0;
}
```

Pada contoh di atas, class Rectangle dan Triangle mewarisi class Shape. Kemudian, kita membuat objek Rectangle dan Triangle yang disimpan dalam pointer dari class Shape. Kita kemudian memanggil fungsi area() dari objek Rectangle dan Triangle. Fungsi area() pada Rectangle dan Triangle meng-override fungsi area() pada class Shape.

Hasilnya, fungsi area() yang dipanggil pada objek Rectangle dan Triangle akan mengeluarkan output sesuai dengan subclass-nya. Ini menunjukkan bahwa inheritance reusability memungkinkan kita untuk menggunakan kembali kode program dari superclass ke dalam subclass-nya, sehingga menghemat waktu dan usaha dalam pengembangan aplikasi.

## dynamic binding

Dalam dynamic binding, kode yang akan dieksekusi sebagai respons terhadap pemanggilan fungsi ditentukan saat runtime. C++ memiliki fungsi virtual untuk mendukung ini. Karena dynamic binding fleksibel, ini menghindari kelemahan dari pengikatan statis, yang menghubungkan pemanggilan fungsi dan definisinya saat build time.

```cpp

// C++ Program to Demonstrate the Concept of Dynamic binding
// with the help of virtual function
#include <iostream>
using namespace std;

class GFG {
public:
    void call_Function() // function that call print
    {
        print();
    }
    void print() // the display function
    {
        cout << "Printing the Base class Content" << endl;
    }
};
class GFG2 : public GFG // GFG2 inherit a publicly
{
public:
    void print() // GFG2's display
    {
        cout << "Printing the Derived class Content"
             << endl;
    }
};
int main()
{
    GFG geeksforgeeks; // Creating GFG's pbject
    geeksforgeeks.call_Function(); // Calling call_Function
    GFG2 geeksforgeeks2; // creating GFG2 object
    geeksforgeeks2.call_Function(); // calling call_Function
                                    // for GFG2 object
    return 0;
}
```

Output:
Printing the Base class Content
Printing the Base class Content

sebagaimana kita lihat, fungsi print() dari kelas induk dipanggil bahkan dari objek kelas turunan. Untuk menyelesaikan ini, kita menggunakan fungsi virtual.
