# The JavaScript Call Stack - What It Is and Why It's Necessary


**1. What is a ‘call’?**

>> Invoking the function to be excuted.

**2. How many ‘calls’ can happen at once?**

>> only one time at once, from the top to bottom.

**3. What does LIFO mean?**

>> It means Las in, First out => In data structure the stack is LIFO, means what comes at the last, goes at first.

**4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.**


```
function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();

```

>> For this example, The target is to excute the thirdFunction(), but to get this secondFunction() need to be excuted first, but its block contains firstFunction() which is another function has to be excuted. So, at the ends you'll see that the last function which is firstFunction() has excuted first, and that's exactly the meaning of LFIO.

<cite>The example above has been taken from</cite> 
[Resource](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)


**5. What causes a Stack Overflow?**

```
function callMyself(){
  callMyself();
}

callMyself();
```

>> By looking at the previous example, we'll find out that we're calling the function inside its block.. that causes ``Stack Overflow``, There's no exit point and it will be calling itself until reaching maximum stack of the browser.


<br>
<br>


# JavaScript error messages && debugging


**1. What is a ‘refrence error’?**

>> using a variable has not declared.

**2. What is a ‘syntax error’?**

>> error occurs when you type the syntax incorrectly, for example missing a comma or curly brackets

**3. What is a ‘range error’?**

>> manipulate the object/array with their lengths

**4. What is a ‘tyep error’?**

>> occurs when a misspelling found.

**5. What is a breakpoint?**

>> Its simply a point in your code, could be a console or condition..etc, to check a block of code (Debugging).

**6. What does the word ‘debugger’ do in your code?**

>> A way of reaching the breakpoint, it shows you the history of the code block that set above it. givs you details of what this block of code contained


## Resources : 

[1. The JavaScript Call Stack - What It Is and Why It's Necessary](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

[2. JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)