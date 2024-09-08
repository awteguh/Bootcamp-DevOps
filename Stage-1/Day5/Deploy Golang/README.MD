# Golang
Bahasa Go, atau sering disebut Golang, adalah bahasa pemrograman yang dikembangkan oleh Google pada tahun 2007 dan dirilis secara publik pada tahun 2009. Go dirancang oleh tiga insinyur Google: Robert Griesemer, Rob Pike, dan Ken Thompson, dengan tujuan untuk menciptakan bahasa yang efisien, sederhana, dan mudah digunakan untuk pengembangan sistem modern, terutama di lingkungan server dan aplikasi yang terdistribusi.


## Konfigurasi
mendownload engin nya terlebih dahulu
```bash
wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su
```
jika sudah masukan path ini
```bash
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit
```
selanjutnya masukan pasth go pada `.bashrc`
```bash
sudo nano .bashrc
```
```bash
export PATH=$PATH:/usr/local/go/bin
```
jika sudah cek versi go
```bash
go version
```
sekarang bisa mebuat aplikasi sederhana menggunakan `go`. lalu membuat file `index.go` dan konfigurasinya
```bash
nano index.go
```
```bash
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
```
untuk menjalankan aplikasi menggunakan perintah
```bash
go run index.go
```
jika  konfigurasi aplikasi yang terbuat ingin di build menjadi aplikasi
```bash
go build index.go
```
sekrang sudah menjadi aplikasi, dah untuk menjalankan perintahnya
```bash
./index
```
