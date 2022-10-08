# Rangkuman Materi Minggu Ke-8
## Day 1 : Js Intermediate - Array dan Multidimensional Array 
- Array adalah tipe data yang dapat menyimpan tipe data apapun di dalamnya.
- Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.
- Array pada javascript dihitung dari index data ke-0.
- cara membuat array menggunakan tanda [].
  ```
  let arr = ["mangga", 8, true]
  console.log(arr[0]) //output: mangga
  console.log(arr[1]) //output : 8
  console.log(arr[2]) //output : true
  ```
- Array.length : mengecek jumlah isi data array.
  ```
  let arr = ["mangga", 8, true]
  console.log(arr.length); //output: 3
  ```
- Array.push : menambahkan data baru diakhir ke dalam array.
- Array.unshift :menambahkan data baru diawal ke dalam array.
- Array.pop : menghapus data terakhir dalam array.
- Array.shift : menghapus data awal dalam array.
- Array.splice: mengubah konten yang ada di dalam array dengan menghapus atau menggantinya.
- Arraty.slice() : mengambil dengan cara mengcopy data array.
  ```
  let buah = ["salak", "apel", "anggur"]
  buah.push("nanas", "kiwi"); //output: ["salak", "apel", "anggur", "nanas", "kiwi"]
  buah.unshift("duku"); //output: ["duku", "salak", "apel", "anggur", "nanas", "kiwi"]
  buah.pop(); //output: ["duku", "salak", "apel", "anggur", "nanas"]
  buah.shift(); //output: ["salak", "apel", "anggur", "nanas"]
  ```
- cara kedua mengubah data array.
  ```
  let hewan = ["kuda", "gajah"]
  hewan[0] = "semut"
  console.log(hewan) //output : ["semut", "gajah"]
  ```
  
- Array loop (for) dan (for..of..)
  ```
  for(let i = 0; i < buah.length; i++) {
    console.log(buah[i]) //ouput : salak, apel, anggur.
  }
  
  for(let i = buah.length - 1; i > 0; i--) {
    console.log(buah[i]) //ouput : anggur, apel, salak.
  }
  
  for(let arrBuah of buah) {
    console.log(arrBuah); /output : salak, apel, anggur.
  }
  ```
- forEach dan map (mengembalikan nilai dalam bentuk array)
  ```
  namaArray.forEach((item, index) => {
    console.log(index, item)
  })
  
  namaArray.map((item, index) => {
    console.log(item);
  })
  ```
  
- Multidimensional Array (array dalam array)
  ```
  let arrMulti = [
    ["nama", "beta"],
    ["umur", 18],
    ["kelas", "JS"],
  ]
  
  console.log(arrMulti[0]baris[1]kolom); //output : beta
  ```

## Day 2 : JS Intermediate Object
- object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)
- object dapat menyimpan banyak data.
  ```
  let siswa = {
    nama: "sarah",
    umur: 18,
    hobi: "menyanyi",
    "nomor handphone": 081278456199, // properti yang menggunakan spasi bisa ditambahkan string ("").
  };
  
  console.log(siswa); //output: {nama: 'sarah', umur: 18, hobi: 'menyanyi', nomor handphone: 081278456199}
  ```
  
- cara akses objek ada 2 :
  - . dot notation // tidak bisa mengeksekusi properti yang menggunakan spasi
    ```
    let siswa = {
      nama: "sarah",
      umur: 18,
      hobi: "menyanyi",
      "nomor handphone": 081278456199,
    };
    
    console.log(siswa.nama); //output: sarah
    ```
  - [] bracket notation // bisa mengeksekusi properti yang menggunakan spasi
    ```
    let siswa = {
      nama: "sarah",
      umur: 18,
      hobi: "menyanyi",
      "nomor handphone": 081278456199,
    };
    
    console.log(siswa["hobi"]); //output: menyanyi
    ```
    
