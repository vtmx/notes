# perl-rename

Preview rename:

```bash
perl-rename -n 's/old/new/' *
```

Rename:

```bash
perl-rename 's/old/new/' *
```

Pesquisa todos os pontos exceto o da extensão

```bash
fd '\..*[^/]\.[^/]+$'
```

Remove todos os pontos exceto do *.mp3

```bash
ren 's/(?<=.)\.(?=.*\.mp3$)//g' *.mp3
```
