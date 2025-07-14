# gpg

Lista chaves públicas:

```bash
gpg -k,--list-keys,--list-public-keys
```

Importa chave pública:

```bash
# Normaly file-signing.key
gpg --import <file>
```

Verifica chave:

```bash
# Normaly file.sig file
gpg --verify <key> <file>
```

Remove chave:

```bash
gpg --delete-keys <id>
```

Especifica texto:

```bash
gpg --armor
```

