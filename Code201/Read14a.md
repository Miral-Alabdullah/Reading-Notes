# Content 

## CSS Animations

>> ## Transforms

>>> **Two-dimensional plane**

>>> **Three-dimensional plane**

>> ## Transitions 

>> ## Animations

>> **Animations Keyframess**





<br>
<hr>
<br>

+ **Transforms**

>> It is a property that applies **2D** and **3D** to the elements, and each one of them has its own individual properties and values.

<br>
<hr>
<br>

**1- Two-dimensional plane:** 

<br>

>> **2D Rotate**

>>> The rotate value provides the ability to rotate an element from 0 to 360 degrees.

![Rotate!](https://i.stack.imgur.com/Tx0YP.gif)


```
transform:rotate(n-deg); // Will rotate from both x and y axises

transform:rotateX(n-deg); // Will rotate only from the x axis

transform:rotateY(n-deg); // Will rotate only from the y axis

```

<br>

>> **2D Scale**

>>> The Scale value allows you to change the appeared size of an element.

![Scale!](https://user.oc-static.com/upload/2019/01/18/15478159288024_pt02ch02_01_scale_v001.gif)


```
.box-1 {
  transform: scale(1); // The default value
}
.box-2 {
  transform: scale(1.25); // The element appear larger
}
.box-2 {
  transform: scale(.75); // The element appear smaller
}

--------------------------------------------------------
.box-1 {
  transform: scaleX(0.75); // Will scale only the width
}
.box-2 {
  transform: scaleY(1.25); // Will scale only the height
}
.box-3 {
  transform: scale(.5, 1.15); // Will scale both of the width and height
}
```

<br>

>> **2D Translate**

>>> The Translate value is for pushing and pulling an element in different directions without interrupting the normal flow of the document.

![Translate!](https://miro.medium.com/max/1268/1*8VJQxe58bXsk6yaYppbwPQ.gif)


```
.box-1 {
  transform: translateX(-10px); // Will push the box to the left among the X axis
}
.box-2 {
  transform: translateY(25%); // Will push the box to the down among the Y axis
}
.box-3 {
  transform: translate(-10px, 25%); // Will push the box to the left and the down among the X and Y axises
}
```

<br>

>> **2D Skew**

>>> The Skew value is used to distort elements on the horizontal axis, vertical axis, or both.


![Skew!](https://miro.medium.com/max/1076/1*85_KIbiKa1MgiQ_PJenJcA.gif)


```
.box-1 {
  transform: skewX(5deg); // distorts an element on the X axis
}
.box-2 {
  transform: skewY(-20deg); // distorts an element on the Y  axis
}
.box-3 {
  transform: skew(5deg, -20deg); // distorts an element on the both X and Y  axises
}
```

<br>
<br>

### Combining Transforms

**Look at these two examples and follow the comments for more details:**


```
Example one: 
----------------------------------------------------
  .box-1 {
    transform: rotate(25deg) scale(.75);
  } // the box will be rotate with 25 degrees and its scale will be smaller than the default at the same time

Example two: 
----------------------------------------------------
.box-1 {
    transform: rotate(20deg);
    transform: scale(1.25);
  } // only the scale will change because in this case we overwrite the values of the transform property 
```

<br>
<br>


**transform-origin**

>> This property allows you to change the position of transformed elements.

>> It take two values or it can be only one. 

>> Default value : 50% 50% 0

>> Its values can be written in many ways as the following:

```
.box-1 {
  transform: rotate(15deg);
  transform-origin: 0 0; // Top and Left
}
.box-2 {
  transform: scale(.5);
  transform-origin: 100% 100%; // Bottom and Right
}
.box-3 {
  transform: skewX(20deg);
  transform-origin: top left; 
}
.box-4 {
  transform: scale(.75) translate(-10px, -10px);
  transform-origin: 20px 50px; // Across and down the element
}
```

<br>
<hr>
<br>


**2- Three-dimensional plane:** 


![cube!](https://i0.wp.com/fribly.com/wp-content/uploads/2020/01/CSS-3D-Boxes-Loader.gif?fit=820%2C820&ssl=1)



**Perspective**

>> The ``perspective`` property is used to give a 3D-positioned element some perspective.

>> The ``perspective`` property defines how far the object is away from the user. So, a lower value will result in a more intensive 3D effect than a higher value.

>> When defining the ``perspective`` property for an element, it is the CHILD elements that get the perspective view, NOT the element itself.




>> **3D Rotate**

>>> The rotate value provides the ability to rotate an element around X, Y, and Z axises.


<br>


>> **3D Scale**

>>> The Scale value allows you to change the appeared size of an element, we need to add rotateX in order to see the changes of the scaleZ.



<br>


>> **3D Translate**

>>> In thiss case, the translateZ might look like the 2D Scale, but it's not! simply because the position will be changed across the Z axis so it might be appeared larger or smaller than the default, and why it's looking like that? because when we give it a positive valuse on the Z axis it will move closer to the eye and the opposite for the negative values.


<br>

>> **3D Skew**

>>> Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale. 


<br>
<br>



<br>
<hr>
<br>

+ **Transitions**

>>> With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

>>> An element must have a change in state, and different styles must be identified for each state. 


| Property                          | How it works?                         |
| --------------------------------- | ------------------------------------- |
| transition-property               | is the only property that will change |
| transition-duration               | How long the effect takes to complete |
| transition-timing-function        | specifies the speed curve of the transition effect|


>> Numbers followed by -webkit-, -moz- or -o- specify the first version that worked with a prefix.


**A handful of the more popular transitional properties include the following:**

![properties!](https://lh3.googleusercontent.com/pw/ACtC-3dQ3mHn0OjOYBeZzr1sZpUElu_SoRDiR2KPinzm_JCnim3aYaZUrnv1b1zj89cD-2Z94fFJVdwBT3oabIiicqAHoq3S68IzvAhwSzp9G25WCXJgELqg50FYHHM73E9Tfg4MTw5ukqVpRYSPZdzX-lw=w872-h447-no?authuser=3)

<br>
<br>
<hr>
<br>
<br>


+ **Keyframes**


>> **To set multiple points at which an element should undergo a transition, use the @keyframes rule.**

>> When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.



![Keyframes!](https://lh3.googleusercontent.com/pw/ACtC-3cPfOgV-0cQH2ksyTyy8NDcHUWtyN7jrAPA82QQzOGvk_UWxMwWRhp4OGvDLIGPfCMygMVMbI_22lPSC3T5IN71FaOammsSNrBhV3pNXzDFPUbB7myJ1LwxVP7P6A21EA_UIIyKyNaaWE9YgHiM_Go=w743-h306-no?authuser=3)


<br>

```
/* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```


<br>
<br>
<br>



**Resources**

**[First](https://learn.shayhowe.com/advanced-html-css/css-transforms/)**

**[Second](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)**

**[Third](https://www.w3schools.com/css/css3_animations.asp)**