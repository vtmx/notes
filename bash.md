# Bash

# Variáveis

| Variável        | Descrição                                                      |
| --------------- | -------------------------------------------------------------- |
| $?              | Recebe última saída recebida                                   |
| $$              | Descrever                                                      |
| !!              | Exibe o último comando                                         |
| $\_             | Pega último parâmetro passado                                  |
| $\*             | Todas as expansões unificadas                                  |
| $@              | Todas as expansões                                             |
| $0              | Exibe shell atual                                              |
| $BASHPID        | Exibe o ID do bash                                             |
| $BASHREMATCH    | Retorna o último padrão criado                                 |
| $CDPATH         |                                                                |
| $PIPESTATUS[@]  |                                                                |
| $PROMPT_COMMAND | Executa o conteúdo antes de devolver ao prompt                 |
| $RANDOM         | Gera número aleatório $((RANDOM%6+1)) dado                     |
| $REPLY          | Conteúdo do último campo válido                                |
| $OLDPWD         | Último diretório visitado echo ~- mesmo resultado ~+ igual PWD |
| $SHLVL          | Exibe a atual instância do shell                               |

Comparar se está ou não em um subshell:

```bash
$$ vs $BASHPID
```

Repete o mesmo comando anterior do usuário:

```bash
sudo !!
```

Cria um arquivo novo ou excluí o conteúdo de um existente:

```bash
ls >teste.txt
```

Adiciona texto no início da linha do arquivo:

```bash
echo "$(echo Meu texto; cat file)" > file
text=$(cat - nums <<< 'I P'); echo "$text" > nums
echo I P | cat /dev/stdin -
cat - nums <<< 'I P' | tee nums
sed -i '1i I P' nums
echo "$(cat - nums <<< 'I P')" > nums
```

Diretório de execução:

```bash
script_dir=${0%/*}
```

Verifica se programa existe:

```bash
type firefox
echo $?
```

Opções bash:

```bash
extglob # Exibe
shopt -s extglob # Ativa
shopt -u globasciiranges # Desativa
```

Adicionaconteúdo em algum arquivo existente:

```bash
ls >>teste.txt
```

Redirecionamento:

```bash
teste < arquivo

cat << eof
teste
eof

grep 'teste' <<< 'teste'
```

Executa o segundo enquanto o primeiro ainda está em execução:

```bash
comando1 & comando2
```

Executa o segundo comando caso o primeiro seja ok:

```bash
comando1 && comando2
```

Pasta atual current dir:

```bash
cwd=$(dirname "$0")
```

Repete var:

```bash
echo ${var}{,}
vida vida
echo ${var}{,,,}
vida vida vida vida
```

Executa o segundo caso o primeiro falhe:

```bash
comando1 || comando2
```

Expandi variável:

```bash
var="banana laranja"
ctrl+alt+e = expandi as variáveis no terminal
```

Executa o segundo sem está em uma nova linha:

```bash
comando1; comando2
```

Recebe argumento de entrada:

```bash
local entrada1=$1
local entrada2=$2
```

Recebe valor de entrada:

```bash
read -rp "Digite um valor: " nome_var
```

Testa saída do comando:

```bash
if ls; then
  echo "comando executado com sucesso"
else
  echo "comando terminado com falha"
fi
```

Oculta qualquer tipo de erro:

```bash
comando &>/dev/null
```

Descobrir variável PS1:

```bash
printf "%q\n" "$PS1"
```

Alinhamento com print:

```bash
printf "%9s:\n" "$file"
#      teste:
# mais teste:

printf "%-9s:\n" "$file"
# teste     :
# mais teste:
```

Parâmetros expansão:

```bash
$0 $1 $2 $3 $4 $5 $6 $7 $8 $9
```

Repetindo parâmetros:

```bash
echo {left,right}{,}
echo go_to {left,right,up,down}{,,,}
```

Tranca a saída de erro, mais rápido que /dev/null:

```bash
ls -la  2>&-
```

Exemplo imagem do kernel:

