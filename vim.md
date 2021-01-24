# Vim

## Navegação
hjkl = setas
^e = 1linha pra baixo
^y = 1 linha pra cima
^d = 1/2 página pra baixo
^u = 1/2 página pra cima
^f = página pra baixo
^b = página pra cima
() = bloco
{} = bloco outro
[m = pula métodos
% = pula agrupadores
H = topo
M = meio
L = baixo
zt = linha de cima
zz = linha meio
zb = linha baixo
b, B = início da palavra
e, E = final da palavra
w, W = próxima palavra
^ = início do texto na linha
0 = início da linha
\$ = final da linha
G = final
gg = inicio
gi = volta para a última linha em inserção
^o = volta ao último salto
^i = retorna ao salto anterior
:[num] = vai ao número da linha
num_linha+G = vai para linha num_linha
50% = vai para 50% do texto

## Inserção
i = inserção
a = inserção na frente
r = substitui o carácter
c = altera a letra
I = inserção no início da linha
A = inserção no final da linha
o = inserção na linha de baixo
O = inserção na linha de cima
cc = deleta linha e entra no modo de inserção
cit = inseri dentro da tag
cat = apaga tag e entra em inserção
C = deleta palavras a direita e entra no modo de inserção
s = deleta carácter e entra no modo de inserção
S = deleta linha e entra no modo de inserção igual cc
^j = adiciona linha no modo de inserção
^a = incremento
^i = decremento
^x ^n = auto-completa palavra
^n ^l = auto-completa linha
^x ^f = auto-completa arquivos
^x ^k = auto-completa dicionários

## Delete
dd = deleta linha inteira
dit = deleta o que está entre tag
d3w = deleta três palavras a frente
d9l = apaga três caracteres pra frente
d3j = apaga 3 linhas pra baixo
d\$ = deleta até o final da linha
x = deleta um carácter de cada vez
X = deleta antes do cursor
^w = apaga palavra anterior em inserção

## Editar
u = desfaz
^r em alguns casos ctrl+shift+r = refaz
yy = copia linha
Y = copia linha
[p = cola antes
p] = cola depois
P = cola pra baixo
^t = indenta pra frente
^d = indenta para trás
^n = auto completa próximo
^p = auto completa anterior

## Visual
v = modo visual
^v = modo visual em bloco
vw = seleciona uma palavra
vi = seleciona um modo específico
va = seleciona incluindo o modo
viw = seleciona palavra
viW = seleciona palavra inteira
vis = seleciona sentença
vip = seleciona parágrafo
vi" = seleciona texto entre "
vi( = seleciona texto entre (
vit = seleciona toda a tag
vat = seleciona com a tag junto
yit = copia entre a tag
dit = apaga entre a tag
vu = torna minúsculo o caracter/seleção
vU = torna maiúsculo o caracter/seleção
v( = seleciona até o final da sentença

## Pesquisa e Substituição
f = busca letra na linha
F = busca letra no sentido inverso
t = busca letra colocando o cursor antes da palavra buscada
- = busca palavra onde está o cursor

# = busca palavra onde está o cursor na ordem inversa
?nome_palavra = pesquisa pra cima
/nome_palavra = pesquisa pra baixo
Dando ENTER
n = pesquisar pra frente
N = pesquisar pra trás
:s/palavra_antiga/palavra_nova = substitui o primeiro encontrado
:s/palavra_antiga/palavra_nova/g = substitui todos da linha
:14,17s/palavra_antiga/palavra_nova = substitui todos da linha 14 a 17
%s/palavra_antiga/palavra_nova = substitui palavras
:nhol = desmarca a pesquisa

## Múltiplos Arquivos

vim arquivo1 arquivo2 = abre mais os dois arquivos
:e = nome do arquivo
:bn = ir para o próximo arquivo
:bp = ir para arquivo anterior
:b1 = vai para o arquivo de buffer 1
:b0 = primeiro arquivo
:b\$ = último arquivo
:ls = lista burfers
:bufdo = executa em todos os buffers
:retab = retabula todos os arquivos
;bufdo = retab = retabula todos os arquivos abertos
:sp ou split = splita janela
^w+j = desce para janela de baixo
^w+k = sobe para janela de cima
:q = fecha janela onde está o cursor
:vsp = vertical split
:^w+l = vai para janela a direita
:^w+h = vai para a janela da esquerda
/p = abre o plugin nerdree
o = abre arquivo do nerdree
:^w+h = volta para a janela do nerdtree
^t = pesquisa arquivos = plugin command t
^< = navegar arquivos abertos
\b = Plugin Buffer Explorer

## Macro

qa = começa a grava macro a
q = termina de gravar
@a = repete a macro
13@a = repete a macro em nas 13 linhas seguintes
:reg a = exibe a macro
:set foldmethod=indent
za = toogle métodos no editor
zo = abre método
zc = fecha métodos
zr = abre todas
zm = fecha todas

:%normal Whd = % executa o comando em normal em todas as linhas
:norm = ||
!comando = executar comando terminal

## Links
https://vim.rtorr.com
r! comando = executar comando terminal
