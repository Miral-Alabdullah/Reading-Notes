# Content

## JAVASCRIPT

>> CHAPTER 3: 
>> * Object Literals

>> CHAPTER 5: 
>> * Document Object Model (DOM)


<br>
<hr>
<br>

+ **CHAPTER 3 :**

![objects!](https://oniondiscussions.files.wordpress.com/2013/04/objects.gif)

> Everything in the picture above is an object for the computers! In another word, anything physically exists in the world is an object 

So, What is the object? 

<cite>Objects group together a set of variables and functions to create a model of a something you would recognize from the real world.  <mark>[1]</mark> </cite>

With the object, we do not call the functions and the variables by their common names. They both have new names which are : 

* Property (variable) : It tells us more about the object, and each object must has different values of properties.

* Method (function) : It represents the behavior of the object.

<br>

**How to declare an object?**

**1-** Name the object.

**2-** Curley brackets.

**3-** declare the keys/names of the properties.

**4-** set the value for each key.

**5-** Declare method (just like declaring the function).

```
var object_name{
   key1: 'value1',
   key2: 'value2',
   key3: 'value3',

   methodName: function(){
       //code
       return this.key //this indicates that this method uses one of the object's keys
   }
}
```

>> <cite> An object cannot have two keys with the same name. This is because keys are used to access their corresponding values. <mark>[2]</mark> </cite>

<br>

**How to access an object?**

![objects-property-access!](https://dmitripavlutin.com/static/50a87420915de18f26da616865fe9825/05127/access-object-properties-2.png)


> Regardless of the third one from the right, The first two ways what are we need for now.

For more details : 

```
object.property/methodName  // the dot called (member operator)
```

And there is another way only for the properties :

```
object['property'];
```
<br>
<br>
<hr>
<br>
<br>



+ **CHAPTER 5 :**


+ **Document Object Model (DOM)**

>> <cite> Specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window. <mark>[3]</mark> </cite>

>> <cite> Is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document. <mark>[4]</mark> </cite>


* Making a model of HTML page

>> **1-** When the browser load the web page, a model of the will be created in the memory.

>> **2-** The DOM specifies how the browser will structure the model using the DOM tree.

>>> The DOM tree is made of objects, each object represent a different part of the loaded page.


* Accessing and changing HTML page

>> **1-** The DOM can access the HTML page and change the elements or attributes. Also, it can delete or add new one. And for the styling (CSS) can do the same also. Beside, the events that can be changed.


* People call the DOM **(API) Application programming interface** --> let programs and scripts interact  (talk to each other).

<br>
<br>

**--> This DOM consists of four main nodes :**

**1- Document Node :** The root that represents the entire page (The current web page loaded into each window is modeled using a document object).

**2- Element Nodes :** The HTML structure is made up of elements, and to display the content you neen an element to mark up this content. So, in order to reach the contect you have to pass by the elements first.

**3- Attribute Nodes :** Each element can have its own attribute to add more information or to describe it much better. It is usually placed inside the angled brackets so it became before the content.

**4- Text Nodes :** The content itself.

<br>
<br>

>> "Each node is an object with methods and properties."

![DOM-tree!](https://miro.medium.com/max/1524/1*ZVg2USWwvFeRcnT2It99QQ.png)

<br>
<br>
<hr>
<br>

**Accessing and updating the DOM tree involves two steps:**

>>1: Locate the node that represents the element you want to work with.

>>2: Use its text content, child elements, and attributes. 

### BUT HOW?

**STEP 1: ACCESS THE ELEMENTS** 

>> Select an individual item node (DOM Queries)

>>> 1- getElementByld() : Using the unique id. --> Returns a single element node.

>>> 2- querySe1ector() : Using the CSS selector. --> Returns a single element node.


>> Select multiple items (DOM Queries)

>>> 3- getElementsByClassName() --> Returns one or more elements as a  NodeList.

>>> 4- getElementsByTagName() --> Returns one or more elements as a  NodeList.

>>> 5- querySelectorAll() --> Returns one or more elements as a  NodeList.

>> Traversing between element nodes (Traversing the DOM)

>>> 6- parentNode

>>> 7- previousSibl ing / nextSibl ing 

>>> 8-firstChild / lastChild 

<br>
<br>


**STEP 2: WORK W ITH THOSE ELEMENTS**

>> Access / Update text nodes, How?

```
1- select the element
2- firstChild 
3- nodeValue // let you access/update the content
```

>> Work with HTML content, How?

```
- innerHTML //allows to access child elements and text content
- text content 
- create Element()
- createTextNode()
- appendChild () / removeChild () 
```

>> Access or update attribute values, How? 

```
- hasAttribute() // check if exists
- getAttribute() // get the value
- setAttribute()
- removeAttribute() 
```

<br>
<br>

**What is the DOM query?** 

>> A method to find an element in the DOM tree. 

>> To use an element more than one, you need to store the result of the query in a variable.

>> We do not really store the element itself, but we store a reference to the node location that represent this element in the DOM tree. 

>> There are queries that usually return a NodeList such as: getElementsByTagName(). On the other hand, there are queries that always take the fastest route such as: getElementByld() --> Because there are no two elements that have the same id. 

```
document.getElementByld('The value of the ID')
```

+ **NodeList :**

>> When a DOM method can return more than one element, it returns a Nodelist (even if it only finds one matching element). 

>> It is a collection of nodes.

>> It shows the elements as the same structured of the HTML.

>> It has a properties and methods : length('To return the lenth of the list-number of items') and item('To return the wanted item by its index or its name').

**To return an item from the NodeList, You can uose either item() or the array syntax :**

**1-** item() :

```
element.item(index);
```

**2-** array syntax :

```
element[index]
```


<br>
<br>
<hr>
<br>
<br>


References : 

* <mark>[1]</mark> [JavaScript and jQuery by Jon Ducket](file:///E:/ASAC/102/Reading/Lecture%204/javascript_and_jquery_interactive_jon_du.pdf)

* <mark>[2]</mark> [JavaScript and jQuery by Jon Ducket](file:///E:/ASAC/102/Reading/Lecture%204/javascript_and_jquery_interactive_jon_du.pdf)

* <mark>[3]</mark> [JavaScript and jQuery by Jon Ducket](file:///E:/ASAC/102/Reading/Lecture%204/javascript_and_jquery_interactive_jon_du.pdf)

* <mark>[4]</mark> [HTML-DOM-W3SCHOOL](https://www.w3schools.com/js/js_htmldom.asp)