# Shell

## Recebe último resposta recebida
```bash
$?
```

## Exibe a quantidade de shells
```bash
$0
$$
$BASHPID
$SHLVL
```

# Comparar se está ou não em um subshell
```bash
$$ vs $BASHPID
```

## Cria um arquivo novo ou excluí o conteúdo de um existente
```bash
ls >teste.txt
```

## Adiciona o conteúdo em algum arquivo existente
```bash
ls >>teste.txt
```

## Redirecionamento
```bash
teste < arquivo

cat << eof
teste
eof

grep 'teste' <<< teste
```

## Executa o segundo enquanto o primeiro ainda está em execução
```bash
comando1 & comando2
```

## Trás o processo de segundo plano para o primeiro
```bash
fg comando
```

## Leva o comando para o segundo plano
```bash
ctrl-z
```

## Executa o segundo comando caso o primeiro seja ok
```bash
comando1 && comando2
```

## Repete var
```bash
echo ${var}{,}
vida vida
echo ${var}{,,,}
vida vida vida vida
```
## Executa o segundo caso o primeiro falhe
```bash
comando1 || comando2
```

## Expandi variaǘel
```bash
var="banana laranja"
ctrl+alt+e = expandi as variáveis no terminal
```

## Executa o segundo sem está em uma nova linha
```bash
comando1; comando2
```

## Recebe argumento de entrada
```bash
local entrada1=$1
local entrada2=$2
```

## Recebe valor de entrada
```bash
read -rp "Digite um valor: " nome_var
```

## Testa saída do comando
```bash
if ls; then
  echo "comando executado com sucesso"
else
  echo "comando terminado com falha"
fi
```

## Oculta qualquer tipo de erro
```bash
comando &>/dev/null
```

## Descobrir variável PS1
```bash
printf "%q\n" "$PS1"
```

## Ligar e desligar opções
```bash
# Ligar
shopt -s globasciiranges

# Ligar
shopt -u globasciiranges
```

## Parâmetros expansão
```bash
$0 $1 $2 $3 $4 $5 $6 $7 $8 $9
```

## Alternativa ao /dev/null
```bash
# Tranca a saída de erro, mais rápido
ls -la  2>&-
# Ligar
```
