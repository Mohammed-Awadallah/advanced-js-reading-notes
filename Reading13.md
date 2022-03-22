# Message Queues


## Questions

- What does it mean that web sockets are bidirectional? Why is this useful?

>It means communication flows both ways between a server and client.
This is useful because a conversation can be kept going between a server and client.
It enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time. In the context of networked AV and control systems, this allows devices to send and receive continuous streams of data to and from any point on the network.

- Does socket.io use HTTP? Why?

>A socket.io server will attach to an HTTP server so it can serve its own client code through /socket.io/socket.io.js to communication with clients.

- What happens when a client emits an event?

>The client emits an event and then the server handles the event using the on method.it would go the event handler.

- What happens when a server emits an event?

>Server emits the event and it is handled by the client side(The server emits an event and then the client that the event was emitted to handles the event.)

- What happens if a client “misses” an event?

>Unhandled messages are just ignored. It’s just like when an event occurs and there are no event listeners for that event. The socket receives the msg and doesn’t find a handler for it so nothing happens with it (Nothing. The event will be ignored if it is missed.)

- How can we mitigate this?

>We could assign unique IDs to events in order to track them, log events, and make sure the client recieved the event.You could avoid missing messages by always having the handlers installed and then deciding in the handlers based on other state whether to do anything with the message or not.


## Terms


- Socket: *a software structure that serves as an endpoint for sending and receiving data across the network. Sockets are created only during the lifetime of a process of an application running in the node. A socket is externally identified to other hosts by its socket address, which is the triad of transport protocol, IP address, and port number.*

- Web Socket: *a computer communications protocol that provides full-duplex (bidirectional) communication channels over a single TCP connection. This protocol is located at layer 7 in the OSI model and depend on TCP at layer 4. It enables interaction between a client and a web server, facilitating real-time data transfer from and to the server through a TCP port*

- Socket.io: *an event-driven library that enables real-time, full-duplex (bidirectional) communication between the Client and the Web servers. It is built on top of the WebSockets API (Client side) to provide the interface and Node.js.*

- Client: *a piece of computer hardware or software that accesses a service made available by a server as part of the client–server model of computer networks.*

- Server: *a computer that provides various shared resources to clients and other servers on a network.*

- OSI Model: *a conceptual framework used to describe how information from a software application in one computer moves through a network to the software application in another computer. This model consists of 7 abstraction layers, and each layer performs a particular network function.*

- TCP Model: *a suite of protocols designed to establish a network of networks to provide a host with access to the internet. TCP/IP prepares and forwards data packets over LANs and WANs, as well as the Internet. In fact, the Internet is the world's largest TCP/IP network. TCP/IP is responsible for full-fledged internet data connectivity and transmitting the data end to end by providing other functions, including addressing, mapping and acknowledgment. TCP/IP contains four layers, which differ slightly from the OSI model.*