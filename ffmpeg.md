# ffmpeg

Convert file:

```bash
ffmpeg -i bigfile.mp4 smallconvertedfile.mp4
```

Otimiza tamanho:

```bash
ffmpeg -i bodas-de-prata.mpg -c:v libx264 bodas-de-prata.mp4
```

Verifica integridade do arquivo:

```bash
ffmpeg -v error -i arquivo_de_video.mp4 -f null -
```
