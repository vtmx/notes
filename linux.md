# Linux

## Fonts
/usr/share/fonts/TTF/
~/.local/share/fonts/source-code/

Font can use with inner folders.

## Apps
KRename
KColorChooser

## Folders Default
/home/vitor/.config/user-dirs.dirs

## Remove cache fonts
sudo rm -f /var/cache/fontconfig/*
rm -f ~/.cache/fontconfig/*

## Access partition
sudo chown -hR vitor /run/media/vitor/db5d4111-906e-4fc2-881a-b8f703167c16/

## Mount partition on boot
sudo fdisk /dev/sdb

# show color system terminal
echo "$TERM"

# kill tmux
tmux kill-server && tmux
prefix + alt + arrow to resize pannel

# start process in background
chromium &
```
# zsh
^u = clear line
^w = clear before word
