# Content

## Javascript


>> CHAPTER 10: 
>> * Error handling and debugging



<br>
<br>
<br>


+ **Error handling and debugging :**


![Debugging!](https://cdn.lynda.com/course/645067/645067-637081444918667146-16x9.jpg)



<br>

**1-** EXECUTION CONTEXT : 

>> Global context -> The code in the script not inside functions, Thre is only one global context in any page.

>> Function cnotext


**2-** VARIABLE SCOPE :

>> Global scope 

>> Function-level scope


**What is the process of executing the code?**

>> One line at a time from the very first beginning, and whaen a statement need data from function it will stack it on the current of the current task.

>> Each time a new item is added to the stack, it creates a new execution context.

For example if we have this code : 


```
function greetUser () {
   return 'He11o ' + getName ();
}

function getName() {
var name= 'Molly ' ;
return name;
}

var greeting= greetUser();
alert(greeting); 
```

How that code above will be executed? 

>> 1- It will declare the variable first and will see that the valuse that sign to it is an invoking to a function.

>> 2- It will go to greetUser() function in order to execute it so it put it above the current task, but this function has another invoking to a function inside of it.

>> 3- It will go to the getName and do the same as will.

>> 4- At the end you will get an alert showing you 'Hello Molly.

>> This meme excatly explain what is going on :

<br>

![I- KNOW-A-GUY!](https://memegenerator.net/img/instances/60973979.jpg)


<br>


![Errors!](/Code201/erroes.jpg)



TRY - CATCH - FINALLY: 

![Errors!](https://res.cloudinary.com/practicaldev/image/fetch/s--6yPAjemU--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/3ufdubowaga0tdehgdin.jpeg)





>> * <cite> The try/catch/finally statement handles some or all of the errors that may occur in a block of code, while still running code. </cite> <mark>[1]</mark>

>> * <cite> Errors can be coding errors made by the programmer, errors due to wrong input, and other unforeseeable things. </cite>  <mark>[2]</mark>

>> * <cite> The try statement allows you to define a block of code to be tested for errors while it is being executed. </cite>  <mark>[3]</mark>

>> * <cite> The catch statement allows you to define a block of code to be executed, if an error occurs in the try block. </cite>  <mark>[4]</mark>

>> * <cite> The finally statement lets you execute code, after try and catch, regardless of the result. </cite>  <mark>[5]</mark>

>> * <cite> Debugging is the process of finding errors. It involves a process of deduction 

>> * The console helps a lot to find the errors


<br>
<br>
<hr>
<br>
<br>

References :

* [<mark>[1-5]</mark> W3School](https://www.w3schools.com/jsref/jsref_try_catch.asp)


