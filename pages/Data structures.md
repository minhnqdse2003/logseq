# Types of Data Structures
	- Two type `Primitive` and `Non-Primitive`
	- Primitive:  They are `not` `objects` and hold simple values `directly`.
	- Non-Primitive (reference types): Include objects and are more complex than primitive types contain, we will have two types for Non-primitive data structure [[Linear data structure & Non-linear data structure]]
	- Static data structure: size is allocated at the `compile time` which mean size is `fixed`.
	- Dynamic data structure: size is allocated at the `run time` which mean size is `flexible`.
	- | **Aspect** | **Primitive** | **Non-Primitive** |
	  | **Definition** | Basic data types defined by Java. | Derived from classes, arrays, etc. |
	  | **Stored** | Value directly stored in memory. | Stores a reference to the object. |
	  | **Default Value** | Default is specific to type (e.g., `0`). | Default is `null`. |
	  | **Mutable** | Immutable (value cannot change). | Usually mutable (can change state). |
	  | **Operations** | No methods or attributes. | Can have methods, attributes, etc. |
	- Primitive types: `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`
	- Note: `String` is not consider as a primitive data type because in java we will have concept named `String pool` to limit the duplicate declaration for string value to improve performance. They will `Find` in the `String pool` which is located in the heap to find if the value exist -> Ref directly to that `otherwise` it will create a new value in `String pool` -> Ref to the value which was declare before.
- # Major Operations
	- `Searching`, `Sorting`, `Insertion`, `Updation`, `Deletion`