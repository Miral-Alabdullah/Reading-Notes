# AGENDA : 

## 1) HTML

> **Text**

>> * Headings and paragraphs
>> * Bold, italics, emphasis
>> * Structrual and semantic markup


## 2) CSS

## 3) JavaScrippts

> **Basics**

> **Decisions and loops.**


<br>
<hr>
<br>


## 1) HTML

<hr>
<br>

+ **Headings AND paragraphs** : 

![HeadingsANDParagraphs!](https://media.gcflearnfree.org/content/5e4182687a65ef28580b7d20_02_10_2020/HeadingAndParagraph.png)

<br>
<br>
<br>



> **Headings** : Title or subtitles that can be displayed on the web page. In HTML there are six different levels of the headings start from 1 to 6. 

``<h1>`` : The largest (Main heading).

.

.

.

.

``<h6>`` : The smallest (Sub-heading).


![Headings!](https://blog.px-lab.com/wp-content/uploads/2017/03/html-headings.jpg)

<br>
<br>
<br>
<br>


> **Paragraphs** : <cite>To create a paragraph, surround the words that make up the paragraph with an opening ``<p>`` tag and closing ``</p>`` tag. <mark>[1]</mark> </cite>

<br>

![Paragraphs!](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started/grumpy-cat-small.png)


<br>
<hr>
<br>





+ **Bold, Italic, Emphasis** : 

Here is a small cheat sheet for those elements : 


| Code-element       | Meaning                                                                                              |
| ------------------ | ---------------------------------------------------------------------------------------------------- |
| ``<b>``            | It shows the text bold ``<b>Miral</b>`` =  **Miral**                                                 |
| ``<i>``            | It shows the text italic ``<i>Miral</i>`` = *Miral*                                                  |
| ``<sup>``          | For superscript ``4<sup>th</sup>`` = 4<sup>th</sup>                                                  | 
| ``<sub>``          | For subscript ``H<sub>2</sub>O`` = H<sub>2</sub>O                                                    |
| ``<br />``         | Line break, To add lines as needed - inside the same paragraph for examole                           |
| ``<hr />``         | To create breaks between themes - Addind a horizontal rule between sections.                         |


<br>
<hr>
<br>

+ **Structural AND semantic markup** : 

![Paragraphs!](https://miro.medium.com/max/1200/1*qBLobOINLXv38nCOmCZW2Q.jpeg)


## What is the meaning of structural and semantis? 
>> Structural : <cite> The elements that you can use to describe both headings and paragraphs. <mark>[2]</mark> </cite> 

>>Semantics: <cite> refers to the correct interpretation of the meaning of a word or sentence. To use a word semantically is to use it in a way that is properly aligned with the meaning of the word. When we misuse a word we are not using it semantically. <mark>[3]</mark> </cite>

<br>
<br>
<br>


Here is a small cheat sheet for those elements : 


| Code-element       | Meaning                                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------------------ |
| ``<strong>``       | It indicates the importance of the text, when it applied the browser will give result bold text        |
| ``<em>``           | It indicates emphasis that subtly changes the meaning of a sentence. The effect will be italic         |
| ``<blockquote>``   | For quoted paragraphs (long quotes)                                                                    | 
| ``<q>``            | For short quotes (within the paragraphs)                                                               |
| ``<abbr>``         | Stands for *Abbreviation* for example CSS is an abbreviation for cascading style sheets                 |
| ``<cite>``         | For referencing from books or other sources                                                            |
| ``<dfn>``          | <cite>The <dfn> element is used to indicate the defining instance of a new term <mark>[4]</mark></cite>|
| ``<address>``      | Contains the information of the author/contacts                                                        |
| ``<ins>``          | To show the inserted content inside the document                                                       |
| ``<del>``          | To show the deleted content from the document                                                          |
| ``<s>``            | To show the content that is not relevant anymore but cannot be deleted                                 |



<br>
<br>
<hr>
<br>


## 2) CSS

> <cite>CSS allows you to create rules that control the way that each individual box (and the contents of that box) is presented. <mark>[5]</mark></cite>


![CSSsElector!](https://hackernoon.com/drafts/2z4a3yh4.png)

>> ``p`` = Which element should be affected by the style.

>> declaration = It splits into two parts: A) property [what effects you want to apply - the aspects],  B) value [to specify the property]


### There are three types of using CSS : 

* Inlline : ``<p style="color:red">Hello World!</p>``

* Internal/Embedded : We add a style tag inside the block of head tag 

```
   <head>
    <style> 
     p {
        color: red;
     }
    </style>
   </head>
```


* External: We create an external file with **.css** extension and inside we put the same thing 

```
     p {
        color: red;
     }

     header nav ul {
         width: 20px
     }
```



<br>
<br>
<hr>
<br>

## 3) JavaScript


+ **Basics** : 

>>Variables are containers for storing data values (can hold or store values).

>>Keyword called (var) : var firstName (camel case) = "Miral".

> Well! That is great so far **But** what are those data types that those variables can hold? 

* String: any text or set of characters "Miral" & 'Miral'

* Number: any kind of numbers (integer/decimal/float..)

* Boolean:  True or False

* "Zero" is a value. It is the unique, known quantity of zero, which is meaningful in arithmetic and other math

* "Null" is a non-value. It is a "placeholder" for a data value that is not known or not specified

### AND Before I forget!! YOU CANNOT NAME THE VARIABLES JUST LIKE YOU WANT

>> There are some rules to name your variable : 

* Must start with a letter, (_) or ($)

* It can contain letters, numbers, (_) or ($) but **NOTHING ELSE**

* **DON'T** use a reserved word!

* The variables are case sensitive so be careful **score** is not like **Score**

* You cannot add spaces but if the name of the variable must contain more than one syllable you can concatenate them using a camel  case

* Use a meaningful name.

<br>
<br>


### ARRAYS : 
It is another type of variable but it can holds(stores) more than one value. 

>> <cite> You should consider using an array whenever you are working with a list or a set of values that are related to each other. <mark>[6]</mark></cite>

```
var array_name = [item1, item2, ...];
```


<br>
<br>


### Operators :
>> It is a symbol that does an action (Allow programmers to create a single value from one or more values). 

* Comparison operators : (<=, >=, > , <  , != , [ === compares the values and the types of the values ] , [== compares the values not the types of the values])

* Arithmetic operators : 
( [ * Multiplication] , [ - Subtract ] , [ / Division ] , [ ++ increment ] ,[ % Modules], [** Power to])

* Logical operators : (&& , || , !)

* Conditional operator : (variablename = (condition) ? value1:value2)


<br>
<br>

### Expressions : 

* EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE. var color = ‘Red’ 

* EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE. var area = 3*2

<br>
<hr>
<br>

# Decision :

![Decision!](https://i.stack.imgur.com/SJj8n.png)


>> Use if to specify a block of code to be executed, if a specified condition is true (It is for checking or evaluating the condition either true or false and depending on that any statements of the subsequent will be executed).

```
if (condition) {
  //  block of code to be executed if the condition is true
}
```

>> Use else to specify a block of code to be executed if the same condition is false (If the condition is true then the code block will be executed, if not then it will go to the else part to be executed).

```
if (condition) {
  //  block of code to be executed if the condition is true
} else {
  //  block of code to be executed if the condition is false
}
```

>>Use else if to specify a new condition to test, if the first condition is false.

```
if (condition1) {
  //  block of code to be executed if condition1 is true
} else if (condition2) {
  //  block of code to be executed if the condition1 is false and condition2 is true
} else {
  //  block of code to be executed if the condition1 is false and condition2 is false
}
```

>>Use switch to specify many alternative blocks of code to be executed (The switch statement starts with a variable placed between to parentheses called switch value, according to this value it will be checked if it matches any of the cases in the block of the switch if it yes then that case will be executed. If NOT it will go to the default case that I have already defined).

```
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```


<br>
<br>
<br>
<br>
<br>
<br>
<br>


References :

* <mark>[1]</mark> HTML and CSS by Jon Duckett. 

* <mark>[2]</mark> HTML and CSS by Jon Duckett. 

* [<mark>[3]</mark> HTML.com](https://html.com/semantic-markup/)

* <mark>[4]</mark> HTML and CSS by Jon Duckett. 

* <mark>[5]</mark> HTML and CSS by Jon Duckett. 

* <mark>[6]</mark> HTML and CSS by Jon Duckett. 

