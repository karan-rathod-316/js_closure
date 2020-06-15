## Hoisting Exercises

1. If the code is `valid` what will be the output and if `invalid` what will be the error. Write the error message.

```js
console.log(animal);
var animal = "monkey";
// undefined
```

```js
console.log(animal);
let animal = "monkey";
//ReferenceError: can't access lexical declaration `animal' before initialization
```

```js
console.log(animal);
const animal = "monkey";
// ReferenceError: can't access lexical declaration `animal' before initialization
```

```js
function sayHello(msg) {
  alert(msg);
}
sayHello("Hey Everyone");
// Hey Everyone
```

```js
sayHello("Hey Everyone");
function sayHello(msg) {
  alert(msg);
}
// Hey Everyone
```

```js
sayHello("Hey Everyone");
var sayHello = msg => {
  alert(msg);
};
// TypeError: sayHello is not a function
```

```js
sayHello("Hey Everyone");
let sayHello = msg => {
  alert(msg);
};
//ReferenceError: can't access lexical declaration `sayHello' before initialization
```
