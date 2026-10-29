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

# Exibe bufferline
[editor.linebufferline] = {never, multiple, always}

# Diff exibe modificações
gutters = ['diff', 'line-numbers', 'spacer']

# Exibe espaços e símbolos
[editor.whitespace]
render = 'all'

# Exibe tooltip
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

<tab> = após {} sai do bloco
t+<enter> = seleciona linha até o fim
:reflow 50 = reposiciona texto com 50 colunas
:readfile <file> = adiciona conteúdo do arquivo no buffer

Saída de comandos no editor:

```bash
# Command mode
:insert-output ls

# Normal mode
!ls
<alt>! ls # append
```

Modificar diretório:


```bash
:cd <dir>
```

## Vantagens

- Leader <space> nativo
- Pickers nativos
- HelpKeys ao pressionar <leader>
- Comando `:54` move cursor automáticamente
- Map `gw` plugin de `hoop,fast` nativo
- Map `f,t` continuam extenden-se além da linha atual
- Map `<c-r>` em insert exibe ajuda dos registros

## Desvantagens

- Limpar trecho de linha a frente como `C` no vim não funciona
- Comandos específicos em linha como `:5{d,y}` para apagar, copiar linha específica não funciona
- Não gera auto-complete das palavras do arquivo nativamente
- Não gera auto-complete de arquivos como `<c-x>f`
- Auto-complete precisa ser completado com <enter>, não aceita <c-y>
- Map de upper e lower case usa ` e <alt>` WTF!

## Links

- https://github.com/helix-editor/helix/wiki/How-to-install-the-default-language-servers
- https://docs.helix-editor.com/themes.html
- http://en.helixgolf.com
