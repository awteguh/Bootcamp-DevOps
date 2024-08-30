# Text Manipulation
Pada dasarnya kita bisa manipulasi pada sebuah file menggunakan terminal, tanpa menggunakan teks editor seperti nano

## Cat
Pada dasarna `cat` tidak hanya perintah untuk menampilkan isi dari sebuah file, tetapi juga bisa berfungsi sebagai perintah untuk manipulasi teks.
```bash
Cat file1
```
Perintah untuk menampilkan isi file1

```bash
cat > file1
```
Ketika kita mengetikan perintah ini maka selanjutnya kita bisa mengisi teks yang kita inginkan, Ctrl C untuk mengakhiri perintah

```bash
cat >> file1
```
Perintah untuk menambahkan isi teks dari file1

```bash
cat file1 file2 > file3
```
Perintah untuk menggabungkan isi teks dari file1 dan file2 menjadi file3

## Sed
Stream editor, memanipulasi teks pada file dengan cepat
```bash
sed -s/Hello/Hai/g' file1
```
Mengganti kata `Hello` menjadi `Hai` pada file1

## Sort
```bash
sort file1
```
Mengurutkan angka secara ascending

```bash
sort -r file1
```
Mengurutkan angka secara descending

