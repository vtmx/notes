# imagemagick

Converter arquivo pdf:

```bash
magick file.jpg -compress jpeg file.pdf
```

Remover senha pdf:

```bash
qpdf --decrypt --password=xxx file-protect.pdf file.pdf
```

Convert and resize:

```bash
magick -resize 2560x1435 src.png dist.avif
```

Convert:

```bash
magick input.jpg output.png
magick input.png output.avif
```

Convert and psd:

```bash
magick input.psd[0] output.jpg
```

Create a wallpaper with a logo:

```bash
inkscape logo.svg --export-filename=logo.png
inkscape logo.svg -o logo.png

magick \
  -size 1920x1080 xc:'#222' \
  -gravity center \( logo.svg -resize 350x -fill '#ffff00' \) \
  -composite wallpaper.png
```

Nice optimize:

```bash
magick out.jpg \        # input
  -strip \              # remove metadata
  -quality 85 \         # quality
  -gaussian-blur 0.05 \ # blur
  out2.jpg              # output
```

Avif format:

```bash
avifenc input.jpg output.avif
avifenc -q 80 input.jpg output.avif
```

Jxl format:

```bash
cjxl input.png output.jxl
```
