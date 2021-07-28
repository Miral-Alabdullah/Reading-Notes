# Object-Oriented Programming Concepts? 

## What is a Object ? 

> Real-world objects share two characteristics: They all have state and behavior.

> Software objects are conceptually similar to real-world objects: they too consist of state and related behavior. 

![object](https://docs.oracle.com/javase/tutorial/figures/java/concepts-object.gif)

<br>

## What is a Class? 

> The blueprint which the instance of object created based on.

## What is Inheritance?

> Object-oriented programming allows classes to inherit commonly used state and behavior from other classes

## What Is an Interface?

> Is a group of related methods with empty bodies.

> To implement this interface, you'd use the implements keyword in the class declaration.

> Interfaces specify what a class must do and not how. It is the blueprint of the class.

## What Is a Package?

> The container that holds the classes of the project.

<br>
<hr>
<br>

# Classes 

1) Declartion => 

```
class MyClass {
    // field, constructor, and 
    // method declarations
}
```

2) Access Modifiers => 

- public modifier—the field is accessible from all classes.

- private modifier—the field is accessible only within its own class.

3) Defining Methods =>

```
public datatype method(params) {
    //do the functionality here
}
```

- The Java programming language supports overloading methods, and Java can distinguish between methods with different method signatures.

- Overloaded methods are differentiated by the number and the type of the arguments passed into the method. 

4) Providing Constructors for Your Classes 

- A class contains constructors that are invoked to create objects from the class blueprint. Constructor declarations look like method declarations—except that they use the name of the class and have no return type.

```
public same_as_the_class_name(int startCadence, int startSpeed, int startGear) {
    gear = startGear;
    cadence = startCadence;
    speed = startSpeed;
}

OR with no arguemnts => 

public same_as_the_class_name() {
    gear = 1;
    cadence = 10;
    speed = 0;
}
```

- A constructor in Java is a block of code similar to a method that’s called when an instance of an object is created.

- A constructor doesn’t have a return type.

- The name of the constructor must be the same as the name of the class.

- Unlike methods, constructors are not considered members of a class.

- A constructor is called automatically when a new instance of an object is created.


<br>
<hr>
<br>


# Binary, Decimal and Hexadecimal Numbers

1) Decimals => Decimal numbers make use of 10 symbols from 0 to 9 and its combinations to represent different values.

2) Binary => Binary number is a number expressed in the base-2 numeral system or binary numeral system, a method of mathematical expression which uses only two symbols: typically "0" and "1".

3) Hexadecimal => Hexadecimal numbers make use of 16 symbols to represent numbers, it uses the 10 symbols of decimal number system to represent values 0 to 9 and additional 6 symbols (A, B, C, D, E, F) to represent values ( 10, 11, 12, 13, 14, 15) respectively.


![object](https://i.redd.it/vfyzgjgxv6541.png)


