# Shell

```bash
$? recebe última saída recebida
$0 exibe shell atual
$$
!! exibe o último comando
$_ pega último parâmetro passado
$* todas as expansões unificadas
$@ todas as expansões
$BASHPID
$BASHREMATCH
$CDPATH
$PIPESTATUS[@]
$PROMPT_COMMAND = executa o conteúdo antes de devolver ao prompt
$RANDOM = gera número aleatório $((RANDOM%6+1)) dado
$REPLY = conteúdo do último campo válido
$OLDPWD = último diretório visitado echo ~- mesmo resultado ~+ igual PWD
$SHLVL

# Comparar se está ou não em um subshell
$$ vs $BASHPID

# Cria um arquivo novo ou excluí o conteúdo de um existente
ls >teste.txt

# Diretório de execução
script_dir=${0%/*}

# Verifica se programa existe
type firefox
echo $?

# Habilita opções
# Ativa e desativa opção
shopt -s extglob

# Exibe a opção se está ativa ou não
extglob

# Adiciona o conteúdo em algum arquivo existente
ls >>teste.txt

# Redirecionamento
teste < arquivo

cat << eof
teste
eof

grep 'teste' <<< teste

# Executa o segundo enquanto o primeiro ainda está em execução
comando1 & comando2

# Executa o segundo comando caso o primeiro seja ok
comando1 && comando2

# Repete var
echo ${var}{,}
vida vida
echo ${var}{,,,}
vida vida vida vida

# Executa o segundo caso o primeiro falhe
comando1 || comando2

# Expandi variável
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

# Descobrir variável PS1
printf "%q\n" "$PS1"

# Ligar e desligar opções
# Ligar
shopt -s globasciiranges

# Ligar
shopt -u globasciiranges

# Parâmetros expansão
$0 $1 $2 $3 $4 $5 $6 $7 $8 $9
# Repetindo parâmetros
echo {left,right}{,}
echo go_to {left,right,up,down}{,,,}

# Tranca a saída de erro, mais rápido que /dev/null
ls -la  2>&-

# Exemplo imagem do kernel
url='https://www.kernel.org'
while read; do
    wget -O /tmp/${REPLY##*/} "$url/$REPLY"
done < <(wget -qO- "$url"|grep -oP 'src="\K.*(png|jpg)(?=")')

# Declara variáveis inteiras 
declare -i a+=b
let a+=b

# Mover múltiplos arquivos
for file in *.json; do
  mv "$file" "${file%.json}.yml"
done
```
