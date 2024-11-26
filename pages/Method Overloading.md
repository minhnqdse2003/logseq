- Method overloading references to those method that have `same name` but have `difference` in method `parameters` define
- ```
  class Calculator {
      // Overloaded method with 2 parameters (int, int)
      public int add(int a, int b) {
          return a + b;
      }
  
      // Overloaded method with 3 parameters (int, int, int)
      public int add(int a, int b, int c) {
          return a + b + c;
      }
  
      // Overloaded method with different parameter types (double, double)
      public double add(double a, double b) {
          return a + b;
      }
  
      public static void main(String[] args) {
          Calculator calc = new Calculator();
  
          // Calls the first overloaded method
          System.out.println("Sum of 2 integers: " + calc.add(5, 10));  // Output: 15
  
          // Calls the second overloaded method
          System.out.println("Sum of 3 integers: " + calc.add(5, 10, 15));  // Output: 30
  
          // Calls the third overloaded method
          System.out.println("Sum of 2 doubles: " + calc.add(5.5, 10.5));  // Output: 16.0
      }
  }
  ```