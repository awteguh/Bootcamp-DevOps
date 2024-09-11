# Implementasi Firewall pada Linux Server
* Buatlah 2 buah Virtual Machine.
* Study case nya adalah agar hanya server A yang hanya dapat mengakses WebServer yang ada pada server B.
* Carilah cara agar UFW dapat memblokir ataupun mengizinkan specific protocol jaringan seperti TCP dan UDP.
* Jelaskan perbedaan protocol Jaringan TCP serta UDP.

## ufw instal (konfigurasi pada server B)
langkah pertama melakukan instalasi ufw
```bash
sudo apt instal ufw -y
```

## ufw deny incoming
```bash
sudo ufw default deny incoming
```
memblokir semua akses yang masuk

## ufw allow outgoing
```bash
sudo ufw default allow outgoing
```
membuka semua akses yang keluar

## ufw app list
```bash
sudo ufw app list
```
untuk menampilkan aplikasi yang di dukubng ufw

## sudo ufw enable
```bash
sudo ufw enable
```
untuk menghidupkan firewalll

## konfigurasi 
```bash
sudo ufw allow from 192.168.1.10 to any port 80
```
hanya mengijinkan dari ip 192.168.1.10/server a ke server b

```bash
sudo ufw deny 80
```
memblokir semua akses ke port 80 dari alamat lain

```bash
sudo ufw allow 80/tcp
```
membuka akses untuk port 80 dengan koneksi tcp

## status verbose
```bash
sudo ufw status verbose
```
untuk melihat status apa saja yang ada

## delete
```bash
sudo ufw delete deny 80
```
menghapus konfigurasi, harus sama dengan perintah

# Perbedaan TCP dan UDP
## Tcp
Transmission Control Protocol adalah protokol berorientasi koneksi, yang berarti ia menetapkan koneksi antara pengirim dan penerima sebelum data dikirim.
Menjamin pengiriman data secara urut dan benar. 
TCP digunakan untuk aplikasi di mana keandalan dan urutan data penting, seperti HTTP/HTTPS (web browsing), FTP (file transfer), dan SMTP (email)
## Udp
User Datagram Protocol adalah protokol tanpa orientasi koneksi, yang berarti tidak ada sesi atau koneksi yang dibuat sebelum data dikirim. Data dikirimkan secara langsung.
UDP lebih cepat dibandingkan TCP karena tidak ada mekanisme untuk pengaturan koneksi, pengurutan, atau kontrol aliran.
UDP digunakan untuk aplikasi di mana kecepatan lebih penting daripada keandalan, seperti streaming video/audio, game online.
