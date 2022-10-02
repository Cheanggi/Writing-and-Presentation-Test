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
- 
