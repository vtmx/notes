# curl

Retorna status da página:

```bash
curl -Is https://www.biggerpockets.com/blue | head -n1 | awk '{print $2}'
curl --head 'https://modules.vlang.io/net.http.html#get' | awk '/HTTP/ {print $2}'
```

Recebe json:

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
