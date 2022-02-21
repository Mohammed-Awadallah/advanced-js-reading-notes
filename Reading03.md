# Reading notes Class 03

 ## Questions :
 ### 1.  Name 3 real world use cases where you’d want to change the request with custom middleware :
 -   Authentcation
-   Data Management
-   Logging Middleware

### 2.  True or false: The route handler is middleware?
False

### 3.  In what ways can a middleware function end the process and send data to the browser?
-   res.send()
-   res.render()
-   res.end()
-   res.json()

### 4.  At what point in the request lifecycle can you “inject” middleware?
Between sending the request and before the response send
### 5.  What can cause express to error with “Request headers sent twice, cannot start a second response”?
function tried to set a statusCode, but we are in the finished state

##  Vocabulary Terms:
Middleware : **Middleware is software that provides common services and capabilities to applications outside of what’s offered by the operating system.**

Request Object : **the main entry point for an application to issue a request to the Library**

Response Object: **an instance of a javax.servlet.http.HttpServletResponse object.**
Application Middleware : **is software that provides common services and capabilities to applications outside of what’s offered by the operating system.**

Routing Middleware : **It is a route which is using to log requests to the console or validate specific parameters If It is for parameters .**

Test Driven Development: **It is a programming practice which involves developing tests for every small functionality of an application.**

Behavioral Testing : **It is a testing of the external behavior of the program, also known as black box testing. It is usually a functional testing.**
## Preview :
1.  Which 3 things had you heard about previously and now have better clarity on?
**Test Driven Development** , **Difference between Response and Request Objects**, **Better understanding of classes and their implementation**
2.  Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
**Im quite intrigued about the middleware and its uses and how to render a side view of it , learning more about the scenarios where i need to use custom made middleware and how to create them and how to know that i need one , even tho i answerd false in the 2nd question it was only based on what i read but i didnt quite understand it**
3.  What are you most excited about trying to implement or see how it works?
**A middleware to authenticate validity of an entered credit card if thats possible**