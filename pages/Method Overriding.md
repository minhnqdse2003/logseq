- Method overriding is a mechanism where a subclass `provides` a `new implementation` for a method that is `already defined` in its `parent class`. This allows the subclass to inherit the behavior of the parent class, but change its behavior to fit its own needs.
- ```
  class Animal {
    makeSound(): void {
      console.log('Making animal sound');
    }
  }
  
  class Dog extends Animal {
    makeSound(): void {
      console.log('Bark');
    }
  }
  
  let animal: Animal;
  
  animal = new Dog();
  animal.makeSound(); // Output: Bark
  ```