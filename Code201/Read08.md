## CSS

> **Layout**

>> * Controlling the position of elements
>> * Creating site layouts
>> * Designing for different sized screens



<br>
<br>
<br>

+ **Key Concepts in Positioning Elements**

<br>
<br>

>> <cite> CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box. </cite> <mark> [1] </mark>


| Block-level element | Inline elements    |
|---------------------|--------------------|
| Start on a new line |between a text, we can't use margin-top/bottom + width/height      |
| example : ``<h1> <p> <ul> <li>`` |example : ``<b> <i> <img> <span>``|

<br>

>> If one block-level placed another one, the outside will be called parent or containing

>> For example : ``<div>`` element -> It is common that this element act like a container of a group of other elements 

![HTML-structure!](https://images.slideplayer.com/25/8067990/slides/slide_8.jpg)


**They are showing themselves as boxes inside boxes (nested boxes), each box has a parent which is the direct container.**

### WHY? 

**To make the positioning much easier and organized**

### HOW? 

<br>

**Positioning schemes**

>> Layout of page :


| Normal flow         | Relative positioning | Absolute posioning |
|---------------------|----------------------|--------------------|
|Every block-level element appears on a new line, causing each item to appear lower down|Shifting the normal position of an element to top, bottom, right or left| It moves as the users scroll up and down the page |

<br>
<br>

**Where should the box be positioned?**

>> * ``position:static`` -> No changes, the default value.

>> * ``position:relative`` -> You can move it but its first place will be reserved.

>> * ``position:absolute`` -> It doesn't reserve the place that moved from. Its place will be changed according to the first container that relatively positioned.

>> * ``position:fixed`` -> The element relative to the browser window.

>> * ``z-index`` ->To give the element priorities.

>> * ``float`` -> Take an element and place it far even to right or to the left.

>> * ``clear`` -> The clear property allows you to say that no element (within the same containing element) should touch the left or righthand sides of a box.


<br>
<br>
<br>

References :

* [<mark>[1]</mark>](https://CSS/book)