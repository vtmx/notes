# Git

## Comandos

Adicionar diretório remoto<br>
`git remote add origin git@github.com:vtmx/repositorio.git`<br>

Adiciona repositorio local para remoto<br>
`git push -u origin branch`

Faz upload das mudanças<br>
`git push origin branch`

Visualiza repositórios remotos conectados<br>
`git remote -v`

Remove repositório remoto<br>
`git remote rm origin`

Faz upload para o branch principal
`git push`

Baixa mudanças do repositório remoto<br>
`git pull`

fatal: refusing to merge unrelated histories - Força pull<br>
`git pull origin branchname --allow-unrelated-histories`<br>

## Soluções

Rejeitar<br>
`! [rejected] master -> master (fetch first)`<br>
`git push --force origin master`

Cria um novo branch e entra nele<br>
`git checkout -b novo-branch`

## Netlify

- `Branch deploy: dev`
- `Build command: hugo`
- `Publish directory: public`

## Limpando cache

`git rm -r --cached .`

Adiciona todos os arquivos novos ou modificados para a área de stage
`git add -A`

Adicionando todos os arquivos e diretorios modificados
`git add .`

`git checkout HEAD -- my-file.txt # remove arquivo do stage`
`git rm --cached <filePath> #unstage a single file`
`git reset #unstage all staged files`
`git commit -am 'git cache cleared'`

## Branch

Cria novo branch e vai para ele
`git checkout -b branch-name`

Vai para o branch
`git checkout branch-name`

Remove branch
`git branch -d branch-name`

Remote<br>
`git push --delete <remote_name> <branch_name>`<br>
`git branch -d <branch_name>`

Local<br>
`git branch -d branch_name`<br>
`git branch -D branch_name`

Erro<br>
Set your username:
`git config --global user.name "FIRST_NAME LAST_NAME"`
Set your email address:
`git config --global user.email "MY_NAME@example.com"`

remove mensagem de erro CRLF
`git config --global core.autocrlf false`

## Nomes de commit

"Fix", "Add", "Change"

## Links
https://www.conventionalcommits.org/en/v1.0.0/
https://chris.beams.io/posts/git-commit/
https://docs.github.com/pt/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent
https://github.com/joshnh/Git-Commands/blob/master/READMEpt.md
https://github.com/bpassos/git-commands/blob/master/translation/README.pt-br.md
https://gist.github.com/digitaljhelms/4287848
https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches
https://help.github.com/articles/closing-issues-using-keywords/
https://pt.stackoverflow.com/questions/210652/qual-objetivo-do-git-push-u
https://stackoverflow.com/questions/34400272/visual-studio-code-always-asking-for-git-credentials
https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-both-locally-and-remotely
