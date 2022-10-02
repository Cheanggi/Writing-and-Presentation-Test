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
