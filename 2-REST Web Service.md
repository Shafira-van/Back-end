# REST Web Service
- REST atau REpresentational State Transfer adalah salah satu gaya arsitektur yang dapat diadaptasi ketika membangun web service.
- REST menggunakan pola request-response dalam berinteraksi, artinya ia memanfaatkan protokol HTTP
- Arsitektur REST benar-benar memisahkan peran client dan server, bahkan keduanya tidak harus saling mengetahui.
 
## REST API
- REST juga merupakan API (application program interface) karena ia digunakan untuk menjembatani antara sistem yang berbeda (client dan server).
- API atau Application Program Interface merupakan antarmuka yang menjadi perantara antara sistem aplikasi yang berbeda. API tak hanya dalam bentuk Web Service, bisa saja berupa SDK (Software Development Kit) ataupun lainnya.

### Berikut beberapa sifat yang menjadi kunci pada REST API:
- Client-Server: Ini merupakan hal yang paling mendasar dalam membangun REST API. Server harus bisa merespons permintaan yang dilakukan client, baik itu respons berhasil maupun gagal. Komunikasi client dan server dilakukan melalui protokol HTTP.
- Stateless: REST API tidak boleh menyimpan keadaan (state) apa pun terkait client. Seluruh state harus tetap disimpan di client. Artinya, tidak ada session di REST API. Permintaan yang dilakukan client harus mengandung informasi yang jelas. Jangan berharap RESTful API akan menyimpan informasi dari permintaan sebelumnya untuk digunakan di permintaan selanjutnya.
- Cacheable: Agar dapat merespons permintaan dengan cepat, sebaiknya REST API menerapkan prinsip cache sehingga setiap permintaan tidak melulu mengambil dari database.
- Layered: Ketika REST API server memiliki arsitektur yang kompleks, client seharusnya tidak perlu tahu bagaimana server melayaninya.

### Empat poin yang harus diperhatikan untuk membangun REST API:
- Format Request dan Response.
  - REST API seringnya menggunakan JavaScript Object Notation atau JSON sebagai format data, baik itu pada request maupun response. 
  - Agar REST API selalu merespons dengan format JSON, pastikan setiap respons terdapat properti Content-Type dengan nilai application/json. 
- HTTP Verbs/Methods.
  - Berikut adalah beberapa contoh HTTP verbs/methods:
    - GET: Untuk mendapatkan data.
    - POST: Untuk mengirimkan data baru.
    - PUT: Untuk memperbarui data yang ada.
    - DELETE: Untuk menghapus data. 
- HTTP Response code.
  - Status-Line merupakan salah satu bagian dari HTTP Response. Di dalam status line terdapat response code yang mengindikasikan bahwa permintaan yang client lakukan berhasil atau tidak.
  - Nilai-nilai status code yang sering digunakan:
    - 200 (OK): Permintaan client berhasil dijalankan oleh server.
    - 201 (Created): Server berhasil membuat/menambahkan resource yang diminta client.
    - 400 (Bad Request): Permintaan client gagal dijalankan karena proses validasi input dari client gagal.
    - 401 (Unauthorized): Permintaan client gagal dijalankan. Biasanya ini disebabkan karena pengguna belum melakukan proses autentikasi.
    - 403 (Forbidden): Permintaan client gagal dijalankan karena ia tidak memiliki hak akses ke resource yang diminta.
    - 404 (Not Found): Permintaan client gagal dijalankan karena resource yang diminta tidak ditemukan.
    - 500 (Internal Server Error):  Permintaan client gagal dijalankan karena server mengalami eror (membangkitkan Exception).
- URL Design.
  - Dengan merancang endpoint yang baik, penggunaan API akan lebih mudah dipahami. 
  - Dalam merancang endpoint, ikutilah aturan umum atau convention agar penggunaan API kita memiliki standar yang diharapkan oleh banyak developer.
  - Standar merancang EndPoint
    - Gunakan Kata Benda ketimbang Kata Kerja pada Endpoint Path
      <br>Karena aksi dapat ditentukan secara jelas melalui HTTP Verb, kita tidak perlu lagi menambahkan kata kerja di endpoint. Dengan adanya HTTP verbs, Anda cukup memberikan endpoint GET /articles untuk mendapatkan data artikel atau POST /articles untuk menambahkan artikel.
    - Gunakan Kata Jamak pada Endpoint untuk Resource Collection
      <br>Selalu gunakan kata jamak (plural) saat memberikan nama endpoint. Ini karena jarang ada data yang hanya memiliki satu item. Dengan menggunakan kata jamak, kita menjadi konsisten dengan apa yang ada di database. 
    - Gunakan Endpoint Berantai untuk Resource yang Memiliki Hierarki/Relasi 
      <br>Endpoint dari resource yang memiliki hierarki/relasi sebaiknya dituliskan secara berantai. Contohnya, untuk mendapatkan daftar komentar dari sebuah artikel, endpoint GET /articles/:id/comments merupakan contoh yang tepat.
