# The HTTP Request Lifecycle : 

## Step 1: Local Processing


*This request is being made by a browser, as opposed to cURL, an API client.*

- The browser extracts the "scheme"/protocol (we have established that this will be HTTP), host and optional port number, resource path, and query strings that are specified in the form `<protocol>://<host><:optional port>/<path/to/resource><?query>`. An example is `|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|`

- The browser has the intended hostname for the request, it needs to resolve an IP address1. The browser will then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.


## Step 2: Resolve an IP

- If the cache lookup fails, your browser fires off a DNS request using UDP3. 

- Your request will now have to travel many network devices to reach its target DNS server.

- Once your request arrives at your configured DNS server, the server looks for the address associated with the requested hostname. 

- We will assume the request is successful though, given that all of this is still a precursor.



## Step 3: Establish a TCP Connection

- One of the key differences between TCP and UDP is that TCP ensures delivery and ordered data transmission.

- These guarantees and more can be found on Wikipedia, and are worth reading about, but what’s most relevant is that TCP connections are opened using what’s known as a three-way handshake.

- We now have a completed three-way handshake and an established connection where both the client and server have received acknowledgment of the connection from the other party.



## Step 4: Send an HTTP Request


- The request is made up of a "request line", request header, and a body. The "request line" is simply a line that indicates the HTTP method, the resource being requested, and the protocol version. 

- Once the HTTP request is sent, it follows a similar routing procedure as the one discussed earlier, with the difference being that using TCPs magic sequence number powers, the server can ensure it receives the whole request, in the correct order.

- Once the server receives the request, processes it, and finds the resource being requested, it generates an HTTP response.

- Once the response is generated, the server responds to the request. At the TCP layer, the client receives the first data packet, the first byte of which should contain the HTTP response header.


## Step 5: Tearing Down and Cleaning Up


<br>
<hr>
<br>



> The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that we need are part of the java.net package.


> We can create an HttpUrlConnection instance using the openConnection() method of the URL class.


