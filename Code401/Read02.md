
# Java Imports (ignore the parts about NetBeans)


<br>

### Package = directory.

> This package works like the directory; Java classes can be grouped together in this package.

> Declaring the package must be the first thing in the java source file.

> Java creats a default package.

<br>

- Package declaration syntax: 

```
// This source file must be Drawing.java in the illustration directory.

package illustration;

import java.awt.*;

public class Drawing {
    . . .
}
```
<br>

- Imports: three options:

<br>

```
import javax.swing.*;  // Make all classes visible altho only one is used.

class ImportTest {
    public static void main(String[] args) {
        JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}
```

<br>

```
import javax.swing.JOptionPane;  // Make a single class visible.

class ImportTest {
    public static void main(String[] args) {
        JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}
```

<br>

```
class ImportTest {
    public static void main(String[] args) {
        javax.swing.JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}
```

<br>

- Common imporst:

<br>

| import  | Usage                           |
| ----------- | ------------------------------ |
| `import java.awt.*;`      | Common GUI elements.    |
| `import java.awt.event.*; `     | The most common GUI event listeners.    |
| `import javax.swing.*; `     | More common GUI elements. Note "javax".   |  
| `import java.util.*; `     | Data structures (Collections), time, Scanner, etc classes.    |
|` import java.io.*;`  | Input-output classes.    |
| `import java.text.*;`   | Some formatting classes.   |
| `import java.util.regex.*;`      | Regular expression classes.  |

	
	
	
	
	
	
	



<br>


# Different types of loops in Java


<br>


- A Guide to Java Loops : 

> Here are the types of loops that we can find in Java:

- Simple for loop

> We use it when we know the number of iterations.

- Enhanced for-each loop

> To loop through an array element by element

- While loop

> We use it when we don't know the number of iterations.

- Do-While loop

> The first condition evaluation happens after the first iteration of the loop.
