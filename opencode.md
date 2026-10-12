# opencode

Referenciar arquivo:

```
@caminho_arquivo
```

Executar comando:

```
!ls
```

Abrir editor:

```
Ctrl+x e
```

Executa prompt:

```
opencode run "Qual a cor da bandeira do brasil?"
```

Apagar todas as sessões:

```
opencode session list --format json | jq -r '.[].id' | xargs -r -n1 opencode session delete
```
