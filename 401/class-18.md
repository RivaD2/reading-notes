# WEBSOCKETS

![sockets](https://media.giphy.com/media/l2Jehp66ZjoDx301G/giphy.gif)

1. **What is the benefit of transforming data into packets?**
Network efficency! According to [computer.howstuffworks.com](https://computer.howstuffworks.com/question525.htm):
>"First, the network can balance the load across various pieces of equipment on a millisecond-by-millisecond basis. Second, if there is a problem with one piece of equipment in the network while a message is being transferred, packets can be routed around the problem, ensuring the delivery of the entire message."
   
2. **UDP is often refereed to as a connectionless protocol. Why is this?**
It is considerd to be connectionless as it allows data to be exchanged without setting up a link between processes. Each unit of data, with all the necessary information to route it to the intended destination, is transferred independent of other data packets and can travel over different paths to reach the final destination.

3. **Can a socket server application have multiple socket connections?**
Yes, [apachebooster.com](https://apachebooster.com/blog/how-does-one-server-handle-multiple-connections-at-a-time/) says:
>"If a single server is listening to the same port it is possible that there are more than one sockets being connected which can be from the same or different clients. As long as this server knows which request is coming from where (via the socket) it can respond to the respective client(s) using the same socket. It does not need to open another port in its own node, but the original one using which the client initially tried to connect, can be used. In fact, it should respond back using the same initial socket in order to not waste the resources."

4. **Can a socket connection application be connected to multiple socket servers?**
Yes. Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to.

5. **Can an application be both a socket server and a socket connection?**
Apparently it can! In Java anyway, there can be an input stream and output stream using what is called an [echo server](https://medium.com/@himalee.tailor/what-is-an-echoserver-b2bfd3b8deeb). This server listens on a single port for incoming UDP datagrams, then sends the payloads back to their senders through the same socket (in fact through the same socket descriptor that it was listening on).


**New Vocabulary to Learn:**

- **OSI Model:** A conceptual framework that describes the functions of a networking or telecommunication system. It consists of 7 layers:

- Layer 7 - Application
- Layer 6 - Presentation
- Layer 5 - Session
- Layer 4 – Transport
- Layer 3 - Network
- Layer 2 – Data Link
- Layer 1 - Physical

- **TCP Model:** Designed and developed by Department of Defense (DoD) in 1960s, this model is based on standard protocols. It stands for Transmission Control Protocol/Internet Protocol. The TCP/IP model is a concise version of the OSI model. It contains four layers, unlike seven layers in the OSI model. The layers are:

- Process/Application Layer
- Host-to-Host/Transport Layer
- Internet Layer
- Network Access/Link Layer

- **TCP:** Transmission Control Protocol is a connection-oriented protocol. Connection-orientation means that the communicating devices should establish a connection before transmitting data and should close the connection after transmitting the data. **It is reliable and provides extensive error checking mechanisms.** It is because it provides flow control and acknowledgment of data.
- 
- **UDP:** User Datagram Protocol is less reliable than TCP as it **does not guarantee data can be delivered to its destination.** This is because there is no overhead for opening a connection, maintaining a connection, and terminating a connection. UDP is however, efficient for broadcast and multicast type of network transmission AND is **UDP is faster, simpler and more efficient than TCP**
- 
- **Packets:** A block of data transmitted across a network.

- **Socket:**A socket is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to.

--------------------
**RESOURCES:**
1. [networkworld.com](https://www.networkworld.com/article/3239677/the-osi-model-explained-and-how-to-easily-remember-its-7-layers.html)
2. [geeksforgeeks.org](https://www.geeksforgeeks.org/tcp-ip-model/)