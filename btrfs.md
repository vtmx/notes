# btrfs

Chegar erros:

```
sudo btrfs device stats /dev/sdb1
```

Teste extresse hd:

```
dd if=/dev/zero of=teste_estresse.img bs=1M count=10000 status=progress conv=fdatasync
```

Acompanhar:

```
journalctl -b -f -p err
```
