# Git
Ada 2 Developer yang sedang melakukan development aplikasi dari perusahaan A sebut saja Reyhan dan Teguh mereka kebetulan sedang mengerjakan suatu proyek yang sama, dan mereka sedang mengerjakan file yang sama index.html. Reyhan membuat perubahan pada file index.html dan melakukan commit: git add index.html; git commit -m "fix: Typo on Description". Teguh kebetulan juga membuat perubahan pada index.html dan melakukan commit: git add index.html ; git commit -m "feat: Header Adjustment". Kemudia disini ternyata Reyhan melakukan push ke repository. Teguh, yang belum melakukan push, mencoba untuk melakukan push ke repositori. Karena ternyata ada perubahan baru di remote yang belum dimiliki Teguh, Git menolak push Teguh dan memberi tahu bahwa ada konflik. Disini Teguh harus melakukan Fix Conflict tersebut agar perubahan yang di buat oleh Teguh dapat tersimpan ke dalam repositori app tersebut. lalu bagaimana cara menangani case yang dimiliki oleh Teguh?

## Installation git
```bash
sudo apt install git
```
pada dasarnya git sudah terinstal pada linux, jika belum bisa menggunakan command ini

## Git Config
```bash
git config --global user.name "your.github-user.name"
```
```
git config --global user.email "your.github-user.email"
```
pastikaan user dan email sesuai dengan akun github

```bash
git config --list
```
untuk melihat nama user dan email yang terhubung

## SSS Keygen
```bash
ssh-keygen
```
untuk mendapatkan kunci ssh
```bash
cat .ssh/id_rsa.pub
```
ketika sudah menggenerate kunci ssh maka akan terdapat kunci unik yang berada pada file di atas, dan isi dari kunci tersebut di salin di masukan ke akun github di bagian pengaturan, ssh key, tempel kunci uniknya dan add ssh key

## Cek koneksi
```bash
ssh -T git@github.com
```
untuk mengecek koneksi local kita sudah terkoneksi dengan github atau belum

## Repository
```bash
git init taskprojek
```
ini akan membuat nama folder yang akan di gunakan di local
```bash
mkdir taskprojek
```
```bash
cd taskprojek
```
```bash
git ini
```
atau bisa menggunakan command ini

## Git Ignore
`.gitignore` sebuah file yang berisi file dan directory yang diasingkan /abaikan oleh git. Perubahan apapun yang kita lakukan terhadap file dan direktori yang sudah masuk ke dalam daftar .gitignore tidak akan dicatat oleh git.

*Pertama membuat beberapa file
```bash
touch file1 file2 file3
```
*Cek status file yang terbuat
```bash
git status
```
*Membuat file ignore terlebih dahulu untuk menampung file yang akan di abaikan
```bash
touch .gitignore
```
*Untuk mengabaikan file3, masukan `file3` kedalam file .gitignore menggunakan teks editor nano
```bash
sudo nano .gitignore
```
*Jika sudah cek status file3 apakah terbaca atau tidak
```bash
git status
```

## Git add / Stage
```bash
git add file1
```
perintah untuk menandai file sebelum melakukan commit
```bash
git add *.html
```
perintah untuk melakukan stage pada semua file yang berakhiran .html
```bash
git add .
```
perintah untuk menandai file yang akan di commit

## Git Commit
``` bash 
git commit -m "pesan yang akan di tulis/commit"
```
perintah untuk menyimpan file kedalam data base git dengan menggunakan pesan commit

## Git remote
Login github lalu pili new repository
```bash
git remote add origin git@github.com:nama repository/nama folder.git
```
copy link tersebut dari github pada bagian ssh

```bash
git remote -v
```
untuk melihat remote yang kita gunakan

## Push
proses upload data local kita ke github
```bash
git push origin master
```
master merupakan branch default yang ada di local kita, sekarang file local kita sudah terupload pada github

## Git Branch
```bash
git branch namabrach
```
perintah untuk mengcloning folder dari repository
```bash
git checkout namabranch
```
untuk pindah branch
```bash
git branch -m (name branch)
```
untuk membuat nama branch serta pindah langsung ke dalam branch tersebut
```bash
git branch - a
```
untuk melihat daftar nama branch

## Pull
```bash
git pull origin namabrach
```
perintah untuk menyamakan perubahan yang terjadi pada server git

## Merge
```bash
git merge master
```
untuk menggabungkan file yang ada di master kedalam development


## konfigurasi
```bash
git checkout master
```
Selanjutnya pindah branch master
```bash
nano index.html
```
melakukan perubahan/menambah isi pada file html
```bash
git add index.html
```
menandai file yang akan di commit
```bash
git status
```
untuk melihat status perubahan
```bash
git commit -m "fix: Typo on Description"
```
file siap untuk di upload ke github
```bash
git push origin master
```
maka file sudah terupload pada github dan update pada branch master

```bash
git checkout development
```
pindah branch development
```bash
nano index.html
```
melakukan perubahan/menambah isi pada file html
```bash
git add index.html
```
menandai file yang akan di commit
```bash
git status
```
untuk melihat status perubahan
```bash
git commit -m "feat: Header Adjustment"
```
file siap untuk di upload ke github
```bash
git push origin development
```
maka file sudah terupload pada github dan update pada branch development

File index.html isinya berbeda berdasarkan branch
