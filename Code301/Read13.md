# Status Codes Based On REST Methods

<br>
<br>

**1. In your own words, describe what each group of status code represents:**

* 100’s = These are informational status codes; From the request of the client the header part will be received and the server will response, for example telling the user to switch the protocol or a failure has occured before sending the body.

<br>

* 200’s = These are the success codes. Accepted request will be shown to the client.

<br>

* 300’s = These are redirection codes. The location that requested from isn't available anymore, so the client has to target a new one.

<br>

* 400’s = These are the client error codes. Timeouts, wrong URI, missing authentication. The user has to make sure to send the correct parameters in the search query.

<br>

* 500’s = These are the server error codes. They indicate problems with overwhelmed servers or unreachable servers behind proxies. Refreshing the request or re-send it againg would be the best to solve this issue from the client side.

<br>

<hr>


<br>

**2. What is a status code 202?**

<br>

* It tells the client the request was valid but the processing will end soon, so It should provide him with another URL or endpoint to reach the tarqet, or when it will be available again.

<br>

**3. What is a status code 308?** 

<br>


* Same like 202 but provided with the location, ome clients follow the status codes of the Redirect-class automatically. This code is usually only used for POST requests.

<br>

**4. What code would you use if an update didn’t return data to a client?**

<br>


* 204 No Content 

<br>

**5. What code would you use if a resource used to exist but no longer does?**

<br>

* 307 Temporary Redirect

<br>

**6. What is the ‘Forbidden’ status code?**

<br>

* The client has already authorized  or maybe doesn't need to do that, but still he can't access the resource.


<br>
<hr>
<br>
<br>
<br>
<br>
<br>


# Build A REST API With Node.js, Express, & MongoDB

<br>

**1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?**

<br>

* To be ignored after pushing the code, to visible ony for me.

<br>

**2. What is middleware?**

<br>

* A function when be called will be move on to the next section of the code. Excuting the code like partitons sequentially. 

<br>

**3. What does ``app.use(express.json())`` do?** 

<br>

* Let the server accept JSON as a body inside a ``POST`` or ``GET`` element.

<br>

**4. What does the ``/:id`` mean in a route?**
    
<br>

* To get only one object.

<br>

**5. What is the difference beween ``PUT`` and ``PATCH``?**

<br>

* PUT: For creating a new route.

* PATCH: Updating a route that already exists.

<br>

**6. How do you make a defalut value in a schema?**

<br>

* Passing inside the object as a parameter a default type then give it the value that we want it to be default. 

```
{
	default: 'Hello'
}
```

<br>

**7. What does a ``500`` error status code mean?**

<br>

* Mean that there's an error on the server(Database)=> Has some errors that caused that actual transactions not to work and had nothing to do with the actuall user or client using the API.

<br>

**8. What is the difference between a status ``200`` and a status ``201``?**

<br>

* ``201`` => Successfully created an object

* ``200`` => 

<br>
<br>
<hr>
<br>
<br>

## Resources : 

[Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

[Build A REST API With Node.js, Express, & MongoDB](https://www.youtube.com/watch?v=fgTGADljAeg)

