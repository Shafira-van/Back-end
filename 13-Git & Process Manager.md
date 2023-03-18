# Git
- Git merupakan sebuah sistem yang membantu developer dalam melakukan versioning atau source code management terhadap aplikasi yang dikembangkan. Melalui Git, kita dapat menelusuri perubahan kode, siapa yang melakukan perubahannya, hingga mengelola code versioning (branching). Tools ini kerap digunakan sebagai tools berkolaborasi antar-developer.
- Ketahuilah bahwa sistem git ini hanya berjalan di lokal komputer Anda saja. Agar repository git dapat diakses di mana saja, oleh siapa saja, dan komputer mana saja (termasuk Compute Engine), kita perlu menyimpan repository-nya di internet. Nah, di sinilah peran dari GitHub. Ia merupakan salah satu vendor yang bergerak di bidang source code hosting menggunakan teknologi git.
- Untuk menetapkan email di git, eksekusi perintah berikut pada PowerShell/CMD/Terminal:
  <br>![image](https://user-images.githubusercontent.com/85721388/226086780-e40c0a28-be0c-4b68-a0e2-91c468166a84.png)
- install git di proyek  
<br>![image](https://user-images.githubusercontent.com/85721388/226086967-836c2e2e-687c-4dd1-9fa1-8ff5cc83775b.png)
- git add . digunakan untuk memasukkan semua berkas ke stash, terkecuali berkas node_modules.
- git commit -m “initial commit” digunakan untuk menyimpan perubahan pada local repository. Setiap perubahan pada sistem git dapat ditelusuri berdasarkan commit history.
- untuk menghubungkan local ke remote![image](https://user-images.githubusercontent.com/85721388/226087112-65a9aad6-6fcd-4716-9cad-5b0343b64c91.png)
- ![image](https://user-images.githubusercontent.com/85721388/226087141-61d298e7-93c3-428c-a8a3-64911154a5db.png)

# Process Manager
- Dengan menggunakan Process Manager, Anda tidak perlu khawatir bila aplikasi Node.js terhenti disebabkan oleh crash, ia akan menjalankan ulang prosesnya secara otomatis hampir tanpa downtime. Selain itu, Process Manager dapat membantu menyeimbangkan muatan proses pada CPU yang tersedia di server atau biasa disebut sebagai load balancing. Dengan begitu, aplikasi server dapat diakses secara lebih cepat dibandingkan bila dijalankan menggunakan node process secara langsung.
- memasang pm2 di ssh
  <br>![image](https://user-images.githubusercontent.com/85721388/226087647-8823a982-6030-4dd3-8215-ff910f5f991d.png)
- menjalankan proses pm 2
  <br>![image](https://user-images.githubusercontent.com/85721388/226087663-6a262bc1-aaa1-457d-bc0e-0ecdb1b43581.png)
- me-restart proses secara manual  
  <br>![image](https://user-images.githubusercontent.com/85721388/226087679-a1f55012-943d-4a47-962c-eada16d50350.png)
- Kita bisa juga menghentikan prosesnya dengan cara:
  <br>![image](https://user-images.githubusercontent.com/85721388/226087686-b4c19b56-5ece-45f1-895d-ab0104931af6.png)
- Untuk menjalankan kembali proses, gunakan perintah:
  <br>![image](https://user-images.githubusercontent.com/85721388/226087688-1f486bab-25bd-4800-a8c7-85279450d373.png)
