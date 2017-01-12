# Iteration & Blocks
## Learning Goals
- Learn what _Iteration_ is and how to do it.
- Learn what _Blocks_ are and how to recognize them.
- Use a _Loop Table_ to clarify how values change over the course of an iteration.

## Iteration
_Iteration_ is the process of systematically interacting with a collection of values, one at a time. We call it "looping" sometimes, and we do a lot of it. Here is a simple loop; copypasta it into the console and give it a try:

```javascript
for (var i = 0; i < 10; i++) { console.log(i); }
// So... what happened
```

### `for` Loop
The most common iterator in Javascript is the `for` loop. It can be executed three different ways, depending on what kind of loop you need

#### The `for` loop
- has three parts:
  - `var i = 0` - **starter**  
    This executes at loop start.
  - `i < 5` - **loop condition**  
    The condition to check if loop is finished. It is checked after every execution of loop body.
  - `i++` - **increment**  
    An action to perform after every iteration, but before the loop condition is checked.

```javascript
for (var i = 0; i < 5; i++) {
  // will execute 5 times
  console.log(i);
}
```

### Let's talk about Blocks...
Blocks are not a unique feature of JavaScript, but they're defs one of my favorite. What is a block? Documentation says a block is:

> A section of code which is grouped together.

Kay.....

A block is a set of instructions that is not executed immediately, but is stored in a variable or passed to a function, and is potentially executed at a later moment in time.

```javascript
for (var i = 0; i < 10; i++) { console.log(i); }
//                             ^ everything between the {} is a block
```

`console.log()` is a chunk of code that you could write out all by itself, but there's not a function called `console.log_five_times()`, so we provide our own code to be performed during each iteration of the loop.

Blocks in JavaScript are always wrapped in _braces_ {}.

### Exercise: Walk Through a Loop:
It's critically important to understand what's happening during iteration. The best way to get comfortable with loops is to make a chart showing how values change during iteration. Here's an example of a loop and it's corresponding value chart:

```javascript
for (var n = 10; n < 300; n = n * 3) {
  console.log(n / 10);
}
```

| loop count | value of n | output |
|------------|------------|---------
| 1          | 10         | 1
| 2          | 30         | 3
| 3          | 90         | 9
| 4          | 270        | 27


With your chair-pair, figure out what's happening on each iteration of the following loop, on paper, using the handy table template:

| loop count | value of x | value of y | output |
|------------|------------|------------|---------
| | | |
| | | |

You'll need more rows, but you get the idea.

```javascript
var y = 0;

for (var x = 10; x > 0; x = x - 1) {
  if (x % 2 == 0) {
    y = y + x;
    console.log(y);
  } else {
    console.log(x);
  }
}
```
