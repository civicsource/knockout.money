# Knockout Money Extender

> A simple knockout extender which wraps [accounting.js](http://josscrowcroft.github.io/accounting.js/).

## Installation

```
npm install knockout-money
```

Then add `knockout.money.js` to your project.

## Usage

`require` the script in your bundle, then:

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