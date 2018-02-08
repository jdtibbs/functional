# functional
notes on functional programming

* pure function, a function that for the same input returns the same output without any observable side effects.
 * function only operates on inputs, not external state.
 * any interaction with then outside world of the function is a side effect (db access, write/read from file, etc.)

## points
* do not enclose a function within another function, just to delay evaluation.
* using generic names enables reusable code: `data.map(v=><div>Value {v}</div>)`. 

## why pure functions
* can be cached per inputs, via memoization.
* portable and self contained
* easily testable
* referential transparency - when a function can be replaced by its evaluated value without changing the behavior of the program. this enables us to reason about and refactor code.
* pure functions can run in parallel, because they are self contained. 

## tools enabling fp
### curry 
a function that when called with fewer paramteres than required returns a function that takes the remaining parameters.
 * `const add = x => y => x + y`
 * curry makes defining and calling functions like this easier.
 * curried functions should take data as the last parameter so that the resulting function can be 'pre-loaded'.
 
