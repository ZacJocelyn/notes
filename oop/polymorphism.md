# Polymorphism

## Objectives
* Describe and give examples of polymorphism
* Implement polymorphism using subclasses
* Implement polymorphism using interfaces

## Abstract Classes

```Java
abstract class Importer {
  int importCount = 0;
  abstract void getCount();
}

class JSONImporter extends Importer {
  public void getCount(){
    System.out.println(importCount);
  }
}
```
## Polymorphism and Inheritance
  * Polymorphism is a way of programming not an explicit language feature. You can program polymorphic code in either FP or OOP.

  * It consists of 2 parts
    - A method or statment that can work with objects of different types
    - A number of different types of methods with the same method Signature

```Java
abstract class Animal {
  abstract void talk();
}

class Cat extends Animal {
  void talk(){
    System.out.println("Meow");
  }
}

class Dog extends Animal {
  void doStuff(){
    System.out.println("woof");
  }
}

class Runner {
  void letsHear(Animal a) {
    a.talk();
  }
}

class Main {
  public static void main(String[] args){
    Runner runner = new Runner();
    runner.letsHear(new Cat());
    runner.letsHear(new Dog());
  }
}
```

## How is Polymorphism different from Inheritance?
  * Methods are defined in the base class
  * Only behaviors are overridden in the sub classes (not method signatures)
