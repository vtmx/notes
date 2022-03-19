# KDE

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
~/.local/share/color-schemes/
/usr/share/color-schemes/

### Global:
~/.local/share/color-schemes/
/usr/share/color-schemes/

## konsole
~/.local/share/konsole/

### Kvantum
/usr/share/themes/
/usr/share/Kvantum/
~/.config/Kvantum/
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
