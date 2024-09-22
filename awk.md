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
