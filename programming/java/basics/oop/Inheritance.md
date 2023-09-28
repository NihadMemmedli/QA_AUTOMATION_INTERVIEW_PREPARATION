# Inheritance:

Inheritance in object-oriented programming is a mechanism by which one class can inherit the fields and methods from another class. It provides a way to establish a parent-child relationship between classes.

##### Key Concepts:

**Base Class (Parent or Superclass):** The class whose properties and functionalities are inherited by another class.

**Derived Class (Child or Subclass):** The class that inherits properties and functionalities from another class.

**_extends_** keyword: In Java, the extends keyword is used to declare inheritance.

###### Example:

Consider a superclass Vehicle and a subclass Car.

``` java
// Base class or Superclass
public class Vehicle {
String brand;
int speed;

    void move() {
        System.out.println("The vehicle is moving.");
    }
}

// Derived class or Subclass
public class Car extends Vehicle {
int numberOfDoors;

    void honk() {
        System.out.println("The car is honking.");
    }
}
```

###### In the example above:

Car inherits the properties (brand and speed) and methods (move()) from Vehicle.
Car also has its own property numberOfDoors and method honk().
Using Inheritance:
``` java
Car myCar = new Car();
myCar.brand = "Toyota";
myCar.speed = 60;
myCar.move();  // Calls the method from the Vehicle class
myCar.honk();  // Calls the method from the Car class
```

#### Key Points:

Method Overriding: If a subclass provides a specific implementation for a method that is already provided by its parent class, it is known as method overriding. The overridden method in the child class should have the same name, return type, and parameters as the method in the parent class.

``` java
@Override
    void move() {
    System.out.println("The car is moving.");
}
```
**_super_** keyword: Used to refer to the immediate parent class instance variable or method. It's handy if you want to invoke the parent class's overridden method.

``` java
@Override
void move() {
    super.move();  // Calls the move method of Vehicle class
    System.out.println("The car is moving.");
}
```

###### Access Control: 

A subclass cannot inherit private members (fields, methods, and constructors) of its parent class. However, if the superclass has public or protected methods for accessing its private fields, those can be inherited.

###### Constructors: 

Constructors are not members, so they are not inherited, but a subclass can call a constructor of the superclass using the super() method.

###### Types of Inheritance: 
Java supports single inheritance only, meaning that a class cannot extend more than one class. However, a class can implement multiple interfaces, making it a way to bypass the restriction and effectively achieve multiple inheritance.

## Conclusion:

Inheritance promotes code reuse and establishes a natural hierarchy between classes. It's a pillar of object-oriented programming, allowing for the creation of a new class based on an existing class while adding or modifying behaviors specific to the new class.