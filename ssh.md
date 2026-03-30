# ssh

Conexão:

```
ssh usuario@ip_da_outra_maquina
```

Recomendação para Rede Local

Mesmo em rede local, o padrão ouro é usar chaves SSH em vez de senha.
Depois disso, o acesso será instantâneo e sem pedir senha.

Gere a chave (no seu PC):

```bash
ssh-keygen -t ed25519
```

Envie para o outro PC:

```bash
ssh-copy-id usuario@ip_da_outra_maquina
```

Inicia servidor:

```
sudo systemctl start ssh
```
