# WM

Create cursor and get attribute of window:

```bash
xprop | grep TYPE
```

Close current window:

```bash
wmctrl -ic $(xprop -root | grep '_NET_ACTIVE_WINDOW(WINDOW)' | awk '{print $5}')
```

Go to workspace:

```bash
case $1 in
  1    ) wmctrl -s 0  ;;
  [2-7]) wmctrl -s $1 ;;
  9    ) wmctrl -s 8  ;;
  next ) wmctrl -s $(( $(wmctrl -d | awk '/*/{print $1}') + 1 )) ;;
  prev ) wmctrl -s $(( $(wmctrl -d | awk '/*/{print $1}') - 1 )) ;;
  *    ) echo 'vwm: desktop not exist'; exit 1 ;;
esac
```