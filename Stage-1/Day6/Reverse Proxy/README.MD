# Reverse Proxy
Reverse proxy adalah konfigurasi standar yang digunakan untuk mengubah jalur traffic, server yang bertindak sebagai perantara antara klien (misalnya, browser web) dan server yang menyediakan sumber daya (misalnya, server web atau aplikasi).


## Konfigurasi 
pertama masuk ke folder nginx dan buat directory
```bash
cd /etc /nginx
```
```bash
sudo mkdir folderproxy
```

masuk ke dalam folder yang sudah di buat danbuat suatu file dengan nama `my.reverse-proxy.conf`
```bash
cd folderproxy
```
```bash
sudo nano my.reverse-proxy.conf
```
setelah itu masukan konfigurasi
```bash
server { 
    server_name namadomain.xyz; 
  
    location / { 
             proxy_pass http://127.0.0.1:3000;
    }
}
```
setelah itu keluar dari folderproxy, selanjutnya masuk ke dalan file `nginx.conf`
```bash
cd ..
```
```bash
sudo nano nginx.conf
```
selanjutnya cari bagian `include` untuk memasukan lokasi file konfigurasi yang telah dibuat
`
include /etc/nginx/folderproxy/*;
`
pastikan mengecek konfigurasi agar telihat jika ada salah atau tidak
```bash
sudo nginx -t
```
jika sudah sekarang `restart/reload`
```bash
sudo systemctl restart nginx
```
selanjutnya membuat sebuah virtual host pada local server `/etc/hosts`
```bash
sudo nano /etc/hosts
```
setelah itu masukan `ip domain` dan `namadomain`
jika sudah jalankan di browser
