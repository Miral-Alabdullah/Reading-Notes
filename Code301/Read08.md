
<br>

# API Design Best Practices


<br>


**1. What does REST stand for?**

>> Representational State Transfer.


**2. REST APIs are designed around a <mark>resources</mark>.**


**3. What is an identifer of a resource? Give an example.**

>> URI that uniquely identifies that resource. For example, the URI for a particular customer order might be: https://adventure-works.com/orders/1

**4. What are the most common HTTP verbs?**

>> ``GET``, ``POST``, ``PUT``, ``PATCH``, and ``DELETE``.

**5. What should the URIs be based on?**

>> URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

**6. Give an example of a good URI.**

>> https://adventure-works.com/orders

**7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**

>> expose a large number of small resources, bad.

**8. What status code does a successful ``GET`` request return?**

>> returns HTTP status code 406 (Not Acceptable).

**9. What status code does an unsuccessful ``GET`` request return?**

>> returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).

**10. What status code does a successful ``POST`` request return?**

>> returns HTTP status code 415 (Unsupported Media Type).

**11. What status code does a successful ``DELETE`` request return?**

>> If the delete operation is successful, the web server should respond with HTTP status code 204.

>> If the resource doesn't exist, the web server can return HTTP 404 (Not Found).



## Resources : 

[API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)