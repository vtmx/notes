# xfce

Como usar o mesmo atalho:

- Abra o editor de configuração com o comando `xfce4-settings-editor`, meu atalho é `Super+Alt+.`
- Na barra lateral, escolha a opção `xfce4-keyboard-shortcuts`
- Escolhi a opção `xfwm4` indo em custom e verificando algum atlaho já usado, abri ele, copiei os dados
- Crie um novo com os mesmos dados só mudando o atalho
- É furada tentar editar o arquivo XML, devido ele não atualizar após a modificação e facilmente gera conflito, reinciando os atalhos padrões

Consulta todos os atalhos:

```
xfconf-query -c xfce4-keyboard-shortcuts -l -v
```

Consulta somente os atalhos customizados:

```
xfconf-query -c xfce4-keyboard-shortcuts -p /commands/custom -l -v && \
xfconf-query -c xfce4-keyboard-shortcuts -p /xfwm4/custom -l -v
```

Adiciona atalhos:

```
xfconf-query -c xfce4-keyboard-shortcuts -p "/xfwm4/custom/<Super>c" -t string -s "close_window_key"
xfconf-query -c xfce4-keyboard-shortcuts -p "/xfwm4/custom/<Super>l" -t string -s "next_workspace_key"
xfconf-query -c xfce4-keyboard-shortcuts -p "/xfwm4/custom/<Super>Right" -t string -s "next_workspace_key"
```

Habilita Debug:

```
gsettings set org.gtk.Settings.Debug enable-inspector-keybinding true
Ctrl + Shift + D
Ctrl + Shift + I

Or

GTK_DEBUG=interactive your-app
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

## Links

- https://man.archlinux.org/search?q=xfce4
- https://docs.xfce.org/xfce/xfwm4/keyboard_shortcuts
- https://gtkthemingguide.surajmandal.in
