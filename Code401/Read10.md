# Serving Web Content with Spring MVC

- The process of creating a *“Hello, World”* web site with Spring: 

  - The following listing shows the build.gradle file that is created when you choose Gradle:

  ```
  plugins {
	id 'org.springframework.boot' version '2.5.2'
	id 'io.spring.dependency-management' version '1.0.11.RELEASE'
	id 'java'
	}
  group = 'com.example'
  version = '0.0.1-SNAPSHOT'
  sourceCompatibility = '1.8'
  
  repositories {
	  mavenCentral()
	  }
	  
   dependencies {
	   implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
	   implementation 'org.springframework.boot:spring-boot-starter-web'
	   developmentOnly 'org.springframework.boot:spring-boot-devtools'
	   testImplementation 'org.springframework.boot:spring-boot-starter-test'
   }
   
   test {
	   useJUnitPlatform()
	}
  ```

<br>

- In Spring’s approach to building web sites, HTTP requests are handled by a controller. You can easily identify the controller by the `@Controller` annotation. In the following example, `GreetingController` handles GET requests for `/greeting` by returning the name of a `View` (in this case, `greeting`). A `View` is responsible for rendering the HTML content. The following listing (from `src/main/java/com/example/servingwebcontent/GreetingController.java`) shows the controller:


```
package com.example.servingwebcontent;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;

@Controller
public class GreetingController {

	@GetMapping("/greeting")
	public String greeting(@RequestParam(name="name", required=false, defaultValue="World") String name, Model model) {
		model.addAttribute("name", name);
		return "greeting";
	}

}
```

* The `@GetMapping` annotation ensures that HTTP GET requests to `/greeting` are mapped to the `greeting()` method.

* `@RequestParam` binds the value of the query string parameter `name` into the `name` parameter of the `greeting()` method. This query string parameter is not `required`. If it is absent in the request, the `defaultValue` of `World` is used. The value of the `name` parameter is added to a `Model` object, ultimately making it accessible to the view template.

* Thymeleaf parses the `greeting.html` template and evaluates the `th:text` expression to render the value of the `${name}` parameter that was set in the controller.

<br>

# Spring MVC and Thymeleaf: how to access data from templates 

1. Spring model attributes

<br>

**Add attribute to `Model` via its `addAttribute` method:**

```
    @RequestMapping(value = "message", method = RequestMethod.GET)
        public String messages(Model model) {
            model.addAttribute("messages", messageRepository.findAll());
            return "message/list";
        }
```


**Return `ModelAndView` with model attributes included:**


```
    @RequestMapping(value = "message", method = RequestMethod.GET)
        public ModelAndView messages() {
            ModelAndView mav = new ModelAndView("message/list");
            mav.addObject("messages", messageRepository.findAll());
            return mav;
        }
```

**Expose common attributes via methods annotated with `@ModelAttribute:`**

```
    @ModelAttribute("messages")
        public List<Message> messages() {
            return messageRepository.findAll();
        }
```

<br>

2. Request parameters =>

<br>

**Request parameters are passed from the client to server like:**

```
https://example.com/query?q=Thymeleaf+Is+Great!
```
- `<p th:text="${param.q}">Test</p>`


<br>

```
https://example.com/query?q=Thymeleaf%20Is%20Great!&q=Really%3F
```

- `<p th:text="${#request.getParameter('q')}" th:unless="${#request.getParameter('q') == null}">Test</p> `

<br>


3. Session attributes => 

<br>

```
    @RequestMapping({"/"})
        String index(HttpSession session) {
            session.setAttribute("mySessionAttribute", "someValue");
            return "index";
        }
```

- `<p th:text="${session.mySessionAttribute}" th:unless="${session == null}">[...]</p>`

- Or by using `#session`, that gives you direct access to the `javax.servlet.http.HttpSession` object: `${#session.getAttribute('mySessionAttribute')}`

<br>

4. ServletContext attributes => 

```

        <table>
                <tr>
                    <td>My context attribute</td>
                    <!-- Retrieves the ServletContext attribute 'myContextAttribute' -->
                    <td th:text="${#servletContext.getAttribute('myContextAttribute')}">42</td>
                </tr>
                <tr th:each="attr : ${#servletContext.getAttributeNames()}">
                    <td th:text="${attr}">javax.servlet.context.tempdir</td>
                    <td th:text="${#servletContext.getAttribute(attr)}">/tmp</td>
                </tr>
        </table>

```


5. Spring beans => 

```

@Configuration
        public class MyConfiguration {
            @Bean(name = "urlService")
            public UrlService urlService() {
                return () -> "domain.com/myapp";
            }
        }

        public interface UrlService {
            String getApplicationUrl();
        }

```

