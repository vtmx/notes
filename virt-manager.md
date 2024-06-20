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
# or
add user myuser libvirg
sudo systemctl restart libvirtd.service
```

## Solution
KVM guest: "network 'default' is not active"

First, confirm that the default network is indeed inactive:
`sudo virsh net-list --all`

If so, start the default network:
`sudo virsh net-start default`

## Links
```
https://youtu.be/D6_95M7_8Rg?feature=shared
```

