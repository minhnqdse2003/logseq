- [[Interface]]
	- ```
	  interface Person {
	    name: string;
	    age: number;
	  }
	  function greet(person: Person) {
	    return 'Hello ' + person.name;
	  }
	  ```
- Class
	- ```
	  class Car {
	    make: string;
	    model: string;
	    year: number;
	  
	    constructor(make: string, model: string, year: number) {
	      this.make = make;
	      this.model = model;
	      this.year = year;
	    }
	  
	    drive() {
	      console.log(`Driving my ${this.year} ${this.make} ${this.model}`);
	    }
	  }
	  ```
- Enum
	- ```
	  enum Direction {
	    Up = 1,
	    Down,
	    Left,
	    Right,
	  }
	  ```
- Array
	- ```
	  const numbers: number[] = [1, 2, 3];
	  ```
- Tuple
	- A tuple type is another `sort of Array` type that knows exactly how many elements it contains, and exactly which types it `contains at specific positions`.
	- ```
	  type StringNumberPair = [string, number];
	  
	  const pair: StringNumberPair = ['hello', 42];
	  
	  const first = pair[0];
	  const second = pair[1];
	  
	  // Error: Index out of bounds
	  const third = pair[2];
	  ```
- Object
	- ```
	  // The parameter's type annotation is an object type
	  function printCoord(pt: { x: number; y: number }) {
	    console.log("The coordinate's x value is " + pt.x);
	    console.log("The coordinate's y value is " + pt.y);
	  }
	  
	  printCoord({ x: 3, y: 7 });
	  ```
- unknown
- any
- never