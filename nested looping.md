# C PLUS PLUS 101 BY HIMATIKA

## Apa itu Nested Looping pada C++?

Nested Looping pada C++ adalah teknik pengulangan dimana sebuah loop ditempatkan di dalam loop lainnya. Teknik ini biasanya digunakan untuk melakukan pengulangan pada data berbentuk matriks atau array multi-dimensi.

Contoh penggunaan Nested Loop pada C++ untuk menampilkan bilangan segitiga:

```cpp
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= i; j++) {
        cout << j << " ";
    }
    cout << endl;
}
```
Penjelasan: Looping pertama akan menentukan jumlah baris dari segitiga, yaitu 5 baris. Looping kedua akan menampilkan bilangan dari 1 hingga i pada setiap baris. Hasil yang akan ditampilkan adalah seperti berikut:

```cpp
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```

Perhatikan bahwa loop kedua bergantung pada loop pertama, sehingga setiap kali loop pertama berjalan, loop kedua akan berulang sesuai dengan nilai i dari loop pertama.

Nested Loop juga dapat digunakan untuk melakukan pengulangan pada array multi-dimensi, seperti contoh berikut:

```cpp
int matrix[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        cout << matrix[i][j] << " ";
    }
    cout << endl;
}
```
Penjelasan: Looping pertama akan menentukan baris dari array multi-dimensi, yaitu 3 baris. Looping kedua akan menampilkan elemen-elemen pada setiap baris. Hasil yang akan ditampilkan adalah seperti berikut:

```cpp
1 2 3 
4 5 6 
7 8 9 
```

Perhatikan bahwa loop kedua bergantung pada loop pertama, sehingga setiap kali loop pertama berjalan, loop kedua akan berulang sesuai dengan jumlah kolom dari array multi-dimensi.