# Inheritance

## Methods Signatures / Overloading
  * The method name
  * The number of parameters
  * The types of parameters
  * The order of parameters
  * Method Overloading is when you have the same 'method' that does different things depended upon the parameters it takes in

```Java
public void doStuff(String message, boolean important){
  // Do a thing
}

public void doStuff(){
  // Do a different thing
}

```

## How do we inherit
  * Extends key word

```Java
Class Vehicle {

}

Class Car extends Vehicle {

}
```

## Method Overriding
  * When a subclass overrides the method itself

```Java
Class Person {
  void speak (String message){
    System.out.println(message);
  }
  // Overloading
  void speak (String message, boolean shout) {
    System.out.println(message);
  }
}

Class Smoker extends Person {
  // Overriding
  void speak (String message){
    System.out.println("*cough*... " + message);
  }
}
```

## Super method
 * Allows you to access the method in the super class.

```Java
Class Person {
  void speak (String message){
    System.out.println(message);
  }
}

Class Smoker extends Person {
  void speak (String message){
    System.out.println("*cough*... " + super.speak(message));
  }
}
```
## Constructors are called from the top down

```Java
class Order {
  Order(){
    System.out.println('thing');
  }
}
class SpecialOrder extends Order{
  SpecialOrder() {
    System.out.println('thing from SpecialOrder');
  }
}
class VerySpecialOrder extends SpecialOrder {
  VerySpecialOrder() {
    System.out.println('thing from VerySpecialOrder');
  }
}

// Would print
// thing
// thing from SpecialOrder
// thing from VerySpecialOrder
```
  * If it takes a parameter

```Java
class Order {
  int amount;
  Order(int amount){
    System.out.println('thing');
  }
}
class SpecialOrder extends Order{
  SpecialOrder(int amount) {
    System.out.println('thing from SpecialOrder');
  }
}
class VerySpecialOrder extends SpecialOrder {
  VerySpecialOrder(int amount) {
    System.out.println('thing from VerySpecialOrder');
  }
}

// Would print
// thing
// thing from SpecialOrder
// thing from VerySpecialOrder
```

## Why??
  * Keep your code DRY (do not repeat yourself)
