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
