# tera

## 1. Funções Nativas (Functions)
Chamadas diretamente no template usando a sintaxe {{ nome_da_funcao(...) }}:

- range: Gera um array de inteiros em um intervalo determinado (end, start, step_by).
- now: Retorna a data/hora atual em UTC ou no formato especificado (timestamp, utc, format).
- get_env: Captura o valor de uma variável de ambiente do sistema (name, default).
- get_random: Retorna um número ou valor aleatório (start, end).
- throw: Interrompe a renderização lançando um erro customizado (message).

---

## 2. Filtros Nativos (Filters)
Aplicados a expressões usando o pipe (|), como {{ valor | filtro }}:

- Texto / Strings:
  - lower: Converte para minúsculas.
  - upper: Converte para maiúsculas.
  - capitalize: Primeira letra maiúscula.
  - title: Primeira letra de cada palavra em maiúscula.
  - trim, trim_start, trim_end: Remove espaços das extremidades.
  - truncate: Corta o texto em um limite especificado.
  - wordcount: Conta a quantidade de palavras.
  - replace: Substitui ocorrências de texto.
  - slugify: Transforma texto em formato de URL amigável.
  - striptags: Remove tags HTML.
  - escape / safe: Controle de auto-escaping de caracteres perigosos.
  - linebreaksbr: Converte quebras de linha em <br>.

- Coleções e Listas:
  - first / last: Pega o primeiro ou último elemento de uma lista.
  - length: Retorna o tamanho do array, string ou objeto.
  - reverse: Inverte a ordem do array ou texto.
  - sort: Ordena os elementos.
  - slice: Fatia um array.
  - unique: Remove elementos duplicados.
  - join: Une elementos de uma lista usando um separador.
  - concat: Une dois arrays.
  - map: Extrai uma chave de um conjunto de objetos.
  - group_by: Agrupa elementos por uma propriedade.
  - filter: Filtra elementos com base em critérios.

- Números e Formatação:
  - abs: Valor absoluto.
  - round: Arredondamento numérico (method, precision).
  - filesizeformat: Converte bytes em formato legível (KB, MB, GB).
  - date: Formata datas a partir de instâncias ou timestamps.

- Conversão e Dados:
  - default: Define um valor padrão caso a variável não exista/seja nula.
  - json_encode: Serializa o valor em formato JSON.
  - as_str, int, float: Converte tipos de dados.

---

## 3. Testes Nativos (Tests)
Usados em condicionais com o operador is (ex: {% if var is defined %}):

- Checagem de Tipos: defined, undefined, null, number, string, boolean, array, object.
- Propriedades e Valores:
  - even: Número par.
  - odd: Número ímpar.
  - divisibleby: Divisível por determinado valor.
  - iterable: Se o elemento permite iteração.
  - starting_with: Se a string começa com determinado trecho.
  - ending_with: Se a string termina com determinado trecho.
  - containing: Se contém um elemento ou sub-string.

---

## Referência:

- Documentação oficial do Tera: https://keats.github.io/tera/#functions
