# curl

Get status code of url:

```bash
curl --head 'https://modules.vlang.io/net.http.html#get' | awk '/HTTP/ {print $2}'
```

Get json:

```bash
curl -s -X POST 'https://api.groq.com/openai/v1/chat/completions' \
  -H "Authorization: Bearer $KEY" \
  -H 'Content-Type: application/json' \
  -d '{
    "messages": [
      {
        "role": "user",
        "content": "'"$MSG"'"
      }
    ],
    "model": "llama3-70b-8192"
  }'
```
