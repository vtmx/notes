# Shell

```sh
# Recebe último resposta recebida
$?

# Cria um arquivo novo ou excluí o conteúdo de um existente
ls >teste.txt

# Adiciona o conteúdo em algum arquivo existente
ls >>teste.txt

# Executa o segundo enquanto o primeiro ainda está em execução
comando1 & comando2

# Executa o segundo comando caso o primeiro seja ok
comando1 && comando2

# Executa o segundo caso o primeiro falhe
comando1 || comando2

# Expandi variaǘel
var="banana laranja"
ctrl+alt+e = expandi as variáveis no terminal

# Executa o segundo sem está em uma nova linha
comando1; comando2

# Recebe argumento de entrada
local entrada1=$1
local entrada2=$2

# Recebe valor de entrada
read -rp "Digite um valor: " nome_var

# Testa saída do comando
if ls; then
  echo "comando executado com sucesso"
else
  echo "comando terminado com falha"
fi

# Oculta qualquer tipo de erro
comando &>/dev/null

# ctrl+i
funciona como tab

# Descobrir variável PS1
printf "%q\n" "$PS1"
```
