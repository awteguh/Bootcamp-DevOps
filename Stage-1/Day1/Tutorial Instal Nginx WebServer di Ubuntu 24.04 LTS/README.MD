# Tutorial Instal Nginx WebServer Ubuntu 24.04

Hal pertama yang harus di lakuan adalah masuk ke multipass

## Install

using update upgrade:

```bash
sudo apt update
```
```bash
sudo apt upgrade
```

using nginx:

```bash
sudo apt install nginx
```

## Usage

```bash
sudo systemctl start nginx
```
```bash
sudo systemctl enable nginx
```
cek status nginx:
```bash
sudo systemctl status nginx
```
launch nginx:
```bash
sudo systemctl is-active nginx
```
 
