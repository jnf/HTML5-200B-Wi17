# Comparisons & Flow Control

## Learning Goals
  - MOAR booleans!
  - Use equality and numeric comparisons to change how code executes.
  - Leverage _conditionals_ and _blocks_ to make decisions in code.

## Comparisons
Equality comparisons can be used on some object types, including `String`, `Number`, and `Boolean`:

- `==` (equal to?)
- `!=` (not equal to?)

Numeric comparisons are used on `Number` objects:

- `>`  (greater than?)
- `<`  (less than?)
- `>=` (greater than or equal to?)
- `<=` (less than or equal to?)

Comparisons result in a `boolean` value and has only two possible values: `true` and `false`.

```javascript
1 > 0
// true

"hello" == "hello"
// true

"hello" == "he110"
// false omg!
```

## Flow Control: Conditionals
`if` and `else` allow you to control the flow of your program. This means that they allow you to define which blocks of code will execute, and which will be skipped.

```javascript
if (<condition>) {
  <block>
}

moar_code('here');
```

When you use an `if`, the code in the _block_ that follows (between the `{}`) will only be executed *if* the _condition_ evaluates to `true`. Awesome, right? It gets better:

```javascript
if (<condition>) {
  <block>
} else {
  <alternate block>
}

moar_code('here');
```

In this case, when _condition_ is `false`, then the _alternate block_ will execute. Otherwise, it will be skipped. When you have an `if` and an `else` only one of _block_ or _alternate block_ will execute, and that is determined by the evaluation of the _condition_.

```javascript
// let's learn something kinda fancy!
var name = prompt("Hey! What's your name?");
var myNameToo = name == "computer";

if (myNameToo) {
  console.log("Weird, that's my name too. Small world!");
} else {
  console.log("That's a great name!");
}

console.log('Well, it was nice to meet you, ' + name + '.');
```

```javascript
if (1 > 0) {
  // this block will always happen
} else {
  // this block will never happen
}
```
