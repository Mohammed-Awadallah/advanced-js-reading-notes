# Mohammed Awadallah
## Reading06
### Questions : 

#### Explain what a “Singleton” is : 
> A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class to only one object. This is helpful usually when a single object is required to coordinate actions across a system.<

#### Explain how the Singleton pattern can be used with Node modules, specifically with classes : 
>By design, singletons create an instance of a class if it does not yet exist. Otherwise, they return the reference to an existing instance. Now, every time we call Singleton. Nothing restricts us from calling the Singleton constructor directly
By making the Singleton constructor private, we can only call it from within the getInstance function. Another approach that we can take is to return an instance straight from within the constructor. The above makes it a bit less transparent because someone might not be aware that the constructor returns the same object every time."

#### If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

> An Express application can use the following types of middleware: Application-level middleware. Router-level middleware. Error-handling middleware.
Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application's request-response cycle. These functions are used to modify req and res objects for tasks like parsing request bodies, adding response headers"

### Document the following Vocabulary Terms : 
* Router Middleware :  >The term is composed of 2 words router and middleware. Middleware. It is a piece of code that comes in the middle of request and response . It kind of hijacks your request so that you can do anything that you want with your request or response eg: Modify the data or call the next middleware"

* Dynamic Module Loading : >a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory"

* Singleton Pattern : >an object which can only be instantiated one time. Repeated calls to its constructor return the same instance and in this way one can ensure that they don't accidentally create, say, two Users in a single User application"

* CRUD -> REST Method Matches : >REST is an architectural system centered around resources and hypermedia, via HTTP protocols. CRUD is a cycle meant for maintaining permanent records in a database setting. CRUD principles are mapped to REST commands to comply with the goals of RESTful architecture."

* Mock Testing : "functions allow you to test the links between code by erasing the actual implementation of a function, capturing calls to the function (and the parameters passed in those calls), capturing instances of constructor functions when instantiated with new , and allowing test-time configuration of return values"


### Preview : 

* Which 3 things had you heard about previously and now have better clarity on? 

>Singleton Pattern,Dynamic Module Loading, Router Middleware"

* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

* What are you most excited about trying to implement or see how it works?
