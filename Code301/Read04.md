
# React Docs - Forms

**1. What is a ‘Controlled Component’?**

>> The form in React is different from the HTML, the fields of the form in HTML can be updated dynamically but in the React the changes in kept in the state and to change it we use the setState() method, and that's how the React CONTROLS the component.

**2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.**

>> No, ``this.state.value`` => the state can't be updated unless we add a behaviour to it to do that.

**3. How do we target what the user is entering if we have an event handler on an input field?**

>> ``this.setState({value: event.target.value});``


<br>

# The Conditional (Ternary) Operator Explained

**1. Why would we use a ternary operator?**

>> Because it always return a value. JS will thorw a syntax error if only one expression is provided.

>> It can save mulitple lines of code and it more readlable.

**2. Rewrite the following statement using a ternary statement:**

**BEFORE**

```
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
```

**AFTER**

```
  x===y ?  console.log(true) : console.log(false);
```