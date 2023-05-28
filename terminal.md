# terminal

```
ctrl + l = clear screen
ctrl + a = move to begin
ctrl + e = move to end
alt  + b = move prev word
alt  + f = move next word
alt  + t  = inverte os argumentos
ctrl + b = move prev letter
ctrl + f = move next letter
ctrl + u = delete all back
ctrl + k = delete all front
ctrl + w = delete prev word
ald  + d = delete next word
ctrl + h = delete prev letter
ctrl + d = delete next letter
ctrl + p = next command
ctrl + n = prev command
ctrl + r = show last commands
ctrl + t = fzf
ctrl + d = close terminal
!!       = repeat last command
!*       = repete os argumentos do comando anterior
```

## Apps
- cmus = player
- entr = hot reload file
- ncdu = show size space
- ranger = file manager
- live-server = npm install -g live-server (elcio): https://github.com/tapio/live-server

## entr
```sh
# http://eradman.com/entrproject/

# with file exec
echo filename.sh | entr ./filename.sh

# celar terminal
echo filename.sh | entr -c ./filename.sh

# no file exec:
echo ls *.sh | entr /bin/bash filename.sh
```

## fish
```
cdh = exibe o histórico

eval (ssh-agent -c)
ssh-add ~/.ssh/id_rsa

ou

ssh-add
ssh-keygen -p -f ~/.ssh/id_ed25519

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases
```

## fzf
```
# custom
https://minsw.github.io/fzf-color-picker
https://github.com/junegunn/fzf/issues/1051
fish example
    set -gx FZF_DEFAULT_OPTS '
   --color=fg:#abb2bf,bg:#23272e,hl:#61afef
   --color=fg+:#abb2bf,bg+:#2c313c,hl+:#61afef,gutter:#23272e
   --color=info:#5c6370,prompt:#98c379,pointer:#abb2bf
   --color=marker:#abb2bf,spinner:#abb2bf,header:#abb2bf'
```

## ranger
```
shift + s = it opens a new shell on the current directory
ctrl + d = on the shell, it goes back to ranger
sudo pacman -S w3m (to preview images)
```

## tmux
```
prefix+{ and } = move pane
prefix+ctrl+o and alt+o = move pane
ctrl+b active copy mode
```

## folder
```
# Create dir with path not exist
mkdir -p /path/path

# Create dir and enter in dir
mkdir dir && cd $_
```


## pacman
```
pacman -S = install
pacman -R = remove
pacman -Qqe = list all packages
pacman -Qqe > packages.txt = create a file with packages
pacman -S --needed - < packages.txt = install all packages uniques packages
```

## python selenium
```
pip install selenium
download google drive
sudo mv /download/chromedriver /user/local/bin
```

## libera acessos
```
chmod -R a+rX *
```

## iso
```
sudo mkdir /mnt/iso
sudo mount -o loop ubuntu-16.10-server-amd64.iso /mnt/iso
ls /mnt/iso/
sudo umount /mnt/iso/
```

## wine config
```
config:
winecfg

restart
mv ~/.wine ~/.wine.old
winebot -u
```

## Rofi itens
```
~/.local/share/applications/
rofi -show keys
```

## Kitty
ctrl+shift+t = new tab
ctrl+shift+w = close tab
ctrl+shift+q = close tab 
ctrl+shift+right = next tab 
ctrl+shift+left = previous tab 
ctrl+shift+f5 = reload
ctrl+shift+enter = new window 
ctrl+shift+w = close window 
ctrl+shift+] = next window 
ctrl+shift+[ = previous window 

- https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/

## Softwares
- screenkey

## Temp
yayi woeusb-ng
