# Content

## 1) HTML


>> CHAPTER 6: 
>> * Tables



## 1) JavaScript


>> CHAPTER 6: 
>> * Function, Methods, and Objects

<br>
<br>
<br>
<hr>


**1) HTML**

>> CHAPTER 6: 
>> * Tables

+ **What is a table?**

> It is a combination between rows and columns. In HTML we write the table row by row and for each block in the table we call it cell.


+ **How to write a code that display a table?**

```
<table> // To create a table
<tr> // Table row -> we create the table row by row as it follows
<th>Assignment</th> // The first row which indicates the heading of the table
<th>Link</th>
</tr>
<tr> // The second row
<td>Read01</td> // Here you can add the data that belongs to the headings (Represnts the number of cells)
<td>[Class1](Code201/Read01.md)</td>
</tr>
</table>
```

| Assignment  | Link                           |
| ----------- | ------------------------------ |
| Read01      | [Class1](Code201/Read01.md)    |

<br>

+ **We use spanning columns in order to skip some columns and leave them empty and the same thing with the rows**

``<thead>`` --> The container for the headings.

``<tbody>`` --> The container for the body of the table.

``<tfooter>`` --> For the footer of the table.

``width`` --> Indicates the width of the cell.

``<cellspacing>`` --> The spaceses between the cells.

``<cellpadding>`` --> The padding between the cells.

``<border>`` --> The border of the table.

``<bgcolor>`` --> Background color.


<br>
<br>
<br>
<hr>



**1) HTML**

>> CHAPTER 6: 
>> * Function, Methods, and Objects


+ **Creating an object: Constructor nation**

```
let music = new object(); // this declaration will give us a black object we can fill with methods and keys later on.
```

+ **Lets add some keys and methods:**

```
music.favSinger = 'Queen'; // property or key
music.favSong = 'Don't stop me now'; 
music.remake(){ // method

}
```

<br>


* To update/delete the value of the key:

```
1- music.favSinger ='Bruno Mars';
2- music['favSong'] = 'When I was your man';
3- delete music.favSong;
4- music.favSinger = '' // to clear the value
```

<br>


* If the code is a comples and has many objects, we can simply create a function template like this **OBJECT CONSTRUCTOR NOTATION**:

```
function Music (favSong, favSinger)
{
    this.favSong = favSong;
    this.favSinger = favSinger; // to indicate that the property or method belongs to the object that this function creates.
}

let object1 = new music ('This is me', 'Demi lovato');
let object2 = new music ('Memories', 'Maroon5');
```

<br>



* A FUNCTION IN GLOBAL SCOPE: At the top of the script and not inside any objects or anything else.

* GLOBAL VARIABLES: Outside the individual curly brackets

* A METHOD OF AN OBJECT: When the function defined inside an object

* FUNCTION EXPRESSION AS METHOD: When the function defined globally then has been used inside another object.

<br>


+ **Arrays are objects:**

>> It is a special type of objects. They hold a set of related key/value pairs but the key here is the index that indicates to each place in the array length (both can contain the other).

<br>


+ **Built-in Objects:**

>> Web browsers implement objects that represent both the browser window and the document loaded into the browser window. 


>>> Select an individual item node (DOM Queries)

>>> 1- getElementByld() : Using the unique id. --> Returns a single element node.

>>> 2- querySe1ector() : Using the CSS selector. --> Returns a single element node.


>> Select multiple items (DOM Queries)

>>> 3- getElementsByClassName() --> Returns one or more elements as a  NodeList.

>>> 4- getElementsByTagName() --> Returns one or more elements as a  NodeList.

>>> 5- querySelectorAll() --> Returns one or more elements as a  NodeList.

<br>
<br>
<br>


A simple list (cheat sheet) of the built-in methods

* ``Math.floor()`` --> The largest integer - less than or equal the given
* ``Math.random()`` --> Generates random numbers
* ``Math.ceil()`` --> The largest integer - larger than or equal the given
* ``Math.sqrt(n)`` --> The sequare of the number
* ``Math.round()`` --> Return to the nearest integer
* ``Math.PI()`` --> 3.14 - const
* ``toFixed()`` --> Converts a number into a string, rounding to a specified number of decimals [1]
* ``toPrecision()`` --> Formats a number to a specified length [2]
* ``isNan()`` --> To check if the value is a number or not
* ``toExponential()`` --> Converts a number into an exponential notation [3]
* ``length()`` --> Returns the length of a given string
* ``toUpperCase()`` --> Turn the letters into an upper case
* ``toLowerCase()`` --> Turn the letters into a lower case
* ``charAt(number)`` --> Returns a character in a given number of index
* ``indexOf()`` --> Returns the index of a given vale
* ``lastIndexOf()`` --> Last index
* ``split()`` --> Split a string into an array of substrings, and returns the new array [4]
* ``replace()`` --> To replace a value with another
* ``trim()`` --> Removes whitespace from both sides of a string [5]
* ``substring()`` --> Returns a specific part of a string


<br>
<br>
<br>
<hr>
<br>
<br>
<br>

References : 

[1]- [5] [W3School](https://www.w3schools.com/)