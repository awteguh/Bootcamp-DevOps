# nvm
Node Version Manager adalah command linux untuk memanage 2 versi node js yang berbeda, berpindah dari versi node ke versi node yang lain.


## nvm
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
```
instal nvm terlebih dahulu dengan mendownload terlebih dahulu
```bash
exec bash
```
untuk mengeksekusi file nvm yang berektensi bash agar bisa digunakan
```bash
nvm --version
```
untuk mengetahui version nvm
```bash
nvm i v14
```
untuk menginstal node js versi 14
```bash
nvm i 14
```
atau bisa menggunakan ini
```bash
node -v
``` 
untuk mengeetahui node js versi berapa yang di pakai
```bash
nvm use v14.21.3
``` 
untuk menggunakan nvm versi 14
```bash
git clone https://github.com/dumbwaysdev/dumbflix-frontend
```
mengclone aplikasi dari github dan akan di deploy


# npm
Node Package Manager adalah alat manajemen paket untuk JavaScript yang digunakan untuk mengelola dependensi (package) dalam proyek Node Js
```bash
npm init -y
```
jika memulai projek baru dan akan menghasilkan file `package.json`
```bash
npm install express --save
```
menginstal dependensial express yang ada di folder node_modules
```bash
npm install
```
untuk menginstal semua dependensial yang ada di folder node_modules
```bash
npm start
```
untuk menjalankan `aplikasi.js` yang ada

*jika buat simple aplikasi
buat file baru
```bash
nano index.js
```
```bash
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Hello World!");
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});
```
contoh aplikasi sederhana
```bash
node index.js
```
jalankan aplikasi tersebut, atu bisa menggunakan `npm start`

## pm2
command linux agar suatu aplikasi bisa berjalan pada background
```bash
npm install -g pm2
```
menginstall paket pm2
```bash
pm2 start npm -- start
```
menjalankan pm2 agar aplikasi berjalan di background
```bash
pm2 stop npm
```
menghentikan aplikasi agar tidak berjalan pada backgroud
