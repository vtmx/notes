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

Converte para html, importa estilo e abre o arquivo:

```bash
# -t html5 → converte para html5
# --standalone → gera <head> completo
# --embed-resources → substitui o --self-contained antigo (mais inteligente com imagens, etc.)
# -c + URL → aplica o CSS externo
# --metadata title="Quiz" → título bonitinho na aba do navegador

pandoc quiz.md -t html5 \
--metadata title='Quiz' \
--embed-resources \
--standalone \
-c 'style.css' \
-o quiz.html && zen-browser quiz.html

#-c 'https://cdn.simplecss.org/simple.css' \
#-c 'https://cdn.jsdelivr.net/npm/@picocss/pico@2/css/pico.min.css' \
# -o quiz.html && xdg-open quiz.html
```

# Links
- https://stackoverflow.com/questions/26483499/pandoc-template-with-yaml-metadata
