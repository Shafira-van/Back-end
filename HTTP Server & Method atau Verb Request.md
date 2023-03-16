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
