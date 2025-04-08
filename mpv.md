# mpv

Create playlist of dir:

```bash
mpv $args --playlist=- <<< ls "$1"/*.mp3 2>&-

cd /home/Music/michael-jackson
IFS=$'\n' ; mpv $(ls -rt1 .)
```

No output in terminal:

```bash
mpv --no-video --realy-quiet *
```
