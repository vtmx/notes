# PKGBUILD

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
```
