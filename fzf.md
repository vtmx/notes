# fzf

```
#fish
set -gx FZF_DEFAULT_OPTS '
  --color=fg:#abb2bf,bg:#23272e,hl:#61afef
  --color=fg+:#abb2bf,bg+:#2c313c,hl+:#61afef,gutter:#23272e
  --color=info:#5c6370,prompt:#98c379,pointer:#abb2bf
  --color=marker:#abb2bf,spinner:#abb2bf,header:#abb2bf'

# bash
export FZF_DEFAULT_OPTS="\
  --height 50% --reverse \
  --margin=0 --padding=0 \
  --border=none --preview-window=''\
  --prompt '❯ ' --marker '❯ ' --pointer '❯' \
  --color=bg:-1,fg:-1 \
  --color=bg+:bright-black,fg+:-1 \
  --color=hl:blue,hl+:blue \
  --color=info:-1,marker:blue \
  --color=prompt:green,spinner:green \
  --color=pointer:-1,header:-1 \
  --color=gutter:-1,border:black"

bindings
Ctrl + T = LS
Ctrl + R = History
 Alt + C = CD
 Tab     = Marca com fzf -m
```

## Links
- https://minsw.github.io/fzf-color-picker
- https://github.com/junegunn/fzf/issues/1051
