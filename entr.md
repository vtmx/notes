# entr

With file exec:

```bash
echo filename.sh | entr ./filename.sh
```

Clear terminal:

```bash
echo filename.sh | entr -c ./filename.sh
```

No file exec:

```bash
echo ls *.sh | entr /bin/bash filename.sh
```

## Links

- http://eradman.com/entrproject
