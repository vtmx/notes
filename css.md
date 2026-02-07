# css

Texto perfeito na caixa:

```css
p { text-box: trim-both cap alphabetic }
```

Scrollbar com cores:

```css
div { scrollbar-color: blue transparent }
```

Nova formatação hsl:

```css
div { background: hsl(10 10 10) }
```

Misturas de cores:

```css
div { background: color-mix(in srgb blue, white 10%) }
```

Justificação avançada:

```css
p { text-wrap: balance }
p { text-wrap: pretty }
```

Validações melhores:

```css
input:user-valid { border-color: green }
input:user-invalid { border-color: red }
```

Atributo existe:

```css
[data-value]

Atributo que possuí o valor exato:

```css
[data-value='foo']
```

Atributo cujo valor contém este trecho em algum lugar:

```css
[data-value*='foo']
```

Atributo que possuí este valor em uma lista separada por espaços:

```css
[data-value~='foo']
```

Atributo cujo valor começa com isto:

```css
[data-value^='foo']
```

Atributo cujo valor começa com isto em uma lista separada por hífen:

```css
[data-value|='foo']
```

Atributo cujo valor termina com isto:

```css
[data-value$='foo']
```

Múltiplos valores:

```css
clamp(min, val, max)
```

Múltiplas cores baseadas em esquema de cores:

```css
:root {
  color-scheme: light dark;
}

body {
  color: light-dark(#333b3c, #efefec);
  background-color: light-dark(#efedea, #223a2c);
}
```

Reset (normalização de estilos):

```css
*, *::after, *::before {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font: inherit;
}

body {
  line-height: 1.5;
}

canvas, img, picture, svg, video {
  display: block;
  max-width: 100%;
}

h1, h2, h3, h4, h5, h6, p {
  overflow-wrap: break-word;
  hyphens: auto;
}

/* Mostrar outline de foco apenas quando o usuário estiver navegando com tab (não ao clicar) /
/ Exceto para input e textarea */
*:focus:not(:is(input, textarea)) {
  outline: none;
}
```

# Links

- https://www.youtube.com/watch?v=2lyDv0wOQuQ
- https://www.joshwcomeau.com/css/custom-css-reset
- https://developer.mozilla.org/en-US/docs/Web/CSS/color-scheme
- https://developer.mozilla.org/pt-BR/docs/Web/CSS/font-weight
- https://drafts.csswg.org/css-color/#system-color
- https://developer.mozilla.org/en-US/docs/Web/CSS/system-color
