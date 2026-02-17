# Vim

## Navegação

```
esc, ctrl+c = sair do insert mode
hjkl = Setas
^e = 1linha pra baixo
^y = 1 linha pra cima
^d = 1/2 página pra baixo
^u = 1/2 página pra cima
^f = Página pra baixo
^b = Página pra cima
() = Bloco
{} = Bloco outro
[m = Pula métodos
% = Pula agrupadores
H = Topo
M = Meio
L = Baixo
zt = Linha de cima
zz = Linha meio
zb = Linha baixo
b, B = Início da palavra
e, E = Final da palavra
w, W = Próxima palavra
^ = Início do texto na linha
0 = Início da linha
\$ = Final da linha
G = Final
gg = Inicio
gi = Volta para a última linha em inserção
^o = Volta ao último salto
^i = Retorna ao salto anterior
:[num] = Vai ao número da linha
num_linha+G = Vai para linha num_linha
50% = Vai para 50% do texto
z= = Exibe opções de auto-correção (lang)
```

## Inserção

```
i = Inserção
a = Inserção na frente
r = Substitui o carácter
c = Altera a letra
ci' = Altera tudo que está dentro de ' na linha
I = Inserção no início da linha
A = Inserção no final da linha
o = Inserção na linha de baixo
O = Inserção na linha de cima
cc = Deleta linha e entra no modo de inserção
cit = Inseri dentro da tag
cat = Apaga tag e entra em inserção
C = Deleta palavras a direita e entra no modo de inserção
s = Deleta carácter e entra no modo de inserção
S = Deleta linha e entra no modo de inserção igual cc
^j = Adiciona linha no modo de inserção
^a = Incremento
^i = Decremento
^n = Próximo item do autocomplete
^p = Item anterior do autocomplete
^x = Exibe auto complete
^x ^n = Auto-completa palavra
^n ^l = Auto-completa linha
^x ^f = Auto-completa arquivos
^x ^k = Auto-completa dicionários
^e = Fecha popup do auto complete
ysiw" = Adicionar aspas entre as palavras
```

## Multiplo cursor

```
* em cima de uma palavra
cgn = Para alterála, n para próxima depois . para repetir
só usando o c também pega
```

## Delete

```
dd = Deleta linha inteira
dit = Deleta o que está entre tag
d3w = Deleta três palavras a frente
d9l = Apaga três caracteres pra frente
d3j = Apaga 3 linhas pra baixo
d\$ = Deleta até o final da linha
x = Deleta um carácter de cada vez
X = Deleta antes do cursor
^w = Apaga palavra anterior em inserção
```

## Editar

```
u = Desfaz
^r = Em alguns casos ctrl+shift+r = Refaz
yy = Copia linha
Y = Copia linha
[p = Cola antes
p] = Cola depois
P = Cola pra baixo
^t = Indenta pra frente
^d = Indenta para trás
^n = Auto completa próximo
^p = Auto completa anterior
```

## Terminal

```
:!hostname -i = Recebe resposta do comando
:r!hostname -i = Recebe resposta do comando no arquivo
!! = Inicia modo de comando na linha atual
:3,5! = Inicia modo de comando entre as linhas 3 até 5
set language in file - comment: vim: ft=sass:
end of line = # set ft=fileformat:
```

## Visual

```
v = Modo visual
^v = Modo visual em bloco
vw = Seleciona uma palavra
vi = Seleciona um modo específico
va = Seleciona incluindo o modo
viw = Seleciona palavra
viW = Seleciona palavra inteira
vis = Seleciona sentença
vip = Seleciona parágrafo
vi" = Seleciona texto entre "
vi( = Seleciona texto entre (
vit = Seleciona toda a tag
vat = Seleciona com a tag junto
yit = Copia entre a tag
dit = Apaga entre a tag
vu = Torna minúsculo o caracter/seleção
vU = Torna maiúsculo o caracter/seleção
v( = Seleciona até o final da sentença
gv = Repete seleção anterior
```

