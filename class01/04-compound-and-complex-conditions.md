# Compound and Complex Conditionals

## Learning Goals
- Explore the _Truth Table_ & the _Precedence List_
- Practice expressing and evaluating complex conditions
- Learn strategies to manage complex conditions with `else if` and `case`.
- Revisit `while()` in the context of a _conditional loop_

## Compound Conditions
Comparisons are often combined. Combinations can take one of two forms, __&& (and)__ and __|| (or)__. When you combine with _and_, __both__ comparisons must be `true` for the entire combination to be `true`. By combining with `or`, when __either__ of the comparisons are `true`, the entire combination is `true`:

### Truth Table
```javascript
true && true   // true and true is true
true && false  // true and false is false
false && true  // false and true is false
false && false // false and false is false

true || true   // true or true is true
true || false  // true or false is true
false || true  // false or true is true
false || false // false or false is false
```

## Evaluating Compound Conditions: Understanding _Precedence_
Compound comparisons often involve a chain of expressions to be evaluated. JavaScript follows strict rules when deciding the order in which expressions are evaluated. These rules can be expressed in terms of their _precedence_.

__Operations with a higher _precedence_ are evaluated before operations with lower _precedence_.__ To change the order in which operations are evaluated, add parenthesis `()` around the operations you want evaluated first.

Here is an abbreviated _Precedence List_ from __highest__ to __lowest__ _precedence_:

1. `++` (postfix increment)
1. `--` (postfix decrement)
1. `!` (logical _not_)
1. `+` (unary plus)
1. `-` (unary negation)
1. `**` (sparkle)
1. `*`, `/`, `%` (multiplication, division, modulo)
1. `+`, `-` (addition, subtraction)
1. `>`, `>=`, `<`, `<=` (comparisons)
1. `==` (equality)
1. `&&` (logical _and_)
1. `||` (logical _or_)

__Note:__ _unary +_ and _unary -_ here means assigning a numeric value (_Fixnum_ or _Float_) as either positive or negative, e.g. `-5`, `-12.2`, `+30` and `+2.0`.

### Using Compound Conditions
```javascript
var firstName = prompt("What's your first name?");
var lastName = prompt("And what's your last name?");

// without compound conditions
if (firstName.length > 10) {
  if (lastName.lenght > 10) {
    console.log('Your name is considerable!');
  }
}

// same code, but with compound conditions
if (firstName.length > 10 && lastName.length > 10) {
  console.log('Your name is considerable!');
}
```

And another example of how compound conditions help eliminate duplicate code:

```javascript
// without compound conditions
if (cmd == 'add') { console.log("We're adding numbers!"); }
if (cmd == '+') { console.log("We're adding numbers!"); }

// with compound conditions
// same outcome, half as much code
if (cmd == 'add' || cmd == '+') { console.log("We're adding numbers!"); }
```


### Complex conditionals
The `if/else` code we've written above is the standard form of a conditional. It is possible to extend this form with one or more `else if` lines. Let's look at something kinda scary first:

```javascript
if (cmd == "add" || cmd == "+") {
  console.log("We're adding numbers!");
} else {
  if (cmd == "subtract" || cmd == "-") {
    console.log("We're subtracting numbers!");
  } else {
    if (cmd == "multiply" || cmd == "*") {
      console.log("We're multiplying numbers!");
    } else {
      console.log("I don't know what you want from me. :(");
    }
  }
}
```

Ooof. That's hard to follow. By leveraging `else if`, the code gets easier to read:

```javascript
// ahhhh! so much better!
if (cmd == "add" || cmd == "+") {
  console.log("We're adding numbers!");
} else if (cmd == "subtract" || cmd == "-") {
  console.log("We're subtracting numbers!");
} else if (cmd == "multiply" || cmd == "*") {
  console.log("We're multiplying numbers!");
} else {
  console.log("I don't know what you want from me. :(");
}
```

This can be very useful, when you have more than one `else if` line, because the indentation, or *nesting*, can quickly become very deep, and more difficult to understand.


### Simplifying really complex conditionals
When you have several `else if` lines within a single `if`, there's a way to write each conditional with much less repetition. First, a really long, really complex conditional:

```javascript
if (cmd == "add" || cmd == "+") {
  console.log("We're adding numbers!");
} else if (cmd == "subtract" || cmd == "-") {
  console.log("We're subtracting numbers!");
} else if (cmd == "multiply" || cmd == "*") {
  console.log("We're multiplying numbers!");
} else if (cmd == "divide" || cmd == "/") {
  console.log("We're dividing numbers!");
} else if (cmd == "exponify" || cmd == "**") {
  console.log("We're sparkling numbers!");
} else if (cmd == "sqrt") {
  console.log("We're finding the square root of numbers!");
} else {
  console.log("I don't know what you want from me. :(");
}

```

The above code works, but it's kinda messy. We can tidy it by using the `switch/case` syntax:

```javascript
switch (cmd) {
  case "add":
  case "+":
    console.log("We're adding numbers!");
    break;
  case "subtract":
  case "-":
    console.log("We're subtracting numbers!");
    break;
  case "multiply":
  case "*"
    console.log("We're multiplying numbers!");
    break;
  case "divide":
  case "/":
    console.log("We're dividing numbers!");
    break;
  case "exponify":
  case "**":
    console.log("We're sparkling numbers!");
    break;
  case "sqrt":
    console.log("We're finding the square root of numbers!");
    break;
  default:
    console.log("I don't know what you want from me. :(");
}
```

There's not a hard-and-fast rule on when to use which conditional. Always choose the combination and syntax that makes the most sense to you and is easiest to read.

## Conditional Loops: Wait a `while`
A `while` loop continues to execute as long as the _condition_ it contains evaluates to `true`.

```javascript
var text = "";
var i = 0;
while (i < 10) {
  text += "The number is " + i;
  i++;
}

console.log(text);
```

Execute the iterator `while` the condition is true:

```javascript
var i = 0;

while (i < 4) {
  console.log("i is: " + i);
  i += 1
}
```

The above code will output the values of i until i is no longer less than 4, resulting in the following output:

```
i is: 0
i is: 1
i is: 2
i is: 3
```

Be careful with `while` loops! All of us will, at some point, write an infinite loop:

```javascript
var command = prompt('wat do?');
while (command != 'add') {
  console.log('please tell me to add!');
  command = prompt('wat do?');
}

console.log("omg it's about time!");
```
