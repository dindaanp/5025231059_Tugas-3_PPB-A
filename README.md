# 5025231059_Tugas-3_PPB-A

# Macam-macam widget yang ada pada kode:

**1. MaterialApp**

MaterialApp adalah widget root aplikasi Flutter berbasis Material Design. Widget ini digunakan untuk menjalankan aplikasi serta menentukan halaman utama yang akan ditampilkan.

Properti:
  - title: judul aplikasi
  - theme: tema dan pengaturan warna aplikasi
  - home: halaman utama yang ditampilkan (RowColumnPage)

**2. Scaffold**

Scaffold digunakan sebagai kerangka dasar halaman aplikasi. Widget ini menyediakan struktur layout utama seperti bagian atas halaman dan area konten.

Properti:
  - appBar: bagian atas halaman aplikasi
  - body: area utama tempat widget lain ditampilkan

**3. AppBar**

AppBar adalah widget yang menampilkan judul di bagian atas halaman aplikasi. Pada kode ini AppBar menampilkan teks “My First App” dengan warna latar oranye muda dan judul berada di tengah.

Properti:
  - title: teks judul aplikasi
  - backgroundColor: warna latar AppBar
  - centerTitle: menentukan posisi judul (true = di tengah)

**4. Column**

Column adalah widget layout yang digunakan untuk menyusun child widget secara vertikal (atas ke bawah).

Properti:
  - crossAxisAlignment: CrossAxisAlignment.center (rata tengah secara horizontal)
  - mainAxisAlignment: MainAxisAlignment.center (rata tengah secara vertikal)
Isi Column pada kode:
  - Container + AspectRatio + Image.network
  - Container + Text
  - Container + Row + beberapa Column di dalamnya
  - CounterCard (StatefulWidget)

**5. Row**

Row adalah widget layout yang digunakan untuk menyusun child widget secara horizontal (kiri ke kanan). Pada kode ini Row digunakan untuk menampilkan beberapa kategori ikon secara sejajar.

Properti:
  - mainAxisAlignment: MainAxisAlignment.spaceEvenly (jarak antar widget sama rata)
  - crossAxisAlignment: CrossAxisAlignment.start (anak widget diatur rata atas)

**6. Container**

Container adalah widget yang membungkus widget lain dan dapat diatur margin, padding, warna latar, dan ukuran. Pada kode ini Container digunakan untuk:
  - Membungkus gambar
  - Membungkus teks
  - Membungkus Row kategori
  - Membungkus CounterCard

**7. Padding (EdgeInsets)**

Padding digunakan untuk memberikan jarak di dalam widget, yaitu jarak antara isi widget dan batas container.

Contoh di kode:

```
EdgeInsets.all(20.0)
EdgeInsets.fromLTRB(20.0, 5.0, 20.0, 10.0)
```

**8. Image**

Widget Image.network digunakan untuk menampilkan gambar dari internet.

Properti:
  - fit: BoxFit.cover (gambar menutupi seluruh area container tanpa mengubah rasio)
  - width: lebar gambar

**9. Icon**

Widget Icon digunakan untuk menampilkan ikon dari Material Icons.

Contoh di kode:
  - Food:     ``` Icons.food_bank ``` 
  
  - Scenery:       ``` Icons.landscape ```
  
  - People:       ``` Icons.people ```

**10. Button**

Widget IconButton digunakan untuk membuat tombol yang menampilkan ikon. Pada kode ini tombol digunakan untuk menambah nilai counter.

Properti:
  - Properti onPressed: fungsi yang dijalankan saat tombol ditekan
  - Properti icon: ikon yang ditampilkan

**11. StatelessWidget**

StatelessWidget adalah widget yang tidak memiliki state yang berubah setelah dibuat.

Contoh di kode:
  - MyApp
  - RowColumnPage

**12. StatefulWidget**

StatefulWidget adalah widget yang memiliki state yang dapat berubah selama aplikasi berjalan.

Contoh di kode:
  - CounterCard
    
    State pada CounterCard:
    
    ``` int _counter = 0; ```

    Fungsi _incrementCounter() memanggil:

    ```
    setState(() {
      _counter++;
    });
    ```
    
    Sehingga nilai counter bertambah dan UI diperbarui secara otomatis.
