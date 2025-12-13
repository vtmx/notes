# icewm

Vantagens com relação ao bspwm, OpenBox e Fluxbox
- Menus nativos
- Não trava ao errar a sintaxe da configguração (descarta somente a linha com erro)
- Atalhos mais simples, no entanto os internos ficam em preferences e externos em keys :( e não permite duplicidade em preferences :(
- pekwm interessante
- Importa múltimplos arquivos

## Openbox

```
~/.config/openbox/rc.xml
<keyboard>
  <keybind key="C-A-t">
    <action name="Execute">
      <command>xterm</command>
    </action>
  </keybind>
  <keybind key="C-A-f">
    <action name="Execute">
      <command>firefox</command>
    </action>
  </keybind>
  <keybind key="W-S-r">
    <action name="Reconfigure"/>
  </keybind>
</keyboard>

<mouse>
  <!-- Clique direito na área de trabalho abre menu -->
  <context name="Desktop">
    <mousebind button="Right" action="Press">
      <action name="ShowMenu"><menu>root-menu</menu></action>
    </mousebind>
  </context>

  <!-- Clique do meio na barra de título fecha janela -->
  <context name="Titlebar">
    <mousebind button="Middle" action="Press">
      <action name="Close"/>
    </mousebind>
  </context>

  <!-- Arrastar com botão esquerdo na barra de título move janela -->
  <context name="Titlebar">
    <mousebind button="Left" action="Drag">
      <action name="Move"/>
    </mousebind>
  </context>
</mouse>

<desktops>
  <number>4</number>
  <names>
    <name>Web</name>
    <name>Code</name>
    <name>Docs</name>
    <name>Media</name>
  </names>
  <firstdesk>1</firstdesk>
</desktops>

<menu>
  <item label="Terminal">
    <action name="Execute"><command>xterm</command></action>
  </item>
  <item label="Navegador">
    <action name="Execute"><command>firefox</command></action>
  </item>
  <item label="Sair">
    <action name="Exit"/>
  </item>
</menu>

<applications>
  <application class="Firefox">
    <maximized>yes</maximized>
  </application>

  <application class="XTerm">
    <position force="yes">100 100</position>
    <size>800 600</size>
  </application>

  <application class="Gedit">
    <desktop>2</desktop>
  </application>
</applications>

~/.config/openbox/autostart
# Iniciar nm-applet
nm-applet &

# Iniciar volumeicon
volumeicon &

# Iniciar conky
conky &

~/.config/openbox/themerc
window.active.title.bg.color: #005f87
window.active.title.text.color: #ffffff
window.inactive.title.bg.color: #444444
window.inactive.title.text.color: #cccccc
window.border.color: #444444
menu.title.bg.color: #1e1e1e
menu.title.text.color: #ffffff
menu.items.bg.color: #1e1e1e
menu.items.text.color: #ffffff
menu.items.active.bg.color: #005f87
menu.items.active.text.color: #ffffff
font: Sans 10

```

## Fluxbox

```
# include
session.keyFile: ~/.fluxbox/mykeys

~/.fluxbox/init
session.screen0.workspaces: 4
session.screen0.workspaceNames: Web, Code, Docs, Media

~/.fluxbox/keys
Control Mod1 t :Exec xterm
Control Mod1 f :Exec firefox
Super Shift R :ReloadConfig

# Clique direito na área de trabalho abre menu
OnDesktop Mouse1 :RootMenu

# Clique do meio na barra de título fecha janela
OnTitlebar Mouse2 :Close

# Arrastar com botão esquerdo na barra de título move janela
OnTitlebar Mouse1 :Move

~/.fluxbox/menu
[begin] (Fluxbox)
  [exec] (Terminal) {xterm}
  [exec] (Navegador) {firefox}
  [exit] (Sair)
[end]

~/.fluxbox/apps
[app] (name=Firefox)
  [Maximized] {yes}
[end]
[app] (name=XTerm)
  [Dimensions] {800 600}
  [Position]   {100 100}
[end]
[app] (name=Gedit)
  [Workspace] {2}
[end]

~/.fluxbox/startup

#!/bin/sh
# Iniciar nm-applet
nm-applet &

# Iniciar volumeicon
volumeicon &

# Iniciar conky
conky &

# Importante: manter o Fluxbox rodando
exec fluxbox

~/.fluxbox/init
# Ativar a toolbar
session.screen0.toolbar.visible: true

# Posição da toolbar (Bottom, Top, Left, Right)
session.screen0.toolbar.placement: Bottom

# Mostrar relógio
session.screen0.toolbar.clock: true
session.screen0.toolbar.clock.format: %H:%M

# Mostrar ícones de janelas abertas
session.screen0.toolbar.icons: true

# Mostrar workspaces
session.screen0.toolbar.workspaceName: true

# Tamanho da toolbar
session.screen0.toolbar.widthPercent: 100

~/.fluxbox/styles/MinimalDark/theme.cfg
background: flat solid #1e1e1e
foreground: #ffffff
borderColor: #444444
borderWidth: 1
window.title.focus: flat solid #005f87
window.label.focus: #ffffff
window.title.unfocus: flat solid #444444
window.label.unfocus: #cccccc
menu.title: flat solid #1e1e1e
menu.title.textColor: #ffffff
menu.frame: flat solid #1e1e1e
menu.frame.textColor: #ffffff
menu.hilite: flat solid #005f87
menu.hilite.textColor: #ffffff
font: Sans-10
```

## Icewm

```
# include
Include "mykeys"

~/.icewm/preferences
WorkspaceNames="Web, Code, Docs, Media"

# Clique direito na área de trabalho abre menu
DesktopMouseButton3=menu

# Clique do meio na barra de título fecha janela
TitleBarMouseButton2=close

# Arrastar com botão esquerdo na barra de título move janela
TitleBarMouseButton1=move

~/.icewm/keys
key "Alt+Ctrl+t" xterm
key "Alt+Ctrl+f" firefox
key "Super+Shift+R" reload

~/.icewm/menu
prog "Terminal" xterm xterm
prog "Navegador" firefox firefox
separator
exit "Sair"

~/.icewm/winoptions
Firefox.Maximized: 1
XTerm.Geometry: 800x600+100+100
Gedit.WorkSpace: 2

~/.icewm/startup
#!/bin/sh
# Iniciar nm-applet
nm-applet &

# Iniciar volumeicon
volumeicon &

# Iniciar conky
conky &

~/.icewm/toolbar
prog "Terminal" xterm xterm
prog "Navegador" firefox firefox
separator
prog "Editor" gedit gedit

~/.icewm/themes/MinimalDark/default.theme
TitleBarActiveColor="#005f87"
TitleBarActiveTextColor="#ffffff"
TitleBarInactiveColor="#444444"
TitleBarInactiveTextColor="#cccccc"
BorderColor="#444444"
MenuTitleColor="#1e1e1e"
MenuTitleTextColor="#ffffff"
MenuItemColor="#1e1e1e"
MenuItemTextColor="#ffffff"
MenuItemActiveColor="#005f87"
MenuItemActiveTextColor="#ffffff"
DefaultFontName="Sans"
DefaultFontSize=10
```
