# sxhkd

Change until esc:

```bash
super + shift + v : {Up,Down}
  {amixer set Master '10%+'; notify-send Volume '10%up',\
   amixer set Master '10%-'; notify-send Volume '10%dw'}
```

Xkeys:

```bash
# Change audio controls
XF86Audio{RaiseVolume,LowerVolume,Mute}
  amixer -q set Master {10%+,10%-,toggle}

XF86Audio{Play,Prev,Next,Stop}
  $HOME/.config/bspwm/scripts/mediacontrolkeys {PlayPause,Previous,Next,Stop}

# Change brightness
XF86MonBrightness{Up,Down}
  xbacklight -{inc,dec} 5
```

Use awk:

```bash
# Change volume
super + {equal,minus,0}
  amixer -q set Master {'10%+','10%-',toggle} && notify-send 'Volume' $(awk -F"[][]" '/Left:/ \{print $2\}' <(amixer sget Master))
```
