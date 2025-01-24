# xargs

Convert all image from ls:

```bash
find . "*.png" | xargs -I{} magick {} -quality 85 {}
ls *.jpg | xargs -I{} magick {} -quality 85 -gaussian-blur 0.05 {}
```
