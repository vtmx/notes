# gsettings and dconf

List global schemas:

```bash
gsettings list-schemas
```

Search key:

```bash
gsettings list-keys org.gnome.desktop.interface | grep cursor
```

Show value of key

```bash
gsettings get org.gnome.desktop.interface cursor-size
```

Set new value of key:

```bash
gsettings set org.gnome.desktop.interface cursor-size 48
```

Watch modification:

```bash
gsettings monitor org.gnome.desktop.interface
dconf watch /
```

Backup settings:

```bash
dconf dump / > dconf-settings.ini
```

Restore settings:

```bash
dconf load / < dconf-settings.ini
```
