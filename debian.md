# debian

Install steam:

```
sudo apt update && sudo apt upgrade
sudo apt install ca-certificates curl -y
sudo dpkg --add-architecture i386
dpkg --print-foreign-architectures
sudo apt install steam-installer -y
sudo apt update
```

https://linuxcapable.com/how-to-install-steam-on-debian-linux/
