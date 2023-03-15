# # C PLUS PLUS 101 BY HIMATIKA
## Tipe Data (Data Type)

Dalam menulis program, diperlukan variabel untuk menyimpan data. Dalam konteks ini, variabel adalah lokasi memori yang digunakan untuk menyimpan nilai atau data dalam program. Selanjutnya sistem operasi dapat mengalokasikan memori dengan melihat tipe data dari sebuah variabel yang dideklarasikan.

Berikut ada tipe data bawaan dari c++:
|Type            |Keyword                        |
|----------------|-------------------------------|
|Boolean		 |`bool`                           
|Character       |`char`                          
|Integer         |`int`
|Floating        |`float`
|Double Floating |`double`
|Valueless       |`void`
|Wide Character  |`wchar_t`

Beberapa tipe data diatas dapat di modifikasi dengan type modifier seperti
1. `signed` = menandakan bahwa tipe data yang digunakan akan memuat nilai negatif atau positif.
2. `unsigned` = menandakan bahwa tipe data yang digunakan hanya akan memuat nilai positif atau nol
3. `short` = memperkecil rentang nilai dari tipe data dasar
4. `long` = memperluas rentang nilai dari tipe data dasar

Untuk penjabaran lebih lengkapnya, bisa dilihat di table dibawah ini

| Data Type              | Size         | Range                           |
|------------------------|--------------|---------------------------------|
| char                   | 1 byte       | -127 to 127 or 0 to 255         |
| unsigned char          | 1 byte       | 0 to 255                        |
| signed char            | 1 byte       | -127 to 127                     |
| int                    | 4 bytes      | -2147483648 to 2147483647       |
| unsigned int           | 4 bytes      | 0 to 4294967295                 |
| signed int             | 4 bytes      | -2147483648 to 2147483647       |
| short int              | 2 bytes      | -32768 to 32767                 |
| unsigned short int     | 2 bytes      | 0 to 65,535                     |
| signed short int       | 2 bytes      | -32768 to 32767                 |
| long int               | 8 bytes      | -2,147,483,648 to 2,147,483,647 |
| signed long int        | 8 bytes      | same seperti long int           |
| unsigned long int      | 8 bytes      | 0 to 4,294,967,295              |
| long long int          | 8 bytes      | -(2^63) to (2^63)-1             |
| unsigned long long int | 8 bytes      | 0 to 18,446,744,073,709,551,615 |
| float                  | 4 bytes      |                                 |
| double                 | 8 bytes      |                                 |
| long double            | 12 bytes     |                                 |
| wchar_t                | 2 or 4 bytes | 1 wide character                |


## Variable
Selain bisa dideklarasikan dengan tipe primitif seperti diatas, variable bisa juga mempunyai tipe data yang advance seperti **Enumeration**, **Pointer**, **Array**, **Reference**, **Data structures**, dan **Classes**. Tipe tersebut tidak akan dibahas di bab ini, tapi penting untuk diketahui bahwa ada tipe yang lain selain tipe primitif.

Berikut contoh penerapan variable dalam menyimpan suatu data.

```C++
#include using namespace std; 
int main () { 
	// Mendefinisikan variable : 
	int a, b; 
	int c; 
	float f;

	// menginisiasi data ke variabel
	a = 10; 
	b = 20; 
	c = a + b; 

	cout << c << endl ; 
	// hasil akhirnya adalah 30
	return 0; 
}
```
