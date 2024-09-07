# Golang

## 
wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit
sudo nano .bashrc
export PATH=$PATH:/usr/local/go/bin
go version
nano index.go
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
go run index.go
go build index.go
./index
