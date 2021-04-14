# Content

## 1) HTML


>> CHAPTER 7: 
>> * Forms


## 2) CSS


>> CHAPTER 14
>> * Lists, Tables and Forms



## 3) JavaScript


>> CHAPTER 6: 
>> * Events


<br>
<br>
<br>


+ **HTML : Form**


![HTML-FORM!](https://jqueryform.github.io/posts/video/form-html.jpg)


> What is the HTML form?
>> It is used to collect user input. The user input is most often sent to a server for processing. <mark>[1]</mark>

**HOW?**

> There are several types of form controls that you can use to collect information from visitors to your site.

>> * Adding Texts

>>> 1- Text input

>>> 2- Password input

>>> 3- Text area


>> * Making Choices

>>> 1- Radio buttons

>>> 2- Checkboxes

>>> 3- Drop-down boxes 


>> * Submitting Forms

>>> 1- Submit buttons

>>> 2- Image buttons

>> * Uploading Files

>>> File upload


**How Forms Work??**

> 1- When the user fill the form and press on a button in order to submit, these values will be sent to the server.

> 2- The server processes the information either using a programming language or storing them into a database.

> 3- The serrver create a new page based on the provided information for the user.

>> Server : Is a piece of computer hardware or software (computer program) that provides functionality for other programs or devices, called "clients" <mark>[2]</mark>



example : 

```
<form>  
First name: <input type=text name=t1>
Last name: <input type=text name=t2>
Password: <input type=password name=p>
</form>
```

**Form tag properties :**

1- Action is the URL of the CGI program(Common Gateway Interface) that is going to accept data from the form

2- Method POST, GET 

>> 1- GET method passes request parameters in the URL string 

>> 2- Get request can only pass limited amount of data while post method can pass a large amount of data

>> 3- GET is mostly used for view data (e.g. SQL SELECT) where Post is used for update data (e.g. SQL update, insert)

>> 4- Use POST if you use sensitive and confidential information 

3- Name

4- Enctype

5- Target 



**Input tag :**

> Input properties :

>> 1- Type: text, password, radio, checkbox, button

>> 2- Name 

>> 3- Value

>> 4- Checked

>> 5- Size: number of character in the text field

>> 6- Max-length: maximum number of characters accepted



<br>
<br>
<hr>
<br>
<br>

+ **CSS : Lists, Tables and Forms**

**How to change the style of lists?**

>> By using this property ``list-style-type`` as it shows in the following picture:


![CSS-List-style!](https://miro.medium.com/max/1700/1*9ZpChSsnbpcqOf3r6HEumA.png)



>> OR by using ``list-style-image`` 

```
list-style-image: url("images/star.png");
```

**HOW To change its position??**

>> By using this property ``list-style-position``, it takes outside / inside values.




+ **Javascript : Events**


When you click on a button for example, you will get a reaction from the webpage itself depending on the purpose of this button. Let's make it more clear; for example when you press login on your facebook page, the reactin will be the page after being logged in! 

![Javascripts-events!](https://cope-ali.github.io/cope-ali261.github.io/img/HTMLevents.png)




References :

* [<mark>[1]</mark> W3School](https://www.w3schools.com/html/html_forms.asp)

* [<mark>[2]</mark> Wikipedia](https://en.wikipedia.org/wiki/Server_(computing))


