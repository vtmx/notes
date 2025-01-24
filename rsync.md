# rsync

Backup espelhando diretório:

```bash
rsync -ahzP --delete --exclude '.*' src/ dst/
```

Usado para backup mantém arquivos:

```bash
rsync -ahzP src/ dst/
```

Backup mas exclui o que for oculto:

```bash
rsync -ahzP --exclude '.*' src/ dst/
```

Espelha diretório, removendo caso não tenha em src:

```bash
rsync -av --delete src/ dst/
```

Using / in end save all files, not using copy dir to another dir

```
-a Mantém timestamp dos arquivos
-h Legível para humanos
-r Recursivo
-v Verboso exibe todos os arquivos um por um
-z Comprimi os arquivos para transferência
-P Exibe progresso
--delete Sincroniza apagando arquivos não iguais
--partial Copia caso corte no meio continua
--progress Exibe tempo de todos os arquivos
--remove-source-file Move arquivos
```

Exemplo remoto: 

```bash
rsync -ahzP src/ root@hostname:/dst
```

## Links

- https://linuxize.com/post/how-to-use-rsync-for-local-and-remote-data-transfer-and-synchronization
- https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories-pt
