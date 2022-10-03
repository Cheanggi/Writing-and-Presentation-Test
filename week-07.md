# Writing Summary Week 07
## Day 1 : Js Dasar - Scope and Function
- Scope adalah konsep dalam flow data variabel.
- Blocks scope adalah code yang berada didalam curly brackets {}.
  - Conditional, function, dan  looping menggunakan blocks.
  - contoh :
    ```
    function greeting () {
      let namaSaya = "Sarah";
    }
    console.log(greeting()); //output : Sarah
    ```
- Local scope adalah variabel yang dideklarasikan di dalam fungsi pada Javascript.
  - contoh :
    ```
    function umurSaya () {
      let umur = 23;
    }
    console.log(umurSaya()); //output : 23
    ```
- Global scope adalah variabel yang dibuat di luar fungsi javascript
  - contoh :
    ```
    let namaSaya = "Andini";
    
    function greeting () {
      return namaSaya;
    }
    console.log (namaSaya); //output : Andini
    ```
    
- Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan satu task/ satu fitur.
  - Parameter adalah kondisi input yang harus dimasukkan ke dalam fungsi dan dideklarasikan dengan deklarasi fungsi.
  - Argumen adalah nilai yang digunakan saat memanggil function.
    ```
    function operasiPerkalian(angka1, angka2){
      return angka1 * angka2;
    }
    console.log(operasiPerkalian(2, 6)) //output: 12
    ```
  - Arrow Function adalah cara penulisan fungsi menjadi lebih singkat dan lebih mudah dibaca.
  - contoh :
    ```
    function greeting(nama) {
      return `Hi ${nama}`;
    }
    console.log(greeting('Tiara')); //output: Hi Tiara
    ```
    
    **kode diatas dapat disingkat menggunakan arrow function**
    ```
    const greeting = (nama) => `Hi ${nama}`;

    console.log(greeting('Tiara')); //output: Hi Tiara
    ```
    
  - Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.
  - contoh :
    ```
    function greetOnWebsite(nama = 'stranger'){
      return 'halo' + name;
    }
    console.log(greetOnWebsite('alma')); //output : halo alma
    console.log(greetOnWebsite()); //output : halo stranger
    ```
    
## Day 2 : 	Data Type Built in Prototype & Method
### string
  contoh :
  ```
  let hewan = "tikus";
  
  console.log("ini adalah " + tikus); // cara menyisipkan variabel ke dalam string versi 1
  cosole.log(`ini adalah ${hewan}`); // versi 2
  
  console.log(typeof hewan); //properti string => typeof : mengecek tipe data
  console.log(hewan.length); // length : untuk mengetahui jumlah karakter string
  
  console.log(hewan.toUpperCase()) // method adalah sebuah fungsi. toUpperCase()=> merapihkan string dengan huruf kapital.
  console.log(hewan.toLowerCase()) // toLowerCase() : merapihkan string dengan huruf kecil.
  
  console.log(hewan.charAt()) // charAt(index) : mengembalikan sebuah karakter berdasarkan pada posisi indexnya. index isi dengan number.
  consolo.log(hewan[1]) // versi 2
  
  console.log(hewan.include()) // include()) : pencarian, jika ditemukan nilainya true jika tidak nilainya false.
  ```
  
### Number
  - isNan() // Not a Number : mengecek apakah termasuk tipe data number atau tidak.
  - contoh :
    ```
    isNan(12345) // output : false, (Number)
    isNaN("banana") // output : true (string)
    isNaN(true) // output : false, karena true bernilai 1 pada boolean, maka bisa dianggap sebagai number.
    isNaN(false) // output : false, karena true bernilai 0 pada boolean, maka bisa dianggap sebagai number.
    isNaN("") // output : false, dianggap bernilai 0, maka bisa dianggap sebagai number.
    ```
    
  - toString : mengubah number menjadi sebuah string.
  - contoh :
    ```
    let angka = 18;
    angka.toString() //output : 18, versi 1
    
    18 + "" //alternatif versi 2
    ```
    
  - toFixed() : mengembalikan sebuah string dan menentukan jumlah angka dibelakang koma.
  - contoh :
    ```
    let pi = 3.1445654
    pi.toFixed(2) //ouput : '3.14' (string)
    Number(pi.toFixed(2)) //output : 3.14, mengubah string menjadi number
    ```
  
### Math : untuk mengolah data.
  - Properti math :
    ```
    Math.E               // Bilangan Euler
    Math.LN2             // Log 2 
    Math.LN10            // Log 10
    Math.LOG2E           // Log E di Basis 2
    Math.LOG10E          // Log E di Basis 10
    Math.PI              // Pi
    Math.SQRT1_2         // Akar Kuadrat dari 0.5
    Math.SQRT2           // Akar Kuadrat dari 2
    ```
  - method math :
    ```
    Math.abs(x) // mengubah angka x yang bernilai negatif menjadi positif.
    Math.pow(x, y) // menghitung hasil dari x pangkat y.
    Math.sqrt(x) // menghitung akar kuadrat dari x.
    Math.cbrt(x) // menghitung akar pangkat 3 dari x.
    Math.round(x) // membulatkan angka desimal x menjadi bilangan bulat.
    Math.max(x, y, z, ..., n) // mencari angka terbesar di antara parameter x, y, z, ..., n.
    ```

## Day 3 : Dom
- DOM (Document Object Model) adalah jembatan supaya bahasa pemrograman dapat berinteraksi dengan html.
### Selecting Element
  - getElementById(id) //  untuk mengakses element HTML berdasarkan nilai id-nya.
  - getElementsByName() // untuk mengakses element HTML berdasarkan nama.
  - getElementsByTagName(tag) // Untuk mengakses element-element HTML berdasarkan jenis tag-nya.
  - getElementsByClassName(className) // Untuk mengakses element-element HTML berdasarkan nilai attribute class-nya.
  - querySelector() // Untuk mengakses element-element HTML berdasarkan CSS Selector-nya HTML.
### Traversing Elements
- atas :
  - parentElement
  - closest()

- samping :
  - nextElementSibling
  - previousElementSibling
  
## Day 4 : DOM
- Manipulating element
  - innerHTML //sebuah atribut di dalam (objek) elemen HTML yang berisi string HTML (versi 1)
  - innerText // semua element yang dimasukkan akan berupa string (versi 2)
  ```
  let app = document.getElementById("app")
  
  console.log(app)
  
  app.innerHTML = "<h1>Halo</h1>" //output : Halo
  app.innerText = "<h1>Selamat Datang</h1>" //output : <h1>Selamat Datang</h1>
  ```
  
  - createElement() // membuat element menggunakan js
  - append() // menyisipkan sebuah element
  - contoh :
    ```
    let p = document.createElement("p")
    p.innerText = "ini adalah paragraf"
    
    app.append(p) //output : ini adalah paragraf
    ```
     
