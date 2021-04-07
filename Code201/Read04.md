# Contents 

## 1) HTML

> **Links**

>> * Creating links between pages
>> * Linking to other sites
>> * Email links

## 2) CSS

> **Layout**

>> * Controlling the position of elements
>> * Creating site layouts
>> * Designing for different sized screens

## 3) JavaScript

> **Functions, methods and objects**


<hr>
<br>
<br>

## 1) HTML


![HTMLHyperlinks!](https://weblog.west-wind.com/images/2019/Non-Navigating-Links-for-JavaScript-Handling/EmptyHref.png)


**How to create a link?**

We use an element called ``<a>`` and more details in the code below :

```
<a href="www.google.com">HOME PAGE</a>
```

> a stands for **anchor** : To lead you into the deep of the related link.

> ``href`` stands for HyperText Reference : It is an attrivute wher you can put the wanted link.

> As you have seen, ``<a> </a>``is an opening and closing tag element. 

> HOME PAGE --> it is an example of text that shows where the user will click to reach the link.

* When you link with another website the URL wil be called absolute URL(starts with the Domain name, followed by a specific path for that page).

* URL --> stands for Uniform Resource Locator

* To link web pages from the same site we use the relative URL

![Directory-structure!](https://i.imgur.com/NwLFL4V.png)

* As you can see the picture above, It shows how you should organize your folders and files (Directory-structure).

* The root folder that holdes all the other files and folders.

* The main homepage is **index.html** and the web server usually setup to return **index.html**



**Email links  :**

```
<a href="mailto:"> </a>
```

**Open links in a new window :**

We use another attribute called **target**

```
<a href="www.google.com" target="_blank">HOME PAGE</a>
```

**Linking to a specific part of the same page  :**

for example : 

```
<h1 id="top"> </h1> //The ID name always starts with a letter

<p><a hreaf=#top> </a></p> // The destination where you put the ID  to link, the ID must start with #HASH symbol
```


<hr>
<br>
<br>

## 2) CSS

>> <cite> CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box. </cite> <mark> [1] </mark>

| Block-level element | Inline elements    |
|---------------------|--------------------|
| Start on a new line |between a text      |
| example : ``<div>`` |example : ``<span>``|


>> If one block-level placed another one, the outside will be called parent or containing



<br>
<br>
<br>

**Positioning schemes**


| Normal flow         | Relative positioning | Absolute posioning |
|---------------------|----------------------|--------------------|
| <cite>Every block-level element appears on a new line, causing each item to appear lower down </cite>  <mark>[2]</mark>  |Shifting the normal position of an element to top, bottom, right or left| It moves as the users scroll up and down the page |


<hr>
<br>
<br>

## 3) JavaScript


| Functions           | Methods              | Objects            |
|---------------------|----------------------|--------------------|
| Series of grouped statements to perform a specific task           | Same as functions except that hte methods are a part of an object              | Made up of properties and mehods            |


+ **Functions :**

>> A reusable set of step-by-step instructions, potentially based on input, to potentially provide some output. 

* When you ask the function to perform a specific task, that means calling the function (We call the function with its name in order to run the block of statements that belong to it).

* Parameters : Named variables in the function are used to import arguments(real values passed to the functions) into this function.

* Arguments can be values or variables: If we used parameters in the function then the arguments will be values that passed to them, But If the function has no parameters and while calling it we declare variables and passed the values to them (Can be values or variables that holds values).

* The response from the performing of the function is called return value.
Sometimes we can call the function before declare it and that is fine because the compiler run through the script before the execution. 

**Types of the function :**

* Named function : 

```
function area(width, height) {
    return width  * height;
};
var size (3, 4);
```

* Function expression : 

```
var area = function (width, height) {
    return width  * height;
};
var size (3, 4);
```

we can immediately call this type of functions like this :

```
var area = ( function () {
    var width = 3;
    var height = 4;
    return width  * height;
}())
```

<hr>
<br>
<br>


References :

* [<mark>[1]</mark> The meaning of the list](https://dictionary.cambridge.org/dictionary/english/list)