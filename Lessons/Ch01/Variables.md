# What's a 'variable'?
A variable is a piece of data which you may or may not change later. It's just like your high school Algebra I class, it's a name for a certain value.

Some variables are constant, or not variable... makes you wonder why we still call them variables but hey, I'm here to inform not question the elders of programming.

Variables tend to come in a few different *types*, though this doesn't matter much in JavaScript. The types are as follows:
* Boolean, a True or False value.
* Number, any number you can think of. 1, 2, 3, 0, -50, 1.23, pi, ect.
* String, a series of letters or numbers, such as this sentence!

## That's cool and all... but how do I make a variable?
```js
let x = 10;
```
The End. No really, that's it! This is all you need to make a variable. Let's pick this line of code apart to know what each thing is doing.

`let`: This is telling JavaScript that whatever follows is a new variable.

`x`: This is the *name* of the variable. This is how you reference the value of it and it must follow the `let` or `const` keyword

`= 10`: This is *assigning* a value to the variable `x`. 

Think of it like this. `f(x) = x^2` says that x is a variable that you fill in, this would be the `let x` portion of the line of code. Plugging a value in for x, like `f(10)`, is actually giving x a value that you can reference. This is the `= 10` part of the code.

The main thing that's special about `let` is the ability to *change* the value of your variable later.
```js
let someNumber = 20;
console.log(someNumber);
console.log(someNumber * 2);
someNumber = 10;
console.log(someNumber);
// In this example, we're reassigning the value of someNumber
```
## Curveball, not all variables can change!
```js
const x = 10;
```
Yeah so turns out there are also constants. It's considered good practice to use constants unless you *need* the ability to change a variable's value later.
```js
const someNumber = 10;
console.log(someNumber);
console.log(someNumber + 5);
console.log(someNumber * 2);
// In the above example, someNumber should be a const since its value is never changed (reassigned)
```
```js
const someNumber = 20;
console.log(someNumber);
console.log(someNumber * 2);
someNumber = 10; 
// Once the code reaches this point, it will throw an error and stop the script.
// The error will say something like "TypeError: invalid assignment to const 'x'"

// Because an error is thrown before this code, the last line of code is never ran.
console.log(someNumber);
// In *this* example, someNumber should be a variable defined with let since we're reassigning to it.
```

## Where can I and should I use variables?
Anywhere you use the same value more than three times, or in more than one file. That's my rule, other people have other guides, but that's my recommendation.
```js
const value = 10;
console.log(value * 8);
// This is an example of somewhere I'd *not* use a variable.
```
```js
const number = 30;
console.log(number);
console.log(number * 10);
// Same here
```

```js
// File1.js
export foo = "Hello!";
// ^^^ Don't worry about that, simple explanation is that it lets you use a value in another file
console.log(foo);


// File2.js
import { foo } from "File1";
// Ignore the above line, summary is that it lets this file use foo from the other file
console.log(foo);

// In this example, I *would* use a variable. This is because it makes it much easier to change what happens in file1 and file2 without having to go into both files
```
# Two Pleas
MAKE THE NAMES OF YOUR VARIABLES RELAVENT TO THE VALUE OF THE VARIABLE!!!
No seriously, you'll do a huge favor to everybody who has to read your code. This applies throughout most of programming, weather it be variable names, filenames, or function names, please make names readable.

Nobody wants to see a variable named `x` and see x defined as `let x = gph()` and have to figure out what the hell gph does. (For reference, gph is an acronym that stands for Get Player Health.) This is just an example, but you can see why this would be horrible to work with.

Also, aside from having good variable names. Above all else, don't use `var`. I bring it up since some code still uses `var` and it *does* have uses, but most of the time when `var` is used it's a bad idea. It's a legacy feature that was replaced over a decade ago in 2015. The value of `var` variables can be changed just like `let`, but it has some odd rules regarding scope.