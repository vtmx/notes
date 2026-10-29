# alass

Utilizado para sincronizar legendas.

```
alass filme.mp4 legenda.str legenda_editada.str
```

Quando gerar erro:

```
alass video.mp4 sub.srt sub2.srt
error: parsing subtitle file 'sub.srt' failedcaused by: error while decoding subtitle from bytes to string (wrong charset encoding?)
```

Converter caracteres:

```bash
iconv -f ISO-8859-1 -t UTF-8 sub.srt -o sub_utf8.srt
```
