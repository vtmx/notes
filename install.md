# install

Copiar Ficheiros com o Comando Install
Simples e direto: o comando install pode ser utilizado como o tradicional cp. O utilizador só precisa indicar o ficheiro de origem e o destino:

```bash
install NomeDoFicheiro NomeDoDiretorio
```

Manter Timestamps Originais com o -p
Por padrão, o comando install atualiza o timestamp do ficheiro copiado. No entanto, com o parâmetro -p, o utilizador pode garantir que os timestamps originais sejam preservados:

```bash
install -p NomeDoFicheiro NomeDoDiretorio
```

Criar Diretórios com o Comando Install
Precisa de criar um novo diretório? O comando install faz isso com o parâmetro -d:

```bash
install -d NomeDoDiretorio
```

Criar Diretórios e Copiar Ficheiros com Apenas um Comando
Aqui é onde o comando install começa a demonstrar o seu verdadeiro poder. Combinando os parâmetros -D e -t, o utilizador pode criar um diretório e copiar ficheiros de uma só vez:

```bash
install -D -t NomeDoDiretorio NomeDoFicheiro
```

Definir Permissões ao Copiar Ficheiros
Com o parâmetro -m, o utilizador pode definir permissões enquanto copia ficheiros ou cria diretórios:

```bash
install -m 755 NomeDoFicheiro NomeDoDiretorio
```

Alterar Propriedade de Ficheiros ou Diretórios
Atribuir a propriedade de ficheiros ou diretórios durante a cópia é simples com o parâmetro -o:

```bash
sudo install -o utilizador NomeDoFicheiro NomeDoDiretorio
```

Alterar Propriedade de Grupo
Com o parâmetro -g, o comando install também permite alterar a propriedade de grupo:

```bash
sudo install -g NomeDoGrupo NomeDoFicheiro NomeDoDiretorio
```

Criar Ficheiros de Backup com o Comando Install
Quer fazer backup de um ficheiro ao sobrescrevê-lo? O parâmetro -b faz isso automaticamente, criando um ficheiro com o sufixo ~ como backup. Pode até personalizar este sufixo com -S:

```bash
install -b -S .backup NomeDoFicheiro NomeDoDiretorio
```
