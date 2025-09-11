# tmux

## Comandos

Exibe todas as árvores de janelas e sessões:

```
tmux choose-tree
```


Exibe opções atuais:

```
tmux show-options -g
```

Exibe opção específica:

```
tmux show-options -g status
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
| `Ctrl + b`          | active copy mode       |
| `Ctrl + q`          | Show panels            |
| `Ctrl + q + 2`      | Go panel 2             |
