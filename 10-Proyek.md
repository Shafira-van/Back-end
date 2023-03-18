# Kriteria Proyek
- Web Server Dapat Menyimpan Catatan
  - Agar web server dapat menyimpan catatan melalui aplikasi client, web server harus menyediakan route dengan path ‘/notes’ dan method POST
  - Jika permintaan client berhasil dilakukan, respons dari server harus memiliki status code 201 (created) dan mengembalikan data dalam bentuk JSON dengan format berikut:
    <br>![image](https://user-images.githubusercontent.com/85721388/226082559-93e3ec13-bffb-4d7a-8691-784ab5288ee5.png)
  - Bila permintaan gagal dilakukan, berikan status code 500 dan kembalikan dengan data JSON dengan format berikut:
    <br>![image](https://user-images.githubusercontent.com/85721388/226082601-27229a8d-61f6-4dd6-bf72-d79f64e875b9.png)
- Web Server Dapat Menampilkan Catatan
  - Ketika client melakukan permintaan pada path ‘/notes’ dengan method ‘GET’, server harus mengembalikan status code 200 (ok) serta seluruh data notes dalam bentuk array menggunakan JSON. Contohnya seperti ini:
    <br>![image](https://user-images.githubusercontent.com/85721388/226082661-38df0b19-2a67-4dcf-94c4-8e41490449c9.png)
  - Selain itu, client juga bisa melakukan permintaan untuk mendapatkan catatan secara spesifik menggunakan id melalui path ‘/notes/{id}’ dengan method ‘GET’. Server harus mengembalikan status code 200 (ok) serta nilai satu objek catatan dalam bentuk JSON seperti berikut:
  - Bila client melampirkan id catatan yang tidak ditemukan, server harus merespons dengan status code 404 dan data dalam bentuk JSON
- Web Server Dapat Mengubah Catatan
  - Ketika client meminta perubahan catatan, ia akan membuat permintaan ke path ‘/notes/{id}’, menggunakan method ‘PUT’, serta membawa data JSON pada body request yang merupakan data catatan terbaru.
    <br>![image](https://user-images.githubusercontent.com/85721388/226083164-40e4dd98-257a-4c6f-b8db-2adab533e2e3.png)
  - Jika perubahan data berhasil dilakukan, server harus menanggapi dengan status code 200 (ok) dan membawa data JSON
  - Bila id catatan tidak ditemukan, server harus merespons dengan status code 404 (not found) dan data JSON seperti ini:
    <br>![image](https://user-images.githubusercontent.com/85721388/226083259-5e71dd54-a1f0-43d0-940d-164586b813f7.png)
- Web Server Dapat Menghapus Catatan
  - Untuk menghapus catatan, client akan membuat permintaan pada path ‘/notes/{id}’ dengan method ‘DELETE’. Ketika permintaan tersebut berhasil, server harus mengembalikan status code 200 (ok) serta data JSON 
  - Bila id catatan tidak ditemukan, server harus mengembalikan respons dengan status code 404 dan membawa data JSON

# Struktur Proyek
- single responsibility approach artinya, kita gunakan satu berkas JavaScript untuk satu tujuan saja
  - server.js: Memuat kode untuk membuat, mengonfigurasi, dan menjalankan HTTP server menggunakan Hapi.
  - routes.js: Memuat kode konfigurasi routing server, seperti menentukan path, method, dan handler yang digunakan.
  - handler.js: Memuat seluruh fungsi-fungsi handler yang digunakan pada berkas routes.
  - notes.js: Memuat data notes yang disimpan dalam bentuk array objek.
<br>![image](https://user-images.githubusercontent.com/85721388/226083404-db0c57e8-db1c-4b9c-881b-d705d09d52d8.png)

     
 
