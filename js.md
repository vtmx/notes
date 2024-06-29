# JS

```js
// Create a method for String
String.prototype.capitalize = function() {
  if typeof('String') {
    if (this.length === 0) {
      return '';
    } else {
      return this.charAt(0).toUpperCase() + this.slice(1);
    }
  } else {
    console.error('SyntaxError: type not String');
  }
}

let text = 'teste de texto';
console.log(text.capitalize())
```
