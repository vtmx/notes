# fdupes

Exibe arquivos duplicados recursivamente:

```bash
fdupes . -r
```

Entra em modo interativo para exclusão:

```bash
fdupes . -r -d
```

No modo interativo:

```bash
shift + left
Seleciona para remover

shift + right
Seleciona para manter
```

Mantém o primeiro arquivo e exclui os arquivos duplicados seguintes:

```bash
fdupes . -dN
```

Para excluir após a seleção pressione a tecla: Delete
