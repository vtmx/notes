# imagemagick

Convert and resize:

```
convert -resize 2560x1435 src.png dist.avif
```

Convert png to jpg:

```bash
magick -format jpg <file.png>
```

Create a wallpaper with a logo:

```bash
inkscape logo.svg --export-filename=logo.png
inkscape logo.svg -o logo.png

magick convert -size 1920x1080 xc:'#222' \
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
