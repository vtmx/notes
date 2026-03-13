# mhwd

Lista os driver pci disponíveis:

```bash
mhwd-kernel -li
```

Remove driver:

```bash
sudo mhwd -r pci video-nvidia
```

Ativa driver padrão:

```bash
sudo mhwd -a pci video-linux
```

Lista os kernels disponíveis:

```bash
mhwd-kernel -li
```

Remove kernel:

```bash
mhwd-kernel -r linux619
```

Grub iniciando no segundo kernel disponível:

```
sudo nvim /etc/default/grub
GRUB_DEFAULT=saved >>> GRUB_DEFAULT="1>2"
```

## Links
https://wiki.manjaro.org/index.php/Configure_Graphics_Cards
