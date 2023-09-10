# Shell

## Recebe último resposta recebida
```sh
$?
```

## Cria um arquivo novo ou excluí o conteúdo de um existente
```sh
ls >teste.txt
```

## Adiciona o conteúdo em algum arquivo existente
```sh
ls >>teste.txt
```

## Executa o segundo enquanto o primeiro ainda está em execução
```sh
comando1 & comando2
```

## Trás o processo de segundo plano para o primeiro
```sh
fg comando
```

## Leva o comando para o segundo plano
```sh
ctrl-z
```

## Executa o segundo comando caso o primeiro seja ok
```sh
comando1 && comando2
```

## Executa o segundo caso o primeiro falhe
```sh
comando1 || comando2
```

## Expandi variaǘel
```sh
var="banana laranja"
ctrl+alt+e = expandi as variáveis no terminal
```

## Executa o segundo sem está em uma nova linha
```sh
comando1; comando2
```

## Recebe argumento de entrada
```sh
local entrada1=$1
local entrada2=$2
```

## Recebe valor de entrada
```sh
read -rp "Digite um valor: " nome_var
```

## Testa saída do comando
```sh
if ls; then
  echo "comando executado com sucesso"
else
  echo "comando terminado com falha"
fi
```

## Oculta qualquer tipo de erro
```sh
comando &>/dev/null
```

## Descobrir variável PS1
```sh
printf "%q\n" "$PS1"
```

## Ligar e desligar opções
```sh
# Ligar
shopt -s globasciiranges

# Ligar
shopt -u globasciiranges
```
