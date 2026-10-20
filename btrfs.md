# btrfs

Chegar erros:

```bash
sudo btrfs device stats /dev/sdb1
```

Teste extresse hd:

```bash
dd if=/dev/zero of=teste_estresse.img bs=1M count=10000 status=progress conv=fdatasync
```

Acompanhar:

```bash
journalctl -b -f -p err
```

Usando o smarth:

```bash
sudo smartctl -a /dev/sdb
```
