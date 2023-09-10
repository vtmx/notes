# Linux

## Fonts
```
/usr/share/fonts/
~/.local/share/fonts/
~/.config/user-dirs.dirs/
```

## Limpa cache de fontes
```
sudo fc-cache -f -v
sudo rm -f /var/cache/fontconfig/_
rm -f ~/.cache/fontconfig/_
```

## Acesso partição
```
sudo chown -hR vitor /run/media/vitor/db5d4111-906e-4fc2-881a-b8f703167c16/
```

## Monta partição no boot
```
sudo fdisk /dev/sdb
```

## Show color system terminal
```
echo "$TERM"
```

## Kill tmux
```
tmux kill-server && tmux
prefix + alt + arrow to resize pannel
```

## Start process
```
chromium &
whereis chromium
which flutter
vivaldi-stable
```

## Enviroment login
```
/usr/share/xsessions
```

## Env
```
whereis firefox
echo $BROWSER
env
printenv
export BROWSER=/usr/bin/opera
```

## fish
```
fish_config
```

## Show all drivers
```
mhwd -l
```

## List driver installed
```
mhwd -li
```

## Path folder
```
/usr/local/bin/
```

## npm folder
```
/usr/local/lib/node_modules/
```

## Mirrors list
```
/etc/pacman.conf
```

## batcat
```
bat --list-themes
export BAT_THEME="ansi"
```

## app-image
```
chmod a+x program*.AppImage
./program*.AppImage
```

## Change shell
```
cat /etc/shells
chsh
/usr/bin/fish
su - yourid
```

## Create simbolic link
```
sudo ln -s /var/lib/snapd/snap /snap
```

## Show
```
ll /snap or readlink -f /snap
```

## Remove
```
sudo rm /snap
```

## Editar montagem das partições
```
# Editar o arquivo como root:
/etc/fstab

# Exemplo
/media/hd1

# Após a edição rodar: systemctl daemon-reload (não lembro)
```
