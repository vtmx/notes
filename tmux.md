# tmux

Exibe todas as árvores de janelas e sessões:

```
tmux choose-tree
```

Opções atuais:

```
tmux show-options -g
```

Opção específica:

```
tmux show-options -g status
```

Listas:

```
tmux list-commands
tmux list-clients
tmux list-commands
tmux list-panes
tmux list-sessions
tmux list-windows
```

## Atalhos

| Atalho              | Descrição              |
| ------------------- | ---------------------- |
| `Prefix + Space`    | Change layout          |
| `Prefix + t`        | Show time              |
| `Prefix + z`        | Zen mode               |
| `Prefix + ?`        | Show keybinds          |
| `Prefix + [`        | Entra no modo de cópia |
| `Prefix + {}`       | move pane              |
| `Prefix + Ctrl + o` | move pane              |
| `Prefix + b`        | active copy mode       |
| `Prefix + q`        | Show panels            |
| `Prefix + q + 2`    | Go panel 2             |
| `Prefix + w`        | Choose tree            |
