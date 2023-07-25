# Grep

-o
Retorna somente o resultado casado.

-v
Exibe linhas que não contenham.

-E
Extendido.

?
Torna valor opcional da letra a esquerda.
chopes? = chope | chopes

cat -et
Exibe final dal linha com o $

## Exemplos
grep -v ^$
Remove linhas vazias.

grep -v '^ *$'
Remove linhas vazias mesmo tendo espaço.

column -c5 arquivo
Um cate colunado.

date '+%d/%m/%Y%nHora: %H:%M'

sed -r 's/([.,:;!?])([^ ])/\1 \2/
Corrigi pontuação mais espaço.

wc -l
Conta total de linha de um arquivo.

ctrl+r
Histórico

set -o vi
set -o emacs
ctrl-v edita comando

extglob usado melhor que o find

shopt extglob # liga
extglob       # desliga

shopt -s extglob # liga
shopt -u extglob # desliga

!w # pega último comando com w
c-r # verifica o último comando com a palavra

set -o vim
set -o emacs
v # entra no editor

# cria arquivo de backup
sed -i.old -f 's/palavra/nova_palavra/g' arquivo

sed -i.old -f 's/palavra/nova_palavra/g; s/palavra/nova_palavra/g' arquivo

seq 3 | sed -e '1 i 0' -e '$ a 4'
seq 3 | sed '1 i\
> 0
> $ a\
> 4'

ls arq | xargs rm # remove o que conseguir e guarda os próximos para depois

ls arq* | cut -s -f2 -d.
