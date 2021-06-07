# React: Component Lifecycle Events:

<br>
<br>

**1.** Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

>> render.

<br>


**2.** What is the very first thing to happen in the lifecycle of React?

>> First of all calling the constructo **Birth of your component**.

<br>


**3.** Put the following things in the order that they happen: ``componentDidMount``, ``render``, ``constructor``, ``componentWillUnmount``, ``React Updates`.

>> **1.** constructor.

>> **2.** render.

>> **3.** componentDidMount.

>> **4.** React Updates.

>> **5.** componentWillUnmount.

<br>


**4.** What does componentDidMount do?

>> Anything that needs to be updated or loaded using a network request or initialize the DOM, it happens here. 

>> <cite> setState() can be called here, but it should be used sparingly, because it will cause a rerender, which can lead to perfomance issues. </cite>


[React: Component Lifecycle Events](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

<br>
<hr>
<br>
<br>
<br>
<br>


# React State Vs Props

<br>
<br>


**1.** What types of things can you pass in the props?

>> Static things that don't has to be changed or to be updated from the user. 

**2.** What is the big difference between props and state?

>> **Props** are handled outside the component and **State** is handled inside of that component.

**3.** When do we re-render our application?

>> When the state is being updated.

**4.**What are some examples of things that we could store in state?

>> Anything that based on something that the user handled such as: the **Form**.

[React State Vs Props](https://www.youtube.com/watch?v=IYvD9oBCuJI)




