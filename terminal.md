# Terminal

## Todos
| Atalho | Descrição
| ---                | ---                                                            |
| `Alt  + c`         | fzf change dir                                                 |
| `Alt  + d`         | Delete next word                                               |
| `Alt  + b`         | Move prev word                                                 |
| `Alt  + f`         | Move next word                                                 |
| `Alt  + t`         | Inverte os argumentos                                          |
| `Ctrl + a`         | Move cursor para início da linha                               |
| `Ctrl + b`         | Move cursor para própxima caractér                             |
| `Ctrl + c`         | Finaliza programa                                              |
| `Ctrl + d`         | Delete próxima letra                                           |
| `Ctrl + d`         | Finaliza terminal                                              |
| `Ctrl + e`         | Move cursor para o final da linha                              |
| `Ctrl + i`         | Simule tab                                                     |
| `Ctrl + f`         | Move cursor para próxima caractér                              |
| `Ctrl + h`         | Delete prev letter                                             |
| `Ctrl + k`         | Delete all front                                               |
| `Ctrl + l`         | Clear screen                                                   |
| `Ctrl + n`         | Prev command                                                   |
| `Ctrl + p`         | Next command                                                   |
| `Ctrl + r`         | Show last commands                                             |
| `Ctrl + r`         | fzf show history                                               |
| `Ctrl + t`         | fzf                                                            |
| `Ctrl + u`         | Delete all back                                                |
| `Ctrl + w`         | Delete prev word                                               |
| `Ctrl + z`         | Deixa program em segundo plano                                 |
| `fg`               | Retorna ao primeiro plano                                      |
| `Ctrl + Shift + c` | Paste                                                          |
| `Shift + Insert  ` | Paste                                                          |
| `Middle Mouse    ` | Paste                                                          |
| `!!      `         | Repeat last command                                            |
| `!*      `         | Repete os argumentos do comando anterior                       |

## Move
| Atalho | Descrição
| --- | --- |
| `Ctrl + a` | Move to begin |
| `Ctrl + e` | Move to end |
| `Alt  + b` | Move prev word |
| `Alt  + f` | Move next word |
| `Ctrl + b` | Move prev letter |
| `Ctrl + f` | Move next letter |

## Delete
| Atalho | Descrição
| --- | --- |
| `Ctrl + u` | Delete all back |
| `Ctrl + k` | Delete all front |
| `Ctrl + w` | Delete prev word |
| `Alt  + d` | Delete next word |
| `Ctrl + h` | Delete prev letter |
| `Ctrl + d` | Delete next letter |

## History
| Atalho | Descrição
| --- | --- |
| `Ctrl + p` | Next command |
| `Ctrl + n` | Prev command |
| `Ctrl + r` | Show last commands |
| `Ctrl + l` | Clear screen |
| `Alt  + t` | Inverte os argumentos |
| `Ctrl + i` | Simule tab |
| `Ctrl + d` | Close terminal |

## Kill
| Atalho | Descrição
| --- | --- |
| `Ctrl + c` | Finaliza programa |
| `Ctrl + z` | Deixa program em segundo plano |
| `fg` | Retorna ao primeiro plano |

## fzf
| Atalho | Descrição
| --- | --- |
| `Ctrl + t` | fzf |
| `Ctrl + r` | fzf show history |
| `Alt  + c` | fzf change dir |

## Shell
| Atalho | Descrição
| --- | --- |
| `!!      ` | Repeat last command |
| `!*      ` | Repete os argumentos do comando anterior |

## Paste
| Atalho | Descrição
| --- | --- |
| `Ctrl + Shift + C` | Paste |
| `Shift + Insert  ` | Paste |
| `Middle Mouse    ` | Paste |

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

## rsync
```
rsync -azP src/ dest/

Using / in end save all files,
not using copy dir to another dir.

-a recursivo
-z comprimi os arquivos para transferência
-P exibe progresso

https://linuxize.com/post/how-to-use-rsync-for-local-and-remote-data-transfer-and-synchronization
https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories-pt
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

## Ffmpeg
```
ffmpeg -i videogrande.mp4 videopequeno.mp4
$ ls -lh videogrande.mp4 videopequeno.mp4
-rw-rw-r-- 1 queiroz queiroz 88M jun 28 11:56 videogrande.mp4
-rw-rw-r-- 1 queiroz queiroz 24M jun 28 12:15 videopequeno.mp4
```

## Temp
yayi woeusb-ng

## Vim
ctrl + z = vai para segundo plano
fg       = volta para primeiro plano

# Links
- https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc
