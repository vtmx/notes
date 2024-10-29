# vlang

Adiciona link:

```bash
sudo ./v symlink
```

Remove link:

```bash
unlink v
```

Executa:

```bash
v run hello.v
```

Hot-reload:

```bash
v watch run hello.v
```

Vigia:

```bash
v watch hello.v
```

Compila:

```bash
v hello.v
./hello
```

Write a file:

```v
import os

filename := './file.txt'
os.create(filename) or { panic('error create $filename') }
print(os.read_file(filename) or { panic('error read $filename') }
os.rwite_file(filename, 'Simple text') or { panic('error write $filename') }
```
