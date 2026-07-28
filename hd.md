# hd

Verificar tabelad e partições:

```
sudo parted -l
```

Simular criação de arquivo grande e acompanhar possível erro:

```bash
# Criando arquivo de 1G
dd if=/dev/zero of=teste_estresse.img bs=1M count=10000 status=progress conv=fdatasync
journalctl -b -p err
```

## Formatação

### Linux (Estrutura Clássica MBR)

/boot (Primária): Cerca de 500 MB a 1 GB (formato ext4). Guarda o kernel e o GRUB. É vital que seja primária e marcada como bootável.

Partição Estendida: Ocupa o restante do disco para abrigar as partições lógicas abaixo:
  / (Raiz - Lógica): Onde o sistema operacional é instalado (20 GB a 50 GB, ext4).
  /home (Lógica): Onde ficam os arquivos pessoais dos usuários (ext4). Separar a /home evita perda de dados em formatações futuras.
  Swap (Lógica): Memória virtual (tamanho varia conforme a RAM, formato swap).

### Estrutura Comum no Linux (UEFI / GPT)

/boot/efi (A ESP descrita acima): 512 MB a 1 GB, formatada em FAT32.
/ (Raiz): Espaço para o sistema operacional (ext4, Btrfs, etc.).
/home (Opcional): Partição separada para os arquivos pessoais.
Swap (Opcional): Partição dedicada para memória virtual (embora sistemas modernos usem cada vez mais um swapfile dentro da própria partição raiz).
