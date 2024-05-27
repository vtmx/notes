# Virt Manager

## Instalation
```
sudo pacman -S qemu virt-manager virt-viewer dnsmasq vde2 bridge-utils openbsd-netcat
```

## Enable and start service
```
sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service
sudo systemctl status libvirtd.service
```

## Prevent always ask password
```
sudo usermod -a -G libvirt $(whoami)
sudo systemctl restart libvirtd.service
```


## Links
```
https://youtu.be/D6_95M7_8Rg?feature=shared
```

