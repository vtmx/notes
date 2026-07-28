# find

Por extensão:

```bash
find src/ -name *.html
```

Somente arquivos:

```bash
find src/ -type f
```

Extens~oes separadas por vírgula: 'file1.mp3' 'file2.mp3':

```bash
find $(pwd) -type f -name "*.mp3" -printf "'%p' "
```

Todos os arquivos em uma linha:

```bash
find . -path "*.mp3" -print0
```

Todos os arquivos em uma nova linha:

```bash
find . -type f -name "*.mp3" -printf "\n%p "
```

Todos os pacotes do diretórionode_modules:

```bash
du -sh ./node_modules/* | sort -nr | grep '\dM.*'
```

Mover todos os arquivos dos subdiretórios para o diretório corrente:

```bash
find . -mindepth 2 -type f -exec mv -n {} . \;
```
