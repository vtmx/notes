# Terminal

## Movimetação

| Atalho     | Descrição                             |
| ---------- | ------------------------------------- |
| `Ctrl + a` | Move cursor para o início da linha    |
| `Ctrl + e` | Move cursor para o final da linha     |
| `Alt  + b` | Move cursor para palavra anterior     |
| `Alt  + f` | Move cursor próxima palavra           |
| `Ctrl + b` | Move cursor para o caractere anterior |
| `Ctrl + f` | Move cursor para o próximo caractere  |

## Deleta

| Atalho     | Descrição                            |
| ---------- | ------------------------------------ |
| `Ctrl + u` | Deleta todo texto atrás do cursor    |
| `Ctrl + k` | Deleta todo texto a frente do cursor |
| `Ctrl + w` | Deleta palavra anterior              |
| `Alt  + d` | Deleta próxima palavra               |
| `Ctrl + h` | Deleta caractere anterior            |
| `Ctrl + d` | Deleta próximo caractere             |

## Histórico

| Atalho     | Descrição                                  |
| ---------- | ------------------------------------------ |
| `Alt + .`  | Adota a última palavra do comando anterior |
| `Ctrl + p` | Próximo comando                            |
| `Ctrl + n` | Comando anterior                           |
| `Ctrl + r` | Exibe últimos comandos                     |
| `Ctrl + g` | Sai do modo de pesquisa de histórico       |
| `Ctrl + l` | Limpa tela                                 |
| `Alt  + t` | Inverte os argumentos                      |
| `Ctrl + i` | Simula tab                                 |
| `Ctrl + d` | Finaliza terminal                          |

## Finaliza

| Atalho     | Descrição                      |
| ---------- | ------------------------------ |
| `Ctrl + c` | Finaliza programa              |
| `Ctrl + j` | Executa tecla ao Enter         |
| `Ctrl + z` | Deixa program em segundo plano |
| `fg`       | Retorna ao primeiro plano      |

## fzf

| Atalho     | Descrição                |
| ---------- | ------------------------ |
| `Ctrl + t` | Executa fzf              |
| `Ctrl + r` | Exibe histórico          |
| `Alt  + c` | Lista diretórios e entra |

## Copia e Cola

| Atalho             | Descrição |
| ------------------ | --------- |
| `Ctrl + Shift + C` | Cola      |
| `Shift + Insert  ` | Cola      |
| `Middle Mouse    ` | Cola      |

## Bash

| Atalho       | Descrição                                                                                                                                           |
| ---------    | --------------------------------------------------------------------------------------------------------------                                      |
| `!*`         | Repete os argumentos do comando anterior                                                                                                            |
| `!!`         | Repete último commando                                                                                                                              |
| `!vi`        | Execute o comando ANTERIOR que COMEÇA com vi                                                                                                        |
| `!vi:p`      | Imprima o comando executado anteriormente que COMEÇA com vi                                                                                         |
| `!n`         | Executar o enésimo comando no histórico                                                                                                             |
| `!$`         | Imprime a última palavra do comando executado anteriormente                                                                                         |
| `!^`         | Primeiro argumento do último comando                                                                                                                |
| `!*:p`       | Imprime um possível substituto para !\*                                                                                                             |
| `!$:p`       | Imprime a palavra substituta para !$                                                                                                                |
| `!ping`      | Executa um comando executado recentemente começando com a palavra ping                                                                              |
| `!ping:p`    | Imprime o comando executado anteriormente associado ao ping e torna-o a última adição no histórico de comandos                                      |
| `^abc^xyz`   | Substitua a primeira ocorrência de abc por xyz no último comando e executa                                                                          |

## Ordenado

