# Modularization
Modularisasi dalam pemrograman merupakan teknik pemisahan kode menjadi modul-modul yang bersifat independen, tetapi bisa saling digunakan untuk membentuk suatu program yang kompleks

- module.exports
  Untuk mengekspor nilai
  <br> ![image](https://user-images.githubusercontent.com/85721388/225368258-7e7a7253-06ad-4b7f-93b5-dec9b526beee.png)
  <br> ![image](https://user-images.githubusercontent.com/85721388/225368629-a8854a26-b57d-45a4-acfb-2c45a37282b2.png)

- require()
  Untuk mengimport nilai
  <br>![image](https://user-images.githubusercontent.com/85721388/225368352-6bf0c811-1dc8-42f3-8e62-b10073633687.png)
  
- 3 jenis modul pada Node.js:
  - local module: module yang dibuat secara lokal berlokasi pada proyek Node.js Anda.
  - core module: module bawaan Node.js berlokasi di folder lib di mana Node.js terpasang pada komputer Anda. Core module dapat digunakan di mana saja.
  - third party module: module yang dipasang melalui Node Package Manager. Bila third party module dipasang secara lokal, module tersebut akan disimpan pada folder node_modules di proyek Node.js Anda. Namun, bila dipasang secara global, ia akan disimpan pada folder node_modules di lokasi Node.js dipasang pada komputer Anda.

# Events
- EventEmitter
  - Fungsi on : Menentukan aksi berdasarkan sebuah kejadian. 
    contoh :
    <br>![image](https://user-images.githubusercontent.com/85721388/225518157-80ec6156-d8d8-404b-b200-90e2bdd1f5da.png)
    <br>Fungsi on menerima dua buah argumen, yang pertama adalah nama event dan yang kedua adalah listener atau fungsi yang akan dieksekusi ketika event terjadi. Dari kode di atas, jika terjadi event ‘coffee-order’, fungsi makeCoffee akan dijalankan.
  - Fungsi emit() : membangkitkan event
    contoh :
    br<>![image](https://user-images.githubusercontent.com/85721388/225518506-80565d9a-3339-4d66-9cd3-e5366e427788.png)
    
  - Jika ada lebih dari satu fungsi listener
  - <br>![image](https://user-images.githubusercontent.com/85721388/225518946-a615f8d0-56bb-4f83-b88e-aa00e5c8d616.png)
  
  - Fungsi khusus
    <br>![image](https://user-images.githubusercontent.com/85721388/225519364-761952a2-5859-423d-ac4d-da176fd54511.png)
    ![image](https://user-images.githubusercontent.com/85721388/225519464-119c46d1-dca4-410e-b79a-f5575fd02af2.png)


