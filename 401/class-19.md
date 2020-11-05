# More on Clients and Servers with Socket.io

![x](https://media.giphy.com/media/1ggzuchWJ0ps4/giphy.gif)

**Ah yes, socket.io...Socket.io allows for cleaner event handling and provides web connectivity. It also manages the connection pool, makes broadcasting much easier to operate, and works well both on the terminal (between servers) and with web clients.**

### Let's answer some questions:

1. **What does it mean that web sockets are bidirectional? Why is this useful?**

Bidirectional just means either the client or server can send a message to the other party whenever a message is available. It is useful because data flows in both directions, so a socket can SEND and RECEIVE data. With this two way communication, we can think of a chat app.


1. **Does socket.io use HTTP? Why?**
   
Yes, it does. Even when websockets can be used, the initial connection setup is done over HTTP. A socket.io server will attach to an HTTP server so it can serve its own client code through /socket.io/socket.io.js.

So, on the server-side, Socket.IO works by adding event listeners to an instance of http.Server. This allows us to attach a Socket.IO server to other HTTP frameworks like Express.

On the client-side, The global `socket` variable is an `EventEmitter`-like object. We can attach a listener to fire when we’ve connected to the server.

   
1. **What happens when a client emits an event?**
   

On the client-side events include:
Connect
Connect_error
Connect_timeout
Reconnect, etc

The client will send the event to the server through the use of sockets. So, after an even is sent, the client will listen for the event and produce an output. However, the client must be connected to the socket for this to occur.

4.**What happens when a server emits an event?**

On the server-side events include:

Connect
Message
Disconnect
Reconnect
Ping
Join and
Leave

When a server emits and event, if it uses emit() then all connected clients will receive the event. Or, `socket.broadcast.emit(`) will only broadcast to the current "connection. The server receives the message and emit out to client with server side socket.io.

5.**What happens if a client “misses” an event?**

I think that that none of the client-side events would fire. Basically this is mishandling client events. 

6.**How can we mitigate this?**
Maybe we can consider the client disconnected after an error event or we could use this to establish a reconnect. Not sure.


------------------------

### New Vocabulary to learn:

- **Web Socket:**
   WebSockets are a connection-based communication protocol. Unlike TCP, WebSockets work in the browser. WebSockets are message-based so we can send a message and the other side receives a message. WebSockets are implemented on top of TCP. 
- **Socket.io:** 
  Socket.IO is a combination of the client-side JavaScript library and Node.js library used to integrate bidirectional communication between a browser and Node.js backend. The Socket.IO client-side library is used to create a Socket.IO client whereas the Socket.IO Node.js library is used to create a Socket.IO server. The Socker.IO client and server can communicate with each other bidirectionally. Socket.IO primarily uses WebSocket to achieve bidirectional communication.
- Client: When using websockets,  the client connects to a the server port; client obtains a socket.
- Server: When we are speaking about websockets,  the server listens on a fixed port, with a given socket. Server accepts the connection, and accept/ returns a new socket for the connection.