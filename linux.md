# Linux

## Fonts

```bash
/usr/share/fonts/
~/.local/share/fonts/
~/.config/user-dirs.dirs/
```

## Limpa cache de fontes

```bash
sudo fc-cache -f -v
sudo rm -f /var/cache/fontconfig/_
rm -f ~/.cache/fontconfig/_
```

## Lista processos

```bash
pstree
ps --forest
```

## Lista processos

```bash
ctrl + z = deixa job rodar em segundo plano
```

## Manual

```bash
# Abre manual em pt
man -L pt_BR.UTF-8 command

# Exibe resumo dos manuais
man -k

# Pesquisa manual
man -f command
```

## Acesso partição

```bash
sudo chown -hR vitor /run/media/vitor/db5d4111-906e-4fc2-881a-b8f703167c16/
```

## Monta partição no boot

```bash
sudo fdisk /dev/sdb
```

## Show color system terminal

```bash
echo "$TERM"
```

## Kill tmux

```bash
tmux kill-server && tmux
prefix + alt + arrow to resize pannel
```

## Start process

```bash
chromium &
whereis chromium
which flutter
vivaldi-stable
```

## Enviroment login

```bash
/usr/share/xsessions
```

## Env

```bash
whereis firefox
echo $BROWSER
env
printenv
export BROWSER=/usr/bin/opera
```

## fish

```bash
fish_config
```

## Show all drivers

```bash
mhwd -l
```

## List driver installed

```bash
mhwd -li
```

## Path folder

```bash
/usr/local/bin/
```

## npm folder

```bash
/usr/local/lib/node_modules/
```

## Mirrors list

```bash
/etc/pacman.conf
```

## batcat

```bash
bat --list-themes
export BAT_THEME="ansi"
```

## app-image

```bash
chmod a+x program*.AppImage
./program*.AppImage
```

## Change shell

```bash
cat /etc/shells
chsh
/usr/bin/fish
su - yourid
```

## Create simbolic link

```bash
sudo ln -s /var/lib/snapd/snap /snap
```

## Show

```bash
ll /snap or readlink -f /snap
```

## Remove

```bash
sudo rm /snap
```

## Editar montagem das partições

```bash
# Editar o arquivo como root:
/etc/fstab

# Exemplo
/media/hd1

# Após a edição rodar: systemctl daemon-reload (não lembro)
```

## Grub

```bash
pegar curso linux
```

## Exibe o tamanho

```bash
df
```

## Exibe linhas iniciais

```bash
header -n arq
```

## Exibe linhas finais

```bash
tail -n arq
```

## Exibe linhas finais em termpo real

```bash
tail -f -no arq
```

## Substitui resultados do comando

```bash
ls | tr design documents
```

## Exibe e executa comando ao mesmo tempo

```bash
ls | tee -a arq
```

## Executa antes

```bash
ls | xargs -a arq
```

## Exibe informações do arquivo

```bash
wc arq
```

## Exibe status do arquivo

```bash
stat arq
```

## Multiplo sed

```bash
sed 's/a/b/g;s/c/d/g'
```

## Organiza pelo tamanho

```bash
ll | sort -h
```

## rsync

```bash
rsync -arzP src/ dest
a = mantém permissões
r = sincroniza
z = comprime durante a transferência
P = exibe progresso
```

## find

```bash
find . -name "name.txt"
find . -name "*.txt"
find . -type f -name "*.jpg"

# para remover todos os arquivos .txt
find . -f -name "*.txt" | xargs rm
```

## Info

```bash
whereis
which
who
whoami
```

## Permissões

```bash
chomod +x
chomod 775
1 = x
2 = w
4 = r

owner, group, others
```

# Hardware

```bash
lsblk
lscpu
lsmod
lspci
lsusb
modprobe
```

## Usuários

```bash
useadd
groupadd
getent
```
