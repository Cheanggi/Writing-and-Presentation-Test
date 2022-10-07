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
- Array.splice: mengubah konten yang ada di dalam array dengan menghapus atau menggantinya. (menghapus data tengah)
- Arraty.slice() : mengambil dengan cara mengcopy data array.
  ```
  let buah = ["salak", "apel", "anggur"]
  buah.push("nanas", "kiwi"); //output: ["salak", "apel", "anggur", "nanas", "kiwi"]
  buah.unshift("duku"); //output: ["duku", "salak", "apel", "anggur", "nanas", "kiwi"]
  buah.pop(); //output: ["duku", "salak", "apel", "anggur", "nanas"]
  buah.shift(); //output: ["salak", "apel", "anggur", "nanas"]
  ```
- 
