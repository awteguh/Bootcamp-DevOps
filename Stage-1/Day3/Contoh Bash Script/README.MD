# Bash Script
Dengan case user menginputkan nomer 1 maka dia akan menginstall WebServer Nginx, jika dia menginputkan nomer 2 makan dia akan menginstal WebServer Apache2.
```bash
#!/bin/bash

echo "Masukan Pilihan Anda!"
echo "1=Nginx"
echo "2=Apache"
echo "3=exit"

read Pilihan
if [ "$Pilihan" = 1 ]; then
	echo "Melakukan Update"
	sudo apt update
	sudo apt upgrade
	echo "Update selesai"
	echo "--------Install Nginx--------"
	sudo apt install nginx
	sudo systemctl sudo enable nginx
	sudo sytemctl start nginx
	sudo systemctl is-active nginx
	echo "Install Selesai"
else

if [ "$Pilihan" = 2 ]; then
	echo "Melakukan Update"
	sudo apt update
	sudo apt upgrade
	echo "Update selesai"
	echo "---------Instal Appache--------"
	sudo apt install apache2
	echo "Install Selesai"
else
	echo "gagal"
fi
fi
```
