# pandoc

Saída de arquivos:

```bash
pandoc -o file.html
```

HTML to MD:

```bash
pandoc arq.html -f html -t markdown book.md
```

Output baseado em template:

```bash
pandoc data.md --template template.html -o index.html
pandoc index.md info.yml --template index.html -o index.html
```

```bash
YML
Author:
  - {name: Iain Banks, book: The Algebraist}
  - {name: Isaac Asimov, book: Foundation} 

TEMPLATE
${for(author)}
  ${author.name} - ${author.book}
${endfor}
```

# Links
- https://stackoverflow.com/questions/26483499/pandoc-template-with-yaml-metadata
