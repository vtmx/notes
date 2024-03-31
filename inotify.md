# inotify

# Commands
```
# Package: inotify-tools
inotifywatch
inotifywait
```

# Loop in file change
```
while true; do
  inotifywait -m -e modify $sassdir/** | \
  sassc -Mt expanded $mainsass $gtkcss && \
  xfconf-query -c xsettings -p /Net/ThemeName -r && \
  xfconf-query -c xsettings -p /Net/ThemeName -s Lightly
done
```
