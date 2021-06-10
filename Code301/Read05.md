# Thinking in React || Read: Class05.

<br>

**1. How would you break a mock into a component hierarchy?**

> Draw boxes around every component.


> ![!](https://reactjs.org/static/1071fbcc9eed01fddc115b41e193ec11/d4770/thinking-in-react-mock.png)

>> By looking at the picture above, we can see how the boxes indicates to the components and thats how you **break a mock into a component hierarchy**.

<br>

**2. What is the single responsibility principle and how does it apply to components?**

>> A component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents. Each component has its own job and properties distinguish it from the other.

<br>

**3. What does it mean to build a ‘static’ version of your application?**

>> It renders your data model; menening build your app without adding interactivity and for that you don't use state because <cite> State is reserved only for interactivity, that is, data that changes over time.</cite> We use props for that.

<br>

**4. Once you have a static application, what do you need to add?**

>> State.

<br>

**5. What are the three questions you can ask to determine if something is state?**

>> Is it passed in from a parent via props? If so, it probably isn’t state.

>> Does it remain unchanged over time? If so, it probably isn’t state.

>> Can you compute it based on any other state or props in your component? If so, it isn’t state.

<br>

**6. How can you identify where state needs to live?**

> By following these steps: 

>> 1. Identify every component that renders something based on that state.

>> 2. Find a common owner component (a single component above all the components that need the state in the hierarchy).

>> 3. Either the common owner or another component higher up in the hierarchy should own the state.

>> 4. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.


<br>
<br>
<br>


## Things I want to know more about:

**1.** Digging deep into props and state. 

**2.** How to build the data model professionally.