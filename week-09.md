# Rangkuman Materi Minggu ke-9
## Day 1 : JavaScript Intermediate - Asynchronous - Fetch and Async Await
- async: mengubah function synchronous menjadi asynchronous.
- await: menunda eksekusi hingga proses asynchronous selesai.
-  cara membuat async await :
  - buat async function
  - try catch()
    ```
    let nonton = (kondisi) => {
      return new promise((resolve, reject) => {
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
        console.log(error); //output: batal nonton
      }
    }  
    ```
