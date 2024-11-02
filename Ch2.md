# Chapter 2
**Layered task/Hierarchical Task**
---
<img src="Images/Screenshot 2024-09-24 223208.png" width="400" height="">

- Each layer at the sending site uses the services of the layer immediately below it. The
sender at the higher layer uses the services of the middle layer. The middle layer uses
the services of the lower layer. The lower layer uses the services of the carrier.

**OSI Model**
---	
<img src="Images/Screenshot 2024-09-24 223947.png" width="" height="">

1. **Physical Layer**
- The physical layer is responsible for movements of
individual bits from one hop (node) to the next

<img src="Images/Screenshot 2024-09-24 225904.png" width="350" height="">

**Characteristics of Physical Layer**
- **Physical characteristics of interfaces and medium:** It deals with the mechanical and electrical specifications of the interface and transmission medium.It also defines the type of transmission medium
    - Mechanical: cable, plugs, pins.
    - Electrical/optical: modulation, signal strength, voltage levels, bit times
- **Representation of bits(Type of encoding):** The physical layer data consists of a stream of bits(sequence of Os or 1s) with no interpretation. To be transmitted, bits must be encoded into signals:electrical or optical. The physical layer defines the type of
encoding (how Os and I s are changed to signals).
- **Data rate:** The number of bits sent each second is also defined by the physical layer.
- **Synchronization of bits:** The sender and receiver not only must use the same bit rate. In other words, the sender and the receiver clocks must be synchronized. 
- **Transmission mode:** The physical layer also defines the direction of transmission between two devices: simplex, half-duplex, or full-duplex.
2. **Data link layer**
- The data link layer is responsible for moving frames from one hop (node) to the next

**Characteristics of Data link Layer**
- **Framing:** The data link layer divides the stream of bits received from the network layer into manageable data units called **frames**.
- **Physical addressing:** If frames are to be distributed to different systems on the network, the data link layer adds a **header** to the frame to define the sender and/or
receiver of the frame. If the frame is intended for a system outside the sender's network, the receiver address is the address of the device that connects the network
to the next one.
- **Flow control:** If the rate at which the data are absorbed by the receiver is less than the rate at which data are produced in the sender, the data link layer imposes a flow control mechanism to avoid overwhelming the receiver."overwhelm" means that the receiver is unable to handle or process the incoming data at the speed or rate it is being sent.
- **Error control:** The data link layer adds reliability to the physical layer by adding mechanisms to detect and retransmit damaged or lost frames. It also uses a mechanism to recognize duplicate frames. Error control is normally achieved through a **trailer** added to the end of the frame.
- **Access control:** When two or more devices are connected to the same link, data link layer protocols are necessary to determine which device has control over the
link at any given time.
3. **Network layer**
- The network layer is responsible for the delivery of individual packets from the source host to the destination host.
- Whereas the data link layer oversees the delivery of the packet between two systems on the same network (links), the network layer ensures that each packet gets from its point of origin to its final destination.
- Hence,if two systems are connected to the same link, there is usually no need for a network layer. However, if the two systems are attached to different networks (links) with connecting devices between the networks (links), there is often a need for the network layer to accomplish **Source-to-destination delivery**.

**Characteristics of Network Layer**
- **Logical  Addressing:**  If  a  packet  has  to  cross  the  network  boundary  then  the  header  contains 
information of the logical addresses of the sender and the receiver. 
- **Routing:** When independent networks or links are connected to create *internetworks* (network of networks) or a large network, the connecting devices (called routers
or switches) route or switch the packets to their final destination. One of the functions of the network layer is to provide this mechanism.
4. **Transport Layer:**
- The transport layer is responsible for the delivery of a message from one process to another.
- A process is an application program running on a host.
- The network layer oversees source-to-destination delivery of individual packets, it does not recognize
any relationship between those packets. It treats each one independently, as though each piece belonged to a separate message, whether or not it does.  
- The transport layer ensures that the whole message arrives intact and in order, overseeing both error control and flow control at the source-to-destination level.

