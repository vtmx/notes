# journalctl

Exibe log do boot mais do último boot:

```
journalctl -b
```

Exibe log em tempo real:

```
journalctl -f
```

Exibe log com foco no erro:

```
journalctl -b -p err
```
