# Pandoc

```
# Saída de arquivos
pandoc -o file.html

# HTML to MD
pandoc arq.html -f html -t markdown book.md

# Output baseado em template
pandoc data.md --template template.html -o index.lhtml
pandoc index.md info.yml --template index.html -o index.html
```

