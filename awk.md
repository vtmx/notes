# awk

Remove linhas em branco:

```bash
awk NF file.txt
```
Imprimi a linha inteira:

```bash
awk '/\<span.*/ {print $0}'
```
