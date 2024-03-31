# Firefox

## Search bookmarks in bar
```
type * and search
ctrl + b = Show bookmarks in sidebar
ctrl + shift + o = show bookmarks in new window
```

## Customizar menu
- Disable titlebar
- Density compact
- Settings > Colors > Manager Colors... (Override the colors...: Always)

## Local da pasta config
~/.mozilla/firefox/.default-release/chrome/userChrome.css

## Debug shortcut
```
ctrl+shift+alt+i
```

## Test extensions
```
about:debugging#/runtime/this-firefox
```

## About
```
about:blank
about:debugging
about:preferences
```

## about:config
<table>
  <tr>
    <th>Config</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>browser.compactmode.show</td>
    <td>true</td>
  </tr>
  <tr>
    <td>browser.urlbar.maxRichResults</td>
    <td>5</td>
  </tr>
  <tr>
    <td>extensions.pocket.enabled</td>
    <td>false</td>
  </tr>
  <tr>
    <td>toolkit.legacyUserProfileCustomizations.stylesheets</td>
    <td>true</td>
  </tr>
  <tr>
    <td>ui.textHighlightBackground</td>
    <td>#abb2bf</td>
  </tr>
  <tr>
    <td>ui.textHighlightForeground</td>
    <td>#23272e</td>
  </tr>
    <td>ui.textSelectAttentionBackground</td>
    <td>#23272e</td>
  </tr>
    <td>ui.textSelectAttentionForeground</td>
    <td>#23272e</td>
  </tr>
  <tr>
    <td>widget.use-xdg-desktop-portal (portal kde)</td>
    <td>1</td>
  </tr>
</table>

## Links
- https://firefox-source-docs.mozilla.org/devtools-user/browser_toolbox/index.html
- https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/theme
