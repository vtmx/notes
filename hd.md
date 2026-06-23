# hd

Verificar tabelad e partições:

```
sudo parted -l
```

Simular criação de arquivo grande e acompanhar possível erro:

```
dd if=/dev/zero of=teste_estresse.img bs=1M count=10000 status=progress conv=fdatasync
journalctl -b -p err
```
