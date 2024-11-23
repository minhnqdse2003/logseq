- As [type]
	- ```
	  let someValue: any = "Hello, TypeScript!";
	  let strLength: number = (someValue as string).length;
	  
	  console.log(strLength); // Outputs: 18
	  ```
- As [const]
	- ```
	  const colors = ['red', 'green', 'blue'] as const;
	  ```
- As [any]
	- ```
	  let anyValue: any = 42;
	  
	  // we can assign any value to anyValue, regardless of its type
	  anyValue = 'Hello, world!';
	  anyValue = true;
	  ```
- Non-null
	- ```
	  let name: string | null = null;
	  
	  // we use the non-null assertion operator to tell the compiler that name will never be null
	  let nameLength = name!.length;
	  ```