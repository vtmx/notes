# awk

Remove linhas em branco:

```bash
awk NF':' file.txt
awk 'BEGIN{FS=","}
```
Imprimi a linha inteira:

```bash
awk '/\<span.*/ {print $0}'
```

Lista todos os arquivos recursivamente de um diretório:

```bash
ls -R | awk '!/:$/ && !/^$/ {print $NF}'
```

Faz pesquisa e altera campo:

```bash
awk -v find="${1,,}" '{line=tolower($0); if(line ~ find) print}' file
awk -v find="${1,,}" '{line=tolower($0); if(index(line, find)) print}' file
awk -v find="${1,,}" '{line=tolower($0); if(match(line, find)) print}' file
```
