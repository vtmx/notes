# find

Extension:

```bash
find src/ -name *.html
```

Only files:

```bash
find src/ -type f
```

Show all file by extension separate by comma: 'file1.mp3' 'file2.mp3':

```bash
find $(pwd) -type f -name "*.mp3" -printf "'%p' "
```

Print all file in unique line:

```bash
find . -path "*.mp3" -print0
```

Print all files with new line:

```bash
find . -type f -name "*.mp3" -printf "\n%p "
```

See all pkg for node_modules

```bash
du -sh ./node_modules/* | sort -nr | grep '\dM.*'
```

Mover todos os arquivos dos subdiretórios para o diretório corrente:

```bash
find . -mindepth 2 -type f -exec mv -n {} . \;
```