## Pesquisa

```
f = Busca letra na linha
F = Busca letra no sentido inverso
t = Busca letra colocando o cursor antes da palavra buscada
T = Busca letra colocando o cursor depois
; = Repeat ação anterior pra frente
, = Repete ação anterio ao contrário
* = Busca palavra onde está o cursor
# = Busca palavra onde está o cursor na ordem inversa
^o = Salto pra frente
^i = Salto pra trás
```

## Substituição

```
?nome_palavra = Pesquisa pra cima
/nome_palavra = Pesquisa pra baixo
Dando ENTER
n = Pesquisar pra frente
N = Pesquisar pra trás
:s/palavra_antiga/palavra_nova = Substitui o primeiro encontrado
:s/palavra_antiga/palavra_nova/g = Substitui todos da linha
:14,17s/palavra_antiga/palavra_nova = Substitui todos da linha 14 a 17
:%s/plavra_antiga/palvra_nova/gc = Substitui todos no arquivo c usado para confirmar
:%s/palavra_antiga/palavra_nova = Substitui palavras
:nhol = Desmarca a pesquisa
:Ctrl+R+" = Cola valor do clipboard
```

## Múltiplos Arquivos

```
vim arquivo1 arquivo2 = Abre mais os dois arquivos
:e = Nome do arquivo
:bn = Ir para o próximo arquivo
:bp = Ir para arquivo anterior
:b1 = Vai para o arquivo de buffer 1
:b0 = Primeiro arquivo
:b\$ = Último arquivo
:ls = Lista burfers
:bufdo = Executa em todos os buffers
:retab = Retabula todos os arquivos
;bufdo = Retab = retabula todos os arquivos abertos
:sp ou split = Splita janela
^w+j = Desce para janela de baixo
^w+k = Sobe para janela de cima
:q = Fecha janela onde está o cursor
:vsp = Vertical split
:^w+l = Vai para janela a direita
:^w+h = Vai para a janela da esquerda
/p = Abre o plugin nerdree
o = Abre arquivo do nerdree
:^w+h = Volta para a janela do nerdtree
^t = Pesquisa arquivos = plugin command t
^< = Navegar arquivos abertos
\b = Plugin Buffer Explorer
```

## Macro

```
qa = Começa a grava macro a
q = Termina de gravar
@a = Repete a macro
13@a = Repete a macro em nas 13 linhas seguintes
:reg a = Exibe a macro
:set foldmethod=indent
za = Toogle métodos no editor
zo = Abre método
zc = Fecha métodos
zr = Abre todas
zm = Fecha todas
ma = Marca local a
Ma = Vai ao local a
!comando = Executar comando terminal
.!bash = Executa linha selecionada com o bash
```

## Norm

```vim
# ctrl+v<esc> fazem o char especial para retornar
# ao modo normal

# Todo arquivo
% norm ci'nova_palavra'<ctrl+v><esc>$

# Linhas específicas
10,15 norm ci'nova_palavra'<ctrl+v><esc>$

# No VsCode
10,15 norm ci'nova_palavra<Esc>$
```

## Verificar log de inicialização

```
nvim --startuptime log.txt
```

## Extras

```
r! comando = Executar comando terminal
:set list = Add marks
:set nolist = Remove marks
:set list! = Toogle marks
gx = Open text in xgd-open
Inspect = Exibe estilo atual sobre o cursor
InspectTree = Exibe pilha da linguagem
```

## Auxliares

```bash
xclip = Usado para coletar ctrl+c do vim
```

Arquivos padrões do nvim:

```bash
/usr/share/nvim/runtime
```

Inspecionar com o treesitter:

## Adicionando corretor ortográfico dicionário

