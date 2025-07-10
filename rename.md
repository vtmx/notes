# perl-rename

Preview rename:

```bash
perl-rename -n 's/old/new/' *
```

Rename:

```bash
perl-rename 's/old/new/' *
```

Pesquisa todos os pontos exceto o da extensão:

```bash
fd '\..*[^/]\.[^/]+$'
```

Renomear sequencialmente:

```bash
rename -n 's/.+/sprintf("palavra-%03d", ++$i)/e' *.ext
rename -n 's/.*/sprintf "palavra-%03d", ++$i/e' *.ext
```

Renomeando grupo de datas:

```bash
rename 's/^(\d{4})(\d{2})(\d{2})/\1-\2-\3/' *
```

Remove todos os pontos exceto do *.mp3

```bash
ren 's/(?<=.)\.(?=.*\.mp3$)//g' *.mp3
```

