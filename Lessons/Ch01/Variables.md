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

## A Plea
MAKE THE NAMES OF YOUR VARIABLES RELAVENT TO THE VALUE OF THE VARIABLE!!!
No seriously, you'll do a huge favor to everybody who has to read your code. This applies throughout most of programming, weather it be variable names, filenames, or function names, please make names readable.

Nobody wants to see a variable named `x` and see x defined as `let x = gph()` and have to figure out what the hell gph does. (For reference, gph is an acronym that stands for Get Player Health.) This is just an example, but you can see why this would be horrible to work with.