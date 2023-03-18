# Postman
- Tools yang sangat cocok untuk menguji sebuah API karena memiliki fungsi yang relatif lengkap sebagai API caller dalam melakukan HTTP Request. Bahkan untuk pengembangan API yang sudah kompleks, pengujian Postman dapat diintegrasikan ke dalam alur CI/CD.
- Postman merupakan tools yang sangat powerful dan mudah untuk digunakan. Ia memiliki graphical user interface (GUI) sehingga dapat digunakan dan dipahami oleh kalangan pemula sekalipun. Sebab, kita tak lagi berhadapan dengan kode yang rumit hanya untuk membuat HTTP request seperti cURL.

## Fitur Postman
- Postman Collection
  - Tempat menyimpan kumpulan request. Kita bisa menganggap collection adalah sebuah folder yang menyimpan berkas, tetapi berkas itu adalah request.

## Postman Environment
- Environment merupakan kumpulan dari variabel yang dapat digunakan pada request di Postman. Ketika melakukan pengujian otomatis, terkadang kita perlu menyimpan nilai pada sebuah variabel. Contohnya, ketika melakukan request menambah catatan, kita akan mendapatkan id catatan tersebut dari server. Id tersebut perlu disimpan pada variabel agar dapat digunakan oleh request selanjutnya.
- Variabel tak hanya digunakan untuk kasus tersebut saja, melainkan juga dapat untuk menyimpan nilai token, auth-key, atau nilai lainnya yang dipakai selama proses pengujian.
- Untuk menggunakan variabel environment pada request, tuliskan nama variabelnya yang dibungkus dengan kurung kurawal ganda seperti ini:
  <br>![image](https://user-images.githubusercontent.com/85721388/226090768-1be502c1-254b-485f-a9f3-c468744097ab.png)
  <br>Notasi tersebut dapat digunakan di request URL, parameters, headers, dan body data.


## Pengujian Otomatis Menggunakan Postman
- Dengan Postman Anda juga bisa melakukan pengujian secara otomatis sehingga tak perlu lagi melihat respons dari server secara manual untuk memastikan responsnya sesuai dengan harapan.
- Melalui testing otomatis ini kita bisa menguji nilai dari status code, properti header, hingga body respons. Pengujian otomatis akan “pass” (berhasil) ketika semua variabel yang diuji sesuai ekspektasi. Bila ada salah satu yang tidak sesuai, pengujian akan “failed” (gagal).
