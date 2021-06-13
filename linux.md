# Linux


# Fonts

/usr/share/fonts/TTF/
~/.local/share/fonts/source-code/
Font can use with folders.

# font clear cache

sudo fc-cache -f -v

# Folders Default

/home/vitor/.config/user-dirs.dirs

# Remove cache fonts

sudo rm -f /var/cache/fontconfig/_
rm -f ~/.cache/fontconfig/_

# Access partition

sudo chown -hR vitor /run/media/vitor/db5d4111-906e-4fc2-881a-b8f703167c16/

# Mount partition on boot

sudo fdisk /dev/sdb

# show color system terminal

echo "$TERM"

# kill tmux

tmux kill-server && tmux
prefix + alt + arrow to resize pannel

# start process in background

chromium &
whereis chromium
which flutter

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

# batcat
bat --list-themes
export BAT_THEME="ansi"
