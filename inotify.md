# inotify

Commands:

```bash
# Package: inotify-tools
inotifywatch
inotifywait
```

Loop in file change:

```bash
while true; do
  inotifywait -m -e modify $sassdir/** | \
  sassc -Mt expanded $mainsass $gtkcss && \
  xfconf-query -c xsettings -p /Net/ThemeName -r && \
  xfconf-query -c xsettings -p /Net/ThemeName -s Lightly
done
```

Loop in file change and show what file:

```bash
while true; do
  inotifywait -m -e modify dir/** | while read path action file; do
    echo "File: $path$file"
    echo "Action: $action"
  done
done
```

To set the theme in Gnome, run the following commands in terminal:

```bash
gsettings set org.gnome.desktop.interface gtk-theme "Numix"
gsettings set org.gnome.desktop.wm.preferences theme "Numix"
```

To set the theme in Xfce, run the following commands in terminal:

```bash
xfconf-query -c xsettings -p /Net/ThemeName -s "Numix"
xfconf-query -c xfwm4 -p /general/theme -s "Numix"
```

Example Numix:

```bash
while true; do
  inotifywait @gtk.gresource -qr -e modify -e create -e delete $(RES_DIR);
done
```

Example Phocus:

```bash
xsettingsd -c <(echo 'Net/ThemeName \"phocus\"') >/dev/null 2>&1 & sleep 0.2 && kill $!
```

