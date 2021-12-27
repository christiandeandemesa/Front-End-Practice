# JavaScript Basics
## Printing Output
```js
// This is an inline comment.
/*
This is a
block comment.
*/

// The console.log function logs/displays whatever is in the parentheses in the console.
console.log('Hello, world!');
// 'Hello, world!'
```

## Literals
- Literals are values that can be strings (e.g. 'Hello, world!'), integers (e.g. 42), floating-point numbers (e.g. 3.14), booleans (viz. true or false), and the absence of a value (viz. null).

## Identifiers
- Identifiers are names given to variables and functions to call on them later.
- Identifiers must start with a letter, underscore, or dollar sign, but can be composed of other letters, underscores, dollar signs, and digits (i.e. 0 to 9).

## Optional Semicolon
- The semicolon used for each line of code is optional, but highly recommended to make your code more readable.

# Data Types
## JavaScript's Data Types
- A primitive data type (i.e. primitive value) is not an object, does not have methods, and is immutable.
- The six primitive values are numbers, strings, booleans, symbols, null, and undefined.

## Number Data Type
```js
```
```js
// Number.MAX_VALUE is the largest positive number JavaScript can use, and all other numbers greater than it are converted to Infinity.
console.log(Number.MAX_VALUE);
// 2 ** 1024 (i.e. 2 to the power of 1024)

// Number.MIN_VALUE is the smallest positive number JavaScript can use, and all other numbers less than it are converted to 0.
console.log(Number.MIN_VALUE);
// 2 ** -1074
```
- There are three symbolic numbers:
    1. Infinity which is any number divided by 0, or Number.MAX_VALUE multiplied by any number greater than 1.
    2. -Infinity which is any number divided by -0, or Number.MIN_VALUE multiplied by any number less than -1.
    3. NaN (Not a Number) for an unrepresentable number (e.g. imaginary numbers).
```js
// The isSafeInteger method determines if the integer is safe, and a safe integers are all integers from -(2 ** 53 - 1) to 2 ** 53 - 1.