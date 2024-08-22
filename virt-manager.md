# Virt Manager

## Instalation

```bash
sudo pacman -S qemu virt-manager virt-viewer dnsmasq vde2 bridge-utils openbsd-netcat
```

Enable and start service:

```bash
sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service
sudo systemctl status libvirtd.service
```

Prevent always ask password:

```bash
sudo usermod -a -G libvirt $(whoami)
# or
add user myuser libvirg
sudo systemctl restart libvirtd.service
```

## Solution

KVM guest: "network 'default' is not active"

First, confirm that the default network is indeed inactive:

```bash
sudo virsh net-list --all
```

If so, start the default network:

```bash
sudo virsh net-start default

# Also solved
Error starting domain: Requested operation is not valid: network 'default' is not active
```

## Links

- https://youtu.be/D6_95M7_8Rg?feature=shared
