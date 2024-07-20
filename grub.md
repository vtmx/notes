# grub

## Editando senha root

### Habilitando atela do grub na incialização
Na inicialização do sistema quando surgir o logo do fabricante manter a tecla Esc pressionada no caso de UFEI, ou a tecla Shift para Bios.

### Editar arquivo de configuração
- Após a inicialização digite a tecla E para editar
- Na linha onde estiver escrito linux /boot...
- Verificar se existe o argumento ro, se existir modifique para rw
- Adiciona o argumento init=/bin/bash
- Pressiona F10 para salvar
- O sistema irá inciar na tela de boot como root, digite o comando `passwd` e digite uma nova senha
- Não precisa editar o grub novamente

### Lembrete de algumas opções para não exibir tela
```
# /etc/default/grub
GRUB_DEFAULT=saved
GRUB_TIMEOUT=5
GRUB_TIMEOUT_STYLE=hidden
```

## Alterando a senha de outro usuário
- Comando `su` para entrar como root
- Comando `passwd <nome-usuario>` para alterar

## Links
https://www.youtube.com/watch?v=xddMl8W0ua0
