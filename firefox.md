# Firefox

Search bookmarks in bar:

```
type * and search
ctrl + b = Show bookmarks in sidebar
ctrl + shift + o = show bookmarks in new window
```

Customizar menu:

- Disable titlebar
- Density compact
- Settings > Colors > Manager Colors... (Override the colors...: Always)

Local da pasta config:

```
~/.mozilla/firefox/.default-release/chrome/userChrome.css
```

Debug shortcut:

```
ctrl+shift+alt+i
```

xdg-portal kde integration:

```
# https://wiki.archlinux.org/title/Firefox
widget.use-xdg-desktop-portal.file-picker = 1
```

Pages:

```
~/.mozilla/firefox/<user>/places.sqlite
chrome://browser/content/browser.xhtml
chrome://browser/content/downloads/contentAreaDownloadsView.xhtml
chrome://browser/content/places/bookmarkProperties.xhtml
chrome://browser/content/places/bookmarksSidebar.xhtml
chrome://browser/content/places/historySidebar.xhtml
chrome://browser/content/places/places.xhtml
chrome://browser/content/safeMode.xhtml
chrome://browser/content/syncedtabs/sidebar.xhtml
chrome://devtools/content/framework/toolbox.xhtml
chrome://global/content/commonDialog.xhtml
chrome://global/content/pictureinpicture/player.xhtml
```

Disable cursor blink in buttons:

```
https://support.mozilla.org/en-US/questions/974774

In addition to the above:
This is likely caused by switching on caret browsing and you can toggle caret browsing on/off by pressing F7 (Mac: fn + F7).
http://kb.mozillazine.org/accessibility.browsewithcaret

Note that this is an accessibility feature of Firefox.
Tools > Options > Advanced > General > Accessibility: [ ] "Always use the cursor keys to navigate within pages"
```

## about:config

```
about:blank
about:config
about:debugging
about:debugging#/runtime/this-firefox
about:preferences
about:support
```

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
    <td>devtools.debugger.remote-enabled</td>
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

## ZenBrowser

Old newtab behavior:

```bash
zen.urlbar.replace-newtab
```

## Links

- https://docs.zen-browser.app/guides/live-editing
- https://firefox-source-docs.mozilla.org/devtools-user/browser_toolbox/index.html
- https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/theme
- https://github.com/QNetITQ/WaveFox
