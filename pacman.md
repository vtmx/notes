# pacman

# Instala
pacman -S

# Remove
pacman -R

# Remove remove with dependencies not used
pacman -Rs

# Lista pacotes
pacman -Qqe

# Lista pacotes não usados
pacman -Qtdq

# Verifica dependência do pacote
pacman -Qi package

# Cria um arquivo com a lista de pacotes instalados
pacman -Qqe > packages.txt 

# Instala todos os pacotse usando um arquivo com listagem
pacman -S --needed - < packages.txt 

## Criando pacotes

```
makepkg
  Cria o pacote.

-s
  Respolve as dependências.

-i
  Instala o pacote.

--check
  Checar o pacote.

--noconfirm
  Sem confirmação.
```

## pkgbuild
- Crie diretório pkgbuild e entre nele
- Crie arquivo PKGBUILD
- `makepkg` cria o pacote
- `makepkg -si` cria e instala o pacote
- `sudo pacman -U --noconfirm packagename-any.pkg.tar.zst`
- `pacman -R --noconfirm packagename`

## Rereferências
https://github.com/kretcheu/dicas/blob/master/pacman.md
