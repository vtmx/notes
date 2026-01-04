# tput

## Posicionamento

| Comando            | Descrição                                  |
| ------------------ | ------------------------------------------ |
| `colors`           | Exibe cores suportadas pelo terminal       |
| `lines`            | Retorna quantidade de linhas               |
| `cols`             | Retorna quantidade de colunas              |
| `el`               | Volta uma linha                            |
| `ed`               | Apaga a tela a partir da posição do cursor |
| `ech 1`            | Apaga um caracter                          |
| `cup $cols $lines` | Move cursor para localização               |
| `sgr0`             | Reseta todas as configurações              |

## Cores

| Comando       | Descrição      |
| ------------- | -------------- |
| `setab {1,8}` | Cor background |
| `setaf {1,8}` | Cor foreground |
| `rev`         | Cores reversas |
| `sgr0`        | Reseta cores   |

## Estilos

| Comando | Descrição                               |
| ------- | --------------------------------------- |
| `bold`  | Bold                                    |
| `smul`  | Sublinhado                              |
| `dim`   | Altera brilho                           |
| `bel`   | Toca alarme                             |
| `civis` | Deixa cursor invisível                  |
| `rmul`  | Remove sublinhado                       |
| `reset` | Reseta valores de bold, rev, sublinhado |
