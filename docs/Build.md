###手动编译替换原版本

```yum install git golang -y
git clone https://github.com/zbuse/bepusdt
cd bepusdt
go build -o bepusdt ./main
mkdir /usr/local/bepusdt/
install -m 755 bepusdt /usr/local/bepusdt/
install -m 755 docs/Environment.conf /usr/local/bepusdt/
install docs/bepusdt.service /etc/systemd/system/
cp -rf static templates /usr/local/bepusdt/
systemctl enable bepusdt
#vim /usr/local/bepusdt/Environment.conf #配置好参数后就可以启动了
