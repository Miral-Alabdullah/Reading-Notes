# Contents 

## 1) HTML

> **Lists**

>> * Numbered lists
>> * Bullet lists
>> * Definition lists

## 2) CSS

> **Boxes**

>> * Controlling size of boxes
>> * Box model for borders, margin, and padding
>> * Displaying and hiding boxes

## 3) JavaScript


<br>
<br>


## 1) HTML

First of all, let me ask you **What is the meaning of the list?**

I googled it and I found the : 

> <cite> A record of short pieces of information, such as people's names, usually written or printed with a single thing on each line and often ordered in a way that makes a particular thing easy to find. <mark>[1]</mark></cite>


![List!](https://www.jotform.com/blog/wp-content/uploads/2018/08/to-do-list-compressor.jpg)

*Okay! that is good so far.* 

## BUT, how can I implement this list to be displayed on my webpage? 

There are three types of lists actually, let's check them together : 

+ **Numbered lists (Ordered list):** 

>> In this list each item will have its own number. We use this kind of list usually for something needs to be done step-by-step.

```
<ol>
    <li>Wake up</li>
    <li>Take a shower</li>
    <li>Get your coffee</li>
    <li>Be ready for the lecture</li>
</ol>
```
This code above will show the list as follows: 

```
1- Wake up
2- Take a shower
3- Get your coffee
4- Be ready for the lecture
```

What if wanted to be ordered by letters, or different numbers maybe? 

You can easily do that by adding ``type`` attribute like this : 

```
<ol type="A">
    <li>Wake up</li>
    <li>Take a shower</li>
    <li>Get your coffee</li>
    <li>Be ready for the lecture</li>
</ol>
```

<br>
<br>


+ **Unordered lists:** 

>> The items here are not being ordered, let's check : 

```
<ul>
    <li>Wake up</li>
    <li>Take a shower</li>
    <li>Get your coffee</li>
    <li>Be ready for the lecture</li>
</ul>
```

This code above will show the list as following : 

<ul>
    <li>Wake up</li>
    <li>Take a shower</li>
    <li>Get your coffee</li>
    <li>Be ready for the lecture</li>
</ul>

What if I wanted to change this bullet? can I? 

Well, yes you can! let's check together : 

```
<ul style="list-style-type:circle;">
    <li>Wake up</li>
    <li>Take a shower</li>
    <li>Get your coffee</li>
    <li>Be ready for the lecture</li>
</ul>
```

This code above will show the list as follows: 


<ul style="list-style-type:circle;">
    <li>Wake up</li>
    <li>Take a shower</li>
    <li>Get your coffee</li>
    <li>Be ready for the lecture</li>
</ul>



<br>
<br>


+ **Definition list:** 

>> It uses to list some terms and add a description to each one

Let's check!!

```
<dl> // defining the list
<dt>ASAC</dt> // defining the term
<dd>- code201</dd> // defining the description
<dl>
```


This code above will show the list as follows : 

<dl>
<dt>ASAC:</dt>
<dd>- code201</dd>
<dl>


### AND, lists can be nested inside each other!!


<br>
<br>
<hr>
<br>
<br>


## 2) CSS

![Boxes!](https://stuyhsdesign.files.wordpress.com/2016/05/yoko-html5.png?w=656)

As you can see in the picture above, the structure of HTML will display the elements as multi-boxes inside each other. To style this structure we need to style these boxes in order to get the good-looking for the page.

**How?**

<br>

> Lets step into details :

| Property                    | Effects                                                                                                |
| ----------------------------| ------------------------------------------------------------------------------------------------------ |
| ``width``, ``Height``       | We can change the width and height of the box using either pixels, percentage, or ems                   |
| ``min-width``               | It uses to display the min-width of the box when the browser is narrow                                 |
| ``max-width``               | It uses to display the max-width of the box when the browser is wide                                   | 
| ``max/min-height``          | To limit the height of boxes and to see if they fit the content enough or not                          |
| ``overflow``                | If the container smaller than the content we can use either scroll or hidden                           |
| ``scroll``                  | This will add a scrollbar to the box                                                                   |
| ``hidden``                  | Will hide any extra content that went out of the box                                                   |

<br>
<br>

>>> When we use percentage the size will be relative to the size of the browser.

>>> When we use ems the size of the box will be depending on the content.

<br>
<br>

![Boxes!](https://chelsey-wiley.github.io/css-reference-guide/box_model.gif)

<br>
<br>


* Margin: The space between the borders.

* Padding: The space between the content and the border.

* Border: The border separates the edge of one box from another.

<br>
<br>


| Property    |      Individual property                                                                                             |
| ------------| -------------------------------------------------------------------------------------------------------------------- |
| ``border``  | border-width / border-style / border-color / And you can change each one from any orientation                        |
| ``Padding`` | Padding-top / Padding-left / Padding-right / Paddting-bottom (The value of it specified with pixsles or it can be ms)| 
| ``Margin``  | Same like the padding                                                                                                |


<br>
<br>

**Change Inline/Block:**

```
li {
    display : inline-block; //Causes a block-level elements and they will be on the same line
    display : block; //Causes a block-level elements
    dsiplay : inline; //Causes a block-level element to act like an inline element
    display : none; //Will hide the elements from the page
}
```
<br>
<br>


**Box Shadows**


| Horizontal offset   | Vertical offset    | Blur distance   | Spread of shadow     |                                                         
| --------------------| -------------------|-----------------| -------------------- |
| To the left of the box| Top of the box| solid line like a border| Expand in all directions|


<br>
<br>
<hr>
<br>
<br>

## 3) JavaScript

**Datatypes**

>Type coercion: Javascript can convert the data types 

>Weak typing: JavaScript is said to use weak typing because the data type for a value can change. 

* String: any text or set of characters "Miral" & 'Miral'

* Number: any kind of numbers (integer/decimal/float..)

* Boolean:  True or False

* "Zero" is a value. It is the unique, known quantity of zero, which is meaningful in arithmetic and other math

* "Null" is a non-value. It is a "placeholder" for a data value that is not known or not specified

* Undefined: Variable has been declared but not yet assigned a value.

<br>
<br>

**TRUTHY & FALSY VALUES**

> Truthy: can be treated a true or 1

> Falsy: can be treated a false or 0


<br>
<br>

**Loops:**

>It is a programming structure that checks a condition firstly then it will execute the code block as soon as the condition evaluates true, once it gives false then the loop will stop checking/executing. In order to reduce redundant code.


* For: The condition in this type of looping will be a counter that counts numbers; It will execute the code as many as the counter counts.

* While: This type of looping has nothing to do with the counting, as soon as the condition is true the code will be executed.

* Do..While: It is pretty much like while instead of executing the statement in the curly braces at least once even if the condition is false.



![Loops!](https://i.stack.imgur.com/ZTRtY.png)



<br>
<br>
<hr>
<br>
<br>

References :

* [<mark>[1]</mark> The meaning of the list](https://dictionary.cambridge.org/dictionary/english/list)
