# sddm

Themes:

```
/usr/share/sddm/themes
```

Altera tema:

```
sudo nvim /etc/sddm.conf

/etc/sddm.conf
[Theme]
Current=name-do-tema
```

Autologin:

```
/etc/sddm.conf.d/autologin.conf

/etc/sddm.conf
[Autologin]
User=john
Session=plasma
```

Session order desktop file:

```
/usr/share/xsessions
```

Splashscreen:

```
~/.local/share/plasma/look-and-feel/
```

Teste de tema:

```bash
# For Qt5 (Legacy):
sddm-greeter --test-mode --theme /usr/share/sddm/themes/pixie

# For Qt6 (Modern):
sddm-greeter-qt6 --test-mode --theme /usr/share/sddm/themes/pixie
```
