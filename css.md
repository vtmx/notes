# CSS

```css
[data-value] {
  /* Attribute exists */
}

[data-value="foo"] {
  /* Attribute has this exact value */
}

[data-value*="foo"] {
  /* Attribute value contains this value somewhere in it */
}

[data-value~="foo"] {
  /* Attribute has this value in a space-separated list somewhere */
}

[data-value^="foo"] {
  /* Attribute value starts with this */
}

[data-value|="foo"] {
  /* Attribute value starts with this in a dash-separated list */
}

[data-value$="foo"] {
  /* Attribute value ends with this */
}

/* Multiple values */
clamp(min, val, max)

/* Multiple colors based color scheme */
:root {
  color-scheme: light dark;
}

body {
  color: light-dark(#333b3c, #efefec);
  background-color: light-dark(#efedea, #223a2c);
}

/* Reset */

*, *::after, *::before {
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

img, canvas, picture, svg, video {
  display: block;
  max-width: 100%;
}

h1, h2, h3, h4, h5, h6, p {
  overflow-wrap: break-word;
  hyphens: auto;
}

/* Reset */
/* https://www.youtube.com/watch?v=2lyDv0wOQuQ */
/* https://www.joshwcomeau.com/css/custom-css-reset */

/* Color schemes */
/* https://developer.mozilla.org/en-US/docs/Web/CSS/color-scheme */

/* Font sizes */
/* https://developer.mozilla.org/pt-BR/docs/Web/CSS/font-weight */

/* System colors */
/* https://drafts.csswg.org/css-color/#system-color */
/* https://developer.mozilla.org/en-US/docs/Web/CSS/system-color */
```
