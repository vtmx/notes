# wmctrl

```bash
# List all ids window
wmctrl -l


# Close active window
wmctrl -ic $(xprop -root | grep '_NET_ACTIVE_WINDOW(WINDOW)' | awk '{print $5}')
```
