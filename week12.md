# Rangkuman Materi Minggu Ke-12
## Day 1 : React Js Lanjutan - PropTypes
- PropTypes adalah sebuah library yang dapat membantu untuk memeriksa data props agar sesuai dengan ekspetasi.
- jika tidak sesuai akan muncul pesan error.
- cara install PropTypes :
  ```
  npm install prop-types
  ```
- Props yang akan dikirim harus sesuai dengan tipe data yang diinginkan.
- PropTypes.element dapat menentukan bahwa hanya menerima satu komponen anak yang dapat dikirimkan ke komponen lain.
- Properti defaultProps akan digunakan untuk memastikan bahwa this.props.name akan memiliki sebuah nilai jika tidak ada nilai yang diberikan oleh komponen induknya.

## Day 2 : React Router 6
- cara install react router
   ```
   npm i react-router-dom
   ```
- konfigurasi router untuk web dapat menggunakan <BrowserRouter> dan untuk mobile dapat menggunakan <NativeRouter>.
- Mendefinisikan route mudah untuk mendefinisikan satu komponen route untuk setiap route dalam aplikasi dan kemudian menempatkan semua komponen route tersebut dalam satu komponen route.
- contoh :
  ```
  <Route path="/books" element={<BookList />} />
  ```
- contoh di atas jika URL kita adalah /books maka komponen BookList akan dirender.
- React Router menggunakan komponen Link kustomnya sendiri untuk menangani navigasi.
- untuk mengatur URL Link pada react menggunakan prop to, contoh :
  ```
   <li><Link to="/books">Books</Link></li>
   ```
- route adalah sebuah component yang mana akan menampilkan sebuah halaman apabila URL yang diberikan itu sesuai.
- Setiap list Route yang ingin kita daftarkan atau gunakan harus dibungkus atau menjadi children dari component menggunakan Routes.
- agar dapat melakukan handling halaman 404 dapat menggunakan simbol *
- Jika memutuskan ingin menggunakan useRoutes, kaitkan semua props yang biasanya diberikan ke komponen Route hanya diteruskan sebagai pasangan kunci/nilai dari suatu objek.
- Parameter pencarian adalah semua parameter yang muncul setelah ? di URL (?name=Kyle&age=27)

## Day 3 & 4 : State Management React-Redux
- Redux berfungsi untuk melakukan perubahan state yang dibutuhkan oleh setiap fungsional yang ada di suatu aplikasi.
- react redux adalah library untuk menghubungkan react dan reduxnya.
- Redux memiliki tiga komponen utama yaitu action, reducer, dan store.
- action : cara agar dapat mengirim data dari aplikasi ke Redux Store. Data tersebut dapat berasal dari interaksi pengguna, panggilan API (API request), atau bisa juga pengiriman formulir. 
- Action harus berisikan type property dan kemudian payload atau muatan yang lain pun dapat disimpan.
- Reducer berfungsi untuk melakukan tindakan,dan mengembalikan status baru (new state).
- Ada 2 parameter wajib dari reducer, yaitu state dan action.
- Store berfungsi untuk menyimpan status aplikasi. dapat mengakses status yang disimpan, mengupdate status, dan mendaftarkan atau membatalkan pendaftaran listener melalui metode helper.

## Day 5 : State Management Async Actions with Redux Thunk and Middleware
- Redux Thunk adalah middleware yang memungkinkan untuk memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi.
- Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.
- cara menambahkan redux thunk menggunakan terminal
  ```
  npm install redux-thunk@version
  ```
- dispatch : metode yang digunakan untuk mengirimkan tindakan, yang dapat diterima oleh reduksi.
- getState : memberikan akses untuk menyimpan di dalam fungsi thunk.
- gunakan useDispatch untuk mengirim tindakan dan useSelector untuk mengakses data di store.
