# grub

## Editando senha root

Habilitando tela do grub na incialização:

Na inicialização do sistema quando surgir o logo do fabricante manter a tecla Esc pressionada no caso de UFEI, ou a tecla Shift para Bios.

Editar arquivo de configuração:

- Após a inicialização digite a tecla E para editar
- Na linha onde estiver escrito linux /boot...
- Verificar se existe o argumento ro, se existir modifique para rw
- Adiciona o argumento init=/bin/bash
- Pressiona F10 para salvar
- O sistema irá inciar na tela de boot como root, digite o comando `passwd` e digite uma nova senha
- Não precisa editar o grub novamente

Opções do grub:

```bash
# /etc/default/grub
GRUB_DEFAULT=saved
GRUB_TIMEOUT=0
GRUB_TIMEOUT_STYLE=hidden

# Ou
GRUB_TIMEOUT=5
GRUB_TIMEOUT_STYLE=menu

GRUB_CMDLINE_LINUX_DEFAULT="quiet splash video=1280x720@60"

# Atualiza alterações na configuração
sudo update-grub
```

Fazendo processo pelo live-usb:

```
sudo mount -o subvol=@ /dev/sda2 /mnt
sudo chroot /mnt
passwd nome-usuario
```

Alterando a senha de outro usuário:

- Comando `su` para entrar como root
- Comando `passwd <nome-usuario>` para alterar

## Links

https://www.youtube.com/watch?v=xddMl8W0ua0


```
lsblk
sudo mount --bind /dev /mnt/dev
sudo mount --bind /dev/pts /mnt/dev/pts
sudo mount --bind /proc /mnt/proc
sudo mount --bind /sys /mnt/sys
sudo mount --bind /run /mnt/run
sudo chroot /mnt
```

/usr/share/xsessions/ (Para sessões X11)
/usr/share/wayland-sessions/ (Para sessões Wayland)
