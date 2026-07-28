# html

Não funcionou muito bem:

```html
<link rel='preload' as='font' type='font/woff2' fetchpriority='low' crossorigin href='/fonts/Inter-Medium.woff2'>
```

Novo método de loading de imagens:

```html
<img src='file.jpg' alt='Img' loading='lazy' sizes='auto'>
```

Datalist:

```html
<input list='data'>
<datalist id='data'>
  <option val='1'>01</option>
  <option val='2'>02</option>
  <option val='3'>03</option>
<datalist>
```
