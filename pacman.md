# pacman

## pkgbuild
- Crie diretório pkgbuild e entre nele
- Crie arquivo PKGBUILD
- `makepkg` cria o pacote
- `makepkg -si` cria e instala o pacote
- `sudo pacman -U --noconfirm packagename-any.pkg.tar.zst`
- `pacman -R --noconfirm packagename`

## Comandos
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

# Instala
pacman -S

# Remove
pacman -R

# Lista pacotes
pacman -Qqe

# Cria um arquivo com a lista de pacotes instalados
pacman -Qqe > packages.txt 

# Instala todos os pacotse usando um arquivo com listagem
pacman -S --needed - < packages.txt 
```
