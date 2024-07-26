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
