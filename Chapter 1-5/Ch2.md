# Chapter 2
**Layered task/Hierarchical Task**
---
<img src="Images/Screenshot 2024-09-24 223208.png" width="400" height="">

- Each layer at the sending site uses the services of the layer immediately below it. The
sender at the higher layer uses the services of the middle layer. The middle layer uses
the services of the lower layer. The lower layer uses the services of the carrier.

## Basic Terminologies
- **Hop to hop delivery:** It is also known as node to node delivery. A node can be any device like a pc,hub,server,etc.So it's a delivery(or node) where data is passed from one device to its immediate connected device.

**Peer to peer processes**
- Peer-to-peer processes are logical communications between corresponding layers on two devices in a network.
- In bottom three layers peer to peer communication occurs by passing through intermediate nodes(routers or switches).
- In top four layers, peer to peer communication occur directly facilitated by peer to peer protocol.

- **Encapsulation:** Encapsulation is the process where each layer in the OSI model adds its own header (and possibly a trailer at data link layer) to the data from the layer above. 

- **Decapsulation:** It is the process of extracting the data by removing the header (and possibly a trailer at data link layer) while sending the data to layer above.
- When the data is finally reached to physical layer it is converted into electromagnetic signals and transmitted to physical layer in the destination device.

<img src="Images/Screenshot 2024-12-10 130603.png" width="350" height="">


**OSI Model**
---	
<img src="Images/Screenshot 2024-09-24 223947.png" width="" height="">




1. **Physical Layer**
- The physical layer is responsible for movements of
data bits from one hop (node) to the next.

<img src="Images/Screenshot 2024-09-24 225904.png" width="350" height="">

**Characteristics of Physical Layer**
- It defines the type of transmission medium used for communication.
- **Encoding of data bits to signals:** It encodes the data bits into signals to make it suitable for transmission.
- **Data rate:** The number of bits sent each second is also defined by the physical layer.
- **Synchronization of bits:** It ensures that the data bits transferred from sender to receiver must be synchronised.It means data bit send by send and data bits received by receiver must be in equilibrium.
- **Transmission mode:** The physical layer also defines the direction of transmission between two devices: simplex, half-duplex, or full-duplex.
2. **Data link layer**
- The data link layer is responsible for moving frames from one hop (node) to the next

**Characteristics of Data link Layer**
- **Framing:** The data link layer divides the stream of bits received from the network layer into manageable data units called **frames**.
- **Physical addressing:** The datalink layer specifies the MAC address of the destination node  connected to source node in the header of the frame, where the frames need to be transferred.
- **Flow control:** If the rate at which the data are absorbed by the receiver is less than the rate at which data are produced in the sender, the data link layer imposes a flow control mechanism to avoid overwhelming the receiver."overwhelm" means that the receiver is unable to handle or process the incoming data at the speed or rate it is being sent.
- **Error control:** The Datalink layer adds redundant bits as the trailer of the frame to detect and handle errors.
- **Access control:** When two or more devices are connected to the same link, data link layer protocols are necessary to determine which device has control over the
link at any given time,to avoid colliosion.
3. **Network layer**
- The network layer is responsible for the delivery of individual packets from the source host to the destination host.
- Whereas the data link layer oversees the delivery of the packet between two systems on the same network (links), the network layer ensures that each packet gets from its point of origin to its final destination.
- Hence,if two systems are connected to the same link, there is usually no need for a network layer. However, if the two systems are attached to different networks (links) with connecting devices between the networks (links), there is often a need for the network layer to accomplish **Source-to-destination delivery**.

**Characteristics of Network Layer**
- **Logical  Addressing:**  If  a  packet  has  to  cross  the  network  boundary  then  the  header  contains 
information of the logical/IP addresses of the sender and the receiver. 
- **Routing:** When independent networks or links are connected to create *internetworks/internet* (network of networks) or a large network, routers operate in the network layer of each network to route and transfer data packets to destination host.
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
- **Flow control:** Like the data link layer, the transport layer is responsible for flow control. However, flow control at this layer is performed source to destination rather than hop to hop.
- **Error control:** The sending transport layer makes sure that the entire message arrives at the receiving transport layer without error
(damage, loss, or duplication). *Error correction is usually achieved through retransmission*.
5. **Session Layer**
-  The session layer is the network **dialog controller**.
It establishes, maintains, and synchronizes the interaction among communicating systems.
- Generally,**dialog** reffers to the interface that helps 2 systems to communicate

**Characteristics of Session Layer**
- **Dialog control:** The session layer allows two systems to enter into a dialog. It allows the communication between two processes to take place in either half-duplex (one way at a time) or full-duplex (two ways at a time) mode.
- The session layer allows a process to add **checkpoints**, or **synchronization points**, to a stream of data. For example, if a system is sending a file of 2000 pages, it is advisable to insert checkpoints after every 100 pages to ensure that each 100-page unit is received and acknowledged independently. In this case, if a crash happens during the transmission of page 523, the only pages that need to be resent after system recovery are pages 501 to 523. Pages previous to 501 need
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
- **Provides user interface**
- **Network virtual terminal(optional):** A network virtual terminal is a software version of a physical terminal, and it allows a user to log on to a remote host. 
- **File transfer, access, and management:** This application allows a user to access files in a remote host (to make changes or read data), to retrieve files from a remote computer for use in the local computer, and to manage or control files in a remote computer locally.
- **Mail services:** This application provides the basis for e-mail forwarding and storage.
- **Directory services:** This application provides distributed database sources and access for global information about various objects and services.

