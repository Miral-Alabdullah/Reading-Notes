
# Primitives vs. Objects

1) Java Type System : 

- (int, boolean, double,... and so).

- Wrapper classes (Integer, Byte, Float...) => Wrapper classes which wrap a primitive type into an object.

```
Integer j = 1;          // autoboxing
int i = new Integer(1); // unboxing
```


<br>
<br>
<br>
<br>

# What Is an Exception?

> An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions. 

![Exception](https://images4.programmersought.com/849/b2/b26b36859c1c149262e7e3f87f1d6259.png)

<br> 

- examples : 

1. FileNotFoundException 

> This Exception is raised when a file is not accessible or does not open.

2. IOException 

> It is thrown when an input-output operation failed or interrupted.

3. NullPointerException 

> This exception is raised when referring to the members of a null object. Null represents nothing.

4. RuntimeException 

> This represents any exception which occurs during runtime.


## To handle the Exceptions => 

- We use try .. catch .. finally.


- The `try` statement allows you to define a block of code to be tested for errors while it is being executed.

- The `catch` statement allows you to define a block of code to be executed, if an error occurs in the try block.

- The finally statement lets you execute code, after try...catch.


```
try {
  //  Block of code to try
}
catch(Exception e) {
  //  Block of code to handle errors
}
finally {
	//  Block of code 
}

```


<br>
<hr>
<br>



# Scanning 

- import java.util.Scanner; => to create a new instance of Scanner.

- A simple text scanner which can parse primitive types and strings using regular expressions. 

```
Scanner myObj = new Scanner(System.in);  // Create a Scanner object
```