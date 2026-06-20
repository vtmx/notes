# manjaro

Falha ao remover de não aceitar senha após remover zsh.
Necessário alterar o shell padrão:

```
Ctrl+Alt+F{3..}
login: root
pass: pass

chsh -s /bin/bash username
```