- cara membuat properti baru.
  ```
  let buku = {
    judul: "hujan",
    penulis: "teresia",
    "jumlah halaman": 200,
  };
  
  buku.tahun = 2020; // penambahan properti: dengan memanggil objek ditambah dot notation ditambah nama properti yang baru.
  buku["penerbit"] = "gramedia"; // cara kedua penambahan properti dengan bracket ([""])
  console.log(buku); // output: {judul: 'hujan', penulis: 'teresia', jumlah halaman: 200, tahun: 2020, penerbit: 'gramedia'}
  ```
  
- cara mengganti value dari objek
  ```
  let hewan = {
    nama: "kucing",
    kaki: 4,
    warna: "putih",
  };
  hewan.warna = "coklat";
  hewan["warna"] = "coklat";
  console.log(hewan); //output: {nama: 'kucing', kaki: 4, warna: 'coklat'}
  ```
 
- cara menghapus isi objek
  ```
  let hewan = {
    nama: "kucing",
    kaki: 4,
    warna: "putih",
  };
  delete hewan.warna;
  console.log(hewan); //output: {nama: 'kucing', kaki: 4}
  ```
  
- method
  ```
  console.log(Object.keys(namaObject)); //output : properti objek
  console.log(Object.value(namaObject)); //output: value objek
  ```
  
- nested objek (objek di dalam objek)
  ```
  console.log(namaObject.properti1.properti2.properti3); //output: properti objek yang diminta.
  ```
  
- loop objek
  - for in
    ```
    for (let key in namaObjek) { //key = properti
      console.log(namaObjek[key]); //output: value dari properti objek
    }
    ```
    
 - Array objek
   ```
   [{}, {}, {}]
   
   (perulangan array)
   let newVariable = namaVariable.map((x) => { //x : contoh penamaan (bebas).
      console.log(x.properti); //output: value properti.
   (menambahkan properti)
      x.newProperti = "value";
      return x;
   })
   
   (memanggil index array dalam objek)
   console.log(namaVariable[index]) //output: properti dan value
   console.log(namaVariable[index].properti) //output: value properti
   ```

## Day 3 : Js Intermediate-Recursive dan Modules
- Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
- Struktur dasar function rekursif adalah sebagai berikut:
  ```
  function namaFuncRekursif() {
    if (condition) {
      // Base case
    } else {
      // Recursion call
      namaFuncRekursif();
    }
  }
  ```

- Modules adalah cara untuk memisahkan kode ke file yang berbeda.
- Export digunakan untuk meng-export variabel pada file JavaScript. Variabel (string, object, array, hingga function).
- contoh export pada objek Js :
  ```
  export let orang = {
    nama: "Radit",
    umur: 25,
    alamat: "Jl. Dukuh Raya",
  };
  ```
- import berfungsi untuk menggunakan variabel yang sudah di-export dari module lainnya.
- contoh import variabel :
  ```
  import { data } from "./namaModul.js";
  ```
- Export As dan Import As : memberi alias (nama pengganti) pada nama data yang ingin kita export maupun import.
  ```
  export namaVariabelLama as namaVariabelBaru;
  import { namaVariabelLama as namaVariabelBaru } from "./namaModul.js";
  ```
- export default digunakan untuk membuat salah satu variabel menjadi data utama yang akan di-export pada sebuah module.
  ```
  export default data;
  import data from "./namaModul.js";
  ```
  
## Day 4 : JavaScript Intermediate - Asynchronous - Introduction dan Promise
- Synchronous adalah saat kita mengeksekusi perintah satu persatu dan berurutan.
- Asynchronous berfungsi untuk memproses perintah lain sambil menunggu suatu proses lain yang sedang berlangsung.
- untuk membuat proses asynchronous ada 2 cara:
  - setTimeout(function, milliseconds) // Pemanggilan hanya dilakukan 1 kali.
  - setInterval(function, milliseconds) // Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan.

- promise
- contoh penggunaan promise
```
  let newPromise = new Promise((resolve, reject) => {
  if (true) {
    // apa yang dilakukan jika promise fulfilled
    resolve("Berhasil");
  } else {
    // apa yang dilakukan jika promise rejected
    reject("Gagal");
  }
});
```
  - resolve(), jika proses berhasil atau fullfilled.
  - reject(), jika proses gagal atau rejected.

## Day 5 : Js Intermediate-Web Storage
