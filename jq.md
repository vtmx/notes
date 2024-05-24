# jq

```bash
# Use curl
curl -s <url> | jq

# Get list of results
jq .results[] <file>

# Get name of results
jq .results[].name

# Get only values without ""
jq -r .results[].name
```
