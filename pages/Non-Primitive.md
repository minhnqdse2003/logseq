- Interface
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
	-
- Tuple
- Object
- unknown
- any
- never