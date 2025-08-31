# fstab

Adicionar o atributo noatime em casos de brtfs ajuda na performance do sistema:

```
# <file system>             <mount point>  <type>  <options>  <dump>  <pass>
UUID=uid /home          btrfs   defaults,noatime   0 0
UUID=uid /media/hd      btrfs   defaults,noatime   0 0
tmpfs                                     /tmp           tmpfs   defaults,noatime,mode=1777 0 0
```
