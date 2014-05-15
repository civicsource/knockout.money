# Knockout Money Extender

> A simple knockout extender that wraps [accounting.js](http://josscrowcroft.github.io/accounting.js/).

## Install with [Bower](http://bower.io/)

```
bower install knockout-money
```

Then add `knockout.money.js` to your project.

## How to Use

Include the script on your page (either via a normal script tag or via an AMD loader). Then use it like so:

```js
var money = ko.observable().extend({ money: true });
money("17000");

console.log(money()); //17000
console.log(money.formatted()); //$17,000.00
```

You can also use it to set formatted money as a value. This is useful for binding user-editable text boxes to the `formatted` computed.

```js
money.formatted("$17,000.56");
console.log(money()); //17000.56
```