- boolean
	- ```
	  let isTrue: boolean = true;
	  let isFalse: boolean = false;
	  ```
- number
	- ```
	  let intValue:* number* = 42;
	  let floatValue:* number* = 3.14;
	  ```
- string
	- ```
	  let name:* string* = 'John Doe';
	  ```
- void
	- ```
	  function noop() {
	    return;
	  }
	  ```
- undefined
	- ```
	  function doSomething(*x*:* string* |* null*) {
	    if (x === null) {
	      // do nothing
	    } else {
	      console.log('Hello, ' + x.toUpperCase());
	    }
	  }
	  ```
- null
	- special syntax for removing `null` and `undefined` from a type without doing any explicit checking.
	- Writing `!` after any expression is effectively a type assertion that the value isn’t `null` or `undefined`
	- ```
	  function liveDangerously(x?: number | null) {
	    // No error
	    console.log(x!.toFixed());
	  }
	  ```
-