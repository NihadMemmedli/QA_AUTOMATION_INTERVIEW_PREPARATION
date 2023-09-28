# Object-Oriented Programming (OOP) Basics:

## Class and objects: 

A blueprint for creating objects. Contains variables (attributes) and methods (functions).
Object: An instance of a class.
Java Example:

```java
class Car { 
    String brand;

    void drive() {
        System.out.println("Driving a " + brand);
    }
}

Car myCar = new Car();
myCar.brand = "Toyota";
myCar.drive();  // Outputs: "Driving a Toyota"
```


## Inheritance:

Enables a new class to inherit properties and behaviors (methods) from an existing class.
Promotes code reuse.
Java uses the extends keyword.
Example: If you have a base class Vehicle, a Car class can inherit from it.

## Polymorphism:

Allows objects to be treated as instances of their parent class rather than their actual type.
Example: Overriding (Method overriding allows subclass to provide a specific implementation of a method already provided by its parent class) and overloading (Overloading allows different methods to have the same name, but different parameters).
Abstraction:

It is the concept of hiding complex implementation details and showing only the essential features.
In Java, this can be achieved using abstract classes and interfaces.

## Encapsulation:

Bundling the data (attributes) and the methods (functions) that operate on the data into a single unit or class.
Restricting direct access to some of the object's components, typically achieved using private access modifiers and public getters and setters.

## Importance in Structuring Automation Frameworks and Scripts:

Code Reuse & Maintenance: Using OOP concepts, common functionalities can be abstracted to parent/base classes and reused across multiple test cases or scripts. For example, a base test class can have setup and teardown methods.

**Modularity:** With classes and objects, you can create modular and independent pieces of your automation framework. For instance, if you're employing the Page Object Model (POM), each web page can be modeled as a class.

**Scalability:** As your application grows, automation needs will also expand. OOP concepts like inheritance allow for easy scalability. New tests or functionalities can be added as subclasses without disturbing existing code.

**Readability:** OOP results in a clear and organized structure. Anyone joining the team or reviewing the code can quickly understand the framework's design and flow.

**Robustness:** Encapsulation ensures that the internal state of objects is shielded from outside interference, leading to fewer unforeseen issues.

**Flexibility:** Polymorphism allows automation engineers to use the same interface for different data types, making scripts flexible and easy to extend.

**Data Protection:** Encapsulation protects data from unintended changes and misuse.