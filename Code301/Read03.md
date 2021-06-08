# Lists and Keys :


**1. What does .map() return?** a copy of the original array.

**2. If I want to loop through an array and display each value in JSX, how do I do that in React?** We use the .map() method.

**3. Each list item needs a unique** <mark>Key</mark>.

**4. What is the purpose of a key?** <cite>Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.</cite>


<br>

# How to Use the Spread Operator (…) in JavaScript.



**1. What is the spread operator?** The three dot ``(...)``, to expand an iterable object into the list of arguments.

**2. List 4 things that the spread operator can do.**

>> 1) Copying an array.

>> 2) Adding an item to a list.

>> 3) Concatenating or combining arrays.

>> 4) Adding to state in React.

**3. Give an example of using the spread operator to combine two arrays.**

```
const arrayOfAges = [20,35,40];
const arrayOfHieghts = [158, 160, 187];
const combineArrays = [...arrayOfAges, ...arrayOfHieghts] //Combining two arrays using spread operator

```

**5. Give an example of using the spread operator to add a new item to an array.**

```
let numberStore = [0, 1, 2];
let newNumber = 12;
numberStore = [...numberStore, newNumber];
```

**6. Give an example of using the spread operator to combine two objects into one.**

```
const object1 = {};
const object2 = {};
const combineObjects = [...object1, ...object2] //Combining two arrays using spread operator
```


<br>


# How to Pass Functions between Components.


**1. In the video, what is the first step that the developer does to pass functions between components?**

>> Declare a function in where the state is going to change.

**2. In your own words, what does the ``increment`` function do?**

>> It loops through the array of objects (people).

>> It checks if the name that passes is the same as the name the object.

>> Increament the count.

>> Return the alter objects.

>> These objects are stored in the ppl varible.


**3. How can you pass a method from a parent component into a child component?**

>> Just like passing the props, like a property of the object.

```
<people
increment = {this.increment} 
/>
```

**4. How does the child component invoke a method that was passed to it from a parent component?**

```
this.props.increment
```