# sed


## Substituição de palavras
```bash
sed 's/old_word/new_word/g' <<< 'The old word.'
> The new world.
```

## Regex extendido
```bash
sed -E 's/old word/new word/g' file
> The new world.
```

## Retrovisor \1..\9
```bash
sed -E 's/(old) word/\1/g' file
> old
```

## Imprimir resultado da substituição
```bash
sed -E 's/(old) word/\1 new word/g' file
> The old new word.
```

## Referências
https://github.com/adrianlarion/useful-sed
