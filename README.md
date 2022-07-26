###### Nama      : Achmad Setiawan Andyatama
###### Kelas     : XII-RPL 1
###### No. Absen : 05

# Modul 1

## Soal Nomor 1 dan 2

Lakukan proses instalasi framework laravel kedalam folder dengan nama masing-masing dan Buatlah projek pertama laravel dengan nama projek “penjualan” dan tampilkan dalam browser.

![image](https://user-images.githubusercontent.com/109930523/180904067-f2d4ae90-1c17-45b1-b0d7-87061faa7864.png)
```
composer create-project laravel/laravel penjualan
```

# Modul 2

## Soal Nomor 1

Buatlah migration tabel kategori dengan menggunakan teknik yang telah di pelajari dalam
modul ini.

### Langkah Pertama

Buatlah Tabel Kategori Terlebih dahulu
```
php artisan make:migration create_kategori_table
```
### Langkah Kedua

Isikan code dibawah ini kedalam File yang sudah dibuat

![image](https://user-images.githubusercontent.com/109930523/180904631-70471a22-8805-4845-9fae-0ea8d338de62.png)

Pastikan Kodenya Berjalan saat dijalankan di terminal menggunakan 
```
php artisan migrate
```
Setelah bisa berjalan mari kita buat model kategori.

### Langkah KeTiga

ketik code ini didalam terminal untuk membuat model

```
php artisan make:model kategori
```

Hasil dari perintah di atas, akan ada satu  file baru pada folder **penjualan/app/models** dengan nama **kategori.php**. hasil dari perintah artisan di atas dapat dilihat pada gambar dibawah.

![image](https://user-images.githubusercontent.com/109930523/180905766-7b772303-80ef-4a8a-97b7-fb10c247f042.png)

jika nama file model disini adalah kategori maka nama tabel yang ada di dalam database adalah kategoris. Namun hal tersebut dapat dikonfigurasi dengan cara membuka file model kategori.php yang baru saja dibuat dan tambahkan script berikut:

![image](https://user-images.githubusercontent.com/109930523/180906073-586ff220-4127-453f-9d1d-9d7b018d085f.png)

value dari variabel ini akan dianggap sebagai nama tabel yang diwakili oleh model ini.

## Soal Nomor 2

Berikan data dengan menggunakan seeder yang telah anda pelajari pada modul ini.

### Langkah Pertama

Untuk Membuat Seeder, gunakan perintah artisan pada **CMD** seperti seperti berikut:

![image](https://user-images.githubusercontent.com/109930523/180907055-3e57b653-1dc5-4b39-8d04-ca0f80a4b2c6.png)

```
php artisan make:seeder kategoriTableSeeder
```

Perintah tersebut akan menghasilkan satu file baru pada folder database/seeders dengan nama
kategoriTableSeeder.php atau yang diketikan pada perintah. Hasil dari perintah artisan diatas dapat dilihat pada gambar dibawah:

![image](https://user-images.githubusercontent.com/109930523/180907161-4db91d87-6eb6-49c8-97cb-ed0544639efd.png)

### Lankah KeDua

buka file kategoriTableSeeder yang telah dibuat dan tambahkan kode sehingga menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/109930523/180907689-b927b03b-c215-45e7-ac56-eb4db2a5fa9d.png)

### Langkah KeTiga

buka file DatabaseSeeder.php yang ada pada folder database/seeds dan panggil seeder yang baru dibuat pada method run dengan menambahkan script sebagai berikut:

![image](https://user-images.githubusercontent.com/109930523/180907829-79a75f27-4cca-4b6a-82d1-a913303e371c.png)

setelah itu jalankan perintah artisan pada **CMD** untuk mengeksekusi seeder yang telah dibuat dengan perintah seperti berikut:
```
php artisan db:seed
```
