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
- Tahapan yang dilakukan oleh team lead.
  1. team lead membuat repo untuk project yang akan dibuat.
  2. invite anggota tim dan jadikan akses sebagai owner.
  3. repo dibuat public, dan ceklis README.
  4. buat branch bernama dev
  
- Mengecek pull request
  - setiap ada pull request, team lead akan mengeceknya.
  - jika pull request belum sesuai, bisa dikasih komen untuk anggota yang melakukan pull request tersebut.
  - jika sudah selesai, lakukan merge.
   
### Kolaborasi
- Tahapan yang dilakukan anggota
  1. masing-masing anggota lakukan clone pada repo yang sudah dibuat(1x)
  2. bagi tugas pada masing-masing anggota kelompok 
  3. sebelum ngoding lakukan git pull untuk update kode terbaru
  4. anggota membuat branch dari dev
  5. melakukan pengerjaan di dalam branch yang sudah dibuat.
  6. jika fitur sudah selesai/butuh kode dari dev, lakukan commit seperti biasa
  7. sebelum push, lakukan git merge dev untuk menghindari conflict di github.
  8. jika ada conflict, bereskan semuanya.
  9. jika sudah aman, commit lalu push branch ke github.
  10. lakukan pull request untuk merge ke branch dev
  11. tunggu pull request di acc oleh team lead

## Day 3 : Responsive Web Design dan Bootstrap 5
