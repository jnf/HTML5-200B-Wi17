# Welcome to JavaScript!

## Learning Goals
- What & Why JavaScript?
- Discover the varying applications of JavaScript
- Learn where web browsers, Node and npm fit in all of this
- Gain some familiarity with JavaScript's core _Object Types_
    + `String`
    + `Number`
    + `Boolean`

## The roots of JS
Straight from [Wikipedia](https://en.wikipedia.org/wiki/JavaScript):

> JavaScript was originally developed in 10 days in May 1995 by Brendan Eich, while he was working for Netscape Communications Corporation.

> Although it was developed under the name Mocha, the language was officially called LiveScript when it first shipped in beta releases of Netscape Navigator 2.0 in September 1995, but it was renamed JavaScript when it was deployed in the Netscape browser version 2.0B3.

> The change of name from LiveScript to JavaScript roughly coincided with Netscape adding support for Java technology in its Netscape Navigator Web browser. The final choice of name caused confusion, giving the impression that the language was a spin-off of the Java programming language, and the choice has been characterized as a marketing ploy by Netscape to give JavaScript the cachet of what was then the hot new Web programming language.

## JavaScript Basics
JavaScript is an _interpreted_ language. It's also object oriented and dynamically typed. It takes inspiration from many languages that came before it, particularly _LISP_ and _C_. Here's what it looks like:

```javascript
var x = 10,
    y = 15;

console.log(x + y);
```

## Ways to interact with JavaScript (JS)
We'll be interacting with JS via the web browser (for now). Let's all open **Google Chrome** and have a look at one of the webpages in the repo we downloaded. Open **01-inline.html** in Chrome, then let's open the _Developer Tools_. The easiest way to open the _Developer Tools_ is by right-clicking anywhere on the page and selecting **Inspect** from the context menu.

The _Developer Tools_ has so many things available! We've used it for playing with CSS before; now we'll use it to interact with JavaScript. Click the tab labeled _Console_ and let's try writing some JS:


```javascript
> var x = 7;
undefined
> x + 2
9
> typeof x
'number'
>
```

Now that we've got a console available to us, let's jump in with some JavaScript specifics. We are going to talk about __variables__, __datatypes__, and __functions__.

### Saying things with `String`
JavaScript _strings_ are a sequence of characters. We use _strings_ for text that's meaningful to humans. Typically, strings are created by enclosing characters (letters, numbers, punctuation symbols, etc.) between a pair of single or double quotes.

```javascript
// Declare a String by using double quotes
"Hello World"
// => "Hello World"


"I'm thirty one characters long!".length
// => 31

// Use the + operator to concatenate strings
"Kit" + "tens!"
// => "Kittens!"
```


#### Single or Double Quotes?
Strings created from single or double quotes are identical in almost every way. Pick one and stick with it! I tend to use single quotes, because pressing shift is _burdensome_. Many programmers I know stick with double quotes because it's more common to need a `'` in a sentance than a `"`.

If you want to use a double quote character inside of a string that is already enclosed by double quotes, use the `/` character to escape the quote character.

```javascript
var str = "This is a string";
str.length;      // 16 - access the length property
str.substr(2,5); // "is is" - call the substr function
"elephant" + "hotdog"; // "elephanthotdog"
```

### Working with `Number`
Working with numbers in JavaScript is mostly trivial. Both whole numbers (integers) and numbers with decimal points (floating point numbers) are covered by the `Number` object.]

`Number` includes integers (1, 2, 3, etc.), floating point values (1.4, -40.1), infinity (+Infinity, -Infinity), and `NaN` which means "not a number." `NaN` is returned when you do a numeric operation on anything that's not a `Number`.

```javascript
10 * 5; // 50

var four = 4;
var two = 2.0;

two + four // 6.0

0.1 + 0.2; // 0.3

"asdf" - 5; // NaN
```

### `Boolean` is `true` or `false`
We're going to talk more about `Boolean` values in a bit. They are extremely important in all programming, as they provide the foundation of allowing computers to make decisions and comparisons.

```javascript
var t = true;
var f = false;
```