```bash
mkdir /tmp/vero && cd /tmp/vero
wget https://pt-br.libreoffice.org/assets/Uploads/PT-BR-Documents/VERO/VeroptBR3215AOC.oxt
unzip VeroptBR3215AOC.oxt

# Demora um bocadinho

# Abra o vim no diretório do arquivo extraído
nvim /tmp/vero

# Execute o comando para compilar
:mkspell pt pt_BR

# Copiar arquivo gerado
sudo cp /tmp/vero/pt.utf-8.spl /usr/share/nvim/runtime/spell

# Em vim
set spell spelllang=pt

# Em Lua
vim.opt.spell = true
vim.opt.spelllang = "pt"

# Atalhos
z=  Vê as sugestões para uma palavra certa, e troca se você escolher alguma delas
zg  Adiciona a palavra (no dicionario) em que o cursor está em cima
zug Remove a última palavra adicionada no dicionario
]s  Move o cursor para a próxima palavra "errada"
[s  Move o cursor para a palavra "errada" anterior
```

Janelas:

```bash
<C-w> c = Fecha janela
<C-w> x = Alterna janela
<C-w> 10+ = Aumenta janela na horizontal
<C-w> 10- = Comprimi janela na horizontal
<C-w> 10> = Aumenta janela na vertical
<C-w> 10< = Comprimi janela na vertical
```

Tamanho da sidebar:

```lua
map(
  'n', '<leader><leader>e', '<cmd>15Lex<cr>',
  { desc = 'Lex' }
)
```

Mapeamento do Nvim:

```lua
-- Forcei a adição do silent=true,
-- mas continuou piscando a tecla na status bar,
-- por isso mantive o comando simplificado
local function map(mode, lhs, rhs, opts)
  opts = opts or {}
  opts.silent = opts.silent ~= false
  vim.keymap.set(mode, lhs, rhs, opts)
end
```

```bash
# Remove linhas em brancos consecutivas
:%s/\n\{2,}/\r/g

# Adiciona uma linha a cada ponto final
:%s/\.\s*/.\r/g
```

Remove linhas em branco:

```vim
:g/^$/d
```

Remove espaços no início da linha:

```vim
:g/^ /d
```

Remover espaços no início e no final:

```vim
:%s/^\s\+|\s\+$//g
:%s/^\s\+//e | %s/\s\+$//e
:%s/\r//g | %s/^\s\+|\s\+$//g
```

## Tecla,Comando Interno,Descrição

```
K,      vim.lsp.buf.hover(),           Exibe a documentação flutuante sob o cursor
K,      Pressionando o K novamente, entra na página documento 'q' para sair
gd,     vim.lsp.buf.definition(),      Salta para a definição do símbolo
gD,     vim.lsp.buf.declaration(),     Salta para a declaração (se suportado)
grn,    vim.lsp.buf.rename(),          Renomeia o símbolo em todo o projeto
gra,    vim.lsp.buf.code_action(),     Abre o menu de ações de código (Code Actions)
grr,    vim.lsp.buf.references(),      Lista todas as referências do símbolo
gO,     vim.lsp.buf.document_symbol(), Lista os símbolos do documento atual
CTRL-S, vim.lsp.buf.signature_help(),  Exibe ajuda de assinatura (em modo Insert)
[d,     Move para o diagnóstico anterior.
]d,     Move para o próximo diagnóstico.
<C-W>d, Abre o diagnóstico atual em uma janela flutuante.
```

## Links

- https://vim.rtorr.com
- https://shapeshed.com/vim-netrw
- https://bitbucket.org/sergio/mylazy-nvim
- http://vimcasts.org/episodes/operating-on-search-matches-using-gn
- https://stackoverflow.com/questions/18948491/running-python-code-in-vim
- https://github.com/jdhao/nvim-config/blob/fc144e08957c39954927ae1f48ce70d8b464d258/core/mappings.lua
- https://vonheikemen.github.io/devlog/tools/configuring-neovim-using-lua
- https://vonheikemen.github.io/devlog/tools/using-netrw-vim-builtin-file-explorer
- https://github.com/echasnovski/nvim/blob/a3916554cb3cada94b7c4a1f7a1c4d6ab4e8b558/src/settings.lua
