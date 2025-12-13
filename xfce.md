# xfce

Habilita Debug

```
gsettings set org.gtk.Settings.Debug enable-inspector-keybinding true
Ctrl + Shift + D
Ctrl + Shift + I

Or
GTK_DEBUG=interactive your-app

https://gtkthemingguide.surajmandal.in/#/getting_started
```

xfce-panel:

```bash
# Number of desktop generic monitor
# No label 0.25 time, use single panel run
sh -c "echo $(wmctrl -d | awk '/\*/ { print $NF }')"
sh -c "echo $(($(xdotool get_desktop) + 1 ))"
```

Recarrega tema:

```bash
xfconf-query -c xfwm4 -p /general/theme -s <theme-name>
xfconf-query -c xsettings -p /Net/ThemeName -r && xfconf-query -c xsettings -p /Net/ThemeName -s [theme-name]
```

Corrigi tamanho dos ícones barra de tarefas:

```bash
https://www.youtube.com/watch?v=WTmA65fURdQ
```
