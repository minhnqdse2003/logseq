- Object:  `real-word` entity that has state and behaviour. Reference to something tangible( touchable ). Object is an `instance` of class (blueprint for an object). Key concept: `real-world entity`, `runtime entity`, `state and behavior`, `Instance of class`.
- A class will contain:
	- `Fields`
	- `Methods`
	- `Constructor` - Unique methods that are use to initialize class object
	- `Blocks`: `Instance blocks` and `Static blocks`
	  collapsed:: true
		- **Instance blocks** : Executed when ever an instance of a class (object) is created to `initialize instance variables` or `perform setup logic`. Executed `before` the `constructor` of the class is `called`.
		- ```
		  class MyClass {
		      // Instance variables
		      int x;
		      int y;
		  
		      // Instance block (initialization block)
		      {
		          // This block will be executed when an instance is created
		          x = 10;
		          y = 20;
		          System.out.println("Instance block executed");
		      }
		  
		      // Constructor
		      MyClass() {
		          System.out.println("Constructor executed");
		      }
		  
		      public static void main(String[] args) {
		          MyClass obj1 = new MyClass();
		          MyClass obj2 = new MyClass();
		      }
		  }
		  -----------------------------------------------------------
		  Output:
		  Instance block executed
		  Constructor executed
		  Instance block executed
		  Constructor executed
		  ```
		- **Static Blocks**: Block of code inside a class that is executed only `once` when the class is `loaded into memory` by the JVM, `NOT` when an instance is created. Static block runs `before any static methods` or `constructors` of the class are `invoked`.
		- ```
		  class MyClass {
		      static int count;
		  
		      // Static block
		      static {
		          // This block will be executed once when the class is loaded
		          count = 100;
		          System.out.println("Static block executed");
		      }
		  
		      public static void main(String[] args) {
		          System.out.println("Main method executed");
		          System.out.println("Count = " + count);
		      }
		  }
		  -----------------------------------------------------------
		  Output:
		  Static block executed
		  Main method executed
		  Count = 100
		  ```
		- `Migrate both`:
		- ```
		  class MyClass {
		      static int staticVar;
		      int instanceVar;
		  
		      // Static block (executed once when class is loaded)
		      static {
		          staticVar = 10;
		          System.out.println("Static block executed: staticVar initialized");
		      }
		  
		      // Instance block (executed every time an object is created)
		      {
		          instanceVar = 20;
		          System.out.println("Instance block executed: instanceVar initialized");
		      }
		  
		      // Constructor
		      MyClass() {
		          System.out.println("Constructor executed");
		      }
		  
		      public static void main(String[] args) {
		          System.out.println("Main method executed");
		  
		          MyClass obj1 = new MyClass();
		          MyClass obj2 = new MyClass();
		      }
		  }
		  -----------------------------------------------------------
		  Output:
		  Static block executed: staticVar initialized
		  Main method executed
		  Instance block executed: instanceVar initialized
		  Constructor executed
		  Instance block executed: instanceVar initialized
		  Constructor executed
		  ```
-