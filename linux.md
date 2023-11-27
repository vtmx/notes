# Linux

## Fonts
```sh
/usr/share/fonts/
~/.local/share/fonts/
~/.config/user-dirs.dirs/
```

## Limpa cache de fontes
```sh
sudo fc-cache -f -v
sudo rm -f /var/cache/fontconfig/_
rm -f ~/.cache/fontconfig/_
```

## Lista processos
```sh
pstree
ps --forest
```

## Lista processos
```sh
ctrl + z = deixa job rodar em segundo plano
```

## Manual
```sh
# Abre manual em pt
man -L pt_BR.UTF-8 command

# Exibe resumo dos manuais 
man -k

# Pesquisa manual
man -f command
```

## Acesso partição
```sh
sudo chown -hR vitor /run/media/vitor/db5d4111-906e-4fc2-881a-b8f703167c16/
```

## Monta partição no boot
```sh
sudo fdisk /dev/sdb
```

## Show color system terminal
```sh
echo "$TERM"
```

## Kill tmux
```sh
tmux kill-server && tmux
prefix + alt + arrow to resize pannel
```

## Start process
```sh
chromium &
whereis chromium
which flutter
vivaldi-stable
```

## Enviroment login
```sh
/usr/share/xsessions
```

## Env
```sh
whereis firefox
echo $BROWSER
env
printenv
export BROWSER=/usr/bin/opera
```

## fish
```sh
fish_config
```

## Show all drivers
```sh
mhwd -l
```

## List driver installed
```sh
mhwd -li
```

## Path folder
```sh
/usr/local/bin/
```

## npm folder
```sh
/usr/local/lib/node_modules/
```

## Mirrors list
```sh
/etc/pacman.conf
```

## batcat
```sh
bat --list-themes
export BAT_THEME="ansi"
```

## app-image
```sh
chmod a+x program*.AppImage
./program*.AppImage
```

## Change shell
```sh
cat /etc/shells
chsh
/usr/bin/fish
su - yourid
```

## Create simbolic link
```sh
sudo ln -s /var/lib/snapd/snap /snap
```

## Show
```sh
ll /snap or readlink -f /snap
```

## Remove
```sh
sudo rm /snap
```

## Editar montagem das partições
```sh
# Editar o arquivo como root:
/etc/fstab

# Exemplo
/media/hd1

# Após a edição rodar: systemctl daemon-reload (não lembro)
```

## Grub
```sh
pegar curso linux
```

## Exibe o tamanho
```sh
df
```

## Exibe linhas iniciais
```sh
header -n arq
```

## Exibe linhas finais
```sh
tail -n arq
```

## Exibe linhas finais em termpo real
```sh
tail -f -no arq
```

## Substitui resultados do comando
```sh
ls | tr design documents
```

## Exibe e executa comando ao mesmo tempo
```sh
ls | tee -a arq
```

## Executa antes
```sh
ls | xargs -a arq
```

## Exibe informações do arquivo
```sh
wc arq
```

## Exibe status do arquivo
```sh
stat arq
```

## Multiplo sed
```sh
sed 's/a/b/g;s/c/d/g'
```

## Organiza pelo tamanho
```sh
ll | sort -h
```

## rsync
```sh
rsync -arzP src/ dest
a = mantém permissões
r = sincroniza
z = comprime durante a transferência
P = exibe progresso
```

## find
```sh
find . -name "name.txt"
find . -name "*.txt"
find . -type f -name "*.jpg"

# para remover todos os arquivos .txt
find . -f -name "*.txt" | xargs rm
```

## Info
```sh
whereis
which
who
whoami
```
## Permissões
```sh
chomod +x
chomod 775 
1 = x
2 = w
4 = r

owner, group, others
```

# Hardware
```sh
lsblk
lscpu
lsmod
lspci
lsusb
modprobe
```

## Usuários
```sh
useadd
groupadd
getent
```
