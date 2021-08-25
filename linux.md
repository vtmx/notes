# Linux

```sh
# fonts
/usr/share/fonts/TTF/
/home/vitor/.config/user-dirs.dirs
~/.local/share/fonts/source-code/

# clear cache
sudo fc-cache -f -v
sudo rm -f /var/cache/fontconfig/_
rm -f ~/.cache/fontconfig/_

# access partition
sudo chown -hR vitor /run/media/vitor/db5d4111-906e-4fc2-881a-b8f703167c16/

# mount partition on boot
sudo fdisk /dev/sdb

# show color system terminal
echo "$TERM"

# kill tmux
tmux kill-server && tmux
prefix + alt + arrow to resize pannel

# start process
chromium &
whereis chromium
which flutter
vivaldi-stable

# var
whereis firefox
echo $BROWSER
env
printenv
export BROWSER=/usr/bin/opera

# fish
fish_config

# zsh
^u = clear line
^w = clear before word

# show all drivers
mhwd -l

# list driver installed
mhwd -li

# folders

# path folder
/usr/local/bin/

# npm folder
/usr/local/lib/node_modules/

# mirrors list
/etc/pacman.conf

# batcat
bat --list-themes
export BAT_THEME="ansi"

## app-image
chmod a+x program*.AppImage
./program*.AppImage

# change shell
cat /etc/shells
chsh
/usr/bin/fish
su - yourid

# simbolic-link
# create
sudo ln -s /var/lib/snapd/snap /snap

# show
ll /snap or readlink -f /snap

# remove
sudo rm /snap
```