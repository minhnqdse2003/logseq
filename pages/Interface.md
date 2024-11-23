# Types vs Interfaces
collapsed:: true
	- In TypeScript, both `types` and `interfaces` can be used to define the `structure of objects` and enforce `type checks`. However, there are some `differences` between the two.
	- `Types` are used to create a `new named` type based on an`existing type`  or to `combine existing types` into a new type. They can be created using the type keyword.
		- ```
		  type Person = {
		    name: string;
		    age: number;
		  };
		  
		  const person: Person = {
		    name: 'John Doe',
		    age: 30,
		  };
		  ```
	- `Interfaces`, on the other hand, are used to `describe the structure` of objects and classes. They can be created using the interface keyword.
		- ```
		  interface Person {
		    name: string;
		    age: number;
		  }
		  
		  const person: Person = {
		    name: 'John Doe',
		    age: 30,
		  };
		  ```
- [External Resource](https://stackoverflow.com/questions/37233735/interfaces-vs-types-in-typescript)
- |               | Types    | Interface | Note                                                                                                                                           |
  |---------------|----------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
  | Objects / Functions | `Yes`   | `Yes`    | Syntax differs                                                                                                                                |
  | Other Types        | `Yes`   | `No`     |                                                                                                                                                |
  | Extend             | `Yes`   | `Yes`    |                                                                                                                                                |
  | Implements         | `Yes`   | `Yes`    | Class and interface are **considered static blueprints**; cannot implement/extend a type alias that names a **union type**.                     |