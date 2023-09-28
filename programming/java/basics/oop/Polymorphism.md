# Polymorphism:

Polymorphism is derived from two Greek words: poly (many) and morphs (forms). In object-oriented programming, polymorphism allows objects of different classes to be treated as objects of a common super class. The most common use of polymorphism is when a parent class reference is used to refer to a child class object.

## Key Concepts:

##### Compile-Time Polymorphism (Static Polymorphism): 

Achieved through method overloading, where two or more methods in the same class have the same name but different parameters.

##### Run-Time Polymorphism (Dynamic Polymorphism): 

Achieved through method overriding, where a subclass provides a specific implementation for a method that is already provided by its parent class.

#### Examples:

##### Compile-Time Polymorphism:

``` java
public class CompileTimePolymorphism {

    void display(int a) {
        System.out.println("Displaying int: " + a);
    }
    
    void display(double b) {
        System.out.println("Displaying double: " + b);
    }
}
```
##### Usage:

``` java
CompileTimePolymorphism obj = new CompileTimePolymorphism();
obj.display(5);       // Calls the method with int parameter
obj.display(5.5);     // Calls the method with double parameter
```
#### Run-Time Polymorphism:

Consider a superclass Animal and two subclasses Dog and Cat.

``` java
// Superclass
class Animal {
    void sound() {
    System.out.println("The animal makes a sound");
}
}

// Subclass Dog
class Dog extends Animal {
    @Override
    void sound() {
    System.out.println("The dog barks");
    }
}

// Subclass Cat
class Cat extends Animal {
    @Override
    void sound() {
    System.out.println("The cat meows");
   }
}
```
##### Usage:

``` java
Animal myDog = new Dog();
Animal myCat = new Cat();

myDog.sound();  // Calls the overridden method in Dog class
myCat.sound();  // Calls the overridden method in Cat class
```
Here, the overridden method to be invoked is determined at runtime based on the type of object, hence it's run-time polymorphism.

### Key Points:

##### Type Casting and Polymorphism: 

With polymorphism, you can assign a subclass object to a parent class reference. If you need to access subclass-specific fields or methods, you'll need to cast the parent class reference back to the subclass type.

Virtual Method Invocation: In Java, all non-static methods are by default "virtual functions." Only the method declared in the superclass determines which method is to be called at runtime (if it's overridden).

##### Benefits: 

Polymorphism aids in writing more generic and reusable code. For example, methods that operate on references to the base class can work with any of its derived classes transparently.

##### Restrictions:

Static methods cannot be overridden, hence cannot achieve runtime polymorphism.
Private, final, or static methods/functions cannot be overridden.

## Conclusion:

Polymorphism, alongside encapsulation and inheritance, is one of the core principles of object-oriented programming. It enhances flexibility and maintains the extensibility of the code, allowing objects of different types to be treated as if they're objects of the same type.