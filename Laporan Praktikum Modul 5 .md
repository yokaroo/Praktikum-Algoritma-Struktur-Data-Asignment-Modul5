# <h1 align="center">Laporan Praktikum Modul Struct dan Implementasi</h1>
<p align="center">Yoka Romadani</p>
<p align="center">2311110060</p>>
<p align="center">SD04-B</p>

## Dasar Teori
Analogi dari variabel seperti sebuah tempat untuk menampung atau 
menyimpan suatu data dengan tipe data tertentu. Format penulisan/deklarasi 
variabel adalah tipe_data nama_variabel, contoh int berat, string mata_kuliah, 
char jenis_kelamin. Secara default sebuah variabel hanya dapat menampung 
sebuah nilai misalnya variabel berat hanya dapat menampung satu nilai berat 
175 kg, tidak bisa diisi lebih dari satu. Jika diinginkan dapat menampung lebih 
dari satu nilai maka deklarasikan variabel sebagai array, dengan format 
penulisan tipe_data nama_variabel [banyak data].
## Guided
## 1. Buatlah sebuah struktur dengan nama buku yang berisi judul_buku, pengarang, penerbit, tebal_halaman, harga_buku. Isi dengan nilai kemudian tampilkan. 
```C++
#include <iostream>
#include <string>

using namespace std;

struct Buku {
string judul_buku;
string pengarang;
string penerbit;
int tebal_buku;
double harga_buku;
}; Buku buku1, buku2;

int main(){ //fungsi program utama
    buku1.judul_buku = "TIME IS MONEY";
	buku1.pengarang = "Yokaro";
	buku1.penerbit = "Gudang Garam Jaya";
	buku1.tebal_buku = 515;
	buku1.harga_buku = 150000;
	
	buku2.judul_buku = "HOW TO FIGHT";
	buku2.pengarang = "Dani Wong";
	buku2.penerbit = "PT. KNTL MANIS";
	buku2.tebal_buku = 276;
	buku2.harga_buku = 200000;
	
	//menampilkan data 
	cout << "Informasi Buku 1\n" << endl;
	cout << "Informasi Buku 1" << endl;
	cout << "Judul : "<< buku1.judul_buku << endl;
	cout << "Pengarang : "<< buku1.pengarang << endl;
	cout << "Penerbit : "<< buku1.penerbit << endl;
	cout << "tebal_buku : "<< buku1.tebal_buku << endl;
	cout << "harga_buku : "<< buku1.harga_buku << endl;

	//menampilkan data
	cout << "Informasi Buku 2\n" << endl;
	cout << "Judul : "<< buku2.judul_buku << endl;
	cout << "Pengarang : "<< buku2.pengarang << endl;
	cout << "Penerbit : "<< buku2.penerbit << endl;
	cout << "tebal_buku : "<< buku2.tebal_buku << endl;
	cout << "harga_buku : "<< buku2.harga_buku << endl;
	
	return 0;
	}
```
### Output
![Screenshot 2024-06-12 231558](https://github.com/yokaroo/Praktikum-Algoritma-Struktur-Data-Asignment-Modul5/blob/main/Screenshot%202024-06-12%20231558.png)
## Iterpretasi
Program tersebut merupakan contoh implementasi struktur (struct) dalam C++, yang digunakan untuk menyimpan informasi mengenai dua buah buku. Setiap buku direpresentasikan sebagai sebuah variabel dengan tipe data `struct Buku`, yang memiliki beberapa atribut seperti judul buku, pengarang, penerbit, tebal buku, dan harga buku. Dalam program tersebut, dua variabel buku (`buku1` dan `buku2`) telah dideklarasikan dan diinisialisasi dengan nilai-nilai yang sesuai. Setelah itu, informasi dari kedua buku tersebut ditampilkan ke layar menggunakan perintah `cout`. Setelah menampilkan informasi buku pertama, program akan menampilkan informasi buku kedua. Setelah itu, program akan berakhir. Dengan menggunakan struktur, kita dapat mengelompokkan informasi yang terkait bersama-sama, sehingga memudahkan dalam pemrosesan dan manajemen data.

## 2. Buatlah sebuah struktur dengan skema seperti dibawah, isi dengan nilai kemudian jalankan.
![Screenshot 2024-06-12 232207](https://github.com/yokaroo/Praktikum-Algoritma-Struktur-Data-Asignment-Modul5/blob/main/Screenshot%202024-06-12%20232207.png)
```C++
#include <iostream>
#include <string>
using namespace std;

struct hewan {
    string nama_hewan;
    string jenis_kelamin;
    string kembangbiak;
    string pernafasan;
    string tempat_hidup;
    bool karnivora;
}; 

struct hewan_darat{
    hewan info_hewan;
    int jumlah_kaki;
    bool apakah_menyusui;
    string suara;
};
hewan_darat hewan1;

struct hewan_laut{
    hewan info_hewan;
    string bentuk_sirip;
    string pertahanan_diri;
};
hewan_laut hewan2;

int main() {
    hewan1.info_hewan.nama_hewan = "Anjing";
    hewan1.info_hewan.jenis_kelamin = "Laki-laki";
    hewan1.info_hewan.kembangbiak = "Melahirkan";
    hewan1.info_hewan.pernafasan = "Paru paru";
    hewan1.info_hewan.tempat_hidup = "Darat";
    hewan1.info_hewan.karnivora = true;
    hewan1.jumlah_kaki = 4;
    hewan1.apakah_menyusui = true;   
    hewan1.suara = "Rawrr, guk, guk,guk";
    
    hewan2.info_hewan.nama_hewan = "Paus";
    hewan2.info_hewan.jenis_kelamin = "Perempuan";
    hewan2.info_hewan.kembangbiak = "Melahirkan";
    hewan2.info_hewan.pernafasan = "paru paru";
    hewan2.info_hewan.tempat_hidup = "Perairan (Laut)";
    hewan2.info_hewan.karnivora = false;
    hewan2.bentuk_sirip = "dosal, sabit, dan gumpalan";
    hewan2.pertahanan_diri = " Menghirup Oksigen di udara";   

	//menampilkan data 
	cout << "\t Hewan Darat" << endl;
	cout << "Nama Hewan :" <<hewan1.info_hewan.nama_hewan << endl;
	cout << "Jenis Kelamin : "<<hewan1.info_hewan.jenis_kelamin << endl;
	cout << "Kembangbiak : "<< hewan1.info_hewan.kembangbiak << endl;
	cout << "Pernapasan : "<< hewan1.info_hewan.pernafasan << endl;
	cout << "Tempat Hidup : "<< hewan1.info_hewan.tempat_hidup << endl;
	cout << "karnivora : "<< hewan1.info_hewan.karnivora << endl;
	cout << "jumlah kaki : "<< hewan1.jumlah_kaki << endl;
	cout << "apakah menyusui?  : "<< hewan1.apakah_menyusui << endl;
	cout << "suara : "<< hewan1.suara << "\n" << endl ;

	//menampilkan data 
	cout << "\t Hewan Laut" << endl;
	cout << "Nama Hewan :" <<hewan2.info_hewan.nama_hewan << endl;
	cout << "Jenis Kelamin : "<<hewan2.info_hewan.jenis_kelamin << endl;
	cout << "Kembangbiak : "<< hewan2.info_hewan.kembangbiak << endl;
	cout << "Pernapasan : "<< hewan2.info_hewan.pernafasan << endl;
	cout << "Tempat Hidup : "<< hewan2.info_hewan.tempat_hidup << endl;
	cout << "apakah karnivora? "<< hewan2.info_hewan.karnivora << endl;
	cout << "bentuk sirip : "<< hewan2.bentuk_sirip << endl;
	cout << "pertahanan diri : "<< hewan2.pertahanan_diri << endl;


	return 0;
	}
```
## Output
![Screenshot 2024-06-12 232657](https://github.com/yokaroo/Praktikum-Algoritma-Struktur-Data-Asignment-Modul5/blob/main/Screenshot%202024-06-12%20232657.png)
## Interpretasi Code
Program tersebut mendemonstrasikan penggunaan struktur (struct) dalam C++. Dua jenis hewan, yaitu hewan darat dan hewan laut, direpresentasikan menggunakan struktur `hewan_darat` dan `hewan_laut`. Setiap jenis hewan memiliki beberapa atribut yang diorganisir dalam struktur, seperti nama hewan, jenis kelamin, kembangbiak, pernafasan, tempat hidup, dan atribut-atribut lain yang sesuai dengan sifat hewan tersebut.

Setelah mendefinisikan struktur hewan darat dan hewan laut, program kemudian membuat dua variabel untuk masing-masing jenis hewan (`hewan1` dan `hewan2`). Setiap variabel tersebut memiliki atribut-atribut yang diisi dengan nilai sesuai dengan spesifikasi hewan yang ditentukan.

Kemudian, program menampilkan informasi tentang kedua hewan tersebut ke layar menggunakan perintah `cout`. Informasi yang ditampilkan mencakup semua atribut yang dimiliki oleh hewan darat dan hewan laut, seperti nama hewan, jenis kelamin, kembangbiak, pernafasan, tempat hidup, jumlah kaki (untuk hewan darat), apakah menyusui (untuk hewan darat), bentuk sirip, dan pertahanan diri (untuk hewan laut).

Dengan menggunakan struktur, program dapat menyimpan dan mengorganisir informasi tentang berbagai jenis hewan dengan cara yang terstruktur dan mudah dipahami.

### UnGuided
## 1. Modifikasi tugas guided pertama, sehingga setiap item yang terdapat pada struct buku berupa array yang berukuran 5, isi dengan data kemudian tampilkan. 
```C++
#include <iostream>
#include <string>

using namespace std;

struct Buku {
    string judul_buku[5];
    string pengarang[5];
    string penerbit[5];
    int tebal_buku[5];
    double harga_buku[5];
}; 

int main() {
    Buku buku1, buku2;

    // Mengisi data untuk buku1
    buku1.judul_buku[0] = "TIME IS MONEY";
    buku1.pengarang[0] = "Yokaro";
    buku1.penerbit[0] = "Gudang Garam Jaya";
    buku1.tebal_buku[0] = 515;
    buku1.harga_buku[0] = 150000;

    // Mengisi data untuk buku2
    buku2.judul_buku[0] = "HOW TO FIGHT";
    buku2.pengarang[0] = "Dani Wong";
    buku2.penerbit[0] = "PT. KNTL MANIS";
    buku2.tebal_buku[0] = 276;
    buku2.harga_buku[0] = 200000;

    // Menampilkan data untuk buku1
    cout << "Informasi Buku 1" << endl;
    for (int i = 0; i < 5; ++i) {
        cout << "Judul : " << buku1.judul_buku[i] << endl;
        cout << "Pengarang : " << buku1.pengarang[i] << endl;
        cout << "Penerbit : " << buku1.penerbit[i] << endl;
        cout << "Tebal Buku : " << buku1.tebal_buku[i] << endl;
        cout << "Harga Buku : " << buku1.harga_buku[i] << endl;
        cout << endl;
    }

    // Menampilkan data untuk buku2
    cout << "Informasi Buku 2" << endl;
    for (int i = 0; i < 5; ++i) {
        cout << "Judul : " << buku2.judul_buku[i] << endl;
        cout << "Pengarang : " << buku2.pengarang[i] << endl;
        cout << "Penerbit : " << buku2.penerbit[i] << endl;
        cout << "Tebal Buku : " << buku2.tebal_buku[i] << endl;
        cout << "Harga Buku : " << buku2.harga_buku[i] << endl;
        cout << endl;
    }

    return 0;
}

```
### Output
![Screenshot 2024-06-12 233121](https://github.com/yokaroo/Praktikum-Algoritma-Struktur-Data-Asignment-Modul5/blob/main/Screenshot%202024-06-12%20233121.png)

## 2.  Apa yang terjadi jika deklarasi variabel struct yang dibuat pada tugas guided I, berjenis Array. Bagaimana cara mengisi data dan menampilkannya ?

Ketika sebuah struktur (struct) dideklarasikan dengan variabel yang merupakan array, maka setiap elemen array dalam struktur tersebut akan memiliki jumlah elemen sesuai dengan yang telah ditentukan dalam deklarasi array. Dalam kasus kode yang diberikan, struktur `Buku` memiliki lima elemen array untuk setiap atributnya, misalnya `judul_buku`, `pengarang`, `penerbit`, `tebal_buku`, dan `harga_buku`.

Untuk mengisi data ke dalam struktur tersebut, Anda dapat menggunakan indeks dari setiap elemen array dan mengisinya dengan nilai yang diinginkan, seperti yang dilakukan dalam kode di atas dengan `buku1` dan `buku2`. Misalnya, `buku1.judul_buku[0]` digunakan untuk mengisi judul buku pertama, `buku1.pengarang[0]` untuk mengisi pengarang buku pertama, dan seterusnya.

Untuk menampilkan data dari struktur yang memiliki variabel array, Anda dapat menggunakan loop, seperti `for` loop, untuk mengakses dan menampilkan setiap elemen array satu per satu, seperti yang dilakukan dalam kode di atas. Dengan menggunakan loop `for`, Anda dapat mengakses setiap elemen array menggunakan indeks dari 0 hingga jumlah elemen array minus 1, dan kemudian menampilkan nilainya.

### Kesimpulan 
Dengan pemahaman tentang berbagai jenis array ini, kita dapat lebih efektif menggunakan dan memahami struktur data yang kompleks dan penggunaannya dalam pemrograman. Array merupakan fondasi yang penting dalam mempelajari struktur data lainnya dan memiliki peran yang krusial dalam pengembangan perangkat lunak.
