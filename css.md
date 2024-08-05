# css

Attribute exists:

```css
[data-value]
```

Attribute has this exact value:

```css
[data-value='foo']
```

Attribute value contains this value somewhere in it:

```css
[data-value*='foo']
```

Attribute has this value in a space-separated list somewhere:

```css
[data-value~='foo']
```

Attribute value starts with this:

```css
[data-value^='foo']
```

Attribute value starts with this in a dash-separated list:

```css
[data-value|='foo']
```

Attribute value ends with this:

```css
[data-value$='foo']
```

Multiple values:

```css
clamp(min, val, max)
```

Multiple colors based color scheme:

```css
:root {
  color-scheme: light dark;
}

body {
  color: light-dark(#333b3c, #efefec);
  background-color: light-dark(#efedea, #223a2c);
}
```

Reset:

```css
*,
*::after,
*::before {
  box-sizing: border-box;
}

* {
  margin: 0;
  padding: 0;
  font: inherit;
}

body {
  line-height: 1.5;
}

canvas,
img,
picture,
svg,
video {
  display: block;
  max-width: 100%;
}

h1,
h2,
h3,
h4,
h5,
h6,
p {
  overflow-wrap: break-word;
  hyphens: auto;
}
```

# Links

- https://www.youtube.com/watch?v=2lyDv0wOQuQ
- https://www.joshwcomeau.com/css/custom-css-reset
- https://developer.mozilla.org/en-US/docs/Web/CSS/color-scheme
- https://developer.mozilla.org/pt-BR/docs/Web/CSS/font-weight
- https://drafts.csswg.org/css-color/#system-color
- https://developer.mozilla.org/en-US/docs/Web/CSS/system-color