| Atalho                               | Descrição                                                                                                                           |
| ---------------------                | ----------------------------------------------------------------                                                                    |
| `Alt + <`                            | Move para a primeira linha do histórico                                                                                             |
| `Alt + >`                            | Move para o final da linha do histórico                                                                                             |
| `Alt + ?`                            | Exibe o arquivo/diretório no path como ajuda                                                                                        |
| `Alt + *`                            | imprima todos os nomes de arquivos/pastas no caminho atual como parâmetro                                                           |
| `Alt + .`                            | Repete o último argumento usado                                                                                                     |
| `Alt + b`                            | Move cursor para palavra anterior                                                                                                   |
| `Alt + c`                            | Muda de diretório usando fzf                                                                                                        |
| `Alt + d`                            | Deleta próxima palavra                                                                                                              |
| `Alt + f`                            | Move cursor para próxima palavra                                                                                                    |
| `Alt + l`                            | Colocar letras minúsculas do cursor até o final da palavra                                                                          |
| `Alt + r`                            | Desfaz todas as alterações na linha                                                                                                 |
| `Alt + t`                            | Inverte palavra atual pela anterior                                                                                                 |
| `Alt + u`                            | Colocar letras maiúsculas do cursor até o final da palavra                                                                          |
| `Alt + Backspace`                    | Deleta palavra anterior                                                                                                             |
| `Ctrl + _`                           | Desfazer                                                                                                                            |
| `Ctrl + a`                           | Move cursor para início da linha                                                                                                    |
| `Ctrl + b`                           | Move cursor para própxima caractere                                                                                                 |
| `Ctrl + c`                           | Finaliza programa                                                                                                                   |
| `Ctrl + d`                           | Deleta próxima letra ou finaliza terminal caso não tenha linha                                                                      |
| `Ctrl + e`                           | Move cursor para o final da linha                                                                                                   |
| `Ctrl + f`                           | Move cursor para próxima caractere                                                                                                  |
| `Ctrl + g`                           | Sai do modo de pesquisa de histórico                                                                                                |
| `Ctrl + h`                           | Deleta próximo caractere                                                                                                            |
| `Ctrl + i`                           | Simula tab                                                                                                                          |
| `Ctrl + k`                           | Deleta todo texto a frente                                                                                                          |
| `Ctrl + j`                           | Executa a tecla Enter                                                                                                               |
| `Ctrl + l`                           | Limpa tela                                                                                                                          |
| `Ctrl + n`                           | Comando anterior usado down                                                                                                         |
| `Ctrl + o`                           | Execute o comando encontrado via Ctrl+r ou Ctrl+s                                                                                   |
| `Ctrl + p`                           | Próximo comando usado up                                                                                                            |
| `Ctrl + q`                           | Retorna saída do terminal após ter sido pausado                                                                                     |
| `Ctrl + r`                           | Exibe últimos comando sou exibe histórico usando fzf                                                                                |
| `Ctrl + s`                           | Pausa saída do terminal                                                                                                             |
| `Ctrl + t`                           | Troque os dois últimos caracteres antes do cursor ou executa fzf                                                                    |
| `Ctrl + u`                           | Deleta todo o texto pra trás                                                                                                        |
| `Ctrl + w`                           | Deleta próxima palavra                                                                                                              |
| `Ctrl + x`                           | Move cursor entre o início e final da linha                                                                                         |
| `Ctrl + y`                           | Cole o que foi cortado pelo último comando de corte                                                                                 |
| `Ctrl + z`                           | Deixa programa em segundo plano                                                                                                     |
| `Ctrl + Shift + -`                   | Desfaz última ação                                                                                                                  |
| `Ctrl + Shift + t`                   | Abre novo terminal                                                                                                                  |
| `Ctrl + Shift + t`                   | Abre nova aba no terminal                                                                                                           |
| `Ctrl + Shift + v`                   | Colar                                                                                                                               |
| `Ctrl + Tab`                         | Navega entre as abas                                                                                                                |
| `Ctrl + PageDown`                    | Navega entre as abas                                                                                                                |
| `Ctrl + Alt + e`                     | Expandir linha de comando                                                                                                           |
| `Ctrl + x + Ctrl + e`                | Entra no modo editor                                                                                                                |
| `Ctrl + x + Ctrl + u`                | Desfaz as últimas alterações o mesmo que Ctrl+_                                                                                     |
| `Shift + Insert  `                   | Colar                                                                                                                               |
| `Tab`                                | Auto completa comando                                                                                                               |
| `~Tab + Tab`                         | Listar todos os usuários                                                                                                            |
| `$Tab + Tab`                         | Listar todas as variáveis do sistema                                                                                                |
| `@Tab + Tab`                         | Listar todas as entradas no seu arquivo /etc/hosts                                                                                  |
| `Up`                                 | Exibe comando anterior do histórico                                                                                                 |
| `Dow`                                | Exibe comando anterior do histórico                                                                                                 |
| `Esc + t`                            | Trocar as duas últimas palavras antes do cursor                                                                                     |
| `Click scroll mouse`                 | Colar                                                                                                                               |
| `fg`                                 | Retorna ao primeiro plano                                                                                                           |

## Links

- https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc
- https://gist.github.com/tuxfight3r/60051ac67c5f0445efee?permalink_comment_id=4465571
- https://github.com/fliptheweb/bash-shortcuts-cheat-sheet/blob/master/README.md
- https://mehmandarov.com/navigating-and-editing-the-command-line
- https://keycombiner.com/collections/terminal
- https://itsfoss.com/linux-terminal-shortcuts
- kitty + list-fonts --psnames | grep "BlexMono Nerd Font Medium"

