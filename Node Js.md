# Node JS
- Diciptakan oleh Ryan Dahl pada tahun 2009
- Node.js banyak digunakan oleh perusahaan besar sekelas Netflix, Uber, Paypal, dan eBay.
- Node.js berhasil menjadi JavaScript Runtime yang dapat mengeksekusi kode JavaScript di luar browser.

## Node.js REPL
- Node.js memiliki fitur REPL atau Read-Eval-Print Loop. fitur ini berfungsi untuk membaca kode JavaScript, mengevaluasi kode tersebut, kemudian mencetak hasil evaluasinya ke console.
- Untuk Masuk ke REPL
  <br>![image](https://user-images.githubusercontent.com/85721388/225309111-db3acc98-dbef-42dd-9298-74315c5d4f80.png)
- Untuk menuliskan kode javascript lebih dari satu baris
  <br>![image](https://user-images.githubusercontent.com/85721388/225310121-2159533d-2d54-4aeb-ac0f-6adef34259bc.png)
- Untuk keluar dari REPL
  <br>![image](https://user-images.githubusercontent.com/85721388/225310477-34f22ce2-6a60-46d0-8c75-8644119141eb.png)
- Untuk mengeksekusi berkas js
  <br>![image](https://user-images.githubusercontent.com/85721388/225310866-bfaead61-3020-4e59-964f-9ad11a9fd2f0.png)

## Node.js Global Object
- Node.js menambahkan objek global guna memberikan fungsionalitas lebih pada JavaScript. Hal ini bertujuan untuk mendukung pengembangan pada environment-nya. Contoh, melalui objek global kita dapat melihat berapa CPU yang digunakan pada komputer, modularisasi berkas JavaScript, menampilkan nilai pada console, dan hal lainnya
- Untuk mengetahui macam macam objek global 
  <br>![image](https://user-images.githubusercontent.com/85721388/225312229-1fff83ed-b79d-4b93-b798-3d06551b722a.png)
- True Globals
  - global: Global namespace. Member apa pun yang ada di dalam object ini dapat diakses pada cakupan global.
  - process: menyediakan interaksi dengan proses Node.js yang berjalan.
  - console: menyediakan berbagai fungsionalitas STDIO.
  - setTimeout, clearTimeout, setInterval, clearInterval: berkaitan dengan waktu.
- Pseudo-globals’ atau objek global semu. 
  - Objek ini tidak terlihat bila dicetak menggunakan Object.getOwnPropertyName(global) sebab ia bukan member langsung dari objek global, melainkan diturunkan dari cakupan module.
    - module: digunakan untuk sistem modularisasi pada Node.js.
    - __filename: keyword untuk mendapatkan lokasi berkas JavaScript yang dieksekusi. Keyword ini tidak tersedia pada Node.js REPL.
    - __dirname: keyword untuk mendapatkan root directory dari berkas JavaScript yang dieksekusi.
    - require: digunakan untuk mengimpor module JavaScript.
- Process Object
  - global objek process memiliki fungsi dan properti yang dapat memberikan informasi mengenai proses yang sedang berjalan
  - Fungsi Process
    -  Menetapkan dan mendapatkan informasi mengenai environment.
      - process.env
        <br>menyimpan nilai atau mendapatkan informasi mengenai environment yang digunakan selama proses sedang berlangsung
      - process.env.PWD
        <br>menyediakan informasi mengenai lokasi di mana proses dijalankan
      - process.env.USER
        <br>menyimpan informasi nama user pada komputer Anda; dan masih banyak properti lainnya
      - Daftar lengkap properti yang ada pada halaman dokumentasi Node.js mengenai process.env.
        <br>link https://nodejs.org/dist/latest-v8.x/docs/api/process.html#process_process_env
      - Menyimpan nilai secara manual di dalam process.env
        <br>Untuk menentukan alur code seperti if-else dalam program berdasarkan environment yang Anda berikan
        <br>Contohnya, ketika Anda ingin nilai variabel host berbeda di kala pengembangan (development) dan produksi (production), Anda bisa membuat properti NODE_ENV pada process.env. Jadi, Anda bisa menentukan nilai host berdasarkan kondisi NODE_ENV.
        <br>![image](https://user-images.githubusercontent.com/85721388/225319170-74426f15-4da5-4bba-9a7e-910ed5be761c.png)
      - Untuk memberikan nilai pada properti process.env, kita dapat memberikannya ketika mengeksekusi berkas JavaScript. Caranya seperti ini:
        <br>![image](https://user-images.githubusercontent.com/85721388/225320339-1253a3b1-e190-44fb-84bc-76d6830ee107.png)
        <br>Nilai yang ada pada process.env hanya dapat diakses di dalam cakupan proses Node.js. Itu berarti, Anda tidak dapat menggunakan nilainya pada program lain seperti menampilkan nilainya melalui program echo.
        <br>![image](https://user-images.githubusercontent.com/85721388/225320463-dcc58afc-4176-4cd4-9495-973d5d8702db.png)
   - Mendapatkan informasi tentang penggunaan CPU ketika proses berjalan 
      - process.memoryUsage()
        <br>![image](https://user-images.githubusercontent.com/85721388/225322147-3d10c376-0506-4279-9926-e7e99de5b619.png)
   - Properti ini dapat menampung nilai baris perintah dalam bentuk array ketika menjalankan proses. 
      - process.argv.
        <br>![image](https://user-images.githubusercontent.com/85721388/225322403-b878660a-d22a-443b-8060-de5af6dec285.png)
        <br>Maka array process.argv akan bernilai:
        - Elemen pertama: Alamat (path) lengkap dari lokasi node yang menjalankan prosesnya. 
        - Element kedua: Alamat (path) berkas JavaScript yang dieksekusi (app.js) 
        - Element ketiga: “harry”
        - Element keempat: “potter”

  
   

