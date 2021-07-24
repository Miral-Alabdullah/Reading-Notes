
# JAVA Basics => 

# Variables : A placeholder for the values in the memory. 

* The Java programming language defines the following kinds of variables: 

- Instance Variables (Non-Static Fields) : declared without the `static` keyword. Non-static fields are also known as instance variables because their values are unique to each instance of a class

- Class Variables (Static Fields) :  is any field declared with the `static` modifier.

- Local Variables : There is no special keyword designating a variable as local; that determination comes entirely from the location in which the variable is declared — which is between the opening and closing braces of a method.

- Parameters : Recall that the signature for the main method is `public static void main(String[] args`). 


<br>
<br>

# Operators : 

| Operators   | Precedence                           |
| ----------- | ------------------------------ |
| postfix      | `expr++ expr--`    |
| unary      |  	`++expr --expr +expr -expr ~ !`    |
| multiplicative      |  	`* / %`    |  
| additive      |  	`+ -`    |
| shift      |  	`<< >> >>>`   |
| relational      | `< > <= >= instanceof`    |
| equality      | `== !=`    |
| bitwise AND      |  	`&`    |
| bitwise exclusive OR      | `^`    |
| Rebitwise inclusive ORad10      |  	`|`   |
| logical AND      | `&&`   |
| logical OR      | `||`   |
| ternary      | `? :`   |
| assignment      |` = += -= *= /= %= &= ^= |= <<= >>= >>>=`   |


<br>
<br>

# Expressions, Statements, and Blocks

- Expressions: 

> An expression is a construct made up of variables, operators, and method invocations, which are constructed according to the syntax of the language, that evaluates to a single value.

```
int cadence = 0;
anArray[0] = 100;
System.out.println("Element 1 at index 0: " + anArray[0]);

int result = 1 + 2; // result is now 3
if (value1 == value2) 
    System.out.println("value1 == value2");
```

<br>

- Statements: 

> Statements are roughly equivalent to sentences in natural languages. A statement forms a complete unit of execution.

> The following types of expressions can be made into a statement by terminating the expression with a semicolon (;): 


>> - Assignment expressions

```
aValue = 8933.234;
```

>> - Any use of ++ or --

```
aValue++;
```

>> - Method invocations

```
System.out.println("Hello World!");
```

>> - Object creation expressions

```
Bicycle myBike = new Bicycle();
```


<br>

- Blocks:

> A block is a group of zero or more statements between balanced braces and can be used anywhere a single statement is allowed. 


```
class BlockDemo {
     public static void main(String[] args) {
          boolean condition = true;
          if (condition) { // begin block 1
               System.out.println("Condition is true.");
          } // end block one
          else { // begin block 2
               System.out.println("Condition is false.");
          } // end block 2
     }
}
```




<br>
<br>


# Control Flow Statements

> The statements of the code will be executed from the top to the bottom, `Control flow statements`, however, break up the flow of execution by employing decision making, looping, and branching, enabling your program to conditionally execute particular blocks of code.

- Decision-making statements : `if-then, if-then-else, switch`.

- Looping statements : `for, while, do-while`.

- Branching statements : `break, continue, return`.