###手动编译替换原版本

```yum install git golang -y
git clone https://github.com/zbuse/bepusdt
cd bepusdt
go build -o bepusdt ./main
#cp  bepusdt /usr/local/bepusdt/

