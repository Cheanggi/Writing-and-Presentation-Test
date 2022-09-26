# Writing Summary Week 1
## Day 1 : Unix Command Line
- Shell merupakan program yang memproses perintah kemudian mengintruksikan ke sistem operasi.
- Command Line Interface (CLI) merupakan jenis shell yang berbasis teks.
- Untuk mengakses CLI pada windows bisa menggunakan Powershell atau command prompt (cmd), sedangkan pada linux menggunakan bash.
- File system structure merupakan cara sistem operasi mengatur bentuk struktur dari file dan direktori dalam bentuk pohon.

### Navigasi Command
- pwd : untuk menampilkan direktori yang sedang digunakan saat ini.
- ls  : untuk melihat isi file direktori
- cd  : untuk berpindah direktori

### File/Directory Manipulation Command
- mkdir : untuk membuat folder direktori
- touch : untuk membuat file
- cat   : untuk melihat isi file
- cp -r : untuk menyalin direktori
- cp    : untuk menyalin file
- mv    : untuk memindahkan atau merename file dan direktori
- rm -r : untuk menghapus direktori
- rm    : untuk menghapus file

## Git dan Github
- Git dan Github merupakan tools wajib digunakan oleh programmer karena dapat berkolaborasi untuk mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate.
- git adalah software berbasis version control system (vcs) yang dapat melacak perubahan seluruh file atau repository suatu project.
- github merupakan layanan cloud yang berguna untuk menyimpan dan mengelola Git Repository.

### Perintah dasar Github
- Setup awal git
```git
$git config --global user.name "usename"
$git config --global user.email "email"
$git config --list
```

- Perintah untuk melakukan inisialisasi pada git (membuat Repository)
```git
$git init <nama-repo>
$git init .
```

- Perintah untuk melakukan commit pada git
```git
$git commit -m "isi-commit"
```

Perintah untuk mempublish aplikasi ke github
```git
$git remote add origin <link-repo>
$git push -u origin <nama-branch>
```

Perintah untuk melakukan clone github
```git
$git clone <link-repo>
```

## Day 2 : HTML
- Hypertext Markup Language (HTML) berfungsi untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet.
- Tools pendukung dalam HTML adalah web browser dan code editor (visual studio code, sublime, dll)
- Struktur HTML sederhana (BIODATA)
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Dasar</title>
</head>
<body>
    <table border="1">
        <tr>
            <td align="center" colspan="3">
                <b>BIODATA</b>
            </td>
        </tr>
        <tr>
            <td rowspan="5">
                <img src="woman.png">
            </td>
            <td>Nama</td>
            <td>Chea anggi</td>
        </tr>
        <tr>
            <td>Track</td>
            <td>Front-End Development</td>
        </tr>
        <tr>
            <td>Kelompok Gabungan</td>
            <td>FEBE 22</td>
        </tr>
    </table>
</body>
</html>
```

- Tag HTML




