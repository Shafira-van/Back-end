# Membuat HTTP Server secara Native
- HTTP module memiliki banyak member seperti objek, properti, atau method yang berguna untuk melakukan hal-hal terkait protokol HTTP
  <br>![image](https://user-images.githubusercontent.com/85721388/225533075-df83012e-893e-4e5e-8370-6600dad91d74.png)
- Method http.createServer()  
  - Berfungsi untuk membuat HTTP server yang merupakan instance dari http.server
  - Method ini menerima satu parameter custom callback yang digunakan sebagai request listener. Di dalam request listener inilah logika untuk menangani dan menanggapi sebuah request dituliskan  
    <br>![image](https://user-images.githubusercontent.com/85721388/225533601-3a565912-b43e-48a7-90e0-990823e734f9.png)
    <br>![image](https://user-images.githubusercontent.com/85721388/225533883-f52da422-0ca8-4a83-990d-6615bb508e24.png)
- Method listen()
  - Membuat http.server selalu standby untuk menangani permintaan yang masuk dari client.
  - Method listen() dapat menerima 4 parameter:
    - port (number): jalur yang digunakan untuk mengakses HTTP server.
    - hostname (string): nama domain yang digunakan oleh HTTP server.
    - backlog (number): maksimal koneksi yang dapat ditunda (pending) pada HTTP server.
    - listeningListener (function): callback yang akan terpanggil ketika HTTP server sedang bekerja (listening).
  - Contoh
  <br>![image](https://user-images.githubusercontent.com/85721388/225534391-ca021dfe-2e44-4bf8-a17a-4a3fd60fd58a.png)
  <br>![image](https://user-images.githubusercontent.com/85721388/225534979-74e69fe9-0069-482d-8104-9de08f36169e.png)

# Method/Verb Request
- menangani permintaan dari method yang berbeda.
- Properti request.method
  <br>![image](https://user-images.githubusercontent.com/85721388/225535779-25c38eb0-308c-455d-9372-3cbf5d07af12.png)
- Contoh 
  <br>![image](https://user-images.githubusercontent.com/85721388/225536476-ca88e66d-f5f6-46e2-ba91-37f37523415a.png)
  
# Body Request
- Ketika client melakukan permintaan dengan method POST atau PUT, biasanya permintaan tersebut memiliki sebuah data yang disimpan pada body request. 
- Data pada body bisa berupa format teks, JSON, berkas gambar, atau format lainnya. 
- Data tersebut nantinya digunakan oleh server untuk diproses di database atau disimpan dalam bentuk objek utuh.
- Contoh
  <br> ![image](https://user-images.githubusercontent.com/85721388/225540996-14f2382d-b7bd-4afd-9079-7ac93c40e043.png)
  - Pertama, kita deklarasikan variabel body dan inisialisasikan nilainya dengan array kosong. Ini berfungsi untuk menampung buffer pada stream. 
  - Lalu, ketika event data terjadi pada request, kita isi array body dengan chunk (potongan data) yang dibawa callback function pada event tersebut.
  - Terakhir, ketika proses stream berakhir, maka event end akan terbangkitkan. Di sinilah kita mengubah variabel body yang sebelumnya menampung buffer menjadi data sebenarnya dalam bentuk string melalui perintah Buffer.concat(body).toString().   
- Latihan
  <br> ![image](https://user-images.githubusercontent.com/85721388/225542480-12ca2ab5-f295-47d8-b58e-3dc81e07b47f.png)
  <br> curl -X POST -H "Content-Type: application/json" http://localhost:5000 -d "{\"name\": \"Dicoding\"}"
  
# Routing Request
- Routing merupakan istilah dalam menentukan respons server berdasarkan path atau URL yang diminta oleh client.
- Contoh
  <br>![image](https://user-images.githubusercontent.com/85721388/225544108-198ac942-c97e-4c74-a1b4-1faeda7433ad.png)
  <br>![image](https://user-images.githubusercontent.com/85721388/225544185-3960db27-d28c-48e2-86ee-0cfc479161e2.png)
- Latihan
  <br>![image](https://user-images.githubusercontent.com/85721388/225548501-666b65a9-9240-437a-8925-350f6013b1c7.png)



 