```bash
url='https://www.kernel.org'
while read; do
    wget -O /tmp/${REPLY##*/} "$url/$REPLY"
done < <(wget -qO- "$url"|grep -oP 'src="\K.*(png|jpg)(?=")')
```

Declara variáveis inteiras :

```bash
declare -i a+=b
let a+=b
```

Renomear múltiplas extednções:

```bash
for file in *.json; do
  mv "$file" "${file%.json}.yml"
done
```

Receber resultado do grap em array:

```bash
readarray ids <<< $(grep -Eo '<Id>[[:digit:]]*</Id> file.xml)
```

Algumas vezes fica com um espaço a mais, para solucionar use o argumento -t:
readarray -t components_files <<< "$(ls ${components_dir}/\*.html)"

Somar valor em xml:

```bash
sed -E "s|<Id>([[:digit:]])*)echo "</Id>|<Id>$((\1 + 2))</Id>"|ge
```

Rename pattern:

```bash
for file in pattern_*;
  do mv "$file" "${file//*_/}";
done
```

Debug:

```bash
set -x
...code debug...
set +x
```

Alinhando texto:

```bash
column -t arq.csv
```

Exibe arquivo formatado com 60 colunas:

```bash
fold -sw 60 arq.txt
```

Curl install:

```bash
curl -sSL https://get.docker.com/ | sh
sh -c "$(curl -sSL https://get.docker.com/)"
```

App exist:

```bash
if type firefox2 >& /dev/null; then
  echo Firefox existe
else
  echo Firefox não existe
fi
```

Ir para a parte final do arquivo:

```bash
less +F arq
```

Exibe texto com marcas de nova linha:

```bash
cat -et
```

Converter PascalCase para kebab-case:

Modo 1:

```bash
sed -E 's/([A-Z])/-\1/2g' <<< 'PalavraCruzadaAlinhada' | tr [[:upper:]] [[:lower:]]
```

Modo 2:

```bash
converter_para_hifen() {
  local palavra="$1"
  palavra_convertida="${palavra//[A-Z]/-&}"
  palavra_convertida="${palavra_convertida,,}"
  palavra_convertida="${palavra_convertida#-}"
  echo "$palavra_convertida"
}

entrada="$1"
saida=$(converter_para_hifen "$entrada")
echo "$saida"
```

Modo 3:

```bash
foo="TestPascalCaseString"
while [[ "$foo" =~ (.*[a-z0-9])([A-Z].*) ]] && foo="${BASH_REMATCH[1]}-${BASH_REMATCH[2]}"; do
  :  # do nothing
done
echo "${foo,,}"
```

Exemplo exercício:

```bash
grep -E -A1 '^(Country|City|Bairro)$' <<< "$var" | paste - - | awk '{print $1 "\t-\t" $2}'
```

Comando date sem utilitário:

```bash
printf '%(%d/%m/%y)T'
```

Nunca usei:

```bash
# Remove espaços e caracteres acentuados do nome do arquivo
new_name=$(echo "$file" | tr '[:upper:]' '[:lower:]' | sed 's/ /-/g' | iconv -f utf8 -t ascii//TRANSLIT)
```

Remover todos os arquivos de uma determinada extensão:

```bash
find . -name "*.psd" -delete
fd -e psd -x rm {}
```

Head Tail:

```bash
head 4 <<< $(file.md)
head -n4 <<< $(file.md)
tail 4 <<< $(file.md)
tail -n4 <<< $(file.md)
```

Ytdlp download playlist:

```bash
yt-dlp -x --audio-format mp3 "URL_DA_PLAYLIST"
```

Check exa:

```bash
if hash exa 2>/dev/null; then
    alias ls='exa'
    alias l='exa -l --all --group-directories-first --git'
    alias ll='exa -l --all --all --group-directories-first --git'
    alias lt='exa -T --git-ignore --level=2 --group-directories-first'
    alias llt='exa -lT --git-ignore --level=2 --group-directories-first'
    alias lT='exa -T --git-ignore --level=4 --group-directories-first'
else
    alias l='ls -lah'
    alias ll='ls -alF'
    alias la='ls -A'
fi
```

List recent files:

