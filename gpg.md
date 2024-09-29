# gpg

List public keys:

```bash
gpg -k,--list-keys,--list-public-keys
```

Import public key:

```bash
# Normaly file-signing.key
gpg --import <file>
```

Verify key:

```bash
# Normaly file.sig file
gpg --verify <key> <file>
```

Delete key:

```bash
gpg --delete-keys <id>
```

Especify plaintext:

```bash
gpg --armor
```

