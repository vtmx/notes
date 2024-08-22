# pacman

# Instalação

```bash
# Instalando pacote
sudo pacman -S package

# Sem confirmação
sudo pacman --no-confirm -S package

# Cria um arquivo com a lista de pacotes instalados:
pacman -Qqe > packages.txt

# Instala todos os pacotse usando um arquivo com listagem:
sudo pacman -S --needed - < packages.txt
```

## Remoção

```bash
# Removendo pacote
sudo pacman -R package

# Sem confirmação
sudo pacman --no-confirm -R package

# Remove com dependências
sudo pacman -Rs package

# Verifica e remove pacotes órfãos:
sudo pacman -Qtdq | pacman -Rns -

# Ou
sudo pacman -Qtdq | sudo pacman -Rns -

# Ou
sudo pacman -Qqd | pacman -Rsu -
```

## Pesquisa

```bash
# Pacote disponíveis para instalção
pacman -Fy package

# Pacotes instalados
pacman -Qqe package

# Pacotes não usados
pacman -Qtdq package

# Verifica dependência do pacote:
pacman -Qi package

```

## Cache

```bash
# Verifica tamanho do cache atual
du -h /var/cache/pacman/pkg

# Remove cache de pacotes removidos
sudo paccache -ruk0

# Remove cache e mantendo última versão de pacotes
sudo paccache -rk1

# Remove cache dos pacotes desinstalados
sudo pacman -Sc

# Limpando totalmente o cache do pacman
sudo pacman -Scc
```

## Repostórios

```bash
# Repositórios
/etc/pacman.conf

# Mirrors
/etc/pacman.d/mirrorlist
```

## Criação

```bash
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

- Crie diretório pkgbuild e entre nele
- Crie arquivo PKGBUILD
- `makepkg` cria o pacote
- `makepkg -si` cria e instala o pacote
- `sudo pacman -U --noconfirm packagename-any.pkg.tar.zst`
- `pacman -R --noconfirm packagename`

## Links

- https://github.com/kretcheu/dicas/blob/master/pacman.md