**TCP/IP PROTOCOL SUITE(80-82)**
---

<img src="Images/Screenshot 2024-09-25 210328.png" width="" height="">

- It was developed prior to OSI model.
- It has generally four layers.
	1. Physical/Datalink layer
	2. Network/Internet layer
	3. Transport layer
	4. Application layer
- We will discuss about the core functionality of each layer, as well as the protocols used in the layer.

1. **Physical-Data Link Layer**
- The physical part of this layer ensures transmission of raw bit streams from hop to hop. 
- Whereas the data link part group these bits into frames and transfer them from hop to hop overseeing flow control, error detection, access control,etc.
- In this layer there is no specific protocol used unlike Internet and Transport Layer.
- Protocol used in this layer are **standard** and **proprietary protocols** applied on the hardware used in the network.
- **Standard protocols(Just for knowledge):** Protocols issued by international organisations like ISO,IEEE,etc.
- **Proprietary protocols(Just for knowledge):** Protocols issued by private organisations like Cisco HDLC,etc.
2. **Internet Layer**
- It helps to route the data packets to ensure they reach the correct destination across interconnected networks.
- These tasks is facilitated by IP(Internetworking protocol) and other supporting protocols.

**IP(Internetworking protocol):** 
- The Internet Protocol (IP) is an unreliable, connectionless protocol that delivers data packets (datagrams) on a best-effort basis (which means without error checking or tracking), leaving additional functionalities to higher layers for efficiency.
- IP is a basic protocol that sends data packets without error checking or tracking, relying on higher layers to handle additional features.(simple definition)
3. **Transport Layer**
- It is responsible for delivering message from process to process.
- This is achieved by protocols like UDP and TCP.
- A new transport layer protocol SCTP has been introduce to meet the needs of some newer applications.

**UDP(User Datagram Protocol)**
- It is the simpler version of the two standard TCP/IP transport protocol.
- It is a process to process protocol that adds only port address, checksum error control and length information to the data of the upper layer.

**TCP(Transmission Control Protocol)**
-  TCP is a reliable *stream* transport protocol.
- The term *stream*, in this con
text, means connection-oriented: A connection must be established between both ends
 of a transmission before either can transmit data.
-  At the sending end of each transmission, TCP divides a stream of data into smaller units called **segments**.
- Each segment is assigned with a sequence number all the segments are received in proper sequence or identifying the missing segment in an wrong message.
-  At the receiving end, TCP collects each datagram as it comes in and reorders the transmission based on sequence numbers.

**Stream Control Transmission Protocol(Just for knowledge)**
-  It is a transport layer protocol that combines the best features of UDP and TCP.
- The Stream Control Transmission Protocol (SCTP) provides support for newer applications such as voice over the Internet. 

4. **Application Layer**
- The application layer in TCP/IP is equivalent to the combined session, presentation and application layers in the OSI model.
- Provides protocols and services for user applications, enabling functionalities like web browsing, file transfer, and email communication.
- Protocols used here is application/software specific.Eg,HTTP for web browsing,SMTP for email,FTP for file transfer,etc.

## Addressing in TCP/IP
-  Four levels of addresses are used in an internet employing the TCP/IP protocols:
 physical (link) addresses, logical (IP) addresses, port addresses, and specific
 addresses 

<img src="Images/Screenshot 2024-12-10 163427.png" width="" height="">

1. **Physical Address(MAC Address)**
- Used to identify devices on the same physical network. 
- Each network interface card (NIC) has a unique MAC address, allowing devices to communicate within a local network.
- The size
 and format of these addresses vary depending on the network. For example, Ethernet
 uses a 6-byte (48-bit) physical address that is imprinted on the network interface card
 (NIC). LocalTalk (Apple), however, has a I-byte dynamic address that changes each
 time the station comes up
- We will discuss about the types of physical address later.
2. **Logical address(IP Address)**
- Provides global identification for devices across networks. IP addresses ensure data can be routed from the source to the destination through different networks.
- Applied in network layer
3.  **Port Addressing**
- Differentiates multiple services or processes running on a single device. Port numbers ensure data is directed to the correct application.
- Applied in transport layer
4. **Specific addressing**
- Human-readable addresses like URLs or domain names are used to identify specific web services or resources. These are mapped to IP addresses using DNS (Domain Name System).
- Applied in application layer

## Types of Physical Addressing
- Physical address can be of three types:
1. **Unicast**
- A one-to-one communication where data is sent from one sender to one receiver.
- The least significant bit (LSB) of the first byte is 0.
- Eg,`00:1A:2B:3C:4D:5E` is unicast because the first byte is $(00)_{16}=(00000000)_2$, the LSB of first byte is 0.
2. **Multicast**
- A one-to-many communication where data is sent from one sender to a specific group of receivers.
- The least significant bit (LSB) of the first byte is 1.
- Example: `01:00:5E:00:00:01` (commonly used for IPv4 multicast addresses) is multicast because the first byte is $(01)_{16}=(00000001)_2$, the LSB of first byte is 1.
3. **Broadcast**
-  A one-to-all communication where data is sent from one sender to all devices in a network.
- The MAC address `FF:FF:FF:FF:FF:FF` is the broadcast address, meaning it's sent to all devices on the local network.
