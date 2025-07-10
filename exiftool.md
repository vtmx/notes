# exiftool

Renomeando arquivo com base na data de criação:

```bash
exiftool '-FileName<DateTimeOriginal' -d %Y-%m-%d_%H-%M-%S%%-2c.%%e *.jpg
```
