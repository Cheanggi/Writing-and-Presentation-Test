# Rangkuman Materi Minggu Ke-13
## Day 1 : React Context
- Context menyediakan cara untuk berbagi nilai seperti ini di antara komponen tanpa harus oper prop secara explisit melalui setiap tingkatan diagram.
- React.createContext
  ```
  const MyContext = React.createContext(defaultValue);
  ```
- Fungsi createContext mengembalikan komponen Penyedia dan Konsumen.
- Argumen defaultValue hanya digunakan ketika komponen tidak memiliki Provider yang cocok di atasnya dalam diagram.
- Context.Provider
  ```
  <MyContext.Provider value={/* beberapa nilai */}>
  ```
- Semua consumer yang merupakan keturunan Provider akan render ulang setiap kali prop value dalam Provider berubah.

## Day 2 : React Context with useReducer
- useReducer adalah pengait yang memungkinkan kita untuk mengelola logika keadaan yang kompleks.
- useReducer umumnya digunakan sebagai pengganti useState dalam suatu komponen, karena dapat memecahkan masalah yang sama.
- contoh :
  ```
  const initialState = {
  theme: 'light',
  }

  const [state, dispatch] = useReducer(ourReducer, initialState)
  ```

## Day 3 : React Testing
- unit testing adalah jenis software testing yang dilakukan untuk menguji suatu bagian atau komponen software.
- Unit dapat berupa fungsi, metode, prosedur, modul, atau objek individual.
- react-testing-library
  ```
  npm install --save-dev @testing-library/react
  ```
- Untuk menggunakan Jest pada aplikasi kita, kita terlebih dahulu memasukan library Jest ke dalam proyek kita.
  ```
  yarn add — dev jest
  ```

