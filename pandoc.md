# Pandoc

```
# Saída de arquivos
pandoc -o file.html

# HTML to MD
pandoc arq.html -f html -t markdown book.md

# Output baseado em template
pandoc data.md --template template.html -o index.html
pandoc index.md info.yml --template index.html -o index.html

# Loop example
https://stackoverflow.com/questions/26483499/pandoc-template-with-yaml-metadata

YML
Author:
  - {name: Iain Banks, book: The Algebraist}
  - {name: Isaac Asimov, book: Foundation} 

TEMPLATE
${for(author)}
  ${author.name} - ${author.book}
${endfor}
```

