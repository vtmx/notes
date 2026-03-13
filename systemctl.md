# systemctl

Verifica login manager instalado:

```
systemctl status display-manager
```

Inicia um serviço imediatamente (apenas para a sessão atual):

```
systemctl start <serviço>
```

Para um serviço imediatamente:

```
systemctl stop <serviço>
```

Para e inicia o serviço novamente (útil após editar configurações):

```
systemctl restart <serviço>
```

Mostra se o serviço está rodando, erros recentes e os logs:

```
systemctl status <serviço>
```

Faz o serviço iniciar automaticamente em todo boot:

```
systemctl enable <serviço>
```

Impede que o serviço inicie no boot:

```
systemctl disable <serviço>
```

Verifica se o serviço está configurado para iniciar no boot:

```
systemctl is-enabled <serviço>
```

Reinicia o computador:

```
    systemctl reboot
    ```

Desliga o computador:

```
systemctl poweroff
```

Coloca o computador em modo de suspensão (dormir):

```
systemctl suspend
```

Hiberna o sistema (salva no disco e desliga):

```
systemctl hibernate
```

Lista todos os serviços que estão carregados no momento:

```
systemctl list-units --type=service
```

Mostra todos os serviços instalados e se estão habilitados/desabilitados:

```
systemctl list-unit-files
```

Lista apenas os serviços que falharam ao iniciar (ótimo para debug):

```
systemctl --failed
```

Recarrega o systemd. Importante: Sempre que você criar ou editar manualmente um arquivo de serviço (como um .service), você precisa rodar isso para o sistema reconhecer a mudança:

```
systemctl daemon-reload
```
