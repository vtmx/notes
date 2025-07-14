# fd

Pesquise recursivamente por arquivos que não são:

```bash
fd -s -t f '[^.mp3|.mid|.wav|.wmv|.ogg]$'
```

Remova recursivamente os arquivos gif:

```bash
fd -s -t f -e 'gif' -x rm {}
```

Pesquisa todos os pontos exceto o da extensão:

```bash
fd '\..*[^/]\.[^/]+$'
```