```bash
ls ** -t | head
```

Move to current dir:

```bash
mv <path> .
```

Edit file with sudo, with current config:

```bash
sudoedit <file>
sudo -Es nvim <file>
```

Size of files:

```bash
ls -sh | sort -hr
```

Show size of dirs:

```bash
du -h --max-depth=1 | sort -hr
ncdu
```

Writing lists:

```bash
declare -c profs=(julio rubens)
echo ${profs[@]}
Julio Rubens
```

List recursive files with path:

```bash
ls -R | grep png | xargs realpth
```

Show cr ms:

```bash
cat -A file.dos

# Solver ^M$
tr -d '\r' < file.dos | cat -et
```

Type effect:

```bash
content='Esse é um texto'
delay=0.01
for((i = 0; i < ${#content}; i++)); do
  echo -n "${content:$i:1}"
  sleep $delay
done
echo
```

Remove blank spaces:

```bash
tr -d '[[:space:]]'
```

## Colors
https://gist.github.com/JBlond/2fea43a3049b38287e5e9cefc87b2124

# Shopts

| Opção                     | Descrição                                                                                  |
|---------------------------|--------------------------------------------------------------------------------------------|
| `autocd`                  | Permite mudar de diretório digitando apenas o nome do diretório (sem o comando `cd`).     |
| `cdspell`                 | Corrige automaticamente erros de digitação no comando `cd`.                               |
| `checkhash`               | Verifica se os comandos no hash table ainda existem ao serem chamados.                    |
| `checkjobs`               | Avisa sobre jobs em execução ou parados ao sair do shell.                                 |
| `checkwinsize`            | Atualiza as variáveis `LINES` e `COLUMNS` após o redimensionamento do terminal.           |
| `cmdhist`                 | Combina comandos multiline em uma única entrada no histórico.                             |
| `dotglob`                 | Inclui arquivos/diretórios ocultos nos padrões glob (ex.: `*`).                           |
| `expand_aliases`          | Expande aliases definidos antes da execução de comandos não-interativos.                  |
| `extdebug`                | Habilita recursos adicionais para depuração de scripts.                                   |
| `extglob`                 | Habilita padrões glob estendidos como `@(foo|bar)`.                                       |
| `failglob`                | Faz com que padrões glob não correspondentes gerem erro em vez de retornar vazio.         |
| `force_fignore`           | Força o uso de exclusão com a variável `FIGNORE` no auto-completar.                       |
| `histappend`              | Adiciona comandos ao histórico em vez de sobrescrevê-lo ao encerrar o shell.              |
| `hostcomplete`            | Habilita a conclusão de nomes de host no auto-completar.                                  |
| `huponexit`               | Envia SIGHUP para jobs ao sair do shell.                                                  |
| `lithist`                 | Salva comandos multiline com quebras de linha no histórico.                               |
| `nocaseglob`              | Faz com que os padrões glob ignorem diferença de maiúsculas/minúsculas.                   |
| `nocasematch`             | Faz com que comparações de padrões ignorem maiúsculas/minúsculas.                         |
| `nullglob`                | Faz com que padrões glob não correspondentes expandam para nada (em vez de permanecerem). |
| `progcomp`                | Habilita a conclusão programável de comandos.                                             |
| `promptvars`              | Habilita a expansão de variáveis no prompt do shell.                                      |
| `sourcepath`              | Procura arquivos para o comando `source` no `PATH`.                                       |

```bash
# Links
#
# Alias
# alias live="live-server"
# alias live=" python -m http.server -b 127.0.0.1 8000 
# alias xf="sassc -M -t expanded $HOME/.local/share/themes/Lightly/gtk-3.0/src/main.scss \
#
# Config
# $HOME/.local/share/themes/Lightly/gtk-3.0/gtk.css && \
# xfce reload theme
# xfconf-query -c xsettings -p /Net/ThemeName -r && \
# xfconf-query -c xsettings -p /Net/ThemeName -s Lightly"
#
# Links
# https://www.npmjs.com/package/live-server
# https://github.com/Browsersync/browser-sync
```
