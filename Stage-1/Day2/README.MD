# Linux Command
Perintah yang diberikan kepada sistem operasi linux untuk menjalankan suatu tugas atau aktivitas tertentu

## sudo
Perintah untuk menjalankan suatu program sebagai super user
```bash
sudo apt update
```
```bash
sudo apt upgrade
```

## mkdir
Perintah untuk membuat suatu directory
```bash
mkdir folder1
```

## rmdir
Perintah untuk menghapus suatu directory
```bash
rmdir folder1
```

## ls
Perintah untuk melihat list apa aja yang ada di directory
```bash
ls
```

## ls -la
Perintah untuk melihat semua list serta menampilkan yang tersembunyi
```bash
ls -la
```

## touch
Perintah untuk membuat suatu file
```bash
touch file1
```

## rm
Perintah untuk hapus file
```bash
rm file1
```

## rm -rf folder1
Perintah untuk menghapus folder & folder yang ada isinya
```bash
rm -rf folder1
```

## cd
Perintah untuk masuk directory
```bash
cd folder1
```

## cd ..
Perintah untuk keluar directory
```bash
cd ..
```

## cp
Perintah untuk mengcopy file serta mengubah namanya
```bash
cp file1 file2
```

## mv
Perintah untuk merename file dan memindahkan file kedalam suatu folder
```bash
mv file1 file3
```
```bash
mv file3 folder1
```

## echo
Perintah untuk menampilkan suatu inputan atau menambahkan suatu teks kedalam file
```bash
echo "hello teguh" > file1
```
```bash
echo "hello teg" >> file1
```

## cat
Perintah untuk menampilkan isi file
```bash
cat file1
```
## find
Perintah untuk mencari suatu file maupun directory dimana f untuk file dan d untuk directory
```bash
find -type f -name file1.html
```
```bash
find -typer d -name folder1
```

## grep
Perintah untuk mencari teks dengan menghighlight teks yang kita cari, untuk mencari teks di seluruh file menggunakan -r
```bash
grep hellow file1.html
```
```bash
grep -r hellow
```

## history
Perintah untuk menampilkan riwayat perintah yang kita sudah gunakan
```bash
history
```
Perintah untuk menampilkan riwayat berdasarkan teks yang dicari
```bash
history | grep hello
```

## chmod
Perintah untuk mengganti permission file ataupun directory. r = read(4), w = write(2), x=execute(1) dengan full permission 777.
```bash
sudo chmod +x index.html
```
```bash
sudo chmod 777 index.html
```

## chown
Perintah untuk mengganti kepemilikan sebuah file ataupun directory, seperti mengganti kepemilikan default sebagai ubuntu menjadi root
```bash
sudo chown root:root index.html
```

## ping
Perintah untuk mengetes koneksi internet
```bash
ping google.com
```

## wget
Perintah untuk mendownload suatu file. Contoh menggunakan link https://wordpress.org/latest.zip
```bash
wget https://wordpress.org/latest.zip
```

## unzip
Perintah untuk meng ekstrak file .zip. Untuk menginstal perintah unzip bisa menggunakan perintah :
```bash
sudo apt install unzip
```
Sekarang bisa mengeksrtrak zip menggunakan perintah :
```bash
unzip latest.zip
```

## zip
Perintah untuk mengkompres suatu file atau directory menjadi .zip. Untuk menginstal perintah zip bisa menggunakan perintah :
```bash
sudo apt install zip
```
Sekarang bisa mengkompres file atau directory menjadi .zip
```bash
zip -r wordpress.zip wordpress
```

## adduser
Perintah untuk membuat user baru
```bash
sudo adduser teguh
```

## usermod
Perintah untuk menambahkan group user yang kita buat ke root
```bash
sudo usermod -aG sudo teguh
```

## sudo su
Perintah untuk bisa masuk ke sistem root dan bisa juga unutk ganti user
```bash
sudo su
```
```bash
sudo su ubuntu
```




















