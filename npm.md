# npm

Error:

```
npm i -g @olrtg/emmet-language-server
/usr/lib/node_modules/npm/lib/cli/validate-engines.js:25
    throw err
    ^

TypeError: Yallist is not a constructor
    at LRUCache.reset (/usr/lib/node_modules/npm/node_modules/semver/node_modules/lru-cache/index.js:136:22)
    at new LRUCache (/usr/lib/node_modules/npm/node_modules/semver/node_modules/lru-cache/index.js:49:10)
    at Object.<anonymous> (/usr/lib/node_modules/npm/node_modules/semver/classes/range.js:196:15)
    at Module._compile (node:internal/modules/cjs/loader:1705:14)
    at Object..js (node:internal/modules/cjs/loader:1838:10)
    at Module.load (node:internal/modules/cjs/loader:1441:32)
    at Function._load (node:internal/modules/cjs/loader:1263:12)
    at TracingChannel.traceSync (node:diagnostics_channel:328:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:237:24)
    at Module.require (node:internal/modules/cjs/loader:1463:12)
```

Solution:

```bash
sudo pacman -R npm semver node-gyp
sudo rm -rf /usr/lib/node_modules/npm/node_modules/semver
sudo pacman -S npm semver
```
