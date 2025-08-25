# cinnamon

Exportar atalhos:

`dconf dump /org/cinnamon/desktop/keybindings/ > keybindings-backup.dconf`

Importar atalhos:

`dconf load /org/cinnamon/desktop/keybindings/ < keybindings-backup.dconf`

Opções:

```
cinnamon-settings <opt> -t <tab>
cinnamon-settings applets -t download -s date

| Módulo              | Abas disponíveis (`-t`)                                 |
|---------------------|---------------------------------------------------------|
| applets             | `installed`, `more`, `download`                         |
| backgrounds         | `images`, `settings`                                    |
| desklets            | `installed`, `more`, `download`, `general`              |
| effects             | `effects`, `customize`                                  |
| extensions          | `installed`, `more`, `download`                         |
| keyboard            | `typing`, `shortcuts`, `layouts`                        |
| mouse               | `mouse`, `touchpad`                                     |
| power               | `power`, `batteries`, `brightness`                      |
| screensaver         | `settings`, `customize`                                 |
| sound               | `output`, `input`, `sounds`, `applications`, `settings` |
| themes              | `themes`, `download`, `options`                         |
| universal-access    | `visual`, `keyboard`, `typing`, `mouse`                 |
| windows             | `titlebar`, `behavior`, `alttab`                        |
| workspaces          | `osd`, `settings`                                       |
```
