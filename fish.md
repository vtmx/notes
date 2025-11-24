# fish

```fish
# Verifica está vazia
if test -z "$var"

# Verifica se a variável não está vazia
if test -n "$var"

# Adiciona valor em $PATH
fish_add_path /usr/local/bin

# Install OhMyFish
curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish

# Install nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

# Histórico
cdh

# SSH
eval (ssh-agent -c)
ssh-add ~/.ssh/id_rsa

# Ou
ssh-add
ssh-keygen -p -f ~/.ssh/id_ed25519
```
