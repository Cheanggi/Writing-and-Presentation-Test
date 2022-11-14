# Rangkuman Materi Minggu Ke-13
## Day 1 : React Context
- Context menyediakan cara untuk berbagi nilai seperti ini di antara komponen tanpa harus oper prop secara explisit melalui setiap tingkatan diagram.
- React.createContext
  ```
  const MyContext = React.createContext(defaultValue);
  ```
- Argumen defaultValue hanya digunakan ketika komponen tidak memiliki Provider yang cocok di atasnya dalam diagram.
- Context.Provider
  ```
  <MyContext.Provider value={/* beberapa nilai */}>
  ```
- Semua consumer yang merupakan keturunan Provider akan render ulang setiap kali prop value dalam Provider berubah.

## Day 2 : 
