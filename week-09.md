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
- Responsive web design bertujuan membuat desain website dapat diakses dalam device apapun.
- Device yang umum digunakan seperti laptop/PC, smartphone dan tablet.
- viewport adalah area website yang dapat diakses oleh user.
  ```
  <meta name="viewport" content="width=device-width; initial-scale=1.0">
  ```
- **max-widht** (css): teknik kedua untuk membuat responsive web.
- Css unit :satuan ukur yang bersifat relative.
  - Absolute lengths : px
  - Relative lengths : em, rem, %, vw, vh
  ```
  font-size untuk html : 16px
  font-size: 2rem // 32px
  font-size: 2em // dikalikan dengan parent terdekat.
  ```
- Media query memberikan kemampuan menggunakan kode css yang sesuai dengan kondisi yang ditentukan. 
- 2 jenis media query : max-widht dan min-widht.
  ```
  @media screen and (min-widht: your pixel) {
  @media screen and (max-widht: your pixel) {
  ```
- properti flexbox(parent)
  - flex-container
  - flex-direction
  - flex-wrap
  - flex-flow
  - justify-content
  - align item
  - align-content
  - gap, row-gap, column-gap

- properti flexbox(child)
  - flex-item
  - flex-grow
  - flex-shrink
  - flex-basis
  - flex
  - align-self

- Properti display pada Grid Container (properti parent) harus bernilai grid, contoh:
  ```
  .container {
    display: grid;
  }
  ```
- Grid juga tersusun dari komponen berikut:
  - Grid Track merupakan baris atau kolom pada Grid.
  - Grid Line merupakan garis yang membatasi setiap Grid Track.
  - Grid Cell merupakan sel atau bagian terkecil dari Grid.
- Grid item (properti child)
  - contoh : Buat "item1" dimulai pada kolom 1 dan diakhiri sebelum kolom 5
    ```
    .item1 {
      grid-column: 1 / 5;
    }
    ````

### Bootstrap 5
- Bootstrap adalah framework web development berbasis HTML, CSS, dan JavaScript yang dirancang untuk mempercepat proses pengembangan web responsive dan mobile-first (memprioritaskan perangkat seluler).
- Developer memilih penggunaan Bootstrap dengan source code, karena lebih bebas menyesuaikan gaya dengan proyek yang dikerjakan.
- Sistem grid Bootstrap memiliki dua kelas container untuk mempermudah penanganan proyek berbasis desktop dan seluler: 
  - fixed container (.container) dan fluid container (.container-fluid).
