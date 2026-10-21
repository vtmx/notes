# Helix

## Comandos

```bash
# Geral
hx --health

# Específico
hx --health bash
hx --health go
```

## Configurações

```bash
# Desabilita dicas
auto-info = false

# Habilita auto pares
auto-pairs = true

# Show bufferline
[editor.linebufferline] = {never, multiple, always}

# Diff exibe modificações
gutters = ['diff', 'line-numbers', 'spacer']

# Exibe white space
[editor.whitespace]
render = 'all'

# Show tip in code
[editor.lsp]
display-inlay-hints = true
```

## Keys

```bash
x = Seleciona toda a linha
s = Pesquisa na seleção
; = Remove seleção
Alt + ; = Altera cursor entre início e fim da seleção

C = Adiciona novo cursor abaixo
, = Remove seleção múltipla

& = Alinha caracteres selecionados baseando-se no cursor

. = Repete ação
Alt + . = Repeat f / t

y = Copia
p = Cola
r = Substitui
R = Substitui seleção pelo conteúdo do clipboard

* = Seleciona todo todas as palavras que está no cursor atual

Ctrl + s = Salva posição
Ctrl + o = Próximo salto
Ctrl + i = Salto anterior
Space + j = Picker de saltos

Space + ? = Exibe todos os comandos

Pesquisa por múltiplas palavras usando s: palavra1|palavra2|palavra3

Alt + o,i = Expande e contraciona seleção baseada no treesiter
Alt + n,p = Próxima seleção e seleção anterior baseada no treesiter

] + space = Adiciona linha abaixo
[ + space = Adiciona linha acima

Alt+s = Adiciona cursor em todas as seleções
S = select invert
` = to lower case
alt+` = to uper case
```

## In picker
alt+<enter> open file mantain picker
ctrl+t toggle previer
%type = select header colun

## Links

- https://github.com/helix-editor/helix/wiki/How-to-install-the-default-language-servers
- https://docs.helix-editor.com/themes.html
