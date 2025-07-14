# entr

Vigia alteração no arquivo:

```bash
echo filename.sh | entr ./filename.sh
```

Limpa terminal:

```bash
echo filename.sh | entr -c ./filename.sh
```

Verifica todos os arquivos:

```bash
echo ls *.sh | entr /bin/bash filename.sh
```

## Links

- http://eradman.com/entrproject
