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

Resize:

```
if bspc query -N -n focused.floating > /dev/null; then
    case "$direction" in
        west)  bspc node -z right -"$step" 0 ;;
        east)  bspc node -z right +"$step" 0 ;;
        north) bspc node -z bottom 0 -"$step" ;;
        south) bspc node -z bottom 0 +"$step" ;;
    esac
else
    case "$direction" in
        west)  bspc node @west  -r -"$step" || bspc node @east  -r -"$step" ;;
        east)  bspc node @west  -r +"$step" || bspc node @east  -r +"$step" ;;
        north) bspc node @south -r -"$step" || bspc node @north -r -"$step" ;;
        south) bspc node @south -r +"$step" || bspc node @north -r +"$step" ;;
    esac
fi
```

## Links
- https://my-take-on.tech/2020/07/03/some-tricks-for-sxhkd-and-bspwm
- https://github.com/Exodia-OS/exodia-bspwm/tree/master/src/config/bspwm

