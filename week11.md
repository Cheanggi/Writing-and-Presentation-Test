# Rangkuman materi minggu ke-11
## Day 1 : React Basic
- React Js adalah sebuah library javascript untuk membuat tampilan (user interface) pada website.
- React Js  dibuat oleh tim engineer Facebook.
- alternatif : angular, vue, svelte
- untuk menjalankan javascript diluar web browser dengan bantuan NodeJS.
- NodeJS berfungsi untuk menginstall react dan beberapa library.
- untuk membuat folder project baru menggunakan perintah :
  ```
  npx create-react-app nama-app
  cd nama-app
  npm start // npm : module package.
  ```
- perbedaan
  - real DOM : ada perubahan elemen maka merender node secara keseluruhan, seperti menambah atau menghapus elemen akan merender ulang.
  - virtual DOM : ada perubahan elemen maka merender node yang akan diubah, seperti ada perubahan pada elemen p maka merender pada bagian p saja.

## Day 2 : React Basic
- component adalah salah satu core dari React Js, bersifat reusable code.
- membuat component jika component tersebut dibutuhkan pada section atau page lain.
- ada 2 cara membuat component : function dan class
- membuat folder component dalam folder src.
- membuat namafile.jsx dalam folder component.
- untuk memanggil external css menggunakan perintah import ./namafile.css; pada file App.jsx
- class pada react menggunakan className.
- jika ingin menampilkan component di browser maka harus ditampilkan di file App.jsx dengan perintah import.
- state sebuah object untuk menyimpan data di react dan akan merender jika ada perubahan data dalam react. 
- props digunakan untuk komunikasi dari component parent ke component child, pengiriman data.
- useState : untuk menyimpan data yang sifatnya berubah-ubah.
- jika ingin menggunakan bootstrap (css dan js) bisa melalui cdn link bootstrap pada file index.html.
- cara kedua untuk menggunakan bootstrap dengan menginstall bootstrap lewat npm : npm install bootstrap.

## Day 3 : React Basic
- handle event : onClick={handleClick}, onMouseOver(hover)={handleMousOver}
- dalam event tidak harus ada state.
- cara handle event dapat menerima parameter menggunakan call back : {() => handleEvent}
- menambahkan argumen pada function yang ada dalam event dengan menjadikan call back ditambah argumen : {() => handleEvent("argumen")}
- solusi loop data array lalu ditampilkan
  ```
  {varaibel.map((item, index) => (
    <element atau component yang dibutuhkan/>
  ))}
  ```
