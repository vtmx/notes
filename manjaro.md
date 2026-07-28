# manjaro

Falha ao remover de não aceitar senha após remover zsh.
Necessário alterar o shell padrão:

```
Ctrl+Alt+F{3..}
login: root
pass: pass

chsh -s /bin/bash username
```

Driver máximo nvidia:

```
nvidia-570
```

Driver recomendado:

```
nvidia-550
```

Recuperação boas dicas:

```
sudo mkdir /mnt/boot
sudo mount /dev/sda1 /mnt/boot

# Usado para brtfs
sudo mount -o subvol=@ /dev/sda2 /mnt/
sudo mount /dev/scc1 /mnt/home
```

# Entrar no sistema

```
sudo manjaro-chroot /mnt
```

Caso apareça em um shell diferente, vc está no sistema anterior
