# SOLID: The First 5 Principles of Object Oriented Design

<br>

## SOLID stands for :

<br>

- **S** - Single-responsiblity Principle.

- **O** - Open-closed Principle.

- **L** - Liskov Substitution Principle.
    
- **I** - Interface Segregation Principle.

- **D** - Dependency Inversion Principle.


![!](https://devopedia.org/images/article/177/8101.1558682601.png)


<hr>
<br>
<br>



## Single-Responsibility Principle =>

* **(SRP)** : A class should have one and only one reason to change, meaning that a class should have only one job.

<br>

## Open-Closed Principle => 

* **(OCP)** : Objects or entities should be open for extension but closed for modification.

> the open/closed principle states that code entities should be open for extension, but closed for modification. to put this more concretely, you should write a class that does what it needs to flawlessly and not assuming that people should come in and change it later. it's closed for modification, but it can be extended by, for instance, inheriting from it and overriding or extending certain behaviors.

<br>

## Liskov Substitution Principle => 

* Is the one here that is most unique to object-oriented programming. the lsp says, basically, that any child type of a parent type should be able to stand in for that parent without things blowing up. 

<br>

## Interface Segregation Principle =>

* says that you should favor many, smaller, client-specific interfaces over one larger, more monolithic interface. in short, you don't want to force clients to depend on things they don't actually need.

<br>

## Dependency Inversion Principle => 

* encourages you to write code that depends upon abstractions rather than upon concrete details. you can recognize this in the code you read by looking for a class or method that takes something generic like "stream" and performs operations on it, as opposed to instantiating a specific filestream or stringstream or whatever.


<br>
<hr>
<br>


![!](https://i2.wp.com/javatechonline.com/wp-content/uploads/2021/05/SOLID_Principles-2.jpg?fit=766%2C661&ssl=1)