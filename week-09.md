# Rangkuman Materi Minggu ke-9
## Day 1 : JavaScript Intermediate - Asynchronous - Fetch and Async Await
- fetch : objek promise {melakukan network request)
  ```
  fetch("input alamat API/URL")
  .then(result => {
    console.log(result);
    return result.json()
  })
  .then (result => {
    console.log(result) //output : mendapat data dari alamat API/URL.
  })
  ```
- fetch => async await
  ```
  let namaVariabel = async () => {
    let response = await fetch("alamat API")
    let result = await response.json()
    console.log(result);
  }
  namaVariabel()
  ```
- async: mengubah function synchronous menjadi asynchronous.
- await: menunda eksekusi hingga proses asynchronous selesai.
- cara membuat async await :
  - harus ada objek promise 
  - buat async function
  - try catch()
    ```
    let nonton = (kondisi) => {
      return new Promise((resolve, reject) => {
        if (kondisi == "jalan") {
          resolve("nonton terpenuhi")
        }
        reject("batal nonton")
      })
    }
    
    async function asyncNonton() {
      let result = await nonton ("jalan") => ada argumen.
      console.log(result);
    }
    asyncNonton() //output: nonton terpenuhi.
    
    async function asyncNonton() {
      try {
        let result = await nonton () => tidak ada argumen
        console.log(result);
      }catch (error) {
        console.log(error)
      }
    }
    asyncNonton() //output: batal nonton
    ```
    
## Day 2 : Git dan Github Lanjutan
- membuat satu repo per kelompok.
- membuat sebuah branch baru dengan nama dev.
- invite member
- akses dibuat owner
