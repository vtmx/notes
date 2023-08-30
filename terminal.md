# Terminal

## Shortcuts
```
Ctrl + A = Move to begin
Ctrl + E = Move to end
Alt  + B = Move prev word
Alt  + F = Move next word
Ctrl + B = Move prev letter
Ctrl + F = Move next letter

Ctrl + U = Delete all back
Ctrl + K = Delete all front
Ctrl + W = Delete prev word
Alt  + D = Delete next word
Ctrl + H = Delete prev letter
Ctrl + D = Delete next letter

Ctrl + P = Next command
Ctrl + N = Prev command

Ctrl + R = Show last commands
Ctrl + L = Clear screen
Alt  + T = Inverte os argumentos
Ctrl + I = Simule tab
Ctrl + D = Close terminal

Ctrl + T = fzf
Alt  + C = fzf change dir

!!       = Repeat last command
!*       = Repete os argumentos do comando anterior
```

## Apps
- cmus = player
- entr = hot reload file
- ncdu = show size space
- ranger = file manager
- screenkey
- live-server = npm install -g live-server (elcio): https://github.com/tapio/live-server

## entr
```sh
# http://eradman.com/entrproject

# With file exec
echo filename.sh | entr ./filename.sh

# Clear terminal
echo filename.sh | entr -c ./filename.sh

# No file exec
echo ls *.sh | entr /bin/bash filename.sh
```

## fish
```
# Exibe o histórico
cdh

# ssh
eval (ssh-agent -c)
ssh-add ~/.ssh/id_rsa

ou

ssh-add
ssh-keygen -p -f ~/.ssh/id_ed25519
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
Shift + S = It opens a new shell on the current directory
Ctrl + D = On the shell, it goes back to ranger
sudo pacman -S w3m (to preview images)
```

## tmux
```
prefix +{ and } = move pane
prefix + ctrl + o and alt + o = move pane
ctrl + b active copy mode
```

## Create dir with path not exist
```
mkdir -p /path/path
```

## Create dir and enter in dir
```
mkdir dir && cd $_
```

## pacman
```
# Install
pacman -S

# Remove
pacman -R

# List all packages
pacman -Qqe

# Create a file with packages
pacman -Qqe > packages.txt 

# Install all packages uniques packages
pacman -S --needed - < packages.txt 
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

## Temp
yayi woeusb-ng

# Links
- https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/