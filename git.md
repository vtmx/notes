# Git

## Comandos
```
# Adicionar diretório remoto
git remote add origin git@github.com:vtmx/repositorio.git

# Adiciona repositorio local para remoto
git push -u origin branch

# Faz upload das mudanças
git push origin branch

# Visualiza repositórios remotos conectados
git remote -v

# Remove repositório remoto
git remote rm origin

# Faz upload para o branch principal
git push

# Baixa mudanças do repositório remoto
git pull

# fatal: refusing to merge unrelated histories - Força pull
git pull origin branchname --allow-unrelated-histories
```

## Soluções
```
# Rejeitar
! [rejected] master -> master (fetch first)
git push --force origin master

# Cria um novo branch e entra nele
git checkout -b novo-branch
```

## Push
```
git init
git add -A
git commit -m 'Added my project'
git remote add origin git@github.com:sammy/my-new-project.git
git push -u -f origin main
```

## Netlify
```
# Branch deploy
dev

# Build command
hugo

# Publish directory
public
```

## Limpando cache
```
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
```
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

## Fishshell
- https://gist.github.com/josh-padnick/c90183be3d0e1feb89afd7573505cab3
- https://stianlagstad.no/2020/03/learning-how-to-use-the-ssh-agent-with-fish/
- https://stackoverflow.com/questions/10032461/git-keeps-asking-me-for-my-ssh-key-passphrase
- https://www.rockyourcode.com/ssh-agent-could-not-open-a-connection-to-your-authentication-agent-with-fish-shell/
- https://github.com/settings/keys


# Exibe a hash para poder comparar com as do github.
```
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
```
"Fix", "Add", "Change"
```

## Clone com o mínimo de commits
```
git clone --depth
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
