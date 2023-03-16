# Response Status

- Status line atau bisa kita sebut response status.
  - Response status merupakan salah satu bagian dari respons yang berisikan tentang informasi apakah sebuah request berhasil atau gagal dilakukan
  - Status code haruslah bernilai 3 digit angka dengan ketentuan berikut:
    - 100-199: informational responses.
    - 200-299: successful responses.
    - 300-399: redirect.
    - 400-499: client error.
    - 500-599: server errors.
  - penetapan nilai status code pada response dilakukan melalui properti response.statusCode
    <br>![image](https://user-images.githubusercontent.com/85721388/225549973-68ffe43e-eaaa-4caf-a6d2-e1871a54d200.png)
  - Latihan
    <br>![image](https://user-images.githubusercontent.com/85721388/225551182-e3173c0c-9ddf-4b55-83b4-e5f865ee8e5f.png)
    <br>![image](https://user-images.githubusercontent.com/85721388/225551333-be1b56d2-d6b2-4c50-8785-664299701b5b.png)

# Response header
  - method setHeader() : Untuk menyisipkan nilai pada header response
    <br>![image](https://user-images.githubusercontent.com/85721388/225551747-e4822969-9a59-4d5f-92a2-89ac8cfb1589.png)
    <br>![image](https://user-images.githubusercontent.com/85721388/225551883-c8f8bedb-aceb-4f37-865b-7e0927b9c013.png)
    <br>![image](https://user-images.githubusercontent.com/85721388/225619143-b1c0d525-cfe5-49ca-bea5-0ea93dd50c1d.png)
  - Link referensi : https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers

# Response body
