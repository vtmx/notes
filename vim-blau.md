# Comandos e atalhos do Vim

Fonte: [Vim Cheat Sheet](https://vim.rtorr.com/lang/pt_br)

## Comandos globais

| Comando           | Descrição                                       |
|-------------------|-------------------------------------------------|
| `:h[elp] keyword` | Abre ajuda para `keyword`                       |
| `:sav[eas] file`  | Salva arquivo com outro nome                    |
| `:clo[se]`        | Fecha painel corrente                           |
| `:ter[minal]`     | Abre terminal em uma janela                     |
| `K`               | Abre a página de manual da palavra sob o cursor |

## Movimento do cursor

| Comando | Descrição |
|---|---|
| `h`         | Move cursor para esquerda |
| `j`         | Move cursor para baixo |
| `k`         | Move cursor para cima |
| `l`         | Move cursor para direita |
| `gj`        | Move cursor para baixo em quebras visuais de linha |
| `gk`        | Move cursor para cima em quebras visuais de linha |
| `H`         | Move cursor para a primeira linha visível |
| `M`         | Move cursor para a linha visível central |
| `L`         | Move cursor para a última linha visível |
| `w`         | Salta para o início da palavra seguinte |
| `W`         | Salta para o início da palavra seguinte (inclui pontuação) |
| `e`         | Salta para o fim da palavra seguinte |
| `E`         | Salta para o fim da palavra seguinte (inclui pontuação) |
| `b`         | Salta para o início da palavra anterior |
| `B`         | Salta para o início da palavra anterior (inclui pontuação) |
| `ge`        | Salta para o fim da palavra anterior |
| `gE`        | Salta para o fim da palavra anterior (inclui pontuação) |
| `%`         | Move para o próximo par correspondente (suporta `()`, `{}` e `[]`) |
| `0`         | Salta para o início da linha |
| `^` ou `0w` | Salta para o primeiro caractere visível da linha |
| `$`         | Salta para o fim da linha |
| `g_`        | Salta para o último caractere visível da linha |
| `gg`        | Vai para a primeira linha do texto |
| `G`         | Vai para a última linha do texto |
| `Ngg` ou `NG` | Vai para a linha `N` |
| `fC`        | Salta para o próximo caractere `C` da linha |
| `tC`        | Salta para antes do próximo caractere `C` da linha |
| `FC`        | Salta para o caractere `C` anterior na linha |
| `TC`        | Salta para depois do caractere `C` anterior na linha |
| `;`         | Repete os movimentos f, t, F ou T |
| `,`         | Repete os movimentos f, t, F or T para trás |
| `}`         | Salta para o próximo parágrafo ou bloco de código |
| `{`         | Salta para o parágrafo ou bloco de código anterior |
| `zz`        | Centraliza a linha corrente na tela |
| `zt`        | Posiciona a linha corrente no topo da tela |
| `zb`        | Posiciona alinha corrente no fim da tela |
| `Ctrl+e`    | Desloca a tela uma linha para cima |
| `Ctrl+y`    | Desloca a tela uma linha para baixo |
| `Ctrl+b`    | Volta uma tela para cima |
| `Ctrl+f`    | Avança uma tela para baixo |
| `Ctrl+u`    | Volta meia tela para cima |
| `Ctrl+d`    | Avança meia tela para baixo |

> Prefixar um movimento com um número faz com que ele seja repetido.

## Modo de inserção

| Comando | Descrição |
|---|---|
| `i`       | Inicia inserção antes do cursor |
| `I`       | Inicia inserção no início da linha |
| `a`       | Inicia inserção depois do cursor |
| `A`       | Inicia inserção no fim da linha |
| `o`       | Adiciona uma nova linha abaixo e inicia a inserção |
| `O`       | Adiciona uma nove linha acima e inicia a inserção |
| `ea`      | Inicia a inserção no fim da palavra |
| `Ctrl+h`  | Remove o caractere antes do cursor |
| `Ctrl+w`  | Remove a parte da palavra antes do cursor |
| `Ctrl+j`  | Quebra a linha no cursor |
| `Ctrl+t`  | Indenta a linha |
| `Ctrl+d`  | Remove uma indentação |
| `Ctrl+n`  | Seleciona o próximo complemento de palavras |
| `Ctrl+p`  | Seleciona o complemento de palavras anterior |
| `Ctrl+o`  | Inicia temporariamente o modo normal para a execução de um comando |
| `Ctrl+rX` | Insere o conteúdo do registrador X |
| `Esc`     | Sai do modo de inserção |

## Edição (modo normal)

| Comando | Descrição |
|---|---|
| `r`         | Entra no modo de inserção para substituir um caractere |
| `R`         | Entra no modo de inserção para substituir caracteres até um `Esc` |
| `J`         | Une a linha abaixo com a corrente com um espaço entre elas |
| `gJ`        | Une a linha abaixo com a corrente sem um espaço entre elas |
| `gwip`      | Refaz a distribuição de palavras em um parágrafo |
| `g~`        | Alterna caixa do texto até a movimentação especificada |
| `gu`        | Transforma texto em caixa-baixa até a movimentação especificada |
| `gU`        | Transforma texto em caixa-alta até a movimentação especificada |
| `cc` ou `S` | Apaga linha corrente e entra em modo de inserção |
| `c$` ou `C` | Apaga linha corrente da posição do cursor ao final e entra em modo de inserção |
| `ciw`       | Apaga palavra e entre no modo de inserção |
| `cw or ce`  | Apaga palavra a partir do cursor e entra em modo de inserção |
| `s`         | Apaga caractere e entra em modo de inserção |
| `xp`        | Troca o caractere corrente de posição com o próximo |
| `u`         | Desfazer |
| `U`         | Desfaz a última linha alterada |
| `Ctrl + r`  | Refazer alterações desfeitas |
| `.`         | Repete o último comando |

## Modo visual (seleções)

| Comando | Descrição |
|---|---|
| `v`          | Inicia seleção para execução de um comando |
| `V`          | Incia seleção de linhas para execução de um comando |
| `o`          | Move cursor para o fim da área selecionada (no modo visual) |
| `Ctrl+v`     | Inicia a seleção de bloco para execução de um comando |
| `O`          | Move o cursor para o fim do bloco (no modo visual) |
| `vaw`        | Seleciona uma palavra |
| `ab` ou `a(` | Seleciona região de `(` a `)` (no modo visual) |
| `aB` ou `a{` | Seleciona região de `{` a `}` (no modo visual) |
| `at`         | Seleciona região de `<` a `>` (no modo visual) |
| `ib`         | Seleciona região entre `(` e `)` (no modo visual) |
| `iB`         | Seleciona região entre `{` e `}` (no modo visual) |
| `it`         | Seleciona região entre `<` e `>` (no modo visual) |
| `Esc`        | Sai do modo visual |

## Comandos no modo visual

| Comando | Descrição |
|---|---|
| `>` | Adiciona uma indentação |
| `<` | Remove uma indentação |
| `y` | Copia o texto selecionado |
| `d` | Recorta o texto selecionado |
| `~` | Alterna a caixa de texto da seleção |
| `u` | Transforma a seleção em caixa-baixa |
| `U` | Transforma a seleção em caixa-alta |

## Registradores

| Comando | Descrição |
|---|---|
| `:reg[isters]` | Exibe o conteúdo dos registradores (modo comando) |
| `"Xy`          | Copia para o registrador `X` |
| `"Xp`          | Cola o conteúdo do registrador `X` |
| `"+y`          | Copia para a área de transferência do sistema |
| `"+p`          | Cola o conteúdo da área de transferência do sistema |

> Os registradores são armazenados no arquivo `~/.viminfo`.

## Registradores especiais

| Comando | Descrição |
|---|---|
| `0` | Último conteúdo copiado |
| `"` | Último conteúdo copiado ou recortado |
| `%` | Caminho e nome do arquivo corrente |
| `#` | Nome alternativo do arquivo no último buffer editado |
| `*` | Conteúdo da área de trabalho primária (X11) |
| `+` | Conteúdo da área de trabalho (X11) |
| `/` | Último padrão buscado |
| `:` | Último comando executado na linha de comandos |
| `.` | Último texto inserido |
| `-` | Menor deleção recente |
| `=` | Registrador de expressões |
| `_` | Registrador "buraco negro" (não registra) |

## Marcadores

| Comando | Descrição |
|---|---|
| `:marks`   | Lista os marcadores |
| `ma`       | Define a posição do marcador `a` |
| `'a`       | Salta para posição do marcador `a` |
| `y'a`      | Copia o texto na posição do marcador `a` |
| `'0`       | Vai para a posição em que o Vim foi terminado |
| `'"`       | Vai para última posição onde o arquivo foi editado |
| `'.`       | Vai para última posição alterada no arquivo |
| `''`       | Vai para a posição anterior ao último salto |
| `:ju[mps]` | Lista os saltos |
| `Ctrl+i`   | Vai para a posição mais recente da lista de saltos |
| `Ctrl+o`   | Vai para a posição mais antiga da lista de saltos |
| `:changes` | Lista as alterações |
| `g,`       | Vai para a posição mais recente da lista de mudanças |
| `g;`       | Vai para a posição mais antiga da lista de mudanças |
| `Ctrl+]`   | Vai para a marcação sob o cursor |

> Para saltar para uma marca, podemos usar o acento grave (\`) ou uma aspa simples (`'`).

## Macros

| Comando | Descrição |
|---|---|
| `qa` | Grava a macro `a`                          |
| `q`  | Para a gravação da macro                   |
| `@a` | Executa a macro `a`                        |
| `@@` | Executa novamente a última macro executada |

## Copiar, recortar e colar

| Comando | Descrição |
|---|---|
| `yy`           | Copia uma linha |
| `Nyy`          | Copia `N` linhas |
| `yw`           | Copia caracteres de uma palavra a partir da posição do cursor até seu final |
| `yiw`          | Copia a palavra sob o cursor |
| `yaw`          | Copia a palavra sob o cursor e o espaço depois dela |
| `y$` ou `Y`    | Copia do cursor ao fim da linha |
| `p`            | Cola o conteúdo copiado depois do cursor |
| `P`            | Cola o conteúdo copiado antes do cursor |
| `gp`           | Cola o conteúdo copiado depois do cursor e posiciona o cursor depois do trecho colado |
| `gP`           | Cola o conteúdo copiado antes do cursor e posiciona o cursor depois do trecho colado |
| `dd`           | Recorta uma linha |
| `Ndd`          | Recorta `N` linhas |
| `dw`           | Recorta os caracteres de uma palavra a partir da posição do cursor até o início da palavra seguinte |
| `diw`          | Recorta a palavra sob o cursor |
| `daw`          | Recorta a palavra sob o cursor e o espaço depois dela |
| `d$` ou `D`    | Recorta até o fim do arquivo |
| `x`            | Recorta um caractere |
| `:INÍCIO,FIMd` | Recorta linhas de `INÍCIO` até `FIM` |

### Outras faixas para recortar e copiar

| Comando | Descrição |
|---|---|
| `:.,$d`  | Da linha corrente ao fim do arquivo |
| `:.,1d`  | Da linha corrente ao início do arquivo |
| `:10,$d` | From the 10th line to the beginning of the file |

### Recortar e copiar padrões

| Comando | Descrição |
|---|---|
| `:g/padrão/d` | Recorta todas as linhas contendo o padrão |
| `:g!/padrão/d` | Recorta todas as linhas que não casem com o padrão |

### Indentação de texto

| Comando | Descrição |
|---|---|
| `:g/padrão/d` | Recorta todas as linhas contendo o padrão |
| `>>`   | Adiciona uma indentação à linha  |
| `<<`   | Remove uma indentação à linha |
| `>%`   | Indenta um bloco delimitado por parêntesis ou chaves |
| `<%`   | Remove a indentação de um bloco delimitado por parêntesis ou chaves |
| `>ib`  | Indenta um bloco entre parêntesis |
| `>at`  | Indenta um bloco entre tags (`<>`) |
| `N==`  | Reindenta `N` linhas |
| `=%`   | Reindenta um bloco delimitado por parêntesis ou chaves |
| `=iB`  | Reindenta o interior de um bloco entre chaves |
| `gg=G` | Reindenta todo o buffer |
| `]p`   | Cola e ajusta a indentação da linha corrente |

## Salvar e sair

| Comando | Descrição |
|---|---|
| `:w`                | Salva o arquivo (*write*) sem sair. |
| `:w !sudo tee %`    | Salva o arquivo como usuário administrativo. |
| `:wq`, `:x` ou `ZZ` | Salva o arquivo e sai. |
| `:q`                | Sai se os aquivos estiverem salvos. |
| `:q!` ou `ZQ`       | Sai descartando mudanças não salvas. |
| `:wqa`              | Salva todas as abas e sai. |

## Busca e substituição

| Comando | Descrição |
|---|---|
| `/PADRÃO`                    | Busca por PADRÃO a partir do cursor. |
| `?PADRÃO`                    | Busca por PADRÃO antes do cursor. |
| `\vPADRÃO`                   | Padrão *very magic*: descarta a necessidade de escapar os metacaracteres das expressões regulares. |
| `n`                          | Localiza o próximo padrão casado. |
| `N`                          | Localiza o padrão casado anterior. |
| `:s/PADRÃO/SUBSTITUIÇÃO`     | Troca a primeira ocorrência de PADRÃO na linha por SUBSTITUIÇÃO. |
| `:s/PADRÃO/SUBSTITUIÇÃO/g`   | Troca todas as ocorrências de PADRÃO na linha por SUBSTITUIÇÃO. |
| `:%s/PADRÃO/SUBSTITUIÇÃO/g`  | Troca PADRÃO por SUBSTITUIÇÃO em todo o documento. |
| `:%s/PADRÃO/SUBSTITUIÇÃO/gc` | Troca PADRÃO por SUBSTITUIÇÃO em todo o documento pedindo confirmação. |
| `:noh[lsearch]`              | Desliga o destaque dos casamentos da busca. |
| `:let @/ = ""`               | Remove o destaque dos casamentos anteriores. |

### Busca em múltiplos arquivos

| Comando | Descrição |
|---|---|
| `:vim[grep] /PADRÃO/ ARQUIVOS` | Busca por PADRÃO em múltiplos ARQUIVOS. |
| `:cn[ext]`                     | Salta para o casamento seguinte. |
| `:cp[revious]`                 | Salta para o casamento anterior. |
| `:cope[n]`                     | Abre uma janela com uma lista de casamentos. |
| `:ccl[ose]`                    | Abre a janela de correção rápida. |

## Abas

| Comando | Descrição |
|---|---|
| `:tabnew [ARQUIVO]`      | Abre ARQUIVO em nova aba. |
| `Ctrl+wT`                | Move a janela corrente para a própria aba. |
| `gt` ou `:tabn[ext]`     | Abre a aba seguinte. |
| `gT` ou `:tabp[revious]` | Abre a aba anterior. |
| `Ngt`                    | Abre a aba de número `N`. |
| `:tabm[ove] N`           | Move a aba corrente para a posição `N`. |
| `:tabc[lose]`            | Fecha a aba corrente e todas as suas janelas. |
| `:tabo[nly]`             | Fecha todas as abas, menos a aba corrente. |
| `:tabdo COMANDO`         | Executa COMANDO em todas as abas. |

## Operações com arquivos

| Comando | Descrição |
|---|---|
| `:e[dit] ARQUIVO`     | Abre ARQUIVO em um novo buffer. |
| `:e[dit] CAMINHO`     | Abre CAMINHO no explorador de arquivos (`netrw`). |
| `:bn[ext]`            | Vai para o buffer seguinte.     |
| `:bp[revious]`        | Vai para o buffer anterior.     |
| `:bd[elete]`          | Deleta o buffer corrente (fecha o arquivo). |
| `:b[uffer]N`          | Vai para o buffer `N`. |
| `:b[uffer] ARQUIVO`   | Vai para o buffer de nome ARQUIVO. |
| `:ls or :buffers`     | Lista todos os buffers abertos. |
| `:sp[lit] ARQUIVO`    | Abre uma janela abaixo com ARQUIVO. |
| `:vs[plit] ARQUIVO`   | Abre uma janela ao lado com ARQUIVO. |
| `:vert[ical] ba[ll]`  | Abre todos os buffers como janelas lado a lado. |
| `:tab ba[ll]`         | Abre todos os buffers em abas. |
| `:[COLS]Lex[plorer]!` | Abre ou fecha uma janela do explorador de arquivos à esquerda com COLS de largura. |

## Operações com janelas

| Comando | Descrição |
|---|---|
| `Ctrl+ws` | Divide a janela abaixo. |
| `Ctrl+wv` | Divide a janela ao lado. |
| `Ctrl+ww` | Circula entre as janelas. |
| `Ctrl+wq` | Fecha a janela corrente. |
| `Ctrl+wx` | Troca da janela corrente pela seguinte. |
| `Ctrl+w=` | Aplica mesma largura e altura a todas as janelas. |
| `Ctrl+wh` | Move o cursor para a janela à esquerda. |
| `Ctrl+wl` | Move o cursor para a janela à direita. |
| `Ctrl+wj` | Move o cursor para a janela abaixo. |
| `Ctrl+wk` | Move o cursor para a janela acima. |
| `Ctrl+wH` | Maximiza janela verticalmente à esquerda. |
| `Ctrl+wL` | Maximiza janela verticalmente à direita. |
| `Ctrl+wJ` | Maximiza janela horizontalmente abaixo. |
| `Ctrl+wK` | Maximiza janela horizontalmente acima. |

## Dobras de texto (folding) 

| Comando | Descrição |
|---|---|
| `zf` | Define uma dobra manualmente. |
| `zd` | Deleta a dobra sob o cursor. |
| `za` | Alterna a dobra sob o cursor. |
| `zo` | Abre a dobra sob o cursor. |
| `zc` | Fecha a dobra sob o cursor. |
| `zr` | Abre todas as dobras em um nível. |
| `zm` | Aumenta todas as dobras (fecha) em um nível. |
| `zi` | Liga e desliga a funcionalidade das dobras de texto. |

> Os comandos de dobras afetam todos os níveis quando utilizadas em maiúsculas (`za` e `zA`, por exemplo).

## Diferenças (diff)

| Comando | Descrição |
|---|---|
| `]c`                 | Salta para o início da mudança seguinte. |
| `[c`                 | Salta para o início da mudança anterior. |
| `do` ou `:diffg[et]` | Captura as diferenças em relação aos outros buffers. |
| `dp` ou `:diffpu[t]` | Aplica as diferenças em outros buffers. |
| `:diffthis`          | Torna a janela corrente parte das diferenças. |
| `:dif[fupdate]`      | Atualiza as diferenças. |
| `:diffo[ff]`         | Desabilita o modo de diferenças na janela corrente. |

> O Vim pode ser iniciado no modo de diferenças se invocado com `vimdiff`.

