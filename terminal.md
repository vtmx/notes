# terminal
```
ctrl + l = clear screen
ctrl + u = clear line back
ctrl + a = jump to begin
ctrl + e = jump to end
ctrl + f = move next letter
ctrl + b = move prev letter
alt + f = jump next word
alt + b = jump prev word
ctrl + d = delete next letter
ctrl + h = delete prev letter
alt + d = delete word in cursor
ctrl + p = next command
ctrl + n = prev command
ctrl + r = show last commands
ctrl + d = close terminal
!! = repeat last command
```

## fish
```
eval (ssh-agent -c)
ssh-add ~/.ssh/id_rsa

ou

ssh-add
ssh-keygen -p -f ~/.ssh/id_ed25519

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases
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
```

## Links

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
