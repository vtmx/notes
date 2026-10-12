# ia

## Configuração

name: google
endpoint: https://generativelanguage.googleapis.com
model: gemini-3.5-flah-lite

name: groq
endpoint: https://api.groq.com/openai/v1
model: openai/gpt-oss-120b

## Harness

### crush

Positivos:
- TUI boa para navegar entre as respostas, abre rápido e tem boa resposta
- Bom para confirmação do código antes de fazer algo

Negativo:
- Interface exagerada, parece que é feita para distrair, cores padrões não conversam tudo pisca
- Cria uma pasta oculta `.crush` em cada pasta que é aberto, criando lixo exagerado
- Não reconhece alguns providers automaticamente


### opencode

Positivo:
- Boa customização de temas e keybinds

Negativo:
- O mais lento testado, chato de limpar as sessões

```
# Limpar sessões
opencode session list --format json | jq -r '.[].id' | xargs -r -n1 opencode session delete
```

### pi

Positivo:
- Resposta mais rápida que os demais no mesmo modelo

Negativo
- Criou diretório na raiz da $HOME
- Em alguns casos aparecia a pergunta em outra língua

### zerostack

Nem consegui configurar, mas parece ser rápido

### zero

Positivo:
- Melhores temas, as cores realmente são harmônicas
- Menu simples

Negativo:
- Interface de settings poderia ser maior

### zot

Positivo:
- O que mais gostei atualmente, minimalista, boas respostas e interface bacana

Negativo:
- Edição de keybindings e navegação entre as mensagens
- Temas reais
