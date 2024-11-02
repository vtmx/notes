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

Get two fields:

```bash
jq -r '.[].id, .[].name'
```

Concat only strings:

```bash
jq -r '.[].name + ": " + .[].username'
```

Get only values without "":

```bash
jq -r .results[].name
```

Get all name of array:

```bash
jq -r '.[].name'
```

Get user name if name is Caramelo Melo:

```bash
jq -r '.[] | select (.name == "Caramelo Melo") | .username'
```

Get user name if name contains Caramelo:

```bash
jq -r '.[] | select (.name | contains("Caramelo") | .username'
```
