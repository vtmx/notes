yt-dlp

Show sizes:

```bash
yt-dlp --list-formats

ID       EXT RESOLUTION │   FILESIZE   TBR PROTO │ VCODEC      ACODEC
────────────────────────────────────────────────────────────────────────
hls-380  mp4 512x288    │ ~139.23MiB  461k m3u8  │ avc1.4d0016 mp4a.40.5
hls-480  mp4 848x480    │ ~252.82MiB  836k m3u8  │ avc1.64001f mp4a.40.2
hls-720  mp4 1280x720   │ ~649.76MiB 2149k m3u8  │ avc1.64001f mp4a.40.2
hls-1080 mp4 1920x1080  │ ~  1.84GiB 6222k m3u8  │ avc1.640028 mp4a.40.2
```

Download especific size:

```bash
yt-dlp -f hls-720
```

Download playlist yt:

```bash
yt-dlp -x --audio-format mp3 --replace-in-metadata title " " "-" --output "%(playlist_index|02)s-%(title)s.%(ext)s"
```

Download song yt:

```bash
yt-dlp -x --audio-format mp3 --embed-thumbnail --add-metadata -o "$filename" "$url"
```
