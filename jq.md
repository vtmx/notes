# jq

Use curl:

```bash
curl -s <url> | jq
```

Get list of results:

```bash
jq .results[] <file>
````

Get name of results:

```bash
jq .results[].name
```

Get only values without "":

```bash
jq -r .results[].name
```
