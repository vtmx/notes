# awk

Variáveis internas (built-in):

| Variável     | Significado |
|--------------|-------------|
| `$0`         | Linha inteira atual sendo processada |
| `$1`, `$2`   | Campos (colunas) da linha atual. `$1` é o primeiro campo, `$2` o segundo, etc |
| `NF`         | Número de campos (`N`umber of `F`ields) na linha atual. Útil para saber quantas colunas a linha tem |
| `NR`         | Número do registro (`N`umber of `R`ecords) — ou seja, o número da linha atual (começa em 1) |
| `FS`         | Separador de campos de entrada (`F`ield `S`eparator). Define como o `awk` divide a linha em campos. Padrão: espaço em branco |
| `OFS`        | Separador de campos de saída (`O`utput `F`ield `S`eparator). Usado ao imprimir campos com vírgula (ex: `print $1, $2`). Padrão: um espaço |
| `RS`         | Separador de registros de entrada (`R`ecord `S`eparator). Define o que separa as linhas. Padrão: `\n` (quebra de linha) |
| `ORS`        | Separador de registros de saída (`O`utput `R`ecord `S`eparator). Usado ao imprimir com `print`. Padrão: `\n` |
| `FILENAME`   | Nome do arquivo atual sendo processado |
| `FNR`        | Igual ao `NR`, mas reinicia a contagem a cada novo arquivo (útil com múltiplos arquivos) |


Exemplos:

```bash
# Exibir o número da linha e a linha completa
awk '{ print "Linha " NR ": " $0 }' arquivo.txt

# Exibir apenas o último campo de cada linha
awk '{ print "Último campo: " $NF }' dados.txt

# Usar vírgula como separador de entrada (CSV)
awk -F',' '{ print "Nome: " $1 ", Idade: " $2 }' pessoas.csv

# Mudar o separador de saída para " | "
awk 'BEGIN { OFS = " | " } { print $1, $2, $3 }' dados.txt
```

Remove linhas em branco:

```bash
awk '!/^$/ {print}' file
```

Field separator:

```bash
awk '!/^$/ {print}' file
awk NF':' file.txt
awk 'BEGIN{FS=","}
```

Imprimi total de linhas:

```bash
awk '{NF}' file
```

Imprimi a linha inteira:

```bash
awk '/\<span./ {print $0}'
```

Lista todos os arquivos recursivamente de um diretório:

```bash
ls -R | awk '!/:$/ && !/^$/ {print $NF}'
```

Faz pesquisa e altera campo:

```bash
awk -v find="${1,,}" '{line=tolower($0); if(line ~ find) print}' file
awk -v find="${1,,}" '{line=tolower($0); if(index(line, find)) print}' file
awk -v find="${1,,}" '{line=tolower($0); if(match(line, find)) print}' file
```

```bash
awk '/wp-manga-chapter-img">$/ {gsub(/<img.+src=\"/, "", $0); print $0}' site.url
```

Linha que começa com erro e termina com horário:

```bash
awk '/^erro/ && /[0-9]{2}:[0-9]{2}$/ {print $0}'
```

Ignora linha iniciada com Música:

```bash
awk '/^Música]/ { next }'
```

Coleta primeiro campo do padrão -->:

```bash
awk '/-->/ {
  split($0, parts, " --> ")
  start_time = start[1]
  next
}'
```

Coleta valor de url de uma linha json:

```bash
awk '/"url":/ {
  url = gensub(/."url": "(.)",?/, "\\1", "g")
  print url
}' data.json
```

Coleta valors de campos json:

```bash
readarray -t sites < <(awk -F'"' '/": \{/ {print $2}' data.json)
readarray -t urls < <(awk -F'"' '/"url":/ {print $4}' data.json)
```
