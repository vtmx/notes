# lua

Lua é uma linguagem interessante, ao estudar um pouco sobre ela notei muitas características que acreditava ser de linguagens modernas.

Lua possuí os seguintes tipos de variáveis:

```
boolean
function
nil
number
string
table
thread
userdata
```

Imprimir:

```lua
print('texto')
```

Imprimir sem quebra de linha:

```lua
io.write('texto')
```

Recebendo número de parâmetros indefinidos:

```lua
function numbers(a, b, ...) end
```

Recebendo todos os valores indefinidos:

```lua
function numbers(...)
  local args = {...}
  return args
end
```

Recevendo valores padrões:

```lua
function numbers(a = 1, b = 2)
  return a + b
end
```

Usando pcall (protect call) para verificar se uma função é válida ou não:

```lua
local function divide(a, b)
  return a / b
end

local status, result = pcall(divide, 10, 5)

if status and type(result) == 'number' and result ~= math.huge then
  print('success: ' .. result)
else
  print('error: ' .. result)
end
```

Assert para verificar um erro:

```lua
local x = 'string'
local isnumber = assert(type(x) == 'number', 'x not a number')
if isnumber then print('number: ' .. x) end
```
