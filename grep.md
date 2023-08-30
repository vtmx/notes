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
```

## Remove linhas vazias
```sh
grep -v ^$
```

## Remove linhas vazias mesmo tendo espaço
```sh
grep -v '^ *$'
```

## Um cate colunado
```sh
column -c5 arquivo
date '+%d/%m/%Y%nHora: %H:%M'
```

## Corrigi pontuação mais espaço
```sh
sed -r 's/([.,:;!?])([^ ])/\1 \2/
```

## Conta total de linha de um arquivo
```sh
wc -l
```

## Histórico
```sh
ctrl+r
```

## Configuração
```sh
set -o vi
set -o emacs
ctrl-v edita comando
v 

# Habilita opções extendidas
shopt -s extglob # ativa
shopt -u extglob # desativa
```

## Pega último comando com w
```sh
!w 
```

## Cria arquivo de backup
```sh
sed -i.old -f 's/palavra/nova_palavra/g' arquivo
sed -i.old -f 's/palavra/nova_palavra/g; s/palavra/nova_palavra/g' arquivo

seq 3 | sed -e '1 i 0' -e '$ a 4'
seq 3 | sed '1 i\
> 0
> $ a\
> 4'
```

## Remove o que conseguir e guarda os próximos para depois
```sh
ls arq | xargs rm 
ls arq* | cut -s -f2 -d.
```