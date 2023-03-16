# Filesystem
- Ketika kita menjalankan kode JavaScript pada browser, sangat penting untuk melimitasi JavaScript dalam mengakses filesystem. 
- Teknik ini dinamakan dengan sandboxing yang berfungsi untuk melindungi kita dari program jahat serta tindakan pencurian yang dapat merampas privasi penggunanya
- Node.js menyediakan core modules fs yang dapat mempermudah kita dalam mengakses filesystem. 
- Setiap method yang ada di module fs tersedia dalam dua versi
  - versi asynchronous (default)  
  - versi synchronous
- Method fs.readFile()
  - Method ini menerima tiga argumen: lokasi berkas, encoding, dan callback function yang akan terpanggil bila berkas berhasil/gagal diakses 
    <br>![image](https://user-images.githubusercontent.com/85721388/225521597-29ccc351-48c0-4b17-9601-acceccac9349.png)
    <br>versi synchronous
    <br>![image](https://user-images.githubusercontent.com/85721388/225521702-9fef931f-df51-4647-810a-c1621b461aba.png)
 - Method createReadStream()
  - Teknik ini dapat menangani kasus baca tulis berkas, komunikasi jaringan, atau beban kerja apa pun agar dapat berjalan dengan lebih efisien.  
    <br>![image](https://user-images.githubusercontent.com/85721388/225523760-b1dee327-20f7-4bde-9146-cc98106cb3da.png)
    <br>![image](https://user-images.githubusercontent.com/85721388/225523806-dedbf651-a15d-4df8-bbe6-e13b558a1181.png)
    <br>Fungsi createReadStream() menerima dua argumen, yang pertama adalah lokasi berkas yang hendak dibaca dan yang kedua adalah objek konfigurasi. Di dalam objek konfigurasi, kita bisa menetapkan ukuran buffer melalui properti highWaterMark. Nilai default dari properti ini adalah 16384 bytes (16kb). Anda tidak perlu menetapkan properti ini bila ingin tetap memiliki nilai default. Namun, karena kita hanya menggunakan berkas teks yang ukurannya sangat kecil, maka kita buat ukuran buffer menjadi 10 bytes. Itu artinya, berkas akan dibaca setiap 10 karakter (1 karakter = 1 bytes).

# Writable Stream
  <br>![image](https://user-images.githubusercontent.com/85721388/225524706-e116549f-1525-4b41-aa70-a88140031bbd.png)
  - createWriteStream() : Untuk membuat writable stream dalam menulis berkas
  - write() : untuk menuliskan data pada writable stream, gunakan method write()
  - end() : untuk menandakan akhir dari writable stream sekaligus bisa digunakan sebagai penulisan writable terakhir
 
