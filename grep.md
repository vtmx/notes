# Grep

## Argumentos
```
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

-r
Exibe caminho do arquivo.
```

Remove linhas vazias:
```bash
grep -v ^$
```

Match até a vírgula:
```bash
grep -E '^[^,]+'
grep -E '^[^,]*'
```

Remove linhas vazias mesmo tendo espaço:
```bash
grep -v '^ *$'
```

Um cate colunado:
```bash
column -c5 arquivo
date '+%d/%m/%Y%nHora: %H:%M'
```

Corrigi pontuação mais espaço:
```bash
sed -r 's/([.,:;!?])([^ ])/\1 \2/
```

Conta total de linha de um arquivo:
```bash
wc -l
```

Histórico
```bash
ctrl+r
```

Configuração:
```bash
set -o vi
set -o emacs
ctrl-v edita comando
```

Habilita opções extendidas
shopt -s extglob # ativa
shopt -u extglob # desativa
```

Pega último comando com w:
```bash
!w 
```

Cria arquivo de backup:
```bash
sed -i.old -f 's/palavra/nova_palavra/g' arquivo
sed -i.old -f 's/palavra/nova_palavra/g; s/palavra/nova_palavra/g' arquivo

seq 3 | sed -e '1 i 0' -e '$ a 4'
seq 3 | sed '1 i\
> 0
> $ a\
> 4'
```

Verifica caracteres com a pontuação errada:
```
grep -E '[[:punct:]][^ ]+'
```

Remove o que conseguir e guarda os próximos para depois:
```bash
ls arq | xargs rm 
ls arq* | cut -s -f2 -d.
```
