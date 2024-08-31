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
