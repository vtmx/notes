# Firefox

## Customizar menu
- Disable titlebar
- Density compact
- Settings > Colors > Manager Colors... (Override the colors...: Always)

## Debug shortcut:
ctrl+shift+alt+i

## Create a Theme
https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/theme

## Habilita customização
about:config

## Test extensions
about:debugging#/runtime/this-firefox

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
    <td>widget.use-xdg-desktop-portal (portal kde)</td>
    <td>1</td>
  </tr>
</table>

## Local da pasta config
~/.mozilla/firefox/.default-release/chrome/userChrome.css
~/.mozilla/firefox/.default-release/chrome/userContent.css

## Enable toolbox para selecionar classes
https://firefox-source-docs.mozilla.org/devtools-user/browser_toolbox/index.html
