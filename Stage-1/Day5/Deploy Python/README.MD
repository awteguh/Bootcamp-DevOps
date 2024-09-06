# Python
pada umumnya sudah terinstal pada linux

##  
```bash
python3 --version
```
cek versi python yang digunakan saat ini
```bash
sudo apt install python3-pip
```
menginstal paket manager dari python
```bash
pip install flask
```
PIP adalah sebuah package management system yang biasa digunakan untuk mengatur dan menginstall package yang berisi modul-modul Python. PIP digunakan untuk menginstall Flask karena Flask ditulis dan dikembangkan dengan bahasa dan modul-modul pemrograman Python. 

## jika gagal menginstal `pip install flask` 
```bash
sudo apt install python3-venv
```
menginstal paket yang digunakan untuk virtual environment
```bash
python3 -m venv myenv
```
embuat Virtual Environment
```bash
source myenv/bin/activate
```
mengaktifkan Virtual Environment agar bisa digunakan
```bash
pip install flask
```
instal kembali flask
```bash
nano index.py
```
```bash
from flask import Flask
app = Flask(__name__)
@app.route("/")
def helloworld():
  return "Hello World"
if __name__ == "__main__":
  app.run(host='0.0.0.0')
```
buat file `index.py` dan sesuaikan ip hostnya
```bash
python3 index.py
```
untuk menjalankan aplikasi

