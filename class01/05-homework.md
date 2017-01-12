# Homework
Complete the following exercises manually. The goal is to understand the underlying concept. **Show your work**

You may use a computer to show your work. Examples include a spreadsheet like Excel or Google Sheets for making loop tables, or making an HTML &lt;table&gt;. It is also perfectly acceptable to do everything with paper and pen. Acceptable file formats for answers include **html**, **pdf**, **jpg/png**, **doc**, **xls**, **txt**, **md/markdown**, and **rtf**. If you're unsure how to present your answers in one of these formats, please reach out to me on Slack and I'll be happy to help. :)

Create a Github repo containing your answers. Separate answers for each section below into their own file (one for _expression evaluation_ and one for _loop tables_). These files should be at the project root of the repo and be easily identfiable, e.g., **loop-tables.html** or **expression-evaluation.pdf**. 

## Expression Evaulation and Precedence
Determine the final `boolean` value of these conditions. You'll need to refer to the _Truth Table_ and _Precedence List_.

```javascript
// let's do these first three together
5 > 4 && false
true && 5 * 2 > 3 + 3 * 2
true && 5 * 2 > (3 + 3) * 2

true && true || false
true && (true || false)
false && false || true
false && (false || true)
(false && false) && false && (true || false) || false

4 == "4"
4 == "4" || 4 == 4
10 % 3 == 10.0 % 3

10 * (5 / 2.0) == 10.0 * (5 / 2)
10 * 5 / 2 > 10 * (5 / 2)

2 * 2 ** 3 == (2 * 2) ** 3
(10 - 4) < +6 || -(2 * -4) > 0
```

## Loop Tables!
1) Create a loop table show the values for **loop count**, **value of x**, and **output** during each iteration.

```javascript
for (var x = 0; x <= 17; x = x + 2) {
  console.log(2 * x + 7);
}
```

2) Create a loop table show the values for **loop count**, **value of index**, **value of s1**, **value of s2**, and **output** during each iteration.

```javascript
// check out page 15 in Head First JavaScript for
// info about the substr() function below

var alpha = 'mpeuorwr';
var s1 = '';
var s2 = '';

for (var index = 0; index < alpha.length; index++) {
  if (index % 2 == 0) {
    s1 = s1 + alpha.substr(index, 1);
  } else {
    s2 = s2 + alpha.substr(index, 1);
  }
}

console.log(s1 + s2);
```
