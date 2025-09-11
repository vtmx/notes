# kitty

Commands for fonts:

```bash
fc-list | grep Mono
kitty list-fonts
kitty + list-fonts --psnames | grep "BlexMono Nerd Font Medium"
```

Default shortcuts:

┌─────────────────────────────┬──────────────────────────────────────────┐
│ Action                      │ Shortcut                                 │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Show this help              │ ctrl+shift+f1                            │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Copy to clipboard           │ ctrl+shift+c                             │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Paste from clipboard        │ ctrl+shift+v                             │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Paste from selection        │ ctrl+shift+s                             │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Pass selection to program   │ ctrl+shift+o                             │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Increase font size          │ ctrl+shift+equal                         │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Decrease font size          │ ctrl+shift+minus                         │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Restore font size           │ ctrl+shift+backspace                     │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Toggle fullscreen           │ ctrl+shift+f11                           │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Toggle maximized            │ ctrl+shift+f10                           │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Input Unicode character     │ ctrl+shift+u                             │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Open URL in web browser     │ ctrl+shift+e                             │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Reset the terminal          │ ctrl+shift+delete                        │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Edit kitty.conf             │ ctrl+shift+f2                            │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Reload kitty.conf           │ ctrl+shift+f5                            │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Debug kitty.conf            │ ctrl+shift+f6                            │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Open a kitty shell          │ ctrl+shift+escape                        │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Increase background opacity │ ctrl+shift+a>m                           │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Decrease background opacity │ ctrl+shift+a>l                           │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Full background opacity     │ ctrl+shift+a>1                           │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Reset background opacity    │ ctrl+shift+a>d                           │
└─────────────────────────────┴──────────────────────────────────────────┘

## Links

- https://github.com/akinsho/dotfiles/blob/0e52b69a72883dcdea174765063f66f93c00a441/.config/kitty/kitty.conf
- https://github.com/tonsky/FiraCode/wiki/How-to-enable-stylistic-sets
- https://defkey.com/kitty-0-25-linux-shortcuts
- https://sw.kovidgoyal.net/kitty/conf
