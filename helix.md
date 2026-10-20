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
x = Select all line if press other lines
s = Search word when line select
; = Deselect one cursor
Alt + ; = Change location of select

C = Multiple cursors
, = Deselect multiple-cursor

& = Align multiple line when multiple cursor

. = repeat
Alt + . = Repeat f / t

y = Copy
p = Paste
r = Replace
R = Replace clipboard

* = In text select, change same word with n/N

Ctrl + s = Jump
Ctrl + o = Next jump
Ctrl + i = Prev jump

Space + ? = Show commands

Using * in word, type v and N,n to select ocorrences.
Select multiple lines, type s, write: word1|word2|word3

Alt + n, p = Next and prev argument
Alt + o    = Expand argument

[ + space = Add new line about
] + space = Add new line below

```

## Theme Location

```bash
/var/lib/helix/runtime/themes/
```

## Links

- https://github.com/helix-editor/helix/wiki/How-to-install-the-default-language-servers
- https://docs.helix-editor.com/themes.html
