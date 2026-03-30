# sudo

No Debian, você pode criar um novo usuário com poder de root (superusuário)
executando os seguintes comandos:

1. Abra o terminal como root: `sudo -i`
2. Crie o novo usuário: `useradd -m -s /bin/bash nome_do_usuario`
3. Defina a senha do novo usuário: `passwd nome_do_usuario`
4. Adicione o novo usuário ao grupo "sudo": `usermod -aG sudo
nome_do_usuario`

Para listar todos os usuários no Debian e saber quem é o root, você pode
seguir os passos abaixo:

1. Listar todos os usuários: Abra o terminal e execute o comando `getent
passwd`
2. Identificar o usuário root: O usuário root tem o UID (User ID) 0. Procure
pela linha que começa com `root:x:0:0:`

Ou, de forma mais simples, use o comando `grep` para encontrar o usuário
root:

```
getent passwd | grep 0
```

Isso mostrará apenas a linha do usuário root.

Observação: O comando `getent passwd` lista todos os usuários do sistema,
incluindo os usuarios systema (com UIDs menores que 1000). Se você deseja
listar apenas os usuários "normais" (com UIDs maiores que 1000), use o
comando:

```
getent passwd | awk -F: '$3 >= 1000 {print $1}'
```

Para remover um usuário no Debian, use o comando:

```
sudo userdel -r nome_do_usuário
```

Substitua "nome_do_usuário" pelo nome do usuário que deseja remover. O
parâmetro "-r" remove também o diretório home e outros arquivos associados
ao
usuário.

