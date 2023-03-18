# Web Framework
- Web Framework adalah sebuah kerangka yang dapat membantu mempermudah pengembangan web, termasuk dalam membuat web server. Dengan menggunakan framework, penulisan kode akan lebih terstruktur, mudah dipelihara, dan gampang dikembangkan.  
- Web Framework menyediakan sekumpulan tools dan library yang dapat menyederhanakan hal-hal yang sering dilakukan dalam pengembangan web, seperti pembuatan server, routing, menangani permintaan, interaksi dengan database, otorisasi, hingga meningkatkan ketahanan web dari serangan luar.
## Web Framework di Node.Js
### Express
  <br>Express.js merupakan web framework tertua dan terpopuler di Node.js saat ini. Framework ini sangat ringan, mudah diintegrasikan dengan aplikasi web front-end, dan penulisan kodenya tidak jauh beda dengan Node.js native. Namun, karena sifat ringannya tersebut, ia menjadi framework yang unopinionated alias tidak memiliki aturan untuk menggunakannya. Express tidak menyediakan struktur atau kerangka kerja yang baku untuk diikuti oleh developer. Sehingga developer menjadi sulit menentukan seperti apa kode yang optimal. 
### Hapi
  - Framework lainnya seperti Hapi menyediakan environment yang lengkap untuk mengembangkan web server yang kompleks. Bila menggunakan Hapi, kita tak perlu tools lain untuk menerapkan layer authentication, tokenize, cors, dan lain sebagainya. Kelemahan Hapi adalah abstraksinya yang terlalu jauh dari Node.js native. 
  - Cara menjalankan framework HAPI
    - ![image](https://user-images.githubusercontent.com/85721388/225904031-ed823de3-3287-44da-a276-b877af26f2de.png)
    - ![image](https://user-images.githubusercontent.com/85721388/225904083-9a687b46-3b1a-47b4-99ed-2c509ac41cf9.png)
    - Dasar kode dalam membuat HTTP server pada HAPI
      <br>![image](https://user-images.githubusercontent.com/85721388/225904356-90ed173c-4f8a-4dd0-b6c7-afd46bf64289.png)
  - Fitur di Hapi
    - Request & Routing
      - routes.js
        <br> ![image](https://user-images.githubusercontent.com/85721388/225910914-15753cb9-26d7-4fef-b5d9-d143eb85d242.png)
        <br> ![image](https://user-images.githubusercontent.com/85721388/225910967-0a570549-7fb9-4e4f-9479-30facf75dffc.png)
      - server.js
        <br> ![image](https://user-images.githubusercontent.com/85721388/225911097-7168da1e-2bf9-4df1-bc60-73189ef8c1a0.png)
    - Path parameter
      <br>![image](https://user-images.githubusercontent.com/85721388/225915898-516d9381-54dc-4e1d-b64a-dae51140f36a.png)
    - Query parameter
      <br>![image](https://user-images.githubusercontent.com/85721388/225919107-3afd1c88-0eaf-4364-8229-7e361b2fa77a.png)
    - Body/Payload Request
      - Hapi secara default akan mengubah payload JSON menjadi objek JavaScript sehingga tidak perlu lagi menggunakan JSON.parse() untuk mendapatkan data
        <br> ![image](https://user-images.githubusercontent.com/85721388/225946664-08f0e512-e6de-4f75-b158-674efb705fac.png)
    - Response Toolkit
      - Parameter yang kedua yaitu h (huruf inisial Hapi) adalah response toolkit, objek yang menampung banyak sekali method yang digunakan untuk menanggapi sebuah permintaan client.
        <br>![image](https://user-images.githubusercontent.com/85721388/225949541-62848247-93e2-4ae8-a4c9-dc69fd84f6c8.png)   
  
#### Note:
     Ketika ingin membangun server yang sederhana, katakanlah untuk mendukung aplikasi front-end di-render di sisi server, express adalah pilihan yang tepat. Namun, bila Anda ingin membangun web server yang kompleks tanpa membutuhkan effort yang besar, Hapi adalah pilihan yang tepat. Hapi memiliki environment yang cukup luas.
