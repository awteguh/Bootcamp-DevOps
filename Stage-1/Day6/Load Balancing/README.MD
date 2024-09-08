# Load Balancing
Load balancing adalah teknik distribusi lalu lintas jaringan atau beban kerja di beberapa server untuk memastikan bahwa tidak ada satu server yang terlalu terbebani.

## konfigurasi
* untuk membuat suatu Load Balancing harus membuat server baru lagi dan aplikasi yang sama seperti sebelumnya
* sekarang sudah ada 2 buah server dan 2 buah aplikasi
* selanjutnya masuk kedalam konfigurasi reverse proxy yang dibuat sebelumnya
```bash 
sudo nano sudo nano /etc/nginx/folderproxy/my.reverse-proxy.conf
```
lalu tambahkan konfigurasi upstream
```bash
upstream namadomain { 
    server 192.168.64.6:3000;
    server 192.168.64.2:3000;
}
server { 
    server_name namadomain.xyz; 
  
    location / { 
             proxy_pass http://namadomain;
    }
}
```
- pada bagian server masukan IP dari server yang dibuat, di ikuti dengan port aplikasi
- pada bagian proxy_pass yang sebelumnya alamat IP dari aplikasi, sekarang di samakan dengan nama upstream yang ada di konfigurasi
- selanjutnya di cek apakan konfigurasi sudah benar atau belum
```bash
sudo nginx -t
```
jika terdapat eror jalankan perintah restart
```bash
sudo systemctl restart nginx
```
selanjutnya jalankan aplikasi yang ada pada server
* untuk make sure load balancing sudah berjalan atau belum, bisa menggunakan cara hidupkan dan matikan salah satu aplikasi atau semuanya