**Characteristics of Transport Layer**
- **Service-point addressing:** Computers often run several programs at the same time. For this reason source-to-destination delivery means delivery not only from
one computer to the next but also from a specific process (running program) on one computer to a specific process (running program) on the other. The transport layer header must therefore include a type of address called a *service-point address (or port address)*.
- **Segmentation and reassembly:** A message is divided into *transmittable segments*, with *each segment containing a sequence number*. These numbers enable the transport layer to *reassemble* the message correctly upon arriving at the destination and to identify and replace packets that were lost in transmission.
- **Connection control:** The transport layer can be either connectionless or connection-oriented. A **connectionless** transport layer treats each segment as an independent packet and delivers it to the transport layer at the destination machine. A **connection-oriented transport layer** makes a connection with the transport layer at the destination machine first before delivering the packets. After all the data are transferred,
the connection is terminated.
- **Flow control:** Like the data link layer, the transport layer is responsible for flow control. However, flow control at this layer is performed end to end rather than across a single link.("end to end" means that the regulation of data flow occurs between the source and destination applications, rather than just between neighboring nodes on the network.)
- **Error control:** Like the data link layer, the transport layer is responsible for error control. However, error control at this layer is performed process-to-
process rather than across a single link. The sending transport layer makes sure that the entire message arrives at the receiving transport layer without error
(damage, loss, or duplication). *Error correction is usually achieved through retransmission*.
5. **Session Layer**
-  The session layer is the network **dialog controller**.
It establishes, maintains, and synchronizes the interaction among communicating systems.
- Generally,**dialog** reffers to the interface that helps 2 systems to communicate

**Characteristics of Session Layer**
- **Dialog control:** The session layer allows two systems to enter into a dialog. It allows the communication between two processes to take place in either half-duplex (one way at a time) or full-duplex (two ways at a time) mode.
- **Synchronization:** The session layer allows a process to add **checkpoints**, or **synchronization points**, to a stream of data. For example, if a system is sending a file of 2000 pages, it is advisable to insert checkpoints after every 100 pages to ensure that each 100-page unit is received and acknowledged independently. In this case, if a crash happens during the transmission of page 523, the only pages that need to be resent after system recovery are pages 501 to 523. Pages previous to 501 need
not be resent. 
6. **Presentation Layer**
- The presentation layer is concerned with the syntax and semantics of the information exchanged between two systems.

**Characteristics of Presentation Layer**
- **Translation:** The processes(running programs)in two systems are usually exchanging information in the form of character strings,numbers,and so on.The information must be changed to bit streams before being transmitted.
- **Encryption:** To carry sensitive information, a system must be able to ensure privacy. Encryption means that the sender transforms the original information to another form and sends the resulting message out over the network. Decryption reverses the original process to transform the message back to its original form.
- **Compression:** Data compression reduces the number of bits contained in the information. Data compression becomes particularly important in the transmission
of multimedia such as text, audio, and video.
7. **Application Layer**
- The application layer enables the user, whether human or software, to access the network. It provides user interfaces and support for services such as electronic mail,remote file access and transfer, shared database management, and other types of distributed information services.

**Characteristics of Application Layer**
- **Network virtual terminal:** A network virtual terminal is a software version of a physical terminal, and it allows a user to log on to a remote host. 
- **File transfer, access, and management:** This application allows a user to access files in a remote host (to make changes or read data), to retrieve files from a remote computer for use in the local computer, and to manage or control files in a remote computer locally.
- **Mail services:** This application provides the basis for e-mail forwarding and storage.
- **Directory services:** This application provides distributed database sources and access for global information about various objects and services.

**TCP/IP PROTOCOL SUITE(80-82)**
---

<img src="Images/Screenshot 2024-09-25 210328.png" width="" height="">

- Whereas the OSI model specifies which functions belong to each of its layers,the layers of the TCP/IP protocol suite contain relatively independent protocols that
can be mixed and matched depending on the needs of the system
- 
- Within a single machine, each layer calls upon the services of the layer just below
it. Layer 3, for example, uses the services provided by layer 2 and provides services for
layer 4. Between machines, layer x on one machine communicates with layer x on
another machine. This communication is governed by an agreed-upon series of rules
and conventions called **protocols**. The processes on each machine that communicate at
a given layer are called **peer-to-peer processes**. Communication between machines is
therefore a peer-to-peer process using the protocols appropriate to a given layer.
- Peer-to-Peer Processes(Side by side)
- Encapsulation & Decapsulation (Down and up)
- Hop-by-hop delivery is a network data transfer technique that involves sending data packets from one node to the next in a store-and-forward manner. It's a method for controlling network data flow that uses short-term credits and long-term path delay estimation to reduce congestion and ensure timely delivery. 
- In hop-by-hop delivery, each intermediate node in the network selects the next hop from one of its neighbors. The retransmission of a lost packet occurs at the sender end of the link where the packet was lost, rather than all the way from the source node. 
- Layers in Osi model
	- Physical layer
	- Datalink Layer
	- Network layer
	- Transport layer
	- Session layer
	- Presentation layer
	- Application layer
- TCP/IP protocol suite
	- Physical and Data Link Layers
	- Network Layer
		- IP
		- Address Resolution Protocol
		- Reverse Address Resolution Protocol 
		- Internet Control Message Protocol
		- Internet Group Message Protocol
	- Transport Layer
- Addressing