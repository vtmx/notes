# KDE

## Configuration Files
- https://opensourcelibs.com/lib/kde-configuration-files

## Current Style
Application Style: Lightly
Plasma Style: Breeze AlphaBlack
Colors: One Dark 2 (me)
Window Decorations = Lightly
Fonts: Segoe UI Semibold 10pt
Icons: Sensual-Breeze-Dark
Cursors: We10xOS Cursors
Shadow Window: 35% Small

## Terminal
Dark One Nuanced - bg #1e222a
BlexMono Nerd Font Mono 11pt
Miscellaneous - Margins: 8px

## Global
Meta + Drag = Arrasta a janela
Meta + , = System Settings
Meta + . = Shortcuts
Meta + I = System Settings
Meta + W = Maximize and Restaure Window
Meta + Tab = Show Desktop Grid
Meta + Space = Kruner
Meta = Kruner
Meta + R = Kruner
Alt + Space = Kruner
Meta + R = Kruner
Meta + Space = Rofi
Ctrl + Esq = System Activity
Ctrl + Shift + Esq = System Monitor
Ctrl + Shift + N = Create Folder
Meta + Ctrl + Right = Switch to Next Desktop
Meta + Ctrl + Left = Switch to Prev Desktop
Ctrl + Alt + Del = Tela para desligar
Ctrl + Shift + Alt + PgDown = Desligar

## Custom Shortcuts
Meta + B = Browser
Meta + C = VS Code
Meta + E = Dolphin
Meta + G = Chromium
Meta + K = KolorChose
Meta + O = Opera
Meta + S = Steam
Meta + T = QBitTorrent
Meta + V = VLC
Meta + Enter = Terminal

## Dolphin
F3 = Open Side
F4 = Open Pane Terminal
Shift + F4 = Open Terminal
Ctrl + 1 = Icon View
Ctrl + 2 = Compact View
Ctrl + 3 = List View
Ctrl + Space = Go Home
Ctrl + , = Preferences
Ctrl + . = Shortcuts
Ctrl + D = Duplicate
Ctrl + L = Go to Adress
Ctrl + F = Search
Ctrl + I = Filter
Tabs = Like Chrome

## Comands
kmenuedit = Shortcuts

## Configs
Desktop Session = On Login: Start with an empty session
Window Behavior = Advanced > Window placement: Centered
General Behavior = Animation speed: Instant

## Prograns
- Subtitle Composer
- KColor Chooser
- Krusader
- KRaname

## Widgets
- Better inline clock
- Virtual desktop bar

```
git clone https://github.com/wsdfhjxc/virtual-desktop-bar.git
./scripts/install-dependencies-arch.sh
./scripts/install-applet.sh
```

## Paths

### Global Themes
/usr/share/plasma/look-and-feel/
~/.local/share/plasma/look-and-feel/

### Plasma Style
/usr/share/plasma/desktoptheme/
~/.local/share/plasma/desktoptheme/

### Window Decorations
~/.local/share/aurorae/themes/

### Icons
/usr/share/icons/
~/.local/share/icons/

### Colors
/usr/share/color-schemes/
~/.local/share/color-schemes/

## Konsole
/usr/share/konsole/
~/.local/share/konsole/

## Kate
/usr/share/org.kde.syntax-highlighting/syntax-bundled/
~/.local/share/org.kde.syntax-highlighting/themes/
~/.config/katerc

### Kvantum
/usr/share/Kvantum/
~/.config/Kvantum/

## Theme
/usr/share/themes/
~/.local/share/plasma/desktoptheme/

### Backgrounds
/usr/share/backgrounds/
/usr/share/wallpapers/

### Plasmoids
.local/share/plasma/plasmoids/
- better inline clock
- shutdown or switch
- virtual desktop bar

### SDDM
/usr/share/sddm/themes/

### Splashscreen
~/.local/share/plasma/look-and-feel/

### Shortcuts
~/.config/kdeglobals
~/.config/kglobalshortcutsrc
~/.config/khotkeysrc
~/.config/kwinrc
~/.config/plasma-org.kde.plasma.desktop-appletsrc
~/.local/share/kxmlgui5/katepart/katepart5ui.rc
~/.local/share/kxmlgui5/konsole/konsoleui.rc
~/.local/share/kxmlgui5/konsole/sessionui.rc
~/.local/share/kxmlgui5/kwrite/kwriteui.rc

### Kruner with Metakey
kwriteconfig5 --file kwinrc --group ModifierOnlyShortcuts --key Meta "org.kde.krunner,/App,,display"
Restart

### Remover Panel Shadow
`xprop -remove _KDE_NET_WM_SHADOW`

## Restart Plasma
```
killall plasmashell
kstart plasmashell

kquitapp5 plasmashell
kstart5 plasmashell
```

## Links
htts://store.kde.org/p/1281798/

## Bugs

### Cursor muda em cada área
- Copiar o cursor atual ./local/share/icons para /usr/share/icons
- Alterar o arquivo default/index.theme com o nome da pasta do seu cursor
```
[icon theme]
Inherits=We10XOS-cursors
```

### Painel volta a versão anterior ao reiniciar
- Ir alterando o arquivo: /home/user/.config/plasma-org.kde.plasma.desktop-appletsrc
- E executando o comando para ver as modificações `kquitapp5 plasmashell && kstart plasmashell`

## Panel não fixa modo opaco
Editar arquivo: /usr/share/plasma/desktoptheme/default/metadata.desktop
```
[AdaptiveTransparency]
enabled=false
```

## Comandos opções
```
https://www.reddit.com/r/kde/comments/m0nj54/how_to_open_kde_plasma_system_settings_using

# exibe opções completo
systemsettings5

# exibe apenas a janela da opção
kcmshell5

systemsettings5 -h
systemsettings5 --list
kcmshell5 -h
kcmshell5 --list

systemsettings5 kcm_keys
kcmshell5 kcm_keys
```

## Atualiza Kwin e Plasma
```
kwin_x11 --replace &
plasmashell --replace &
```

## App para adicionar apps no autostart
```
kcmshell5 autostart
```

## Remove KwinScript
```
kpackagetool5 -r script-id
~/.local/share/kservices5/
```

## Dolphin
Systemsettings > Application Appearance >Style Configure...->Views->Draw focus indicator.
Systemsettings > preview uncheck folder

## Add bookmarks gnome
```
~/.config/gtk-3.0/bookmarks
file://name-folder name-icon
```

## Manter clipborad habilitado para continuar colando após software for fechado
