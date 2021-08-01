# What is Inheritance?

<br>

- <b>Definitions</b>: A class that is derived from another class is called a subclass (also a derived class, extended class, or child class). The class from which the subclass is derived is called a superclass (also a base class or a parent class).

<br>

> Object-oriented programming allows classes to inherit commonly used state and behavior from other classes

> The idea of inheritance is simple but powerful: When you want to create a new class and there is already a class that includes some of the code that you want, you can derive your new class from the existing class. In doing this, you can reuse the fields and methods of the existing class without having to write (and debug!) them yourself.


<br>


- A subclass inherits all of the public and protected members of its parent, no matter what package the subclass is in. If the subclass is in the same package as its parent, it also inherits the package-private members of the parent. You can use the inherited members as is, replace them, hide them, or supplement them with new members:

    * The inherited fields can be used directly, just like any other fields.

    * You can declare a field in the subclass with the same name as the one in the superclass, thus hiding it (not recommended).
    
	* You can declare new fields in the subclass that are not in the superclass.
    
	* The inherited methods can be used directly as they are.
    
	* You can write a new instance method in the subclass that has the same signature as the one in the superclass, thus overriding it.
    
	* You can write a new static method in the subclass that has the same signature as the one in the superclass, thus hiding it.
    
	* You can declare new methods in the subclass that are not in the superclass.
    
	* You can write a subclass constructor that invokes the constructor of the superclass, either implicitly or by using the keyword super.


<br>

![!](https://i.ytimg.com/vi/-b08i7w163o/maxresdefault.jpg)

<br>


- Example : 


![!](https://images.slideplayer.com/25/7950350/slides/slide_5.jpg)

<br>


# What Is an Interface?

> Is a group of related methods with empty bodies.

> To implement this interface, you'd use the implements keyword in the class declaration.

> Interfaces specify what a class must do and not how. It is the blueprint of the class.

> In the Java programming language, an interface is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Method bodies exist only for default methods and static methods. Interfaces cannot be instantiated—they can only be implemented by classes or extended by other interfaces.


![!](https://techvidvan.com/tutorials/wp-content/uploads/sites/2/2020/02/difference-between-class-and-interface-in-java.jpg)
