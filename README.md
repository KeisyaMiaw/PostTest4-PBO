# PostTest4-PBO

# Deskripsi
Program ini menerapkan CRUD guna mengelola data kos. Data yang disimpan pada program ini berisi nomor kamar, nama penyewa, status kamar (kosong/terisi), nomor telepon, dan lantai kamar. Prorgram ini menggunakan ArrayList untuk menampung data-data kos. User bisa menambahkan data, melihat data-data, update data, dan juga menghapus data. Dan juga disini saya amenambahkan 1 menu baru yaitu menu search/cari yang guna untuk mencari data dari kos itu. Selanjutnya, pada post test ini saya menambahkan 2 subclass yaitu "KosBulanan" dan "KosTahunan" pada 1 superclass yaitu "Kos", dan juga pada tahap ini saya menerapkan getter dan setter serta overriding pada program kos saya ini. Guna dari getter dan setter adalah untuk menjaga keamanan data dari program yang telah saya buat, agar data tersebut tidak bocor ke class lainnya. Program ini menerapkan polymorphism, contoh method **infoKos()** di override pada masing-masing subclass dengan superclass "Kos". Ada juga diterapkan pada method **hitungBiaya()** dengan 2 metode yaitu menghitung kos bulanan atau tanpa mendapatkan diskon.

# Alur Program
1. Menu utama ditampilkan
   - user memilih salah satu menu dari 6 menu
2. Tambah kos
   - User dapat menginput nomor kamar, nama penyewa, status, no telp, dan lantai
   - data disimpan ke ArrayList
   - Memilih jenis kos:
       - 1 > Kos Bulanan
       - 2 > Kos Tahunan
   - Menginput harga kos per bulan jika pilihan jenis kos Bulanan. Jika memilih jenis kos Tahunan maka akan ada pertanyaan apakah si penyewa mendapatkan diskon, jika iya (true) maka penyewa akan mendapatkan diskon jika tidak(false)
   - Program membuat objek KosBulanan atau KosTahunan sesuai dengan inputan dan akan ditambahkan ke list.

<img width="566" height="291" alt="image" src="https://github.com/user-attachments/assets/8a54727b-b311-444c-833a-22bb5d588424" />


<img width="589" height="283" alt="image" src="https://github.com/user-attachments/assets/9baea883-7ee7-4909-b2a5-3e54e5b99f0b" />


3. Tampil Kos
   - Program akan mengecek apakah daftar kamar itu kosong
   - Jika ada data, maka program akan menampilkan semua kos dengan toString()

<img width="1105" height="319" alt="image" src="https://github.com/user-attachments/assets/78543aca-7f96-49bb-a95d-1009d7fa990c" />


4. Update Kos
   - User akan diminta untuk memasukkan nomor kamar, nama penyewa baru, status kamar apakah terisi, no telp baru, lantai baru
   - Jika ada maka data berhasil diubah, jika tidak ada maka akan ada ouput "Data kamar tidak valid"
  
<img width="411" height="259" alt="image" src="https://github.com/user-attachments/assets/88fe2108-e21a-4cfa-9a20-8fc7bacec213" />

5. Hapus Kos
   - User diminta memasukkan nomor kamar yang ingin dihapus
   - Jika nomor ada data telah berhasil dihapus, jika tidak ada akan ada output "Data kamar tidak valid"

<img width="1147" height="444" alt="image" src="https://github.com/user-attachments/assets/46d6a303-33ab-4898-b59f-3cfbd94a1358" />

Setelah dihapus dicek lagi dengan memilih menu 2 "Tampil Kos", maka output menunjukkan bahwa data telah berhasil di hapus.

6. Cari Kos
   - User diminta untuk memasukkan nama penyewa atau keyword
   - Program akan mencari data yang diinput

<img width="1120" height="194" alt="image" src="https://github.com/user-attachments/assets/6abadc5c-4e8e-41f8-9e3f-dd424d758e6c" />

Data telah berhasil dihapus.

6. Keluar
   - User dikeluarkan dari program dengan output "Anda telah keluar dari program"

<img width="343" height="166" alt="image" src="https://github.com/user-attachments/assets/c12e56d6-84e9-4383-9d95-645565444645" />

# Package
1. Package model berisi beberapa class, yaitu:
  - *Kos* guna sebagai tempat atribut & struktur dari data kos itu
  - *KosBulanan* guna untuk menginput harga kos per bulan
  - *KosTahunan* guna sebagai menginput apakah si penyewa akan mendapatkan harga yang berbeda dibandingkan kos bulanan/diskon
  - 
3. Package KosService berisi class Service sebagai tempat logika CRUD pada data kos, dan juga sebagai tempat logika dari subclass
4. Package Main berisi Main, ini merupakan titik awal pada program data kos ini, menampilkan menu & memanggil class Service

# Penjelasan Tambahan Code
Pada program ini saya abstraction dengan minimal 1 abstrak dan 1 interface. Untuk penerapan abstrak saya terapkan pada class **Kos** dengan method **infoKos();** dan wajib diimplementasikan setiap subclass. Kemudian untuk penerapan interface saya terapkan dengan membuat package baru dengan nama **Interfaces** dan di dalamnya memiliki 1 class yaitu Fasilitas yang berisikan 2 method yaitu **tampilFasilitas** dan **infoKos**. Selanjutnya, penerapan polymorphism dengan minimal 1 overloading dan 1 overriding, untuk penerapan overloading diterapkan pada class **Kos** yaitu **hitungBiaya()**, begitupun dengan penerapan overriding juga di class yang sama yaitu class **Kos** dengan method**toString()**.
