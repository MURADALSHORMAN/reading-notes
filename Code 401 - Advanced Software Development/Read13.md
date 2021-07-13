# Message Queues:
## What does it mean that web sockets are bidirectional? Why is this useful?
it mean there are two wey connection from client to server and server to client.because the webSocket increases speed and real-time capability on the web. WebSockets also enable servers to keep track of clients and “push” data to them as needed, which was not possible using only HTTP.
## Does socket.io use HTTP? Why?
a socket.io server will attach to an HTTP server so it can server it is own client code through/socket.io/soccker.io.js
## What happens when a client emits an event?
The event gets passed to the server through websockets. Its a tcp connection from the browser to the server. The connection is full duplex meaning the server can send real time data to the client and vise versa.
## What happens when a server emits an event?
Event is thrown into an event pool and is triggered by any client/event that is listening for the event
listeners typically have a callback function which runs a codeblock when the event is triggered
## What happens when a server emits an event?
event is sent to specific subs, all clients, or both.
triggers a callback that is assigned to the listener and runs the code
## What happens if a client “misses” an event?
missed events are ignored which prevents the rest of a chain of code to run (which is bad)
## How can we mitigate this?
unheard events should be stored in a queue system on the server that is resumed as a client connects

# Terms
- Socket vs. Web Socket: “WebSockets typically run from browsers connecting to Application Server over a protocol similar to HTTP that runs over TCP/IP. So they are primarily for Web Applications that require a permanent connection to its server. On the other hand, plain sockets are more powerful and generic. They run over TCP/IP but they are not restricted to browsers or HTTP protocol. They could be used to implement any kind of communication.” source (Links to an external site.)

- Socket.io: “is a library that enables real-time, bidirectional and event-based communication between the browser and the server” source (Links to an external site.)

- Client: can be thought of as the browser. It connects to an established server and makes requests.

- Server: responds to requests from the client.

- TCP Model: is a suite of communication protocols used to interconnect network devices on the internet.*
- TCP: is a standard that defines establishing and maintaining a network conversation through which application programs can exchange*
- UDP:is part of the TCP/IP suite of protocols used for data transferring.*
- Packets:it is a form of data that consists of a small amount of information with a port number, IP addresses to the sender and the caller, and a tail part that contains some protocol information.
