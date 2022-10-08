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
