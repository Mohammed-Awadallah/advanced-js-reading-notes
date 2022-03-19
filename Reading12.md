# Socket.io


## Questions : 

 - What is the benefit of transforming data into packets?
 > TDM-based networks must transform into packet-based networks to meet the demands of pervasive data-centric applications and services. Packet-based networks not only enable new innovations, services, and business opportunities, they are also the most cost-effective, efficient, and scalable networks for content delivery.

- UDP is often refereed to as a connectionless protocol. Why is this?
> UDP is a connectionless protocol. It is known as a datagram protocol because it is analogous to sending a letter where you don't acknowledge receipt. Examples of applications that use connectionless transport services are broadcasting and tftp .

 - Can a socket server application have multiple socket connections?
 > Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to

- Can a socket connection application be connected to multiple socket servers?
 > You cannot use a single socket to connect to multiple servers. You must create a separate socket for each connection

- Can an application be both a socket server and a socket connection?
> if you want to use a client socket and a server socket within a single application, then yes! You can do that if you're willing to use two different ports. Or if the sockets won't be using the same port at the same time.



## Terms :


**Term** | **Defintion**
------------ | -------------
 Observer Pattern | The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.
 Listener | An event listener is a procedure in JavaScript that waits for an event to occur. The simple example of an event is a user clicking the mouse or pressing a key on the keyboard.
 Event Handler | Event handling (overview) Events are signals fired inside the browser window that notify of changes in the browser or operating system environment. Programmers can create event handler code that will run when an event fires, allowing web pages to respond appropriately to change.
 Event Driven Programming | programming paradigm in which the flow of the program is determined by events.
 Event Loop | a programming design pattern that waits for events in a program. It works by making a request to some internal or external event providers, then calls the relevant event handlers which dispatches the event.
 Event Queue |responsible for sending new functions to the track for processing. It follows the queue data structure to maintain the correct sequence in which all operations should be sent for execution.
 Call Stack | responsible for keeping track of all the operations in line to be executed. Whenever a function is finished, it is popped from the stack.
 Emit/Raise/Trigger | The emit method (the publish method), on the other hand, allows you to “emit” an event, which causes all callbacks registered to the event to ‘fire’, (get called). Short: Emit’s job is to trigger named event(s) which in turn cause functions called listeners to be called.
 Subscribe | This is the function that is executed when a consumer calls the subscribe() method. … To execute the observable you have created and begin receiving notifications, you call its subscribe() method, passing an observer. This is a JavaScript object that defines the handlers for the notifications you receive.
 database | A database is an organized collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). … The data can then be easily accessed, managed, modified, updated, controlled, and organized.


 ## Preview 


Which 3 things had you heard about previously and now have better clarity on?
>  Emit/Raise/Trigger, Event Queue, Observer Pattern

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
>  Emit/Raise/Trigger, Event Queue, Observer Pattern

What are you most excited about trying to implement or see how it works?
> Subscribe