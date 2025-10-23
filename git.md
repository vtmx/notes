# Git

## Comandos

Adicionar diretório remoto:

```bash
git remote add origin git@github.com:vtmx/repositorio.git
```

Adiciona repositorio local para remoto:

```bash
git push -u origin branch
```

Faz upload das mudanças:

```bash
git push origin branch
```

Geralmente usado no início:

```bash
git push -u -f origin main
```

Visualiza repositórios remotos conectados:

```bash
git remote -v
```

Remove repositório remoto:

```bash
git remote rm origin
```

Faz upload para o branch principal:

```bash
git push
```

Baixa mudanças do repositório remoto:

```bash
git pull
```

fatal: refusing to merge unrelated histories - Força pull:

```bash
git pull origin branchname --allow-unrelated-histories
```

## Soluções

```bash
# Rejeitar
! [rejected] master -> main (fetch first)
git push --force origin main

# Cria um novo branch e entra nele
git checkout -b novo-branch
```

## Push

```bash
git init
git add -A
git commit -m 'Added my project'
git remote add origin git@github.com:sammy/my-new-project.git
git push -u -f origin main
```

## Netlify

```bash
# Branch deploy
dev

# Build command
hugo

# Publish directory
public
```

## Limpando cache

```bash
# Remove cache
git rm -r --cached .

# Adiciona todos os arquivos novos ou modificados para a área de stage
git add -A

# Adicionando todos os arquivos e diretorios modificados
git add .

# Não sei
git checkout HEAD -- my-file.txt # remove arquivo do stage
git rm --cached <filePath> #unstage a single file
git reset #unstage all staged files
git commit -am 'git cache cleared'
```

## Branch

```bash
# Cria novo branch e vai para ele
git checkout -b <branch_name>

# Vai para o branch
git checkout <branch_name>

# Remove branch local
git branch -d <branch_name>
git branch -D <branch_name>

# Remove branch remoto
git push --delete <remote_name> <branch_name>
git branch -d <branch_name>

# Set your config
git config --global user.name "name"
git config --global user.email "email"

# Remove mensagem de erro CRLF
git config --global core.autocrlf false

# Adiciona ssh para não pedir senha
eval (ssh-agent -c)
ssh-add ~/.ssh/id_rsa

# Verifica se a chave no git está correta
ssh -T git@github.com
```

# Exibe a hash para poder comparar com as do github.

```bash
ssh -l

eval (ssh-agent c)

# Não tenho certeza se isso funcionou nessa etapa:
echo "set SSH_AUTH_SOCK \"$SSH_AUTH_SOCK\"; export SSH_AUTH_SOCK"
echo "set SSH_AGENT_PID \"$SSH_AGENT_PID\"; export SSH_AGENT_PID"

ssh-add ~/.ssh/id_ed25519
```

## Manjaro foi necessário instalar o x11-ssh-askpass

https://archlinux.org/packages/community/x86_64/x11-ssh-askpass/

## Nomes de commit

```bash
"Fix", "Add", "Change"
```

## Clone com o mínimo de commits

```bash
git clone --depth 1
```

## Clone com um único branch

```bash
git clone [url] --branch [branch] --single-branch
```

## Resolvendo problema arquivos

```bash
# GH001: Large files detected. You may want to try Git Large File Storage
# 2 número de commits para trás
git rebase -i HEAD~2

# s no commmit que deseja remover, salva
# https://youtu.be/TXSmxtU2tOk?feature

# Ou
git reset --soft HEAD^2

# Ou força dando prioridade para o remoto
git reset --hard origin/main
```

# Lembrar credencial

```bash
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=600'
```

## Links

- https://www.conventionalcommits.org/en/v1.0.0/
- https://chris.beams.io/posts/git-commit/
- https://docs.github.com/pt/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent
- https://github.com/joshnh/Git-Commands/blob/master/READMEpt.md
- https://github.com/bpassos/git-commands/blob/master/translation/README.pt-br.md
- https://gist.github.com/digitaljhelms/4287848
- https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches
- https://help.github.com/articles/closing-issues-using-keywords/
- https://pt.stackoverflow.com/questions/210652/qual-objetivo-do-git-push-u
- https://stackoverflow.com/questions/34400272/visual-studio-code-always-asking-for-git-credentials
- https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-both-locally-and-remotely
- https://github.com/joshnh/Git-Commands
- https://github.com/bpassos/git-commands
- https://gist.github.com/josh-padnick/c90183be3d0e1feb89afd7573505cab3
- https://stianlagstad.no/2020/03/learning-how-to-use-the-ssh-agent-with-fish/
- https://stackoverflow.com/questions/10032461/git-keeps-asking-me-for-my-ssh-key-passphrase
- https://www.rockyourcode.com/ssh-agent-could-not-open-a-connection-to-your-authentication-agent-with-fish-shell/
- https://github.com/settings/keys
