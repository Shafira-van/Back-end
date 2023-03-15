# Back-End 
merupakan bagian dari aplikasi yang bertanggung jawab untuk menyediakan kebutuhan yang tak terlihat oleh pengguna(tidak berinteraksi langsung dengan pengguna), seperti bagaimana data disimpan, diolah, serta ditransaksikan secara aman.

## Server 
-Server merupakan sebuah sistem yang dapat menyediakan sumber daya berupa data, layanan, atau program untuk disajikan ke komputer lain 
-merupakan suatu perantara antara back-end dan front-end
![image](https://user-images.githubusercontent.com/85721388/225283636-b340cdc7-e071-4e87-9f80-963ce5501aed.png)

### Tipe server sesuai dengan layanan
- File Server :   melayani penyimpanan dan pendistribusian berkas.
- Application Server : melayani hosting sebuah program atau aplikasi.
- DNS Server : mengubah nama domain (contoh: dicoding.com) ke dalam bentuk IP address (contoh: 75.2.21.170).
- Web Server : melayani hosting sebuah program atau aplikasi (seperti Application Server) yang dapat diakses oleh client melalui internet maupun intranet.
- Database Server : melayani penyimpanan dan pendistribusian data terstruktur.

### Hal yang dibutuhkan untuk membuat sistem aplikasi
- Web Server: Server yang dapat menjalankan program dan dapat diakses melalui internet atau intranet. 
- Web Service: Program yang dijalankan di web server agar kebutuhan bisnis terpenuhi.

Web service berjalan di dalam web server sehingga ia dapat diakses melalui internet. Melalui web service inilah aplikasi Front-End (client) dan Back-End dapat bertransaksi.

### Komunikasi Client-Server
- HTTP/HTTPS merupakan salah satu protokol yang dapat digunakan untuk berinteraksi dengan web server. Protokol tersebut terkenal dengan pola request-response. Artinya, untuk mendapatkan sesuatu (response), kita perlu melakukan permintaan terlebih dahulu (request).

### Informasi pada request dapat mengandung poin-poin berikut
- Request line: berisikan method/verb seperti GET (mengambil data), POST (menambahkan/mengirim data), PUT (memperbaharui data), atau DELETE (menghapus data); path atau alamat yang diminta; dan versi HTTP yang digunakan.
- Header: memuat informasi yang dilampirkan terkait request seperti format dokumen (contoh: application/json, text/html, dsb), kunci akses, dll.
- Body (opsional): mengandung data yang dibutuhkan oleh server, bisa dalam bentuk teks, JSON, dll. Body tidak wajib dilampirkan bila server tidak membutuhkan data apa pun.

### Beberapa informasi yang dilampirkan oleh respons
- Status line: berisikan HTTP versi yang digunakan; status code berupa tiga digit angka yang menandakan keberhasilan dari permintaan; reason phrase atau status text yang merupakan pesan berdasarkan status code dalam bentuk teks sehingga lebih mudah dimengerti.
- Header: mengandung informasi yang dilampirkan terkait response seperti format dokumen.
- Body (opsional, tetapi biasanya selalu dilampirkan): memuat data yang dikirimkan oleh server. Data dapat berupa HTML, JSON, gambar, dsb.

## CURL
cURL atau Client URL merupakan software berbasis command line yang dapat melakukan transaksi data melalui beberapa protokol internet, salah satunya HTTP/S. cURL dapat diakses secara langsung tanpa proses install melalui Terminal (Linux dan Mac) atau CMD (Windows)[4].

### Membuat Permintaan HTTP
- GET
  <br>![image](https://user-images.githubusercontent.com/85721388/225288836-68ccb48f-901a-4656-8a55-3e00ef132871.png) <br>
  - curl: merupakan perintah untuk menggunakan program cURL pada Terminal atau CMD.
  - X GET: menetapkan HTTP method/verb yang kita gunakan. GET berarti kita ingin mendapatkan sebuah data.
  - https://coffee-api.dicoding.dev/coffees: merupakan alamat request yang dituju.
  - i : memberikan informasi detail terhadap response yang diberikan (HTTP response headers).
  <br>![image](https://user-images.githubusercontent.com/85721388/225289063-2a23deb9-2096-4775-9068-01ae8e29f5e7.png) <br>
  - HTTP/1.1: merupakan HTTP version yang digunakan oleh web server dalam menanggapi permintaan.
  - 200: merupakan status code dari request. Karena status code diawali dengan angka 2, berarti request kita berhasil dilakukan.
  - OK: merupakan pesan teks dari status code, 200 berarti “OK”.
  - Content-Type: application/json;: merupakan tipe konten yang digunakan web server dalam memberikan data. Karena nilainya application/json, itu berarti server menggunakan format JSON.
  - JSON Data (kode di bagian bawah): merupakan data yang diberikan oleh web server. Kita bisa melihat web server memberikan informasi kopi yang tersedia beserta harganya menggunakan format JSON.

- POST
  <br>![image](https://user-images.githubusercontent.com/85721388/225289699-6b909d15-d635-430a-93aa-e3510f950878.png) <br>
  - X POST: dalam request kali ini kita menggunakan method POST karena membeli bukan hanya meminta data, melainkan akan mengubah jumlah stok kopi yang ada. Selain itu, kita juga melampirkan data berupa kopi apa yang akan dipesan. Sehingga tidak masuk akal bila kita menggunakan GET request.
  - H “Content-Type: application/json”: menetapkan nilai “Content-Type: application/json” pada Header request. Fungsinya untuk memberitahu server bahwa kita melampirkan data dalam bentuk JSON.
  - d <JSON Content>: merupakan data yang dilampirkan pada request. Data ini berformat JSON dan memiliki informasi kopi apa yang ingin dipesan.
  - https://coffee-api.dicoding.dev/transactions: merupakan alamat request yang dituju untuk membeli kopi.
  <br>![image](https://user-images.githubusercontent.com/85721388/225290135-1751d024-60b8-4ba7-bdcd-f861ee2e35cb.png)


