# keyd

Utilitário para uso específico para customizar teclas do teclado.
Não recomendado para usar como gerenciador de atalhos.

Habilita keyd:

```bash
sudo systemctl enable keyd
```

Habilita e inicia: 

```bash
sudo systemctl enable keyd --now
```

Verifica status:

```bash
systemctl status keyd
```

Para serviço:

```bash
sudo systemctl stop keyd
```

Desabilita serviço:

```bash
sudo systemctl disable keyd
```

Recarrega arquivo localizado:

```bash
sudo keyd reload -c ~/.config/keyd/default.conf
```

Command: 

```
monitor [-t]                   Print key events in real time.
list-keys                      Print a list of valid key names.
reload                         Trigger a reload .
listen                         Print layer state changes of the running keyd daemon to stdout.
bind <binding> [<binding>...]  Add the supplied bindings to all loaded configs.
```

Exemplo de layer ao pressionar capslock:

```bash
[main]
capslock = layer(nav)

[nav]
h = left
k = up
j = down
l = right
```

Verificar log:

```bash
journalctl -u keyd -f
```
